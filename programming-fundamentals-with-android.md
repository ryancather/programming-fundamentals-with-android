#Programming Fundamentals with Android

This tutorial introduces you to the fundamental concepts of programming through creating an Android application.

Through this tutorial, you will learn the following concepts:

* Variables / Constants
* Arithmetic Operators
* Boolean Expressions
* Decision Making - If...Then...Else
* Loops
* Arrays
* Functions
* Basic User Interface design

The app created will be a Utility app which allows for different problems to be solved. These problems are, but not limited to, the following:

* **Tip Calculator**
* **Change Calculator**
* **Coin Flip generator**

## 1. Software Versions

This tutorial was written for Android Studio 1.0.2. The app was tested on Android versions 4 (API15) to 5. Earlier or later versions may not work in the same fashion as is described in this tutorial. You may need to modify steps to achieve the same goals.

## 2. Main App

First, you will need to create a project to hold all these utilities.

In order for the utilities to be accessible from the main page, you'll need to create a basic interface, primarily of buttons, to link to the separate utilities.

## 3. Create Project

To begin with, you'll need to create a project to hold all the different utilites.

### 3.1 Project Name

In Android Studio, go to File and choose New Project.

The New Project Wizard will appear. Enter the name of the project and the Company Domain. Name the project "<YourName>'s Utilty App"

Click the browse button to save the project in the desired location.

Click Next

![][1]

[1]: images/programming-fundamentals-with-android/project-name.png

### 3.2 Android Versions

In this step of the wizard, you need to select the platform and version of Android you are targeting the app for. 

For this tutorial, set the minimum SDK to be API14 which is version 4.0 of Android, or better known as Ice Cream Sandwich.

Click Next.

![][2]

[2]: images/programming-fundamentals-with-android/android-versions.png

### 3.3 Create Activity

In this step, you have options for a number of predefined activities for different uses. In this tutorial, you'll just start with a blank activity. Select that and click Next.

![][3]

[3]: images/programming-fundamentals-with-android/create-activity.png

### 3.4 Name the activity

In this step you can set the name of the Java and User Interface file, but you don't need to do that in this case. 

The only setting you will need to change is the Title. Change that to "<YourName>'s Utility App" and click Finish.

Your project will then be created and loaded with the required components to run an Android App.

![][4]

[4]: images/programming-fundamentals-with-android/name-the-activity.png

### 3.5 Make a test run

After the project has been created, you'll notice that it displays the Design view of your User Interface. 

You can run this app in the emulator or on a device by clicking the green play button in the tool bar. Android Studio will then prompt you for which device or emulator you wish to run your app on. Choose an appropriate option and click Ok.

![][5]

[5]: images/programming-fundamentals-with-android/make-a-test-run.png

### 3.6 The app is running!

Your app should load on the device or emulator you chose!

Hello World, indeed.

![][6]

[6]: images/programming-fundamentals-with-android/the-app-is-running-.png

### 3.7 Configure the first screen

Open the activity_main.xml file under res/layout and delete the Text View which reads "Hello World".

![][7]

[7]: images/programming-fundamentals-with-android/configure-the-first-screen.png

### 3.8 Change to the Text Editor

To configure the layout manager, you will need to edit the XML text directly. 

Click on the Text editor tab at the bottom of the window.

![][8]

[8]: images/programming-fundamentals-with-android/change-to-the-text-editor.png

### 3.9 Set the Layout Manager

The main screen is going to be initially a list of buttons linking to the various utilities with a heading. For this, a relative layout (the default) may be too complex.

A vertically organised linear layout will be easier to organise for this purpose. 

Change the references to RelativeLayout to LinearLayout and add in the attribute android:orientation and set it to vertical.

![][9]

[9]: images/programming-fundamentals-with-android/set-the-layout-manager.png

### 3.10 Create a heading

Switch back to the Design view and drag out a Large View from the palette and drop it in the centre at the top of the Screen.

![][10]

[10]: images/programming-fundamentals-with-android/create-a-heading.png

### 3.11 Configure the Heading

To change what the Text View displays and how it displays it, select the element in the Design view and look at the properties. There are a number of properties that you'll need to change in the list.

The first is the layout:width. Set this to "match_parent"

The second is Gravity. Expand the list and tick the box for Center-Horizontal

The last is the Text. Change the text entry to the name of your app. In this case it's "<YourName>'s Utility App"

![][11]

