
# Ex.No:12 Design an application that draws basic graphical primitives on the screen.


## AIM:

To create and design an android application that draws basic graphical primitives on the screen using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “graphical″ and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Draw basic object details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to create and design an android application that draws basic graphical primitives on the screen.
Developed by: PREETHI S
Registeration Number : 212221040132
*/
```
activity_main.xml:
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android" xmlns:app="http://schemas.android.com/apk/res-auto" xmlns:tools="http://schemas.android.com/tools" android:layout_width="match_parent" android:layout_height="match_parent"
tools:context=".MainActivity">
<ImageView
android:layout_width="match_parent" android:layout_height="match_parent" android:id="@+id/imageView" />
</RelativeLayout>
MainActivity.java:
package com.example.graphica;
import androidx.appcompat.app.AppCompatActivity; import
androidx.constraintlayout.widget.ConstraintLayout;
import android.graphics.Bitmap;
import android.graphics.Canvas;
import android.graphics.Color; import
android.graphics.Paint;
import android.graphics.drawable.BitmapDrawable;
import android.os.Bundle;
import android.widget.ImageView;
public class MainActivity extends AppCompatActivity {
@Override
protected void onCreate(Bundle savedInstanceState)
{super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
Bitmap bg = Bitmap.createBitmap(720, 1280, Bitmap.Config.ARGB_8888);
//Setting the Bitmap as background for the ImageView ImageView
i = (ImageView) findViewById(R.id.imageView);
i.setBackgroundDrawable(new BitmapDrawable(bg));
//Creating the Canvas Object Canvas
canvas = new Canvas(bg);
//Creating the Paint Object and set its color & TextSizePaint
paint = new Paint(); paint.setColor(Color.GREEN);
paint.setTextSize(50);
//To draw a Rectangle canvas.drawText("Rectangle", 420, 150, paint);
canvas.drawRect(400, 200, 650, 700, paint);
//To draw a Circle canvas.drawText("Circle", 120, 150, paint);
canvas.drawCircle(200, 350, 150, paint);
//To draw a Square canvas.drawText("Square", 120, 800, paint);
canvas.drawRect(50, 850, 350, 1150, paint);
//To draw a Line canvas.drawText("Line", 480, 800, paint);
canvas.drawLine(520, 850, 520, 1150, paint);
}
}


## OUTPUT

![image](https://github.com/Preethi132/Mobile-Application-Development/assets/136288465/bebd6d58-8a39-414d-bbe3-4a7084b58f31)



## RESULT
Thus a Simple Android Application to create and design an android application that draws basic graphical primitives on the screen using Android Studio is developed and executed successfully.
