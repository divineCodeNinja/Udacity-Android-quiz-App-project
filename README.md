# Udacity-Android-quiz-App-project
This project is a simple app that creates a list of questions for a user to answer. the user  clicks the buttons 
and the app keeps record of the correct answers and displays a toast message of the grades when the user clicks on the submit button.

This is what I have done so far:

For the xml:
<ScrollView
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="wrap_content">
  <android.support.constraint.ConstraintLayout
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical"
        android:padding="10dp"
        tools:layout_editor_absoluteX="0dp"
        tools:layout_editor_absoluteY="0dp">

        <RelativeLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content">

            <TextView
                android:layout_width="161dp"
                android:layout_height="wrap_content"
                android:layout_centerHorizontal="true"
                android:text="Google quiz"
                android:textSize="24sp" />
        </RelativeLayout>

        <EditText
            android:id="@+id/editText"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:hint="Name"
            android:inputType="textMultiLine" />

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="1)When was Google founded?"
            android:textSize="24sp" />

        <RadioGroup
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="vertical">

            <RadioButton
                android:id="@+id/radio_wrongAnswerOne"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="1964"
                android:textAppearance="?android:textAppearanceMedium" />

            <RadioButton
                android:id="@+id/radio_answerOne"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:onClick="onCheckboxClicked"
                android:text="1998"
                android:textAppearance="?android:textAppearanceMedium" />

            <RadioButton
                android:id="@+id/checkbox_wrongAnswerTwo"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="  2000"
                android:textAppearance="?android:textAppearanceMedium" />

            <RadioButton
                android:id="@+id/checkbox_wrongAnswerThree"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="  2002"
                android:textAppearance="?android:textAppearanceMedium" />
        </RadioGroup>

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="2)Who founded Google"
            android:textAppearance="?android:textAppearanceMedium"
            android:textSize="24sp" />

        <RadioGroup
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="vertical">

            <RadioButton
                android:id="@+id/checkbox_wrongAnswerFour"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Bill Gates"
                android:textAppearance="?android:textAppearanceMedium" />

            <RadioButton
                android:id="@+id/checkbox_wrongAnswerFive"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Larry Page"
                android:textAppearance="?android:textAppearanceMedium" />

            <RadioButton
                android:id="@+id/checkbox_wrongAnswerSix"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Mark Zuckerberg"
                android:textAppearance="?android:textAppearanceMedium" />

            <RadioButton
                android:id="@+id/button_correctAnswerTwo"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Larry Page and Sergy Brin"
                android:textAppearance="?android:textAppearanceMedium" />
        </RadioGroup>

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="3)How old is Google now?"
            android:textSize="24sp" />

        <RadioGroup
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:orientation="vertical">

            <RadioButton
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text=" 12 yrs"
                android:textAppearance="?android:textAppearanceMedium" />

            <RadioButton
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text=" 40 yrs"
                android:textAppearance="?android:textAppearanceMedium" />

            <RadioButton
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text=" 45 yrs"
                android:textAppearance="?android:textAppearanceMedium" />

            <RadioButton
                android:id="@+id/button_correctAnswerThree"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text=" 20 yrs"
                android:textAppearance="?android:textAppearanceMedium" />
        </RadioGroup>

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="4)Who is the current CEO of Google?"
            android:textAppearance="?android:textAppearanceMedium"
            android:textSize="24sp" />

        <RadioGroup
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="vertical">

            <RadioButton
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Larry Page"
                android:textAppearance="?android:textAppearanceMedium" />

            <RadioButton
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Sergy Brin"
                android:textAppearance="?android:textAppearanceMedium" />

            <RadioButton
                android:id="@+id/correctAnswerFour"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Sundar Pichai"
                android:textAppearance="?android:textAppearanceMedium" />

            <RadioButton
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Satya Nadella"
                android:textAppearance="?android:textAppearanceMedium" />
        </RadioGroup>

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="5)Where is Googles headquarters?"
            android:textSize="24sp" />

        <RadioGroup
            android:layout_width="match_parent"
            android:layout_height="wrap_content">

            <RadioButton
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="San Francisco"
                android:textAppearance="?android:textAppearanceMedium" />

            <RadioButton
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="San Diego"
                android:textAppearance="?android:textAppearanceMedium" />

            <RadioButton
                android:id="@+id/correctAnswerFive"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="California"
                android:textAppearance="?android:textAppearanceMedium" />

            <RadioButton
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Boston"
                android:textAppearance="?android:textAppearanceMedium" />
        </RadioGroup>

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="6)Which of these is a google product? "
            android:textSize="24sp" />

        <RadioGroup
            android:orientation="vertical"
            android:layout_width="match_parent"
            android:layout_height="wrap_content">
        <RadioButton
            android:id="@+id/correctAnswerSix"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Gmail"
            android:textAppearance="?android:textAppearanceMedium" />

        <RadioButton
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Candy crush"
            android:textAppearance="?android:textAppearanceMedium" />

        <RadioButton
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Firefox"
            android:textAppearance="?android:textAppearanceMedium" />

        <RadioButton
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Windows"
            android:textAppearance="?android:textAppearanceMedium" />
        </RadioGroup>

        <RelativeLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content">

            <Button
                android:id="@+id/submit_button"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_centerHorizontal="true"
                android:onClick="submit"
                android:text="Submit" />
        </RelativeLayout>

    </LinearLayout>
</android.support.constraint.ConstraintLayout>
</ScrollView>

For the MainActivity code:

package com.example.android.googlequizlet;

import android.app.Activity;
import android.content.Context;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.CheckBox;
import android.widget.EditText;
import android.widget.RadioButton;
import android.widget.TextView;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {
    int quizGrade = 0;
    String answerOne;
    String answerTwo;
    String answerThree;
    String answerFour;
    String answerFive;
    String answerSix;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        }
        
//This is the method for the radio buttons for the user to check the right answers

public void onCheckboxClicked(View view){
        boolean checked = ((RadioButton)view).isChecked();
        switch (view.getId()){

            case R.id.radio_answerOne:
                if (checked){
                    quizGrade = quizGrade + 1;
                }
            case R.id.button_correctAnswerTwo:
                 if (checked){
                    quizGrade = quizGrade +1;
                }
            case R.id.button_correctAnswerThree:
                if(checked){
                    quizGrade = quizGrade +1;
                }
            case R.id.correctAnswerFour:
                if (checked){
                    quizGrade = quizGrade + 1;
                }
            case R.id.correctAnswerFive:
                if (checked){
                    quizGrade = quizGrade +1;
                }
            case R.id.correctAnswerSix:
                if (checked){
                    quizGrade = quizGrade +1;
                }
        }
    }
    //Method for the toast displaying user grade
    public void submit (View view){
        Context context = getApplicationContext();
        CharSequence text = "You scored " + quizGrade;
        int duration = Toast.LENGTH_LONG;

        Toast toast = Toast.makeText(context, text, duration);
        toast.show();
    }
}

Please any help or idea on how to complete this project would be appreciated.
Thanks in advance.
