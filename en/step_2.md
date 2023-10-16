## Create your machine learning model

Imagine you're trying to cut down on hotdogs and eat more healthily. This detector can help keep you on track by alerting you whenever a sneaky hotdog is on your plate! (In case you couldn't tell!)

First, create your machine learning model on Machine Learning for Kids:

--- task ---

Open the website [Machine Learning for Kids](https://machinelearningforkids.co.uk/#!/login){:target="_blank"}.

--- /task ---

--- task ---

On the screen that appears, choose **Log In** if your mentor gave you some login details. Enter your username and password on the next screen.

![A picture of the blue log in button.](images/singup_login.png)

Choose **Sign Up** if you are creating your own account and follow the prompts to create a new account.

--- /task ---

--- task ---

Select **Go to your projects**.
![Image of the blue 'go to your projects' button on Machine Learning for Kids.](images/go2projects.png)

--- /task ---

--- task ---

Select **Add a new project**.
![Image of a grey button that reads 'Go to your projects'.](images/add_new_project.png)

--- /task ---

--- task ---

Give the project a name and set it to recognise **images**.
![](images/name_project.png)

--- /task ---

--- task ---

Select **CREATE**. Once created, click on the project title.

![](images/create_button.png)

--- /task ---


Now that you have created a project that identifies images, you need to set out the different ways your images will be classified - `hotdog` and `nothotdog` - these will be our **classes**.

--- collapse ---
---
title: Classes and labels
---

**Labels** are the specific names we give to each picture so the model knows what it's looking at, while **classes** are the major categories we're trying to sort those pictures into. In our case, we only have two classes: 'hotdog' and 'not hotdog'.

For instance, if you see an image of a hotdog, you'll label that picture as 'hotdog'. By doing this, you're telling the model that this image belongs to the 'hotdog' class. Similarly, if you have a picture of a banana, you'll label it 'not hotdog', placing it in the 'not hotdog' class. The model will then use these labels to differentiate between images that are hotdogs and those that aren't.

![An image explaining that a class is a major category images can be sorted into, showing a group of apple pictures in one box, next to an explanation that a label is given to each image to show which class it fits into, with a single apple picture.](images/class_vs_label.png)

Remember, the classes you select should help the model make clear predictions. In our scenario, it's pretty straightforward: every image is either a `hotdog` or `not hotdog`. But in other projects, you could have multiple classes based on various characteristics of the data you're working with.

--- /collapse ---


--- task ---

Select **Train**. This will let you add new training data to your model.
![](images/train.png)

--- /task ---
