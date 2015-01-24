# Configure Change Calculator

Before you can start programming the change calculator, you need to create the new activity, create a button to link and then write the code to link. This is a similar process you will need to perform before each new utility that you create.

### 4.1 Create a new Activity

An Activity in Android is an easy way to refer to a User Interface and the code associate with it.

To create a new Activity, go to File and click New. A menu appears and Choose Blank Activity under Activity.

![][13]

[13]: images/programming-fundamentals-with-android/create-a-new-activity.png

### 4.2 Configure the Activity

Set the details to the activity to uniquely identify it.

In this case, set the Activity Name to be "Change Calculator". All the other values will change accordingly.

Click Finish.

This will create the necessary files to run an activity as well as the basic structure to those files.

![][14]

[14]: images/programming-fundamentals-with-android/configure-the-activity.png

### 4.3 Create the linking button from the Main Activity

Now that you've created the activity, you will need to create a button which links from the main page to the newly created ChangeCalculator activity.

Open the activity_main and drag a button from the palette onto the screen under the heading.

### 4.4 Configure the button

There are a number of settings you need to change for this button to display correctly. Look in the Properties list to change the following settings:

     layout_width: fill_parent
     id: btnChangeCalc
     onClick: changeCalc
     text: Change Calculator

The new attributes are id and onClick. id uniquely identifies the button so you can access it in code, and the onClick attribute tells Android which method to run when the button is clicked.

Save the file.

![][15]

[15]: images/programming-fundamentals-with-android/configure-the-button.png

### 4.5 Create the changeCalc() method

Open the MainActivity file in the java folder (and then the reverse domain name folder).

Towards the end of the file, create the empty method stub for chanceCalc(). You need to include the View v arguments to make sure it runs correctly. You will learn about method and arguments in more detail later.

![][16]

[16]: images/programming-fundamentals-with-android/create-the-changecalc---method.png

### 4.6 Run the new Activity

When the user taps the Change Calculator Button, the new ChangeCalculator activity needs to open. Include the code to do this.

Make sure that ChangeCalculator.class is spelled the **exact** same way as the Java file.

![][17]

[17]: images/programming-fundamentals-with-android/run-the-new-activity.png