[11]: images/programming-fundamentals-with-android/configure-the-heading.png

### 3.12 The structure is complete

The main app has now been configured so that you can easily add new elements to the User Interface to link to new Activities.

![][12]

[12]: images/programming-fundamentals-with-android/the-structure-is-complete.png

## 4. Configure Change Calculator

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

## 5. Change Calculator

In this section you will create a utility to calculate the change required from a purchase in a shop. Given the total of the purchase as well as how much the customer handed over, the utility will inform the user how many $2, $1, 50c, 20c, 10c & 5c pieces are needed to return to the customer.

This section of the tutorial will demonstrate the use of variables, arithmetic operations, sequencing and modular programing.

### 5.1 Configure the User Interface's Layout Manager

To start with, change the layout of the User Interface in the same manner as you did for the main activity.

In the Text editor, change the overall layout manager to Linear Layout and set the orientation to vertical.

![][18]

[18]: images/programming-fundamentals-with-android/configure-the-user-interface-s-layout-manager.png

### 5.2 Prompt and Collect the Total Amount

Switch back to the Design editor, drag out a Plain Text View, then under Text Fields, drag out "Number Decimal" into the design view.

Change the attributes of the Text View so that the layout:width is "fill_parent" and the Text is "Enter the Total Amount".

Select the Edit Text and change the id to "edtTtotalAmount". This will allow you to access the value entered when writing code.

![][19]

[19]: images/programming-fundamentals-with-android/prompt-and-collect-the-total-amount.png

### 5.3 Add the Amount Handed In values.

Perform the same step as above, instead this time add in Plain Text View and Number (decimal) elements underneath the existing ones.

Set the text of the label to "Enter the Amount Handed In" and the layout:width to "match_parent".

Set the id of the Edit Text to be "edtHandedIn"

![][20]

[20]: images/programming-fundamentals-with-android/add-the-amount-handed-in-values.png

### 5.4 Add the Calculate button

Drag a Button from the palette and place it in the centre of the view underneath the Edit Text. Set the following attributes:

     text: Calculate Change
     layout_width: fill_parent
     id: btnCalc
     onClick: calculateChange



![][21]

[21]: images/programming-fundamentals-with-android/add-the-calculate-button.png

### 5.5 Add the result fields

You will need to create two Plain Text views to display the result. The first is simply a heading, and the second is showing the calculated result as a string.

For the heading Text View, drag out a Plain Text View and set the following attributes:

     text: You will need the following coins to make the change
     layout_width: fill_parent
     gravity: center_horizontal

For the result, drag out another Plain Text View and set the following attributes:

     layout_width: fill_parent
     layout_height: fill_parent
     id: txtResult
     text: The result will display here



![][22]

[22]: images/programming-fundamentals-with-android/add-the-result-fields.png

### 5.6 User Interface complete!

That's it for the UI. To ensure that you have it all completed, you can change to the text editor view and confirm that the XML matches below:

     <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
         xmlns:tools="http://schemas.android.com/tools" android:layout_width="match_parent"
         android:layout_height="match_parent" android:paddingLeft="@dimen/activity_horizontal_margin"
         android:paddingRight="@dimen/activity_horizontal_margin"
         android:paddingTop="@dimen/activity_vertical_margin"
         android:paddingBottom="@dimen/activity_vertical_margin"
         tools:context="com.rustyoldcatgames.ryansutilityapp.ChangeCalculator"
         android:orientation="vertical">
         <TextView
             android:layout_width="match_parent"
             android:layout_height="wrap_content"
             android:text="Enter the Total Amount"
             android:id="@+id/textView2"
             android:layout_gravity="center_horizontal" />
         <EditText
             android:layout_width="fill_parent"
             android:layout_height="wrap_content"
             android:inputType="numberDecimal"
             android:ems="10"
             android:id="@+id/edtTtotalAmount"
             android:layout_gravity="center_horizontal" />
         <TextView
             android:layout_width="match_parent"
             android:layout_height="wrap_content"
             android:text="Enter the Amount Handed In"
             android:id="@+id/textView3" />
         <EditText
             android:layout_width="match_parent"
             android:layout_height="wrap_content"
             android:inputType="numberDecimal"
             android:ems="10"
             android:id="@+id/edtHandedIn"
             android:layout_gravity="center_horizontal" />
         <Button
             android:layout_width="fill_parent"
             android:layout_height="wrap_content"
             android:text="Calculate Change"
             android:id="@+id/btnCalc"
             android:layout_gravity="center_horizontal" 
             android:onClick="calculateChange"/>
         <TextView
             android:layout_width="match_parent"
             android:layout_height="wrap_content"
             android:text="You will need the following coins to make the change."
             android:id="@+id/textView4"
             android:gravity="center_horizontal" />
         <TextView
             android:layout_width="fill_parent"
             android:layout_height="fill_parent"
             android:text="The result will display here"
             android:id="@+id/txtResult"
             android:layout_gravity="center_horizontal" />
     </LinearLayout>

