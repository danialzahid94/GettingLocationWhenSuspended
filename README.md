Getting Location Updates for iOS 7 and 8 Even when the App is Killed/Terminated/Suspended
============================

A clean way to get location updates from iOS 7 and 8 even when the app is not 
active on foreground and not in the background. Yes, you may get the GPS coordinates from the iOS devices 
even when the app is killed/terminated either by the user or the iOS itself.

Steps to Test this Solution
============================

Here are the steps to use this solution:-

    1. Download the project from Git Hub.
    2. Change to your own Bundle Identifier (If need to)
    3. Connect your iPhone with your mac.
    4. Launch the app into your iPhone.
    5. Killed the app. (Double tap and remove the app from the App Preview)
    6. Travel around with your iPhone for a few days.
    7. Download the LocationArray.plist to inspect from the File Sharing interface in iTunes.
    8. From the PLIst, you will see something like the screen shot below:-
![Getting Location Even When the App is Suspended/Killed/Terminated](http://mobileoop.com/wp-content/uploads/2015/01/GettingLocationWhenTheAppIsSuspended.png "Getting Location Even When the App is Suspended/Killed/Terminated")

When you see the key “UIApplicationLaunchOptionsLocationKey” under “Resume“, it means that the iOS has relaunched the app after the devices has moving significantly from the last known location. If you create a new location Manager instance, you will get new location from delegate method “didUpdateLocations“.

For the detail information, Please read: [Getting Location Updates for iOS 7 and 8 when the App is Killed/Terminated/Suspended]
(http://mobileoop.com/getting-location-updates-for-ios-7-and-8-when-the-app-is-killedterminatedsuspended 
"Getting Location Updates for iOS 7 and 8 when the App is Killed/Terminated/Suspended").
