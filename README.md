# Android-UI-Note

## reference

padding : http://android4beginners.com/2013/07/lesson-2-2-how-to-use-margins-and-paddings-in-android-layout/

constraintlayout : https://medium.com/@loutry/guide-to-constraintlayout-407cd87bc013

### single line

xml :

    android:maxLines="1" // or android:singleLine="true"

### limit text with dot(...)

xml :

    android:ellipsize="end"

## About TextSize
### auto size text

limit : use this can't use wrap_content, textSize and gravity(content left, right, etc...)

xml :

    app:autoSizeTextType="uniform"

Java : 

    TextViewCompat.setAutoSizeTextTypeWithDefaults(tvNewsSource, TextViewCompat.AUTO_SIZE_TEXT_TYPE_UNIFORM);  

### const size

Java :
    
    // params : units, value such as 14
    setTextSize(TypedValue.COMPLEX_UNIT_PT, 14);
    // config value can use like context.getResources().getInteger(R.integer.yourDefinedValue) 
    // ** ps : if original use autoSize, need set noneAutoSize before setTextSize
    // TextViewCompat.setAutoSizeTextTypeWithDefaults(tv, TextViewCompat.AUTO_SIZE_TEXT_TYPE_NONE);// params : textView, int    

### text lineSpacingMultiplier

xml :
        
    android:lineSpacingMultiplier="float val"
