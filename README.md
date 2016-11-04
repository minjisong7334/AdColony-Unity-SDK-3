AdColony SDK 3 Unity Plugin
============================================
* Modified: November 4, 2016
* Unity Plug-in Version: 3.0.0
* iOS SDK Version: 3.0.4.1
* Android SDK Version: 3.0.4

Please Review the [Change log](CHANGELOG.md)

Download:
---------------------------------------
The simplest way to obtain the AdColony SDK 3 Unity Plugin is to click the "Clone or download" button located on the upper, right-hand side of the Github repository page.

Contains:
---------------------------------------
* AdColony.unitypackage - A Unity assets package containing the AdColony plugin.
* Unity Sample App

Getting Started with AdColony Unity:
---------------------------------------
First time users should review the [quick start guide](https://github.com/AdColony/AAdColony-Unity-SDK-3/wiki).

How to Set Up the ADCUnity Sample App:
--------------------------------------
1) Open the sample app (ADCUnity) in Unity:
    Go to ADCUnitySample/Assets/Scenes and open Main.unity. This should cause Unity to open the sample app.

2) Add the AdColony plugin package.
    In the Unity menu, go to Assets->Import Package->Custom Package, then find and open AdColonyUnityPlugin/AdColony.unitypackage. 

How to Build the Sample App for iOS:
--------------------------------------
1) In Unity, go to "File->Build Settings". This brings up the build dialog. Under Platforms, select iOS. Then select whether you want a Debug or Release build (Release is the default).

2) Then click the "Build" button, and select where to create the XCode iOS project.

3) Open the generated project in XCode.

4) Set up code signing.

5) Build to a device (running in the Simulator is not recommended).

How to Build the Sample App for Android:
--------------------------------------
1) In Unity, go to "File->Build Settings". This brings up the build dialog.  Under Platforms, select Android.

2) Click the "Build & Run" button, and select where to store the generated file. After creating the file, it should automatically install and run the app onto a connected Android device if one is attached.
