---
layout: post
title:  "Android Implementation"
date:   2015-04-29 15:07:04
categories: General
---

This quick guide will teach you how to implement our SDK.

The end result should look something like that:
![Example App](/images/android_mock.gif)


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
<script src="https://gist.github.com/chenb67/002155bc1c3bf63f2e10.js"></script>

* #### Don't forget to fill your Developer ID under `bavel:developer_id`
* Now you should see our button in your layout
![native android final result](/images/android_mock.gif)


<br><br>


### Continue to [Step 3](/getting-started/#step-3)
