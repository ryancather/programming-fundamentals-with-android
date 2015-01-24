# New Utility - Dice Roll Simulator

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
