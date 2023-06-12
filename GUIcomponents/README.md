# Ex.No: 2 To develop an application that uses GUI Components with Fonts and Colors. 
Note: Create button for colors and fonts while clicking color or font button should change 


## AIM:

To create an application that uses GUI Components with Fonts and Colors using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:


## PROGRAM:
```
/*
Program to print the text “GUIcomponent”.
Developed by: PREETHI S
Registeration Number : 212221040132
activity_main.xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
212221040132|PREETHI S|CSE
android:layout_width="match_parent"
android:layout_height="match_parent"
android:orientation="vertical"
tools:context=".MainActivity">
<TextView
android:id="@+id/textView"
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:layout_margin="30dp"
android:gravity="center"
android:text="Student Details"
android:textSize="25sp"
android:textStyle="bold" />
<TextView
android:id="@+id/textView2"
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:layout_margin="30dp"
android:gravity="left"
android:text="Name:Preethi S"
android:textSize="25sp"
android:textStyle="bold" />
<TextView
android:id="@+id/textView3"
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:layout_margin="30dp"
android:gravity="left"
android:text="Reg_NO:212221040132"
android:textSize="25sp"
android:textStyle="bold" />
<TextView
android:id="@+id/textView4"
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:layout_margin="30dp"
android:gravity="left"
android:text="Department:CSE"
android:textSize="25sp"
android:textStyle="bold" />
<TextView
android:id="@+id/textView5"
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:layout_margin="30dp"
android:gravity="left"
android:text="Year:2nd Year"
android:textSize="25sp"
android:textStyle="bold" />
<LinearLayout
android:layout_width="match_parent"
android:layout_height="match_parent"
android:orientation="horizontal">
<Button
android:id="@+id/button1"
android:layout_width="108dp"
android:layout_height="wrap_content"
android:layout_margin="18dp"
android:text="size"
android:textSize="14sp" />
<Button
android:id="@+id/button2"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_margin="18dp"
android:text="color"
android:textSize="14sp" />
<Button
android:id="@+id/button3"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_margin="18dp"
android:text="Style"
android:textSize="15sp" />
</LinearLayout>
</LinearLayout>
MainActivity.java
package com.example.Project02;
import androidx.appcompat.app.AppCompatActivity;
import android.graphics.Color;
import android.graphics.Typeface;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;
public class MainActivity extends AppCompatActivity {
int ch = 1;
float font = 30;
@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
TextView t = findViewById(R.id.textView);
TextView t1 = findViewById(R.id.textView2);
TextView t2 = findViewById(R.id.textView3);
TextView t3 = findViewById(R.id.textView4);
TextView t4 = findViewById(R.id.textView5);
Button b1 = findViewById(R.id.button1);
b1.setOnClickListener(new View.OnClickListener() {
@Override
public void onClick(View view) {
t.setTextSize(font);
t1.setTextSize(font);
t2.setTextSize(font);
t3.setTextSize(font);
t4.setTextSize(font);
if (font == 50) {
font = 30;
} else {
font += 5;
}
}
});
Button b2 = findViewById(R.id.button2);
b2.setOnClickListener(new View.OnClickListener() {
@Override
public void onClick(View v) {
switch (ch) {
case 1:
t.setTextColor(Color.RED);
t1.setTextColor(Color.RED);
t2.setTextColor(Color.RED);
t3.setTextColor(Color.RED);
t4.setTextColor(Color.RED);
break;
case 2:
t.setTextColor(Color.GREEN);
t1.setTextColor(Color.GREEN);
t2.setTextColor(Color.GREEN);
212221040132|PREETHI S|CSE
t3.setTextColor(Color.GREEN);
t4.setTextColor(Color.GREEN);
break;
case 3:
t.setTextColor(Color.BLUE);
t1.setTextColor(Color.BLUE);
t2.setTextColor(Color.BLUE);
t3.setTextColor(Color.BLUE);
t4.setTextColor(Color.BLUE);
break;
case 4:
t.setTextColor(Color.CYAN);
t1.setTextColor(Color.CYAN);
t2.setTextColor(Color.CYAN);
t3.setTextColor(Color.CYAN);
t4.setTextColor(Color.CYAN);
break;
case 5:
t.setTextColor(Color.YELLOW);
t1.setTextColor(Color.YELLOW);
t2.setTextColor(Color.YELLOW);
t3.setTextColor(Color.YELLOW);
t4.setTextColor(Color.YELLOW);
break;
case 6:
t.setTextColor(Color.MAGENTA);
t1.setTextColor(Color.MAGENTA);
t2.setTextColor(Color.MAGENTA);
t3.setTextColor(Color.MAGENTA);
t4.setTextColor(Color.MAGENTA);
break;
}
ch++;
if (ch == 7) {
ch = 1;
}
}
});
Button b3 = findViewById(R.id.button3);
b3.setOnClickListener(new View.OnClickListener() {
@Override
public void onClick(View v) {
switch (ch) {
case 1:
t1.setTypeface(null, Typeface.BOLD);
t.setTypeface(null, Typeface.BOLD);
t2.setTypeface(null, Typeface.BOLD);
t3.setTypeface(null, Typeface.BOLD);
t4.setTypeface(null, Typeface.BOLD);
break;
case 2:
t1.setTypeface(null, Typeface.ITALIC);
t.setTypeface(null, Typeface.ITALIC);
t2.setTypeface(null, Typeface.ITALIC);
t3.setTypeface(null, Typeface.ITALIC);
t4.setTypeface(null, Typeface.ITALIC);
break;
case 3:
t.setTypeface(null, Typeface.BOLD_ITALIC);
t1.setTypeface(null, Typeface.BOLD_ITALIC);
t2.setTypeface(null, Typeface.BOLD_ITALIC);
t3.setTypeface(null, Typeface.BOLD_ITALIC);
t4.setTypeface(null, Typeface.BOLD_ITALIC);
break;
case 4:
t.setTypeface(null, Typeface.NORMAL);
t1.setTypeface(null, Typeface.NORMAL);
t2.setTypeface(null, Typeface.NORMAL);
t3.setTypeface(null, Typeface.NORMAL);
t4.setTypeface(null, Typeface.NORMAL);
break;
}
ch++;
if (ch == 5) {
ch = 1;
}
}
});
}
}
*/
```

## OUTPUT




## RESULT
Thus a Simple Android Application that uses GUI Components with Fonts and Colors using Android Studio is developed and executed successfully.


