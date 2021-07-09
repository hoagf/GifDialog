# GifDialog-Android
[![platform](https://img.shields.io/badge/platform-Android-yellow.svg)](https://www.android.com)
[![API](https://img.shields.io/badge/API-15%2B-brightgreen.svg?style=plastic)](https://android-arsenal.com/api?level=15)
[![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg?style=flat-square)](https://www.apache.org/licenses/LICENSE-2.0.html)
[![](https://jitpack.io/v/hoagf/GifDialog.svg)](https://jitpack.io/#hoagf/GifDialog)




## Prerequisites

Add this in your root `build.gradle` file (**not** your module `build.gradle` file):

```gradle
allprojects {
	repositories {
		...
		maven { url "https://jitpack.io" }
	}
}
```

## Dependency

Add this to your module's `build.gradle` file (make sure the version matches the JitPack badge above):

```gradle
dependencies {
	        implementation 'com.github.hoagf:GifDialog:1.6'
	}
```
## Gif Dialog

Dialog with two buttons:

``` java
new FancyGifDialog.Builder(this)
                .setTitle("Granny eating chocolate dialog box") // You can also send title like R.string.from_resources
                .setMessage("This is a granny eating chocolate dialog box. This library is used to help you easily create fancy gify dialog.") // or pass like R.string.description_from_resources
                .setTitleTextColor(R.color.titleText)
                .setDescriptionTextColor(R.color.descriptionText)
                .setNegativeBtnText("Cancel") // or pass it like android.R.string.cancel
                .setPositiveBtnBackground(R.color.positiveButton) 
                .setPositiveBtnText("Ok") // or pass it like android.R.string.ok
                .setNegativeBtnBackground(R.color.negativeButton)
                .setGifResource(R.drawable.gif1)   //Pass your Gif here
                .isCancellable(true)
                .OnPositiveClicked(new FancyGifDialogListener() {
                    @Override
                    public void OnClick() {
                        Toast.makeText(MainActivity.this,"Ok",Toast.LENGTH_SHORT).show();
                    }
                })
                .OnNegativeClicked(new FancyGifDialogListener() {
                    @Override
                    public void OnClick() {
                        Toast.makeText(MainActivity.this,"Cancel",Toast.LENGTH_SHORT).show();
                    }
                })
                .build();
```

Dialog with one button:

``` java
new FancyGifDialog.Builder(this)
                .setTitle("Granny eating chocolate dialog box")
                .setMessage("This is a granny eating chocolate dialog box. This library is used to help you easily create fancy gify dialog.")
                .setTitleTextColor(R.color.titleText)
                .setDescriptionTextColor(R.color.descriptionText)
                .setPositiveBtnText("Ok")
                .setPositiveBtnBackground(R.color.positiveButton)
                .setGifResource(R.drawable.gif1)   //Pass your Gif here
                .isCancellable(true)
                .OnPositiveClicked(new FancyGifDialogListener() {
                    @Override
                    public void OnClick() {
                        Toast.makeText(MainActivity.this,"Ok",Toast.LENGTH_SHORT).show();
                    }
                })
                .build();
```

## Screenshots

**Please click the image below to enlarge.**


<img src="https://github.com/Shashank02051997/FancyGifDialog-Android/blob/master/Screenshot/20180106_215855.gif" height="420" width="240" hspace="20"><img src="https://github.com/Shashank02051997/FancyGifDialog-Android/blob/master/Screenshot/20180106_220303.gif" height="420" width="240" hspace="20"><img src="https://github.com/Shashank02051997/FancyGifDialog-Android/blob/master/Screenshot/20180106_220829.gif" height="420" width="240">

<img src="https://github.com/Shashank02051997/FancyGifDialog-Android/blob/master/Screenshot/20180106_221054.gif" height="420" width="240" hspace="20"><img src="https://github.com/Shashank02051997/FancyGifDialog-Android/blob/master/Screenshot/20180106_221227.gif" height="420" width="240" hspace="20"><img src="https://github.com/Shashank02051997/FancyGifDialog-Android/blob/master/Screenshot/20180106_221357.gif" height="420" width="240">

<img src="https://github.com/Shashank02051997/FancyGifDialog-Android/blob/master/Screenshot/Screenshot_2018-01-07-10-24-37.png" height="420" width="240" hspace="20"><img src="https://github.com/Shashank02051997/FancyGifDialog-Android/blob/master/Screenshot/Screenshot_2018-01-07-10-25-07.png" height="420" width="240" hspace="20"><img src="https://github.com/Shashank02051997/FancyGifDialog-Android/blob/master/Screenshot/Screenshot_2018-01-07-10-25-26.png" height="420" width="240">


 



## License

* [Apache Version 2.0](http://www.apache.org/licenses/LICENSE-2.0.html)

```
Copyright 2018 Shashank Singhal

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

 http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
# GifDialog
