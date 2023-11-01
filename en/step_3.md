## Train the model

Imagine teaching a friend how to differentiate between two types of fruits, let's say apples and bananas, by showing them pictures. At first, they might get confused, especially if they've never seen these fruits before. But as you keep showing them more pictures and they get a better understanding of the patterns in the differences and similarities, they start to get the hang of it. After a while, they will be able to correctly identify apples and bananas on their own.

Training a machine learning model is kind of like this process, but with a computer instead of a friend. For your classifier, we want to determine 'hotdogs' and 'not hotdogs', so you need to define these two groups to the model, then provide lots of examples of each.

--- task ---

Select **Add new label** and create a label for the `hotdog` class.
![](images/add_hotdog.png)

**Repeat** this step to create a second label for the `nothotdog` class.

--- /task ---

--- task ---

We have collected two image sets for you to train your new machine learning model. Click the plus sign to expand the collapses here:

[[[hotdog-train]]]

[[[not-hotdog-train]]]

Look through the training data and **choose several images of hotdogs and several images of other things** from the data. The more images of each type you pick, the more accurate your model will be. 

--- /task ---

--- task ---

Drag and drop your chosen images into the relevant class (`hotdog` or `nothotdog`).
![](images/hotdog_classes.png)

--- collapse ---
---
title: Adding training images with drag & drop
---

To 'drag and drop' images into your classes easily, you can set up the windows on your screen side-by-side by clicking on and dragging the tab you are working on to one side of the screen:
![Image showing two windows side-by-side on a computer screen. On the left are several images of hotdogs, on the right is a window showing a machine learning model's classes page.](images/splitscreen.png)

Once you have set up your screen like this, you can simply click on the training images you want to use and drag them into the right class, then release the mouse button:

![](images/dragdrop.gif)

--- /collapse ---

--- /task ---

--- task ---

Select **Back to project**.
![](images/back_to_project.png)

--- /task ---

--- task ---

Next, select **Learn & Test**.

![](images/learn_test.png)


Your model is now ready to be trained. 

--- /task ---

--- task ---

Select **Train new machine learning model**.
![](images/train_new.png)

You will have to wait a moment while the model trains.

--- /task ---

### Test your model

Now that you have trained your model, it is time to test it to see how successful it is.  
Some data has been kept aside to use as test data.

--- collapse ---
---
title: Training data vs. testing data
---

To teach a machine learning model to classify a specific item, we provide it with a particular set of data called **training data**. This data set is similar to the exercises in a textbook that have answers; they help in understanding and practicing the topic.

After processing the training data, it's essential to check the program's performance. For this, we introduce it to a new set of data known as **testing data**. Think of this as taking a quiz or test at school: the questions aren't identical to what you practiced, but they cover the same topic.

**Why keep them separate?**
If we use the same data for both training and testing, it's like giving you a maths test with the exact same questions you practised with. You might get all the answers right, but it doesn't show if you understand the topic broadly. It only shows that you know those specific questions.

Similarly, if we test the model with the same data it was trained on, we can't be sure if it has analysed enough data to make accurate predictions or if it just "remembers" that specific data. By using different data for testing, we can get a better idea of how well the model can handle new, unseen situations.

So, it's essential to keep the training and testing data separate to ensure that the model can perform the task accurately in various situations, not just the ones it has seen before.

--- /collapse ---

To see how successful your model is at classifying the test data, test your model with some of the images:

--- task ---

Drag and drop an image into the link box (next to the **Test with www** button):

![](images/test_with_www.png)

--- collapse ---
---
title: Add a test image without drag and drop
---

Alternatively, you can:

+ Right-click on an image
+ Select **Copy image address**
+ Paste the image address into the link box

--- /collapse ---

**You can find the testing images here:**

[[[hotdog-test]]]

[[[nothotdog-test]]]

--- /task ---

--- task ---

Click the **Test with www** button to test your model.

--- /task ---


--- task ---

Once you have tested a few of the images, answer the following questions in your **Blueprint**:

1. Describe the results of your testing. How accurate was the model? 
2. Why do you think the prediction is sometimes wrong?
3. How could you improve the accuracy of the model?

--- /task ---

--- collapse ---
---
title: Bias and data
---

When we train a model to classify different things, like dogs and cats, we need to give it lots of examples. These examples are called **training data**.

If we use a training data set that contains mostly small dogs and large cats, this does not accurately represent the real world as there are also large dogs and small cats. If the data used to train the model is not representative of what you're trying to model, the prediction that your model makes won't be either.

This is called **bias**, which means the model favours one thing over another. We can fix this by using a more diverse training data set that includes different sizes and breeds of dogs and cats. By doing this, we can help the model identify the features that distinguish each type of animal, rather than just relying on the animal's size.

--- /collapse ---

<p style='border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;'>
Imagine you are making an app that predicts the age of people. 
<br><br>
Now think of ten people whose pictures you could use for your training data? What bias would you introduce? Have you picked people from a range of age groups? Would your app work with people from all over the world with different face shapes and skin tones?
<br><br>
By using more diverse and representative training data to avoid <strong>bias</strong>, we can help ensure that the model makes accurate and fair predictions when it encounters new examples. This can make the computer more useful and reliable for different applications, from sorting pet adoption photos to assisting veterinarians in diagnosing animal health issues.
</p>

Let's start making your machine learning application in Scratch and think about what it will do!
