# CORDOVA SAMPLE 

## To launch and utilize a sample with Pushwoosh SDK integration, clone or download the repository archive.

### iOS
 <img src="https://github.com/Pushwoosh/pushwoosh-cordova-sample/blob/main/Screenshots/iOS.png" alt="Alt text" width="300"> 

### Android 
 <img src="https://github.com/Pushwoosh/pushwoosh-cordova-sample/blob/main/Screenshots/Android.png" alt="Alt text" width="300"> 

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
    pushwoosh.onDeviceReady({        
        appid: "XXXXX-XXXXX",
        projectid: "XXXXXXXXXXXXXXX",
        serviceName: "XXXX"
    });
```


