# Ex.No:3 Develop program to create a text field and a button “Navigate”. When you enter “www.google.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the google page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
```
Step-1: Create a layout XML file that contains a EditText for entering the URL and a Button for
navigation.
Step-2: Define an EditText element with an appropriate ID in the XML layout.
Step-3: Define a Button element with an appropriate ID in the XML layout.
Step-4: In your activity class, inflate the XML layout in the onCreate method using setContentView.
Step-5: Get references to the EditText and Button views using findViewById.
Step-6: Set a click listener on the Button to handle the navigation action.
Step-7: Inside the click listener, retrieve the text from the EditText view.
Step-8: Create an implicit intent with the action Intent.ACTION_VIEW.
Step-9: Set the data of the intent to the URL entered in the EditText.
Step-10: Verify if there's an app capable of handling the intent using resolveActivity method.
Step-11: If there's an app capable of handling the intent, start the activity using startActivity
method with the intent.
```


## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by:Thanga Deepika R
Registeration Number :212221040170
*/
```
## activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">
    <EditText
        android:id="@+id/editTextText"
        android:layout_width="290dp"
        android:layout_height="48dp"
        android:ems="10"
        android:inputType="text"
        android:text=" Enter the link"
        app:layout_constraintBottom_toTopOf="@+id/button"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.497"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.723" />
    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="340dp"
        android:text="Navigate"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
## MainActivity.java
```
package com.example.deepsimplicit;

import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        EditText editText;
        Button button;

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        button = findViewById(R.id.button);
        editText = (EditText) findViewById(R.id.editTextText);
        button.setOnClickListener(view -> {
            String url=editText.getText().toString();
            Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
            startActivity(intent);
        });
    }
}
```

## OUTPUT
```
![image](https://github.com/suryacse05/Mobile-Application-Development/assets/125663099/4cd635a6-71f8-48b6-8507-d64f7d82b23d)
```
```
![image](https://github.com/suryacse05/Mobile-Application-Development/assets/125663099/92ec9406-e795-4711-b348-b5a3a0955ea2)
```



## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the google page using Android Studio is developed and executed successfully.


