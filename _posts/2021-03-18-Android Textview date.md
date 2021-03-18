---
layout: post
title: "안드로이드 Edittext 날짜 점(.) 자동 입력"
subtitle: "안드로이드 개발"
categories: [Android]
tags: [Android]
date: 2021-03-18 08:00:00
background: '/img/10.jpg'
---

# 안드로이드 Edittext 날짜 점(.) 자동 입력하는 법

### Edittext에 날짜 입력시 날짜 형식에 맞추어 점(.) 생성하는 법 ex) 2020.01.01처럼..
1. xml파일 Edittext 부분에 다음과 같이 추가
    ```xml
    android:hint="ex) 2021.01.01"
    android:inputType="number"
    android:maxLength="10"
    ```
 2. java 파일 
    ```java
    Edittext변수명.addTextChangedListener(new TextWatcher() {
        @Override
        public void beforeTextChanged(CharSequence s, int start, int count, int after) {
        }

        @Override
        public void onTextChanged(CharSequence s, int start, int before, int count) {
            if(Edittext변수명.isFocusable() && !s.toString().equals("")) {
                try{
                    textlength = Edittext변수명.getText().toString().length();
                }catch (NumberFormatException e){
                    e.printStackTrace();
                    return;
                }

                if (textlength == 4 && before != 1) {
                
                    Edittext변수명.setText(et_spec_content_2.getText().toString()+".");
                    Edittext변수명.setSelection(Edittext변수명.getText().length());
                    
                }else if (textlength == 7&& before != 1){
                
                    Edittext변수명.setText(et_spec_content_2.getText().toString()+".");
                    Edittext변수명.setSelection(Edittext변수명.getText().length());
                    
                }else if(textlength == 5 && !Edittext변수명.getText().toString().contains(".")){
                
                    Edittext변수명.setText(Edittext변수명.getText().toString().substring(0,4)+"."+Edittext변수명.getText().toString().substring(4));
                    Edittext변수명.setSelection(Edittext변수명.getText().length());
                    
                }else if(textlength == 8 && !Edittext변수명.getText().toString().substring(7,8).equals(".")){
                
                    Edittext변수명.setText(Edittext변수명.getText().toString().substring(0,7)+"."+Edittext변수명.getText().toString().substring(7));
                    Edittext변수명.setSelection(Edittext변수명.getText().length());
                    
                }
            }


        }

        @Override
        public void afterTextChanged(Editable s) {

        }
    });
    ```

[맨위로👆](#){: .btn .btn--primary }