Save the file.

### 5.7 Create the variables for UI Elements

Open the ChangeCalculator java file and define variables for the two Edit Texts and the final results Text View.

Make sure these are placed in the correct position as they are global variables, meaning that all methods can access them.

![][23]

[23]: images/programming-fundamentals-with-android/create-the-variables-for-ui-elements.png

### 5.8 Link the UI Elements to code

Modify the onCreate() method to include the code to link each of the variables you created to the relevant UI elements.

![][24]

[24]: images/programming-fundamentals-with-android/link-the-ui-elements-to-code.png

### 5.9 Create the calculateChange() method

Towards the bottom of the java file, create the method stub for the calculateChange() that will be called when the user taps the button on screen.

![][25]

[25]: images/programming-fundamentals-with-android/create-the-calculatechange---method.png

### 5.10 Define the required variables

You will need a number of variables for this method to run correctly. The first is a value to store the total amount of purchases, the second is the amount handed over by the customer.  The third is a variable to keep track of the how much money is left to process. These will be defined as "double"s as they will need to contain decimal values.

You will also need separate variables to hold each of the calculated amounts of $2, $1, 50c, 20c, 10c, and 5c coins. These will be defined as "int"s as they will only hold whole numbers.

The last is the String which will contain the final answer to provide back to the user.

![][26]

[26]: images/programming-fundamentals-with-android/define-the-required-variables.png

### 5.11 Collect the user provided values

Now that you've linked the code to the UI Elements, it is time to extract the values that the user has entered. At this point, you're assuming the user has entered something - this can be fixed later as an extension exercise.

These two lines of code are complex lines which access the Edit Text, run a method which extracts the text from the UI Element and converts it to a string value using toString(). Then converts that string into a variable which is a double.

![][27]

[27]: images/programming-fundamentals-with-android/collect-the-user-provided-values.png

### 5.12 Calculate the difference between the amounts

Use the remainder variable to calculate the difference between the customerTotal and total values.

![][28]

[28]: images/programming-fundamentals-with-android/calculate-the-difference-between-the-amounts.png

### 5.13 Calculate the number of $2 coins needed

Now you have all the information you need to start calculating the result. 

To calculate the number of $2 coins needed, all you need to do is strip the decimal value from the double by casting it as an int and then dividing it by 2.

Set the change variable to concatenate "$2: " and the value stored in the two variable.

![][29]

[29]: images/programming-fundamentals-with-android/calculate-the-number-of--2-coins-needed.png

### 5.14 Calculate the number of $1 coins needed

Before you can calculate the $1 coins, you will need to update the remainder by reducing it by the number of $2 coins already calculated.

Then you can perform a similar process as previously done for the $2 coins. This time however you don't need to divide by anything, simply casting it as an int is sufficient.

Update the change String to include the new one variable. The \n part of the string creates a new line character.

![][30]

[30]: images/programming-fundamentals-with-android/calculate-the-number-of--1-coins-needed.png

### 5.15 Calculate the remainder of the coins

To make the code simpler, you can multiply the remainder by 100 so that you can continue to deal in whole numbers.

The remainder of the coins are calculated in the same fashion as previously done.

![][31]

[31]: images/programming-fundamentals-with-android/calculate-the-remainder-of-the-coins.png

### 5.16 Update the Change string

Update the change string to include all the values calculated.

![][32]

[32]: images/programming-fundamentals-with-android/update-the-change-string.png

### 5.17 Inform the user!

Now that all the values have been calculated, update the screen to show the user.

![][33]

[33]: images/programming-fundamentals-with-android/inform-the-user-.png

### 5.18 Test the app

Run the app, and click on the Change Calculator button. Enter some values and click on the Calculate Change button to test the output.

There are a few bugs in the app, but basically it works! Congratulations. 

Try an identify the bugs.

![][34]

