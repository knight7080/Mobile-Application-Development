# Ex.No: 2 To develop an application that uses GUI Components with Fonts and Colors. 
Note: Create button for colors and fonts while clicking color or font button should change 


## AIM:

To create an application that uses GUI Components with Fonts and Colors using Android Studio.

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
Program to print the text GUIcomponent.
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

    <Button
        android:id="@+id/colbut"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="128dp"
        android:layout_marginTop="120dp"
        android:backgroundTint="#FFC107"
        android:text="Change Color"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/fonbut"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="132dp"
        android:layout_marginTop="48dp"
        android:backgroundTint="#FF5722"
        android:text="Change Font"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/colbut" />

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="48dp"
        android:layout_marginTop="152dp"
        android:text="PRIME PLAYS"
        android:textSize="40dp"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/fonbut" />
    </androidx.constraintlayout.widget.ConstraintLayout>
```        
**MAINACTIVITY:**
```java    
    package com.example.guicomps;

    import androidx.appcompat.app.AppCompatActivity;

    import android.content.res.AssetManager;
    import android.graphics.Color;
    import android.graphics.Typeface;
    import android.os.Bundle;
    import android.view.View;
    import android.widget.Button;
    import android.widget.TextView;

    import java.io.IOException;
    import java.io.InputStream;

    public class MainActivity extends AppCompatActivity implements View.OnClickListener {

    private TextView textView;
    private Button colorButton;
    private Button fontButton;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        textView = findViewById(R.id.textView);
        colorButton = findViewById(R.id.colbut);
        fontButton = findViewById(R.id.fonbut);

        colorButton.setOnClickListener(this);
        fontButton.setOnClickListener(this);
    }

    @Override
    public void onClick(View view) {
        switch (view.getId()) {
            case R.id.colbut:
                changeTextColor();
                break;
            case R.id.fonbut:
                changeFont();
                break;
        }
    }

    private void changeTextColor() {
        int randomColor = generateRandomColor();
        textView.setTextColor(randomColor);
    }

    private void changeFont() {
        Typeface newFont = Typeface.createFromAsset(getAssets(), "font/pacifico.ttf");
        textView.setTypeface(newFont);
    }

    private int generateRandomColor() {
        int red = (int) (Math.random() * 256);
        int green = (int) (Math.random() * 256);
        int blue = (int) (Math.random() * 256);
        return Color.rgb(red, green, blue);
    }
    }

```
## OUTPUT
   ![240196753-a9d93852-9167-4979-83bd-113e30a3de00](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/15c3d055-81d9-4b44-8288-564fd9db294a)
![240197186-0a2161d3-b710-4d9f-b68b-a6c6da46c6d4](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/fd57f6f2-47b8-4179-9c7c-95f34b6278cd)

![240198282-b8b0f459-6f99-4f93-8eb6-7bb3bedea355](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/a1f4b875-7f8a-4f00-8c0e-ade88f79de15)![240198349-d1c087eb-2ecd-4232-be79-060657466d7e](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/672e8289-7ba3-4846-872f-945e709f738f)

![240198494-f7cbe2f7-2997-4fe1-8584-8d205737c6d9](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/f7f29bc8-7db2-42c8-86c5-7b8a83b61514)

![240198641-f674f5b4-273d-44ba-aff0-dd5a79bf838c](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/1abc074d-5704-43dd-8323-e61a11c6e076)
![240198848-1f7b7c03-4498-4c5c-81d7-1a81ea59c420](https://github.com/knight7080/Mobile-Application-Development/assets/88542035/7436e103-de86-4c22-9136-907e7beaf8d5)



## RESULT
Thus a Simple Android Application that uses GUI Components with Fonts and Colors using Android Studio is developed and executed successfully.
