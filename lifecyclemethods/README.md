# Ex.No:1 To create a HelloWorld Activity using all lifecycles methods to display messages.


## AIM:

To create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
Program to print the text “Hello World”.
Developed by: KAUSHIK R
Registeration Number :212221040077
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

    <TextView
        android:id="@+id/textView"
        android:layout_width="298dp"
        android:layout_height="90dp"
        android:layout_marginBottom="341dp"
        android:text="ACTIVITY CYCLE"
        android:textColor="@color/teal_200"
        android:textSize="36sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.588"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/imageView"
        app:layout_constraintVertical_bias="0.499" />

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="92dp"
        android:layout_height="91dp"
        android:layout_marginBottom="32dp"
        android:src="@drawable/img"
        app:layout_constraintBottom_toTopOf="@+id/textView"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.498"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        tools:srcCompat="@tools:sample/avatars" />
        </androidx.constraintlayout.widget.ConstraintLayout>
```        
**MAINACTIVITY:**
```java   
    package com.example.activity_cycle;
    import androidx.appcompat.app.AppCompatActivity;
    import android.os.Bundle;
    import android.widget.Toast;

    public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Toast toast = Toast.makeText(getApplicationContext(),"Oncreate",Toast.LENGTH_SHORT);
        toast.show();
    }
    protected void onStart(){
        super.onStart();
        Toast toast = Toast.makeText(getApplicationContext(),"Onstart",Toast.LENGTH_SHORT);
        toast.show();
    }
    protected void onPause(){
        super.onPause();
        Toast toast = Toast.makeText(getApplicationContext(),"Onpause",Toast.LENGTH_SHORT);
        toast.show();
    }
    protected void onResume(){
        super.onResume();
        Toast toast = Toast.makeText(getApplicationContext(),"onResume",Toast.LENGTH_SHORT);
        toast.show();
    }
    protected void onStop(){
        super.onStop();
        Toast toast = Toast.makeText(getApplicationContext(),"OnStop",Toast.LENGTH_SHORT);
        toast.show();
    }
    protected  void onDestroy(){
        super.onDestroy();
        Toast toast = Toast.makeText(getApplicationContext(),"onDestroy",Toast.LENGTH_SHORT);
        toast.show();
    }
    protected void onRestart(){
        super.onRestart();
        Toast toast = Toast.makeText(getApplicationContext(),"onRestart",Toast.LENGTH_SHORT);
        toast.show();
    }
    }

```
## OUTPUT
  ![image](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/0b14f019-dd74-4ba9-b030-50972da62bb8)
   ![image](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/5321666a-e54e-4a99-a91b-cbfeef2e8cb3)
  ![image](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/86093af7-7f4b-4ea6-8796-105247fda06a)
  ![image](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/42d37a26-0c1c-44ba-abc0-40dbaa239ea9)
  ![image](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/489a05d1-3246-41d5-af12-2fa88ec57118)
  ![image](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/8bf899b5-4788-4f24-9377-7717aa285709)
![image](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/f22e04e4-1a6d-494c-9f12-9afedd45d15a)
![image](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/e97f1aeb-52b8-41d8-98eb-49d81ee6793f)


## RESULT
Thus a Simple Android Application create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio is developed and executed successfully.
