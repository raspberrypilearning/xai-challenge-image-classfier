
## Make a Scratch application to classify images

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Your model is trained and ready to test, but to do that you need to create a scratch project that can allow your user to input images and classify the input as `hotdog` or `nothotdog`.
</div>
<div>
![Image showing four screenshots of different Scratch classification applications](images/demo_shot.png){:width="300px"}
</div>
</div>


### **Your project will:**
+ Take image input from the user
+ Use your trained ML model to classify images
+ Tell the user whether the thing in the picture is a 'hotdog' or not

--- task ---

On your [**project page**](https://machinelearningforkids.co.uk/#!/projects){:target="_blank"}, select **Make**:
![Image showing a button reading Make and the explanation 'Use the machine learning model you've trained to make a game or app, in Scratch, Python, or App Inventor'](images/make_button.png)

--- /task ---

--- task ---

On the next page, select Scratch 3
![](images/scratch3_button.png)

--- /task ---

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
A special fork of Scratch will open in a new tab. When it does, you will see an item in the left-hand menu with the same name as your machine learning project.

The new grey blocks you can see in that menu allow you to access your machine learning model from within your project:
</div>
<div>
![Image showing several Scratch block menus, with the final one being titled MusicWellness with the machine learning for kids logo](images/model_blocks_menu.png){:width="100px"}
</div>
</div>

--- collapse ---
---
title: Pro tip - Save your work!
---

This special version of Scratch allows you to access your machine learning model, as well as use the music database blocks - **if you try to open your project in another version of Scratch online it won’t work**. 

A hack you can use is to save your work to your computer often. Once you have the .sb3 file for your project saved you can open it again later, or on another computer:
+ Go to [rpf.io/mlscratch](rpf.io/mlscratch){:target="_blank"} to get to this special fork of Scratch 
+ Once Scratch opens choose File > Load from your Computer
+ Select your file in the window that appears to get back to where you left off

![Image showing the Scratch file menu with the Load from your computer option highlighted](images/load_menu.png)


Save your work as often as you can to make sure you don’t lose any progress!

--- /collapse ---

--- task ---

Add a `when green flag clicked`{:class="block3events"} block to your workspace. This is the script that will run the first time we start the project. 

```blocks3
when green flag clicked
```

--- /task ---

The next thing we want our application to do is ask the user to input some images - this is the data that will be compared by the model and classfied as `hotdog` or `nothotdog`.

--- task ---

In the blue `Sensing`{:class="block3sensing"} menu, add an `ask (What's your name?) and wait`{:class="block3sensing"} block:

```blocks3
when green flag clicked
ask [What's your name?] and wait
```

--- /task ---

--- task ---

Change the question text to something you like. Ask your user to enter a quote. You could say something like:
+ What is your quote?
+ Halt! Who goes there?
+ Enter your favourite quote to start!
+ Type something to see if you are a hotdog or a nothotdog!

```blocks3
when green flag clicked
ask [You there! What say you?] and wait
```

--- /task ---

--- task ---

From the purple `Looks`{:class="block3looks"} menu, add a `say (Hello!)`{:class="block3looks"} block to your script.

```blocks3
when green flag clicked
ask [You there! What say you?] and wait
say [Hello!]
```

--- /task ---

Now, we're going to create the message your application will show the user when it has classified the image they entered. To do that, we're going to `join`{:class="block3operators"} some bits of text (called strings) with data from your machine learning model using specific blocks. 

The example message will say: "I am `(model confidence: number)`% certain you are a `(model label: hotdog/nothotdog)`!

--- task ---

From the green `Operators`{:class="block3operators"} menu, place a round `join (apple) (banana)`{:class="block3operators"} block into the hole in the purple `say`{:class="block3looks"} block:

```blocks3
when green flag clicked
ask [You there! What say you?] and wait
say ((join [apple] [banana]))
```

--- /task ---

--- task ---

Add another round `join (apple) (banana)`{:class="block3operators"} block into the hole in the one you just added (it doesn't matter which hole):

```blocks3
when green flag clicked
ask [You there! What say you?] and wait
say (join ((join [apple] [banana])) [banana])
```

--- /task ---

--- task ---

Add one last round `join (apple) (banana)`{:class="block3operators"} block into the hole in the one you just added (it doesn't matter which hole):

```blocks3
when green flag clicked
ask [You there! What say you?] and wait
say (join (join [apple] [banana]) ((join [apple] [banana])))
```
--- /task ---

--- task ---

Into the first hole that says `apple`, type `I am ` 
Make sure you include a space at the end!

```blocks3
when green flag clicked
ask [You there! What say you?] and wait
say (join (join [I am ] [banana]) (join [apple] [banana]))
```
--- /task ---

--- task ---

Into the second hole, that says `banana`, drag a black `recognise image [text] (confidence)` block from the Machine learning for kids menu at the very bottom:

```blocks3
when green flag clicked
ask [You there! What say you?] and wait
say (join (join [I am ] (recognise image [text] confidence :: #4b4c60)) (join [apple] [banana]))
```
--- /task ---

--- task ---

Into the next (third) hole, that still says `apple`, type `% sure you are a  ` 
Make sure you include a space at the end!

```blocks3
when green flag clicked
ask [You there! What say you?] and wait
say (join (join [I am ] (recognise image [text] confidence :: #4b4c60)) (join [% sure you are a  ] [banana]))
```
--- /task ---

--- task ---

Into the last (fourth) hole, that still says `banana`, drag a black `recognise image [text] (label)` block from the Machine learning for kids menu at the very bottom:

```blocks3
when green flag clicked
ask [You there! What say you?] and wait
say (join (join [I am ] (recognise image [text] confidence :: #4b4c60)) (join [% sure you are a  ] (recognise image [text] label :: #4b4c60)))
```

--- /task ---

The final piece of the puzzle is to now use the image your user entered as the information sent back to the model for classification!

--- task ---

From the light blue `Sensing`{:class="block3sensing"} menu, drop a round `answer`{:class="block3sensing"} bubble into the two white slots which say `text`:

```blocks3
when green flag clicked
ask [You there! What say you?] and wait
say (join (join [I am ] (recognise image (answer) confidence :: #4b4c60)) (join [% sure you are a  ] (recognise image (answer) label :: #4b4c60)))
```

--- /task ---

--- task ---

**Click the green flag**, then type or paste some text into the prompt that appears and press **Enter**.

Your character will say whether the speaker of those words is a hotdog or a nothotdog and to what certainty!

--- /task ---

In the next step, you can customise the way your application looks by adding costumes and add some new features that activate depending on the classification of your input.