[34]: images/programming-fundamentals-with-android/test-the-app.png

## 6. New Utility - Dice Roll Simulator

Before you can create this new utility in your app, you'll need to create a new activity and link to it from the main screen - much like you did for the Change Calculator.

### 6.1 Create a new Activity

In the same manner as you did for the Change Calculator, create a new activity to hold the dice rolling simualtor.

To create a new Activity, go to File and click New. A menu appears and Choose Blank Activity under Activity.

![][35]

[35]: images/programming-fundamentals-with-android/create-a-new-activity-1.png

### 6.2 Configure the Activity

Set the details to the activity to uniquely identify it.

In this case, set the Activity Name to be "DiceRollSimulator". All the other values will change accordingly.

Click Finish.

This will create the necessary files to run an activity as well as the basic structure to those files.

![][36]

[36]: images/programming-fundamentals-with-android/configure-the-activity-1.png

### 6.3 Drag out new Button

Open the activity_main.xml and make sure you're on the Design view.

Drag out a new button onto the view underneath the existing "Change Calculator" button.

![][37]

[37]: images/programming-fundamentals-with-android/drag-out-new-button.png

### 6.4 Define the attributes for the button

Change the attributes so the following are changed:

     android:layout_width="fill_parent"
     android:text="Dice Roll Simulator"
     android:id="@+id/btnDice"
     android:onClick="diceRoll" 

![][38]

[38]: images/programming-fundamentals-with-android/define-the-attributes-for-the-button.png

### 6.5 Create the diceRoll() method

Open the MainActivity file in the java folder (and then the reverse domain name folder).

Towards the end of the file, create the empty method stub for diceRoll(). You need to include the View v arguments to make sure it runs correctly. You will learn about method and arguments in more detail later.

This method is extremely similar to the changeCalc() method, except for only two changes.

![][39]

[39]: images/programming-fundamentals-with-android/create-the-diceroll---method.png

## 7. Dice Roll Simulator

The dice roll simulator utility will allow the user to select the number of sides of a dice and how many times the dice is rolled. After processing, the app will output the number of time each value was rolled.

Now that you've created all the necessary files and connections, it's time to design the UI. The design of the UI will be similar to the Change Calculator Utility.

### 7.1 Set the Layout Manager to be LinearLayout

Open the activity_dice_roll_simulator.xml and change to the Text Editor view. Change the RelativeLayout in the XML to LinearLayout and add the orientation attribute and set it to vertical.

![][40]

[40]: images/programming-fundamentals-with-android/set-the-layout-manager-to-be-linearlayout.png

### 7.2 Prompting the user - How many sides?

Switch back to the Design view and drag out a label to prompt the user to select how many sides. Drop it at the top of the view.

Set the following attributes to the label

     android:layout_width="fill_parent"
     android:text="How many sides does the dice have?"

![][41]

[41]: images/programming-fundamentals-with-android/prompting-the-user---how-many-sides-.png

### 7.3 Collect the number

In this version of your dice roll simulator, you will specify the number of sides of the dice to be a standard 6 sided dice.

In a later version you will be able to modify this to allow for any number of sides.

Drag out a Medium Text field and set the attributes to be the following:

     android:layout_width="fill_parent"
     android:text="6"

![][42]

[42]: images/programming-fundamentals-with-android/collect-the-number.png

### 7.4 Prompt the user for the number of times to roll

Drag out a label and an edit text (number) onto the view underneath the other elements setting the following attributes:

The Label:

     android:text="How many rolls?"
     android:layout_width="fill_parent"

The Number Text Field

     android:id="@+id/edtNoOfRolls"

![][43]

[43]: images/programming-fundamentals-with-android/prompt-the-user-for-the-number-of-times-to-roll.png

### 7.5 Create the Processing button

This button will be the start the processing of rolling the dice and then outputting to the user. 

Drag out a button and the set the following attributes:

     android:layout_width="fill_parent"
     android:text="Roll the Dice!"
     android:id="@+id/btnRoll"
     android:onClick="rollDice"

![][44]

[44]: images/programming-fundamentals-with-android/create-the-processing-button.png

### 7.6 Output Window

Drag out a Plain TextView to act as the output for the utility. Set the following attributes:

     android:layout_width="fill_parent"
     android:layout_height="fill_parent"
     android:text="The result will display here"
     android:id="@+id/txtResult"
     android:layout_gravity="center_horizontal"

The UI is now complete for this Utility!

