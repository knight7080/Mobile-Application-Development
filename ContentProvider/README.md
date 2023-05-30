
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
Program to create Your Own Content Providers to get Contacts details.
Developed by: KAUSHIK R
Registeration Number : 212221040077
```
**XML FILE:**
```xml
    <?xml version="1.0" encoding="utf-8"?>
    <androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="129dp"
        android:layout_marginTop="302dp"
        android:text="GET CONTACTS"
        android:onClick="btnGetContactPressed"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />
    </androidx.constraintlayout.widget.ConstraintLayout>
```
**MAINACTIVITY:**
```java
    package com.example.contactsgetter;

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


    //        Button show = (Button) findViewById(R.id.button2);
    //        show.setOnClickListener(view->
    //        {
    //            getPhoneContacts();
    //        });

    }
    private void getPhoneContacts(){
        if(ContextCompat.checkSelfPermission(this, Manifest.permission.READ_CONTACTS) != PackageManager.PERMISSION_GRANTED) {
            ActivityCompat.requestPermissions(this,new String[] {Manifest.permission.READ_CONTACTS},0);

        }
        ContentResolver contentResolver = getContentResolver();
        Uri uri = ContactsContract.CommonDataKinds.Phone.CONTENT_URI;
        Cursor cursor = contentResolver.query(uri,null,null,null,null);
        Log.i("CONTACT_PROVIDER_DEMO","TOTAL # COUNTS :::"+cursor.getCount());
        if(cursor.getCount() > 0)
        {
            while(cursor.moveToNext()){
                @SuppressLint("Range") String contactName = cursor.getString(cursor.getColumnIndex(ContactsContract.CommonDataKinds.Phone.DISPLAY_NAME));
                @SuppressLint("Range") String contactNumber = cursor.getString(cursor.getColumnIndex(ContactsContract.CommonDataKinds.Phone.NUMBER));
                Log.i("Content_provider_demo","Name: # "+contactName+"Number: # "+contactNumber);
            }

        }
    }

    public void btnGetContactPressed(View view) {
        getPhoneContacts();
    }
    }

```

## OUTPUT

  ![image](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/86760748-1a6e-4cc1-9bd8-c5c45e12de38)
  ![image](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/3fbc8760-d7e5-4e7a-91d4-106828bdcf3e)
  ![image](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/b9c04f7b-44e9-484f-8567-208a92dacf93)
  ![image](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/8f691873-18f0-4c08-a098-7a5e0bc4a41f)
  ![image](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/04649d53-045c-4902-a213-966384eac736)

  <br>
  <br><br><br><br><br><br>

## RESULT
Thus a Simple Android Application create your own content providers to get contacts details using Android Studio is developed and executed successfully.
