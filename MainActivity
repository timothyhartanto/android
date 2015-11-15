package com.example.proto.xmlsetting;

import android.app.Activity;
import android.graphics.Typeface;
import android.os.Bundle;
import android.view.Gravity;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.RadioGroup;
import android.widget.TextView;

public class MainActivity extends Activity implements RadioGroup.OnCheckedChangeListener {

    TextView textOut;
    EditText textIn;
    RadioGroup gravity, style;
    Button submit;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        textOut = (TextView)findViewById(R.id.tvInsert);
        textIn = (EditText)findViewById(R.id.editText);

        gravity = (RadioGroup)findViewById(R.id.rgGravity);
        gravity.setOnCheckedChangeListener(this);

        style = (RadioGroup)findViewById(R.id.rgStyle);
        style.setOnCheckedChangeListener(this);

        submit = (Button) findViewById(R.id.submit);

        submit.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                textOut.setText(textIn.getText());
            }
        });
    }

    public void onCheckedChanged(RadioGroup group, int checkedId){
        switch(checkedId){
            case R.id.rbCenter:
                textOut.setGravity(Gravity.CENTER);
                break;
            case R.id.rbLeft:
                textOut.setGravity(Gravity.LEFT);
                break;
            case R.id.rbRight:
                textOut.setGravity(Gravity.RIGHT);
                break;
            case R.id.rbNormal:
                textOut.setTypeface(Typeface.defaultFromStyle(Typeface.NORMAL));
                break;
            case R.id.rbItalic:
                textOut.setTypeface(Typeface.defaultFromStyle(Typeface.ITALIC));
                break;
            case R.id.rbBold:
                textOut.setTypeface(Typeface.defaultFromStyle(Typeface.BOLD));
                break;
        }

    }

}
