# Create Project

To begin with, you'll need to create a project to hold all the different utilities.

### 3.1 Project Name

In Android Studio, go to File and choose New Project.

The New Project Wizard will appear. Enter the name of the project and the Company Domain. Name the project "<YourName>'s Utility App"

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