# CORDOVA SAMPLE 

## To launch and utilize a sample with Pushwoosh SDK integration, clone or download the repository archive.

### iOS, Android
 <img src="https://github.com/Pushwoosh/pushwoosh-cordova-sample/blob/main/Screenshots/iOS.png" alt="Alt text" width="300"> <img src="https://github.com/Pushwoosh/pushwoosh-cordova-sample/blob/main/Screenshots/Android.png" alt="Alt text" width="300"> 

### 1. Go to 'newdemo' folder and install the package from the command line:

```
cordova plugin add pushwoosh-cordova-plugin
```

### 2. Navigate to the js folder within the www directory and open the file named index.js. Add your App ID and FCM Sender ID

```
/**
* Function: onDeviceReady
* [android, ios, wp8, windows] Initialize Pushwoosh plugin and trigger a start push message
* Should be called on every app launch
* Parameters:
* "config.appid" - Pushwoosh application code
* "config.projectid" - GCM project number for android platform
* "config.serviceName" - MPNS service name for wp8 platform
*/

function initPushwoosh() {
	 var pushwoosh = cordova.require("pushwoosh-cordova-plugin.PushNotification");

//Should be called before pushwoosh.onDeviceReady
  document.addEventListener('push-notification', function(event) {
      var notification = event.notification;
      // handle push open here
	 });

 pushwoosh.onDeviceReady({        
   appid: "XXXXX-XXXXX",
   projectid: "XXXXXXXXXXXXXXX",
   serviceName: "XXXX"
 });
}
```

### 3. [Android] Add the 'google-services.json' file to the app folder in Android 

### 4. [Android] Add the following section to your config.xml:

```
<platform name="android">
   <resource-file src="google-services.json" target="app/google-services.json" />
   ...
</platform>

```

###



## The guide for SDK integration is available on the Pushwoosh [website](https://docs.pushwoosh.com/platform-docs/pushwoosh-sdk/cross-platform-frameworks/cordova/integrating-cordova-plugin)


