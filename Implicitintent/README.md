# Ex.No:3 Develop program to create a text field and a button “Navigate”. When you enter “www.google.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the google page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
Step  1: Open Android Studio and create a new project.

Step 2:In the activity_main.xml file, design the layout with a TextInputEditText element for the text field and a Button element for the "Navigate" button.

Step 3:In the MainActivity.java file, retrieve references to the text field and the button using their IDs.

Step 4:Set an OnClickListener for the button.

Step 5:Inside the OnClickListener, retrieve the text entered in the text field using the getText() method.

Step 6:Create an Intent object to open a web page with the URL obtained from the text field.

Step 7:Set the action of the intent to Intent.ACTION_VIEW to indicate that the intent is used for viewing something.

Step 8:Set the data of the intent to the URL obtained from the text field using the Uri.parse() method.

Step 9:Set the type of the intent to "text/html" or "text/plain" to specify the type of data being viewed.

Step 10:Use the startActivity() method with the intent to start the activity that can handle the implicit intent.

Step 11:Run the application on an Android device or emulator to see the desired functionality.


## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by: PREETHI S
Registeration Number : 212221040132
*/
```
activity_main.xml:
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
xmlns:android="http://schemas.android.com/apk/res/android" xmlns:app="http://schemas.android.com/apk/res-auto" xmlns:tools="http://schemas.android.com/tools" android:layout_width="match_parent" android:layout_height="match_parent"
tools:context=".MainActivity">
<EditText android:id="@+id/editText" android:layout_width="wrap_content" 
android:layout_height="wrap_content" 
android:layout_marginStart="8dp" 
android:layout_marginEnd="8dp" android:ems="10" 
android:importantForAutofill="no" android:inputType="text" 
android:minHeight="48dp" 
app:layout_constraintBottom_toBottomOf="parent" 
app:layout_constraintEnd_toEndOf="parent" 
app:layout_constraintHorizontal_bias="0.589" 
app:layout_constraintStart_toStartOf="parent" 
app:layout_constraintTop_toTopOf="parent" 
app:layout_constraintVertical_bias="0.476"
tools:ignore="LabelFor,TextFields,SpeakableTextPresentCheck" />
<Button
android:id="@+id/button" android:layout_width="wrap_content" 
        android:layout_height="wrap_content" android:layout_marginStart="156dp" 
        android:layout_marginTop="172dp" android:text="@string/app_name" 
        app:layout_constraintBottom_toBottomOf="parent"
app:layout_constraintEnd_toEndOf="parent" 
        app:layout_constraintHorizontal_bias="0.089" 
        app:layout_constraintStart_toStartOf="parent" app:layout_constraintTop_toTopOf="parent" 
        app:layout_constraintVertical_bias="0.518" />
</androidx.constraintlayout.widget.ConstraintLayout>
MainActivity.java
package com.example.implicitint;
import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.net.Uri; import
android.os.Bundle; import
android.widget.Button;
import android.widget.EditText;
public class MainActivity extends AppCompatActivity
{Button button;
EditText editText;
@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
button = findViewById(R.id.button); editText =findViewById(R.id.editText);
button.setOnClickListener(view -> { String
url=editText.getText().toString();
Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
startActivity(intent);
});
}
}


## OUTPUT

![image](https://github.com/Preethi132/Mobile-Application-Development/assets/136288465/1c13ba5c-963d-4c16-be1a-766144ae5e76)
![image](https://github.com/Preethi132/Mobile-Application-Development/assets/136288465/4dedb88d-a00a-48b1-b427-7a3f00e6bb88)



## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the google page using Android Studio is developed and executed successfully.


