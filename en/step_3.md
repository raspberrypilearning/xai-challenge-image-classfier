## Make a Machine Learning model

A supermarket has asked you to create a machine learning model that will recognise images of apples and tomatoes.

Your task is to set up and train a machine learning model which can do this by completing the following steps:

--- task ---

Open the website [Machine Learning for Kids](https://machinelearningforkids.co.uk/#!/login){:target="_blank"}.


--- /task ---

--- task ---

Select **Try it now**.
![](images/try_it_now.png)

--- /task ---

--- task ---

Select **Add a new project**.
![](images/add_new_project.png)

--- /task ---

--- task ---

Give the project a name and set it to recognise **images**.

![](images/supermarket_ai.png)

--- /task ---

--- task ---

Select **CREATE**. Once created, click on the project title.

![](images/create_button.png)



--- /task ---

--- task ---

Select **Train**.
![](images/train.png)

--- /task ---

--- task ---

Select **Add new label** and create a label for the **apple** class.
![](images/add_apple.png)

**Repeat** this step to create a second label for the **tomato** class.

--- /task ---

--- task ---

Visit the following webpage to find the data set you can use to train your model: [Apples and Tomatoes](https://ai-activities.raspberrypi.org/project-files/){:target="_blank"} 
![](images/apples.png)

There are two sets of data on this page under the headings **Training Data** and **Test Data**.

--- /task ---

--- task ---

Look through the training data and **choose 5 images of apples and 5 images of tomatoes** from the data.

Drag and drop your chosen images into the relevant class (Apple or Tomato).
![](images/apple_classes.png)

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

--- /task ---

### Testing your model

Now that you have trained your model, it is time to test it to see how successful it is.  
Some data has been kept aside to use as test data. You can find the images at the bottom of the [webpage hosting the data set](https://ai-activities.raspberrypi.org/project-files/){:target="_blank"}.

To see how successful your model is at classifying the test data, test your model with some of the images:

--- task ---

Drag and drop an image into the link box (next to the Test with www button):

![](images/test_with_www.png)

--- collapse ---
---
title: Adding a test image without drag and drop
---

Alternatively, you can:

+ Right-click on an image
+ Select Copy image address
+ Paste the image address into the link box

--- /collapse ---

--- /task ---

--- task ---

Click the **Test with www** button to test your model.

--- /task ---

--- task ---

Once you have tested a few of the images, answer the following questions in your **blueprint**:

1. Describe the results of your testing. How accurate was the model? 
2. Why do you think the prediction is sometimes  wrong?
3. How could you improve the accuracy of the model?

--- /task ---

### Bias and data

When we teach a computer to recognize different things, like apples and tomatoes, we need to give it lots of examples to learn from. These examples are called **training data**.

If we use a training dataset that contains mostly red tomatoes and green apples, this does not accurately represent the real world as there are also red apples and even green tomatoes. If the data used to train the model is not representative of what you're trying to model, neither will the prediction be which your model makes.

This is called **bias**, which means the computer is favouring one thing over another. We can fix this by using a more diverse training dataset that includes different types and colours of apples and tomatoes. By doing this, we can help the computer learn to recognize the features that distinguish each type of fruit, rather than just relying on the colour of the training examples.

<p style='border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;'>
By using more diverse and representative training data, we can help ensure that the computer makes accurate and fair predictions when it encounters new examples. This can make the computer more useful and reliable for different applications, from identifying objects in photos to making decisions in healthcare or finance.
</p>

Let's start making your machine learning application and think about what it will do!