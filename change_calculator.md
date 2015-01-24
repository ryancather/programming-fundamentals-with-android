# Change Calculator

In this section you will create a utility to calculate the change required from a purchase in a shop. Given the total of the purchase as well as how much the customer handed over, the utility will inform the user how many $2, $1, 50c, 20c, 10c & 5c pieces are needed to return to the customer.

This section of the tutorial will demonstrate the use of variables, arithmetic operations, sequencing and modular programming.

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