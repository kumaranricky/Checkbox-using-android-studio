# Unit 4 Workshop2
# To create an application and display the fruit name while clicking any three checkbox.Give input more than 6 fruit name in that select three fruit name.

## Aim:
 To create an application and display the fruit name while clicking any three checkbox.Give input more than 6 fruit name in that select three fruit name.
 
 
## PROGRAM:
``` java
## activity_main.xml:


<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@drawable/blue"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Fruits"
        android:textColor="#5E35B1"
        android:textSize="32dp"
        android:textStyle="bold"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintHorizontal_bias="0.422"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintRight_toRightOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.097" />

    <CheckBox
        android:id="@+id/checkBox"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:buttonTint="#76FF03"
        android:text="Mango"
        android:textColor="#D84315"
        android:textSize="15dp"
        android:textColorLink="#4527A0"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.414"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.185" />

    <CheckBox
        android:id="@+id/checkBox2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:buttonTint="#76FF03"
        android:text="Apple"
        android:textColor="#6A1B9A"
        android:textColorLink="#C62828"
        android:textSize="15dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.407"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/checkBox"
        app:layout_constraintVertical_bias="0.068" />

    <CheckBox
        android:id="@+id/checkBox3"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:buttonTint="#76FF03"
        android:text="Orange"
        android:textColor="#9E9D24"
        android:textColorLink="#6A1B9A"
        android:textSize="15dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.41"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/checkBox2"
        app:layout_constraintVertical_bias="0.068" />

    <CheckBox
        android:id="@+id/checkBox4"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:buttonTint="#76FF03"
        android:text="Pineapple"
        android:textColor="#00838F"
        android:textColorLink="#D84315"
        android:textSize="15dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.44"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/checkBox3"
        app:layout_constraintVertical_bias="0.083" />

    <CheckBox
        android:id="@+id/checkBox5"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:buttonTint="#76FF03"
        android:text="Guava"
        android:textColor="#F9A825"
        android:textColorLink="#AD1457"
        android:textSize="15dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.409"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/checkBox4"
        app:layout_constraintVertical_bias="0.091" />

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Fruits are good for health"
        android:textColor="@color/teal_700"
        android:textSize="20dp"
        android:textStyle="bold"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.453"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/checkBox5"
        app:layout_constraintVertical_bias="0.511" />

    <CheckBox
        android:id="@+id/checkBox6"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="24dp"
        android:buttonTint="#76FF03"
        android:text="Banana"
        android:textColor="#F9A825"
        android:textColorLink="#AD1457"
        android:textSize="15dp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.429"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/checkBox5" />

</androidx.constraintlayout.widget.ConstraintLayout>
## MainActivity.java:


package com.example.fruits;


import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.CheckBox;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {
    CheckBox ch1, ch2, ch3, ch4, ch5,ch6;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        ch1 = (CheckBox) findViewById(R.id.checkBox);

        ch2 = (CheckBox) findViewById(R.id.checkBox2);

        ch3 = (CheckBox) findViewById(R.id.checkBox3);

        ch4 = (CheckBox) findViewById(R.id.checkBox4);

        ch5 = (CheckBox) findViewById(R.id.checkBox5);
        ch6 = (CheckBox) findViewById(R.id.checkBox6);


        ch1.setOnClickListener(new View.OnClickListener() {

            @Override
            public void onClick(View view) {
                Toast.makeText(getApplicationContext(), "mango", Toast.LENGTH_LONG).show();

            }
        });
        ch2.setOnClickListener(new View.OnClickListener() {

            @Override
            public void onClick(View view) {
                Toast.makeText(getApplicationContext(), "apple", Toast.LENGTH_LONG).show();

            }
        });

        ch3.setOnClickListener(new View.OnClickListener() {

            @Override
            public void onClick(View view) {
                Toast.makeText(getApplicationContext(), "Orange", Toast.LENGTH_LONG).show();

            }
        });

        ch4.setOnClickListener(new View.OnClickListener() {

            @Override
            public void onClick(View view) {
                Toast.makeText(getApplicationContext(), "Pineapple", Toast.LENGTH_LONG).show();

            }
        });

        ch6.setOnClickListener(new View.OnClickListener() {

            @Override
            public void onClick(View view) {
                Toast.makeText(getApplicationContext(), "Banana", Toast.LENGTH_LONG).show();

            }
        });

        ch5.setOnClickListener(new View.OnClickListener() {

            @Override
            public void onClick(View view) {
                Toast.makeText(getApplicationContext(), "Guava ", Toast.LENGTH_LONG).show();
            }
        });
    }
}

```
## OUTPUT
![Screenshot (312)](https://user-images.githubusercontent.com/75243072/174973628-1eeabd05-8a04-4153-8201-0100588fd9d0.png)
![Screenshot!(313)](https://user-images.githubusercontent.com/75243072/174973642-530e65d7-6a13-4e94-935f-7f54839be6d8.png)
![Screenshot (338)](https://user-images.githubusercontent.com/75243072/174975875-a7a1a1b4-75f5-4d48-99f6-50b24b84824f.png)
![Screenshot (339)](https://user-images.githubusercontent.com/75243072/174976089-c0f601a1-d372-4380-ae26-62edeb84a899.png)



## Result
Thus,the program to create an application and display the fruit name while clicking any three checkbox.Give input more than 6 fruit name in that select three fruit name is implemented
 


