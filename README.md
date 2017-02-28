
# RangeSeekBar 

## [中文文档](https://github.com/Jay-Goo/RangeSeekBar/blob/master/README_ZH.md) 

##Added 
markers 
hintDirection
hintTextColor

fix:
custom thumb position  

![image](https://github.com/guojilong/RangeSeekBar/blob/master/Gif/marker.png)


![image](https://github.com/Jay-Goo/RangeSeekBar/blob/master/Gif/2017-02-08%2019_27_55.gif)

##Attributes
attr | format | description
-------- | ---|---
min|float|min value, `Float.MIN_VALUE` <= min < max，Default：0
max|float|max value, min < max <= `Float.MAX_VALUE`, Default: 100
reserve|float|The minimum distance between two buttons
cells|int|Cells equal to 0 for the normal mode, greater than 1 to switch to scale mode
hideProgressHint|boolean|Whether to close the progress prompt
lineColorSelected|color|The Seekbar color after dragging
lineColorEdge|color|The default Seekbar color
thumbPrimaryColor|color|The color of the thumb when the progress is the minimum or maximum，default：none
thumbSecondaryColor|color|The color of the thumb when the progress is not the minimum or maximum，default：none
markTextArray|reference|Scale text, do not set the default when hidden
seekBarResId|reference|Button background resources, do not set the default when the circular button
progressHintResId|reference|Progress prompt background resources, you must use the **9 path file**
textPadding|dimension|The distance between the scale text and the progress bar
textSize|dimension|Scale text, and the size of the progress prompt text
hintBGHeight|dimension|The height of the progress prompt background, not set according to the text size adaptive
hintBGWith|dimension|The with of the progress prompt background, not set according to the text size adaptive
hintBGPadding|dimension|The progress indicates the distance between the background and the progress bar
seekBarHeight|dimension|The height of the progress bar
thumbSize|dimension|The size of the button
cellMode|enum|Scale mode **number** according to the scale of the actual proportion of the distribution of the location *（markTextArray must be a number）* **other** bisects the current layout*（markTextArray can be any character）*
seekBarMode| enum |One-way, two-way mode **single** like normal seekbar **range** Bidirectional selection SeekBar

##Usage
###Step1：
```xml
    allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
	
	dependencies {
	        compile 'com.github.Jay-Goo:RangeSeekBar:v1.0.6'
	}
   
```


###Step2：
```xml
    <com.jaygoo.widget.RangeSeekBar
        android:id="@+id/seekbar1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        app:markTextArray="@array/markArray"
        app:lineColorSelected="@color/colorAccent"
        app:seekBarResId="@drawable/seekbar_thumb"
        app:lineColorEdge="@color/colorSeekBarDefault"
        app:cellMode="number"
        app:seekBarMode="range"
    />
```

## [Update]
version | message
-------- | ---
v1.0.1 | add thumbPrimaryColor、thumbSecondaryColor Attributes
v1.0.2 | fix Scroll conflict and make padding attributes efective
v1.0.3 | fix bugs when range is 0 ~ 1
v1.0.6 | config jitPack to make you can see real source(why is 1.0.6 ? god knew it……)
## [Blog](http://blog.csdn.net/google_acmer/article/details/54971421)


##Others 

I hope you like this RangeSeekBar. `Star` is the greatest support for me！ Thank U




