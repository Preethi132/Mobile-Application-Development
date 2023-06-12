
# Ex.No:7 Develop an android application to display the place name with image using list view in android studio.


## AIM:

To create and develop the application to display the place name with image using list view in android studio

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “listview″ and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Get contacts details and Display details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the list of item.
Developed by: PREETHI S
Registeration Number : 212221040132
*/
```
activity_main.xml:
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android" xmlns:app="http://schemas.android.com/apk/res-auto" xmlns:tools="http://schemas.android.com/tools" android:layout_width="match_parent" android:layout_height="match_parent" android:orientation="vertical"
tools:context=".MainActivity">
<ListView
android:id="@+id/simpleListView"
android:layout_width="fill_parent" android:layout_height="wrap_content" android:divider="@color/white" android:dividerHeight="1dp" android:footerDividersEnabled="false" />
</LinearLayout>
activity_listview.xml:
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android" android:layout_width="match_parent" android:layout_height="match_parent" android:orientation="horizontal">
<ImageView
android:id="@+id/icon" android:layout_width="100dp" android:layout_height="100dp" />
<TextView
android:id="@+id/textView" android:layout_width="fill_parent" android:layout_height="wrap_content" android:layout_gravity="center" android:textColor="@color/black" />
</LinearLayout>
MainActivity.java:
package com.example.listview;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.widget.ListView;
public class MainActivity extends AppCompatActivity {
ListView simpleList;
String countryList[] = {"Eiffel Tower", "Mahabalipuram", "Hawai",};
int flags[] = {R.drawable.eiffel, R.drawable.maha, R.drawable.hawai};
@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
simpleList = (ListView) findViewById(R.id.simpleListView);
CustomAdapter customAdapter = new CustomAdapter(getApplicationContext(), countryList, flags);
simpleList.setAdapter(customAdapter);
}
}
CustomAdapter.java:
package com.example.listview;
import android.content.Context;
import android.view.LayoutInflater;
import android.view.View;
import android.view.ViewGroup;
import android.widget.BaseAdapter;
import android.widget.ImageView;
import android.widget.TextView;
public class CustomAdapter extends BaseAdapter {
Context context;
String countryList[];
int flags[];
LayoutInflater inflter;
public CustomAdapter(Context applicationContext, String[] countryList, int[] flags) {
this.context = context;
this.countryList = countryList;
this.flags = flags;
inflter = (LayoutInflater.from(applicationContext));
}
@Override
public int getCount() {
return countryList.length;
}
@Override
public Object getItem(int i) {
return null;
}
@Override
public long getItemId(int i) {
return 0;
}
@Override
public View getView(int i, View view, ViewGroup viewGroup) {
view = inflter.inflate(R.layout.activity_listview, null);
TextView country = (TextView) view.findViewById(R.id.textView);
ImageView icon = (ImageView) view.findViewById(R.id.icon);
country.setText(countryList[i]);
icon.setImageResource(flags[i]);
return view;
}}


## OUTPUT

![image](https://github.com/Preethi132/Mobile-Application-Development/assets/136288465/df72d9a0-f1b9-4ed8-b878-fde53eb0c7c2)



## RESULT
Thus a Simple Android Application to create and develop the application to display the place name with image using list view in android studio is developed and executed successfully.
