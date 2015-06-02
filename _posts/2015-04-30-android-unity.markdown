---
layout: post
title:  "Android Unity Implementation"
date:   2015-04-29 15:07:04
categories: General
---

##Android Unity3D
1. ####[Download](http://bit.ly/1H8HkR3) the SDK package(UnityPackage file)
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

### Continue to [Step 3](/getting-started/#step-3)
