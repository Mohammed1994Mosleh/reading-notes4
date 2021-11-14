# class26 Reading Notes:Application Fundamentals 

* Android application can be written using Kotlin, Java, and C++ languages.

![](https://www.illusiongroups.com/blog/wp-content/uploads/2019/06/Capture2-4.jpg)

### Each Android app  protected by the following Android security features:

   1. The Android operating system is a multi-user Linux system in which each app is a different user.
   2. The system assigns each app a unique Linux user ID.
   3. Each process has its own virtual machine (VM), so an app's code runs in isolation from other apps.
   4. By default, every app runs in its own Linux process.

  * Android application implements privilege 
      App has access only to the components that it requires to do its work ,so its more secure.

  * Applocation can shre data with other application  by this ways:
    1. It's possible to arrange for two apps to share the same Linux user ID.
    2. An app can request permission to access device data such as the device's location, camera, and Bluetooth.


### App components:

   #### Types of componenet:

![](https://miro.medium.com/max/2000/1*33hzCoxAoUehHrHeBJi-VA.png)

  ##### Activities
       
        - It represents a single screen with a user interface
        
        - An activity facilitates the following key interactions between system and app:
           1. Keeping track of what the user currently cares about.
           2. Knowing that previously used processes contain things the user may return to.
           3. Helping the app handle having its process killed.
           4. Providing a way for apps to implement user flows between each other.

  ##### Services

         - It is a component that runs in the background to perform long-running operations or to perform work for remote processes.
  
         - Their are two types of services manges application through system :
           1. Started services
               - tell the system to keep them running until their work is completed.
               
           2. Bound services 
              
              -  It allows components such as activities to bind to the service, send requests, receive responses.
                


 ##### Broadcast receivers
         
          - A broadcast receiver is a component that enables the system to deliver events to the app outside of a   regular user flow.
          
          - a broadcast receiver is just a gateway to other components and is intended to do a very minimal amount of work.


 ##### Content providers

          - A content provider manages access to a central repository of data, and primarily intended to be used by other applications, which access the provider using a provider client object.
          
          - Application maniging data and can use them through this :
           
            1. Assigning a URI doesn't require that the app remain running
            2. These URIs also provide an important fine-grained security model.

         - A content provider is implemented as a subclass of ContentProvider and must implement a standard set of APIs that enable other apps to perform transactions.


### Activating components:

- activities, services, and broadcast receivers are activites through asynchronous message called intent.

- For activities and services, an intent defines the action to perform.

- For broadcast receivers, the intent simply defines the announcement being broadcast.

- content providers they are activated when targeted by a request from a ContentResolver.

- Separte method for activating component:

   1. Passing  Intent to startActivity() or startActivityForResult()
   2. Use JobScheduler class to schedule actions,on Android 5 and up.
   3. Initiate brodcast by passing Intent to methods such as sendBroadcast(), sendOrderedBroadcast(), or sendStickyBroadcast().
   4. You can perform a query to a content provider by calling query() on a ContentResolver.

##### The manifest file:

- app's manifest file, AndroidManifest.xml Reading to Khnow component exists.

- The manifest deos this 

1. Identifies any user permissions the app requires.
2. Declares the minimum API Level required by the app.
3. Declares hardware and software features used or required by the app.
4. Declares API libraries the app needs to be linked against .


##### Declaring app requirements:

- To prevent your app from being installed on devices that lack features needed by your app, it's important that you clearly define a profile for the types of devices your app supports by declaring device and software requirements in your manifest file.


#### App resources:

- An application requires resources that are separate from the source code, such as images, audio files.

- To make application east to deal with these resoureces.

- the SDK build tools define a unique integer ID, which you can use to reference the resource from your app code or from other resources defined in XML.


