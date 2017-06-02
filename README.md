# Change log
- AdColony Unity Plugin is containing Android SDK 3.1.2 but Android SDK 3.1.0 is more stable than 3.1.2.
- Removed the file "ADCDependencies.cs" which is located in Assets>AdColony>Editor so If you need that file please copy from the AdColony-Unity-SDK-3 github(https://github.com/AdColony/AdColony-Unity-SDK-3).


# AdColony SDK Unity Plugin
- Modified: April 7, 2017
- Unity Plugin Version: 3.1.0
- iOS SDK Version: 3.1.1
- Android SDK Version: 3.1.0

## Overview
Increase your revenue with the advertising SDK trusted by the world’s top publishers. AdColony delivers high-definition Instant-Play™ video ads that can be displayed anywhere within your application. AdColony contains V4VC™, a secure system for rewarding users of your app with virtual currency upon the completion of video plays.

The AdColony SDK Unity Plugin combines the native iOS and Android SDKs into an easy to use package for Unity applications.

For detailed information about the AdColony SDK, see our [Unity Plugin documentation](https://github.com/AdColony/AdColony-Unity-SDK-3/wiki), [iOS SDK documentation](https://github.com/AdColony/AdColony-iOS-SDK-3/wiki), or [Android SDK documentation](https://github.com/AdColony/AdColony-Android-SDK-3/wiki).

**Note:** The AdColony Compass™ early access program has ended, and we are no longer accepting new partners. Publishers who are currently using those services should email compass@adcolony.com for more details.

## Usage

### Installation

1. In the Unity Editor, select "Assets"->"Import Package"->"Custom Package". Navigate to the location of the AdColony SDK Unity Plugin and select "AdColony.unitypackage".
1. Select "Import" to import all the assets into your project.
1. The AdColony SDK Unity Plugin includes Google's PlayServicesResolver to automatically pull in necessary Google Play Services libraries. If there are conflicts with this, the `play-services-ads` library is the only required. You can choose to ignore this PlayServicesResolver installation, remove the `AdColony/Editor/ADCDependencies.cs` file, and include the `play-services-ads` in another way.
1. The Plugins/Android/AdColony/AndroidManifest.xml file is automatically generated. To update manually, select "Tools"->"AdColony"->"Update AndroidManifest.xml".

#### Updating from 3.0.x:
In order to support thin/fat Android builds, we moved the native .so files from the `Plugins/Android/AdColony/libs` folder to the `Plugins/Android/libs` folder. Removing the `Plugins/Android/AdColony` folder before importing AdColony SDK Unity Plugin 3.1.0 is recommended. Otherwise, simply remove the `Plugins/Android/AdColony/libs/armeabi-v7a` and `Plugins/Android/AdColony/libs/x86` folders.

#### Updating from 2.x:
Please note that updating from our 2.x Unity Plugin is not a drag and drop update, but rather includes breaking API and process changes. In order to take advantage of the 3.x Unity Plugin, a complete re-integration is necessary. Please review our [documentation](https://github.com/AdColony/AdColony-Unity-SDK-3/wiki) to get a better idea on what changes will be necessary in your app.


### Quick Start
The basics of using the AdColony SDK to serve ads to your users are:
1. Configure the service
1. Request an ad *(We recommend requesting a new ad when an ad expires)*
1. Show the ad

For example:

```csharp

AdColony.InterstitialAd _ad = null;

void ConfigureAds() {
    AdColony.Ads.Configure("app_id", null, "zone_id_1", "zone_id_2");
    AdColony.Ads.OnRequestInterstitial += (AdColony.InterstitialAd ad) => {
        _ad = ad;
    };
}

void RequestAd() {
    AdColony.Ads.RequestInterstitialAd("zone_id_1", null);
}

void PlayAd() {
    if (_ad != null) {
        AdColony.Ads.ShowAd(_ad);
    }
}
```

For detailed information about the AdColony SDK, see our [Unity Plugin documentation](https://github.com/AdColony/AdColony-Unity-SDK-3/wiki).

## Legal Requirements
By downloading the AdColony SDK, you are granted a limited, non-commercial license to use and review the SDK solely for evaluation purposes.  If you wish to integrate the SDK into any commercial applications, you must register an account with AdColony and accept the terms and conditions on the AdColony website.

Note that U.S. based companies will need to complete the W-9 form and send it to us before publisher payments can be issued.

## Contact Us
For more information, please visit AdColony.com. For questions or assistance, please email us at support@adcolony.com.
