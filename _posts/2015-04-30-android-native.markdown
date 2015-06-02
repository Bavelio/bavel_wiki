---
layout: post
title:  "Android Native Implementation"
date:   2015-04-29 15:07:04
categories: General
---

This quick guide will teach you how to implement our SDK.

The end result should look something like that:
![Example App](/images/example_app.png)


##Android Native - Android Studio
* [Download](http://bit.ly/1IDLaqZ) the SDK package(AAR file)
* Copy the AAR file into the libs folder of your project
<br/>
![Import AAR](/images/android_native_import_aar.png)
<br/>
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
compile(name:'bavel_android_sdk', ext:'aar')
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
* Now you should see our button in your layout
![native android final result](/images/android_native_final_result.png)


<br><br>


### Continue to [Step 3](/getting-started/#step-3)