Save the file.

![][45]

[45]: images/programming-fundamentals-with-android/output-window.png

### 7.7 Connect the code to the UI

Open the DiceRollSimulator.java file to define the variables and create the connections required to the code.

![][46]

[46]: images/programming-fundamentals-with-android/connect-the-code-to-the-ui.png

### 7.8 Define the method

Define the method stub for rollDice() that you entered into the onClick attribute for the button.

![][47]

[47]: images/programming-fundamentals-with-android/define-the-method.png

### 7.9 Collect the variables required

Define two integer variables to extract and store the values the EditText UI elements.

You'll notice that you have to run the getText() command on each of the EditText's, and then convert the result from that into a string using the toString() command. The resulting String then needs to be parsed to convert it from a string to an Integer.

Now you have integer values that you can use to finalise the functionality.

![][48]

[48]: images/programming-fundamentals-with-android/collect-the-variables-required.png

### 7.10 Define the counter variables

To keep track of how many times each number is rolled, you will need to define integer values to keep track of them.

There are more efficient methods to do this (for instance using Arrays) but you'll learn about that later. 

Define 6 integer values, initially set at 0;

![][49]

[49]: images/programming-fundamentals-with-android/define-the-counter-variables.png

### 7.11 Set up the Loop Control Variable

The basic outline of what needs to happen now is:

     Loop Start
     Generate a random number between 1 and the 6 inclusive
     Add one to the counter for that number
     Has the code looped enough? Yes, break out. No? Go back to the start and go again.

In this step, you'll need to define an integer variable to keep track of how many times the loop has been run. This value will be checked against the value the user entered. If the loop counter is less than the user value, then the loop continues. Once the loop counter reaches the user value, the loop is finished.

Many of the loops you write will need a variable to keep track of how many times the loop runs and it is referred to as the s.

![][50]

[50]: images/programming-fundamentals-with-android/set-up-the-loop-control-variable.png

### 7.12 Define the loop

Define the basic structure of a for loop.

In the for loop definition there are three components separated by semi-colons (;). The first component, in this case loopCounter = 0, is the starting position of the loop counter variable.

The second component - loopCounter < totalNumberOfRolls - is the condition that is tested after each time the code in the loop is executed. If the condition result is true, then the loop runs through again. If it is false, then the program code resumes after the loops closing }.

The third component - loopCounter++ - is the code that is run after each time the code in the loop is executed, but *before* the condition is tested. In this case, loopCounter++ increases the value in loopCounter by 1.

It is important to note that any or all of these components can be empty and will still be considered a valid loop. So this code is perfectly valid:

     for ( ; ; ) {
                 
     }

You, as the developer would have to do more work inside the loop however.

![][51]

[51]: images/programming-fundamentals-with-android/define-the-loop.png

### 7.13 Generate a random number

First off, define an integer value to store the random number that will be generated.

Next, inside the loop, generate a random number and store it into the variable.

Math.random() generates and returns a random decimal value between 0.0 and 1.0, however it won't generate 1.0. So, you will need to multiply the result of that by 6 to get a range of values between 0.0 and 5.99999.. and then add 1 to it to get the range between 1.0 and 6.99999..

Converting it from a decimal value to an integer through the (int) cast, drops the decimal value, giving you a possible range from 1 to 6.

![][52]

[52]: images/programming-fundamentals-with-android/generate-a-random-number.png

### 7.14 Increase the value counters

Now that a random number has been generated, you will want to find out what the number is and increase the counter for whichever value it is.

So, if the random roll is 1, then increase countOne by 1.

If it's 2 then increase countTwo by 1

etc.

![][53]

[53]: images/programming-fundamentals-with-android/increase-the-value-counters.png

### 7.15 Generate the result string

After the loop runs, you have all the information to report back to the user.

Define a new result string and concatenate all integer values into one string to output.

![][54]

[54]: images/programming-fundamentals-with-android/generate-the-result-string.png

### 7.16 Update the Result to screen

After generating the resultString, set the text view to display the result string.

![][55]

[55]: images/programming-fundamentals-with-android/update-the-result-to-screen.png

### 7.17 Run the app!

Test your app. Test it a few times with the same values and see the differences between then runs.

Check that the addition of all the results equals the number of rolls. For instance, 336+330+300+376+319+339 = 2000 (it should).

![][56]

[56]: images/programming-fundamentals-with-android/run-the-app-.png