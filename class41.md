# class 38 Reading Notes: Intent Filter

![](https://sites.google.com/site/mobilesecuritylabware/_/rsrc/1351190193805/6-mobile-coding-vulnerability/lab-activities/lab2-android-activities-with-intent-security/1.png)

* Intent filter is a property that used in your app to allow other apps use a feature of your app.

* It is added in the manifest file if you want to use it


## Allowing Other Apps to Start Your Activity

 **If your app can perform an action that might be useful from another app, your app should be prepared to respond to action requests by specifying the appropriate intent filter in your activity.**

* to allow other apps to start your activity in this way, you need to add an `<intent-filter>` element in your manifest file for the corresponding `<activity>` element.

### Add an Intent Filter

The system may send a given Intent to an activity if that activity has an intent filter fulfills the following criteria of the Intent object:

* Action: string naming the action to perform. Usually one of the platform-defined values such as ACTION_SEND or ACTION_VIEW.

* Data: description of the data associated with the intent.

* Category: Provides an additional way to characterize the activity handling the intent, usually related to the user gesture or location from which it's started.

example of the intent filter:

java
<activity android:name="ShareActivity">
    <intent-filter>
        <action android:name="android.intent.action.SEND"/>
        <category android:name="android.intent.category.DEFAULT"/>
        <data android:mimeType="text/plain"/>
        <data android:mimeType="image/*"/>
    </intent-filter>
</activity>


* Each incoming intent specifies only one action and one data type, but it's OK to declare multiple instances of the `<action>`, `<category>`, and `<data>` elements in each `<intent-filter>` .

* One activity can have multiple intent filters like this:

 java
<activity android:name="ShareActivity">
    <!-- filter for sending text; accepts SENDTO action with sms URI schemes -->
    <intent-filter>
        <action android:name="android.intent.action.SENDTO"/>
        <category android:name="android.intent.category.DEFAULT"/>
        <data android:scheme="sms" />
        <data android:scheme="smsto" />
    </intent-filter>
    <!-- filter for sending text or images; accepts SEND action and text or image data -->
    <intent-filter>
        <action android:name="android.intent.action.SEND"/>
        <category android:name="android.intent.category.DEFAULT"/>
        <data android:mimeType="image/*"/>
        <data android:mimeType="text/plain"/>
    </intent-filter>
</activity>




## Handle the Intent in Your Activity

* In order to decide what action to take in your activity, you can read the Intent that was used to start it.

* As your activity starts, call `getIntent()` to retrieve the Intent that started the activity. You can do so at any time during the lifecycle of the activity, but you should generally do so during early callbacks such as `onCreate()` or `onStart()`.


## Return a Result

* If you want to return a result to the activity that invoked yours, simply call `setResult()` to specify the result code and result Intent. When your operation is done and the user should return to the original activity, call `finish()` to close (and destroy) your activity.