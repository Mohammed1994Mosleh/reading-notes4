# class26 Reading Notes:Android Tasks and the Back Stack And SharedPreferences

### Tasks and the back stack:

  - A task is a collection of activities that users interact with when trying to do something in your app.


#### Lifecycle of a task and its back stack:
![](https://media.geeksforgeeks.org/wp-content/uploads/20210612202233/article-660x339.png)

* When the current activity starts another, the new activity is pushed on the top of the stack and takes focus

* When an activity stops, the system retains the current state of its user interface.

* When the user performs the back action, the current activity is popped from the top of the stack and the previous activity resumes

* Activities in the stack are never rearranged, only pushed and popped from the stack—pushed onto the stack.

* If the user continues to press or gesture Back, user returns to the Home screen.


#### Back press behavior for root launcher activities:

* Root launcher activities are activities that declare an Intent filter with both ACTION_MAIN and CATEGORY_LAUNCHER.

* When a user presses or gestures Back from a root launcher activity:

1. System behavior on Android 11 and lower :The system finishes the activity.
2. System behavior on Android 12 and higher: The system moves the activity and its task to the background instead of finishing the activity

#### Background and foreground tasks:

* A task is a cohesive unit that can move to the background when a user begins a new task or goes to the Home screen. 

#### Multi-window environments

* When apps are running simultaneously in a multi-windowed environment, supported in Android 7.0 (API level 24) and higher, the system manages tasks separately for each window; each window may have multiple tasks.


#### Lifecycle recap:

- When Activity A starts Activity B, Activity A is stopped, but the system retains its state 

- Leaving task using the Home button or gesture then current stopped and its task goes to background

- If presses or gestures Back the current activity is popped from the stack and destroyed.

- Activities can be instantiated multiple times, even from other tasks.

#### Manage tasks
- you might decide that you want to interrupt the normal behavior,by Using Attributes in the <activity>

* taskAffinity
* launchMode
* allowTaskReparenting
* clearTaskOnLaunch
* alwaysRetainTaskState
* finishOnTaskLaunch
And these are the principal intent flags that you can use:
* FLAG_ACTIVITY_NEW_TASK
* FLAG_ACTIVITY_CLEAR_TOP
* FLAG_ACTIVITY_SINGLE_TOP


#### Defining launch modes:

* To define how a new instance of an activity is associated with the current task. 

* By these ways

1. Using the manifest file
2. Using Intent flags



##### Using Intent flags

-The flags you can use to modify the default behavior are:
- FLAG_ACTIVITY_NEW_TASK
- FLAG_ACTIVITY_SINGLE_TOP
- FLAG_ACTIVITY_CLEAR_TOP


##### Clearing the back stack
There are some activity attributes that you can use to modify this behavior:
- alwaysRetainTaskState
- clearTaskOnLaunch
- finishOnTaskLaunch


##### Handling affinities
- affinity indicates which task an activity prefers to belong to.
- all the activities from the same app have an affinity for each other


## Android SharedPreferences:
![Android SharedPreferences](https://tutorial.eyehunts.com//wp-content/uploads/2018/07/Android-SharedPreferences-Tutorial-Save-Key-Value-data-example-in-kotlin-1.png)

#### Save key-value data

* A SharedPreferences object points to a file containing key-value pairs and provides simple methods to read and write them. Each SharedPreferences file is managed by the framework and can be private or shared.

- If you have a relatively small collection of key-values that you'd like to save, you should use the SharedPreferences APIs.


##### Get a handle to shared preferences:

* You can create a new shared preference file or access an existing one by calling one of these methods:

1. getSharedPreferences()
2. getPreferences().


* the following code accesses the shared preferences file that's identified by the resource string R.string.preference_file_key and opens it using the private mode so the file is accessible by only your app:


          SharedPreferences sharedPref = context.getSharedPreferences(
          getString(R.string.preference_file_key), Context.MODE_PRIVATE);


#### Write to shared preferences:

* To write to a shared preferences file, create a SharedPreferences.Editor by calling edit() on your SharedPreferences.

* Pass the keys and values you want to write with methods such as putInt() and putString(). Then call apply() or commit() to save the changes.

#### Read from shared preferences:

* To retrieve values from a shared preferences file, call methods such as getInt() and getString(), providing the key for the value you want, and optionally a default value to return if the key isn't present.