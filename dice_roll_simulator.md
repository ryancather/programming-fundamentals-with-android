# Dice Roll Simulator

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