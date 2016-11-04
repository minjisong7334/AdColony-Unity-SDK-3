# AdColony-Unity-SDK-3
AdColony Plug-In for Unity

(NOTE: This ReadMe is a quick first pass, and will be improved soon).

How to build the ADCUnity Sample App:
--------------------------------------
1) Open the sample app (ADCUnity) in Unity:
  Go to ADCUnity/Assets/Scenes and open Main.unity. This should cause Unity to open the sample app.

2) add the AdColony plugin package.
	In the Unity menu, go to Assets->Import Package->Custom Package, then find and open UnityPlugin/AdColony.unitypackage. 

To build for iOS:
-------------------
1) In Unity, go to "File->Build Settings". This brings up the build dialog.  Under 
Platforms, select iOS. Then select whether you want a Debug or Release build (Release is 
the default).

2) Then click the "Build" button, and select where to create the XCode iOS project.

3) Open the generated project in XCode.

4) Set up code signing.

5) Build to a device (running in the Simulator is not recommended).

To build for Android:
----------------------
1) In Unity, go to "File->Build Settings". This brings up the build dialog.  Under 
Platforms, select Android.

2) Click the "Build & Run" button, and select where to store the generated file. After 
creating the file, it should automatically install and run the app onto a connected 
Android device.
