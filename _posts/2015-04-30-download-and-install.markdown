---
layout: post
title:  "SDK Download and installation"
date:   2015-04-29 15:07:04
categories: General
---

This quick guide will teach you how to implement our SDK.

The end result should look something like that:
![Example App](/images/example_app.png)

##Jump to platform
1. ####[Android Native(Android Studio)](#android-native)
2. ####[Android Unity3D](#android-unity3d)
<br><br>

##Android Native - Android Studio
* [Download](http://bit.ly/1Ea6vR5) the SDK package(AAR file)
* Copy the file AAR file into the libs folder of your project
![Import AAR](/images/android_native_import_aar.png)

* Add the following lines into your `build.gradle` file
{% highlight js %}
repositories{
    flatDir{
        dirs 'libs'
    }
}
{% endhighlight %}

* Add the following line into your `build.gradle` file under dependencies section
{% highlight js %}
compile(name:'android_sdk-release', ext:'aar')
{% endhighlight %}

![build.gradle](/images/android_native_build_gradle.png)


* #### Add Bavel button to your layout using the following lines
{% highlight xml %}
<io.bavel.android_sdk.button.Button
    xmlns:bavel="http://schemas.android.com/apk/res-auto"
    bavel:developer_id="FILL_DEVELOPER_ID_HERE"
    android:layout_height="100dip"
    android:layout_width="100dip" />
{% endhighlight %}

* #### Don't forget to fill your Developer ID under `bavel:developer_id`

![native android final result](/images/android_native_final_result.png)


<br><br>

##Android Unity3D
1. ####[Download](http://bit.ly/1Kbb6uO) the SDK package(UnityPackage file)
2. #### Import the package to your Unity project
Double click on the unity package file and click on Import
![Import Package](/images/unity_import.png)
3. #### Place our button in the scenes you want
  a. Select our prefab from the Assests/bavel folder
  ![Prefab Selection](/images/unity_prefab.png)
  b. Drag the prefab to the Canvas

4. #### !!! Important !!! Insert your developer id in the button property
  You can find your developer id in the developers console: [Console](http://www.bavel.io/developers)

![Button Developer Id](/images/unity_dev_id.png)

#### Note: The SDK require these permissions:
{% highlight xml %}
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>
{% endhighlight %}
