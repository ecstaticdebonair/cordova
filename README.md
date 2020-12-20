# cordova COMMANDS TO CREATE APP

1.command to create app directory
cordova create <FOLDER-NAME> <com.YOUR-NAME.NAME> Erudite

cd <FOLDER-NAME>

2.commands to add platform
cordova platform add android 
cordova platform add windows 
cordova platform add ios 



3.command to remove platform
cordova platform rm ios 


4.command to build app
cordova build android 
cordova build ios
cordova build windows
cordova build 
cordova build --release android

step 5:---
keytool -genkey -v -keystore NAME-mobileapps.keystore -alias NAMEmobileapps -keyalg RSA -keysize 2048 -validity 10000

 Step 6:------------------------------------------------------------------------------------------------------------------------------
Place the generated keystore in

old version cordova

D:\projects\Phonegap\Example\platforms\android\ant-build
New version cordova

D:\projects\Phonegap\Example\platforms\android\build\outputs\apk\
To sign the unsigned APK, run the jarsigner tool which is also included in the JDK:

jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore <keystorename> <Unsigned APK file> <Keystore Alias name>

D:\projects\Phonegap\Example\platforms\android\ant-build> 
jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore NAME-mobileapps.keystore app-release-unsigned.apk NAMEmobileapps

help website:
https://shatter-box.com/knowledgebase/android-apk-signing-tool-apk-signer/#

Step 7:--------------------------------------------------------------------------------------------------------------------------------
give the path of zipalign which is found in build tools
Finally, we need to run the zip align tool to optimize the APK:

D:\projects\Phonegap\Example\platforms\android\ant-build> zipalign -v 4 app-release-unsigned.apk Example.apk 
OR

D:\projects\Phonegap\Example\platforms\android\ant-build> C:\Program Files (x86)\Android\android-sdk\19.1.0\zipalign -v 4 Example-release-unsigned.apk Example.apk
OR

D:\projects\Phonegap\Example\platforms\android\build\outputs\apk> C:\Program Files (x86)\Android\android-sdk\19.1.0\zipalign -v 4 Example-release-unsigned.apk Example.apk
Now we have our final release binary called example.apk and we can release this on the Google Play Store.





appid--ca-app-pub-8599562304011202~3108630526

cordova plugin add com.google.cordova.admob
cordova plugin add cordova-plugin-admobpro
cordova plugin add cordova-plugin-admobpro --save --variable PLAY_SERVICES_VERSION=16.0.0 --variable ADMOB_APP_ID="ca-app-pub-8599562304011202~3108630526"

cordova plugin add cordova-plugin-startapp-ads
// cordova plugin add cordova-plugin-startapp-ads --variable APP_ID_ANDROID="<your_android_app_id>"
//help https://portal.startapp.com/#/download-sdk
//help   https://support.startapp.com/hc/en-us/articles/360002411114-Native-Standard-
//great help  https://docs.branch.io/apps/android/


test ads
Banner	ca-app-pub-3940256099942544/6300978111
Interstitial	ca-app-pub-3940256099942544/1033173712
Interstitial Video	ca-app-pub-3940256099942544/8691691433
Rewarded Video	ca-app-pub-3940256099942544/5224354917
Native Advanced	ca-app-pub-3940256099942544/2247696110
Native Advanced Video	ca-app-pub-3940256099942544/1044960115


get mobile themes
https://themeforest.net/category/site-templates/mobile


applovin
cordova plugin add https://github.com/Heyzap/heyzap-cordova-applovin.git


sign apk
https://docs.catappult.io/docs/windows-10

jarsigner -keystore “C:\Users\Aptoide\Signature.jks “C:\Users\Akshay Mayekar\Downloads\Sign_blank_APK_to_certify_WeightLoss.apk” Signature

https://webservices.aptoide.com/webservices/3/uploadAppToRepo


ket store
https://docs.catappult.io/docs/windows-10

jarsigner -keystore <path to the keystore file> <path to the unsigned APK> <keystore alias>

 jarsigner -keystore “C:\Users\Aptoide\Signature.jks “C:\Users\Downloads\Unsigned_Test.apk” Signature




https://www.udemy.com/course/android-game-development-tutorial/learn/lecture/17499950#overview
