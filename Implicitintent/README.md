# Ex.No:3 Develop program to create a text field and a button “Navigate”. When you enter “www.google.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the google page using Android Studio.

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
Program to print the text Implicitintent.
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

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="4dp"
        android:layout_marginTop="52dp"
        android:text="@string/enter_an_url"
        android:textSize="26sp"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        tools:ignore="ExtraText" />

    <EditText
        android:id="@+id/E1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="120dp"
        android:ems="10"
        android:inputType="textPersonName"
        android:text=""
        android:textColor="#2196F3"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.791"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="484dp"
        android:text="Jump Into"
        app:backgroundTint="#4CAF50"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.462"
        app:layout_constraintStart_toStartOf="parent" />


    </androidx.constraintlayout.widget.ConstraintLayout>
```       
**MAINACTIVITY:**
```java    
    package com.example.intent_implementation;

    import androidx.appcompat.app.AppCompatActivity;

    import android.content.Intent;
    import android.net.Uri;
    import android.os.Bundle;
    import android.view.View;
    import android.widget.Button;
    import android.widget.EditText;

    public class MainActivity extends AppCompatActivity {
    Button button;
    EditText e1;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        button = findViewById(R.id.button);
        e1 = findViewById(R.id.E1);
        button.setOnClickListener(view -> {
            String url = e1.getText().toString();
            Intent i1 = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
            startActivity(i1);
        });
    }
    }
```
## OUTPUT
  XML:<br>
  ![240207475-b1ed6ed0-17df-47b6-8127-1de06ae6dbd3](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/746e52f3-4e4c-4071-a8a6-11c8dadb9acf)

  MAIN:<br>
  ![240207524-0ad0b719-2862-4b24-9149-9b880e70f580](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/dedb21c7-1e4d-458e-be80-714094532ef7)
![240207642-5cbec425-a6f8-4827-abf7-375a2de3c6b0](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/99aa6714-19fb-47ea-a8b5-fb1e3b1e625b)
![240207686-85440148-dd0b-423e-9f49-e4fee90d75ee](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/0f8b86b9-2b8d-4b8e-83e1-21b4b54d7cdd)
![240291829-1179e99d-c44a-48b7-b1ad-817c22a18522](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/00401aed-d198-47ad-8c5c-f500f7c90ca5)

  <br><br><br><br><br><br><br><br><br><br><br><br><br><br>

## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the google page using Android Studio is developed and executed successfully.
