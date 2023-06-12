# Ex.No:10 To create a option menu to display menu items.


## AIM:

To create a option menu to display menu items using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
Step 1: Start the program
Step 2: Create a new Android project in Android Studio or open an existing project. Step 3: Open the XML layout file for the activity where you want to display the options menu(usually
named activity_main.xml). Step 4: Add a Toolbar widget to the layout file to act as the action bar for the activity. Step 5: In the Java file for the activity (usually named MainActivity.java):
Step 6: Override the onCreateOptionsMenu() method to inflate the menu resource file and
display the options menu. Step 7: Implement the onOptionsItemSelected() method to handle the selected menu item's
actions. Step 8: Create an XML file in the res/menu directory to define the menu items. Step 9: Specify the menu items in the XML file, including their IDs, titles, and other
attributes. Step 10: Handle the selected menu item's actions in the onOptionsItemSelected() method
based on its ID. Step 11: Customize the menu items and their behavior as per your requirements. Step 12: Run the Android application to see the options menu displayed in the activity's actionbar. Step 13: Implement the desired actions for each menu item by adding the necessary code
within the onOptionsItemSelected() method. Step 14: End the program

## PROGRAM:
```
/*
Program to print the text “optionmenu”.
Developed by: PREETHI S
Registeration Number : 212221040132
*/
```
activity_main.xml:
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
xmlns:android="http://schemas.android.com/apk/res/android" xmlns:app="http://schemas.android.com/apk/res-auto" xmlns:tools="http://schemas.android.com/tools" android:layout_width="match_parent" android:layout_height="match_parent"
tools:context=".MainActivity">
<TextView
android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="Hello World!" app:layout_constraintBottom_toBottomOf="parent" app:layout_constraintEnd_toEndOf="parent" app:layout_constraintStart_toStartOf="parent" app:layout_constraintTop_toTopOf="parent" />
</androidx.constraintlayout.widget.ConstraintLayout>
menu_item.xml:
<?xml version="1.0" encoding="utf-8"?>
<menu xmlns:android="http://schemas.android.com/apk/res/android" xmlns:app="http://schemas.android.com/apk/res-auto" xmlns:tools="http://schemas.android.com/tools"
tools:context=".MainActivity">
<item
android:id="@+id/message" android:icon="@android:drawable/ic_menu_send" android:title="message" app:showAsAction="always" />
<item
android:id="@+id/picture" android:icon="@android:drawable/ic_menu_gallery" android:title="picture" app:showAsAction="always|withText" />
<item
android:id="@+id/mode" android:icon="@android:drawable/ic_menu_call" android:title="mode" app:showAsAction="always" />
<item
android:id="@+id/about" android:icon="@android:drawable/ic_dialog_info" android:title="calculator" app:showAsAction="never|withText" />
<item
android:id="@+id/exit" android:title="exit" app:showAsAction="never" />
</menu>
MainActivity.java:
package com.example.optionmenu;
import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.os.Bundle;
import android.view.Menu;
import android.view.MenuItem;
import android.widget.Toast;
public class MainActivity extends AppCompatActivity
{
private Intent i2;
@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
}
public boolean onCreateOptionsMenu(Menu menu) {
getMenuInflater().inflate(R.menu.my_menu, menu);
return true;
}
public boolean onOptionsItemSelected(MenuItem
item) {
switch (item.getItemId()) {
case R.id.message:
Toast.makeText(getApplicationContext(), "Shows
share icon", Toast.LENGTH_SHORT).show();
return true;
case R.id.picture:
Toast.makeText(getApplicationContext(), "Shows
image icon", Toast.LENGTH_SHORT).show();
startActivity(i2);
return (true);
case R.id.mode:
Toast.makeText(getApplicationContext(), "Shows
call icon", Toast.LENGTH_SHORT).show();
return (true);
case R.id.about:
Toast.makeText(getApplicationContext(), "calculator
menu",
Toast.LENGTH_SHORT).show();
return (true);
case R.id.exit:
finish();
return (true);}
return (super.onOptionsItemSelected(item)); }

## OUTPUT

![image](https://github.com/Preethi132/Mobile-Application-Development/assets/136288465/4859c71d-1880-4e47-b4c2-b240cfe77c48)
![image](https://github.com/Preethi132/Mobile-Application-Development/assets/136288465/bca0bead-1eab-4b80-81c9-e8c63b25d1e8)



## RESULT
Thus a Simple Android Application to create a option menu to display menu items using Android Studio is developed and executed successfully.


