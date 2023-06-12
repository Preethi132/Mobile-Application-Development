# Ex.No:8 To create a gallery control using android studio to display images or photos.


## AIM:

To create a gallery control using android studio to display images or photos.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
Step 1: Create a new Android Studio project.
Step 2:Open the layout file "activity_main.xml". 
Step 3:Add a container layout to hold the gallery images (e.g., GridLayout, RecyclerView, or
ViewPager). 
Step 4:Within the container layout, add ImageView elements to display the images. You canset
the image source using the android:src attribute or programmatically in the code.
Step 5:If using a GridLayout, specify the number of columns using the android:columnCount
attribute. 
Step 6:Customize the layout and appearance of the ImageView elements as desired. 
Step 7:Add any necessary attributes or listeners to handle user interactions, such as clicks onthe
images. 
Step 8:Optionally, create a data source to store the images (e.g., a list or an array of imagereferences). 
Step 9:Bind the data source to the gallery control to populate the images dynamically. 
Step 10:Implement any additional functionality, such as zooming, sliding, or image
transitions, if desired. 
Step 11:Build and run the application to see the gallery control displaying the im


## PROGRAM:
```
/*
Program to print the text “GalleryControl”.
Developed by: PREETHI S
Registeration Number : 212221040132
*/
```
activity_main.xml:
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
xmlns:android="http://schemas.android.com/apk/res/android" xmlns:app="http://schemas.android.com/apk/res-auto" xmlns:tools="http://schemas.android.com/tools" android:layout_width="match_parent" android:layout_height="match_parent"
tools:context=".MainActivity">
<ImageView
android:id="@+id/imageView" android:layout_width="wrap_content" android:layout_height="wrap_content" android:layout_marginTop="36dp" app:layout_constraintBottom_toTopOf="@+id/languagesGallery" app:layout_constraintEnd_toEndOf="parent" app:layout_constraintHorizontal_bias="0.498" app:layout_constraintStart_toStartOf="parent" app:layout_constraintTop_toTopOf="parent"
tools:srcCompat="@tools:sample/avatars" />
<Gallery
android:id="@+id/languagesGallery" android:layout_width="match_parent" android:layout_height="wrap_content" android:layout_marginTop="171dp" android:layout_marginBottom="204dp" android:animationDuration="2000" android:padding="10dp" android:spacing="5dp" android:unselectedAlpha="50" app:layout_constraintBottom_toBottomOf="parent"
app:layout_constraintEnd_toEndOf="parent" app:layout_constraintStart_toStartOf="parent" app:layout_constraintTop_toBottomOf="@+id/imageView" />
</androidx.constraintlayout.widget.ConstraintLayout>
MainActivity.java:
package com.example.gallery_view;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.widget.Gallery;
import android.view.View;
import android.widget.AdapterView;
import android.widget.Gallery;
import android.widget.ImageView;
public class MainActivity extends AppCompatActivity {
Gallery simpleGallery;
CustomizedGalleryAdapter customGalleryAdapter;
ImageView selectedImageView;
int[] images = {R.drawable.bird, R.drawable.bt21,R.drawable.bts,R.drawable.grin};
@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
simpleGallery = (Gallery) findViewById(R.id.languagesGallery);
selectedImageView = (ImageView) findViewById(R.id.imageView);
customGalleryAdapter = new CustomizedGalleryAdapter(getApplicationContext(), images);
simpleGallery.setAdapter(customGalleryAdapter);
simpleGallery.setOnItemClickListener(new AdapterView.OnItemClickListener() {
@Override
public void onItemClick(AdapterView<?> parent, View view, int position, long id) {
selectedImageView.setImageResource(images[position]);
}
});
}
}
CustomizedGalleryAdapter:
package com.example.gallery_view;
import android.content.Context;
import android.view.View;
import android.view.ViewGroup;
import android.widget.BaseAdapter;
import android.widget.Gallery;
import android.widget.ImageView;
public class CustomizedGalleryAdapter extends BaseAdapter {
private Context context;
private int[] images;
public CustomizedGalleryAdapter(Context c, int[] images) {
context = c;
this.images = images;
}
public int getCount() {
return images.length;
}
public Object getItem(int position) {
return position;
}
public long getItemId(int position) {
return position;
}
public View getView(int position, View convertView, ViewGroup parent) {
ImageView imageView = new ImageView(context);
imageView.setImageResource(images[position]);
imageView.setLayoutParams(new Gallery.LayoutParams(200, 200));
return imageView;
}
}



## OUTPUT

![image](https://github.com/Preethi132/Mobile-Application-Development/assets/136288465/e48ec71e-171a-4786-a012-115b6f63374d)



## RESULT
Thus a Simple Android Application to create a gallery control using android studio to display images or photos is developed and executed successfully.


