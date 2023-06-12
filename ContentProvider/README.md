
# Ex.No:5 Create Your Own Content Providers to get Contacts details.


## AIM:

To create your own content providers to get contacts details using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “contentprovider″ and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Get contacts details and Display details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the text create your own content providers to get contacts details.
Developed by: PREETHI S
Registeration Number : 212221040132
*/
```
activity_main.xml:
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
xmlns:android="http://schemas.android.com/apk/res/android" xmlns:app="http://schemas.android.com/apk/res-auto" xmlns:tools="http://schemas.android.com/tools" android:layout_width="match_parent" android:layout_height="match_parent"
tools:context=".MainActivity">
<Button
android:id="@+id/button" android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="Get Contacts" android:onClick="btnGetContactPressed" app:layout_constraintBottom_toBottomOf="parent" app:layout_constraintEnd_toEndOf="parent" app:layout_constraintStart_toStartOf="parent" app:layout_constraintTop_toTopOf="parent"
/>
</androidx.constraintlayout.widget.ConstraintLayout>
AndroidManifest.xml:
<?xml version="1.0" encoding="utf-8"?>
<manifest
xmlns:android="http://schemas.android.com/apk/res/android" xmlns:tools="http://schemas.android.com/tools" package="com.example.contenprovider">
<uses-permission
android:name="android.permission.READ_CONTACTS"></
uses-permission>
<uses-permission
android:name="android.permission.WRITE_CONTACTS"><
/uses-permission>
<application
android:allowBackup="true" android:dataExtractionRules="@xml/data_extraction_rules" android:fullBackupContent="@xml/backup_rules" android:icon="@mipmap/ic_launcher" android:label="@string/app_name" android:supportsRtl="true" android:theme="@style/Theme.ContenProvider"
tools:targetApi="31">
<activity
android:name=".MainActivity" android:exported="true">
<intent-filter>
<action
android:name="android.intent.action.MAIN" />
<category
android:name="android.intent.category.LAUNCHER" />
</intent-filter>
</activity>
</application>
</manifest>
MainActivity.java:
package com.example.contenprovider;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.app.ActivityCompat;
import androidx.core.content.ContextCompat;
import android.Manifest;
import android.annotation.SuppressLint;
import android.content.ContentResolver;
import android.content.pm.PackageManager;
import android.database.Cursor;
import android.net.Uri;
import android.os.Bundle;
import android.provider.ContactsContract;
import android.util.Log;
import android.view.View;
public class MainActivity extends AppCompatActivity {
@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
}
public void btnGetContactPressed(View v){
getPhoneContacts();
}
private void getPhoneContacts(){
if(ContextCompat.checkSelfPermission(this , Manifest.permission.READ_CONTACTS)
!= PackageManager.PERMISSION_GRANTED){
ActivityCompat.requestPermissions(this,new String[]
{Manifest.permission.READ_CONTACTS},0);
}
ContentResolver contentResolver = getContentResolver();
Uri uri = ContactsContract.CommonDataKinds.Phone.CONTENT_URI;
Cursor cursor = contentResolver.query(uri,null,null,null,null);
Log.i("CONTACT_PROVIDER_DEMO","TOTAL # O of Contacts ::: "+
(cursor.getCount()));
if (cursor.getCount()>0){
while (cursor.moveToNext()){
@SuppressLint("Range") String contactName =
cursor.getString(cursor.getColumnIndex(ContactsContract.CommonDataKinds.Phone.DISPLAY_NA
ME));
@SuppressLint("Range") String contactNumber =
cursor.getString(cursor.getColumnIndex(ContactsContract.CommonDataKinds.Phone.NUMBER));
Log.i("CONTACT_PROVIDER_DEMO","Contact Name :::"+contactName+" Ph# ::: "+contactNumber);
}
}
}
}


## OUTPUT

![image](https://github.com/Preethi132/Mobile-Application-Development/assets/136288465/7d7f0906-8b8f-41ed-98b3-a146a8367c11)



## RESULT
Thus a Simple Android Application create your own content providers to get contacts details using Android Studio is developed and executed successfully.
