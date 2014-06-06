Windows Push Sample
-------------------

In order to use Windows Push Sample (Native push notifications sample for Windows) with Telerik Backend Services you need to enable push notifications for Windows. This can be done by opening your Backend Services application from your Telerik Platform account and then open **Settings -> Push notifications** and choose Windows you should set Package Security ID and Client Secret of your Windows Store Dashboard. For more information you can refer to [this MSDN article](http://msdn.microsoft.com/en-us/library/windows/apps/hh913756.aspx).

Second step is to set your Telerik Backend Services API Key. Open MainPage.xaml.cs file and find the string "your-api-key-here" and replace it with your key. It can be found after logging to Telerik Platform, open your Backend Services application and click on API Keys link on the left column.

> Note: That Package SID should be equal to the Package info of your device (desktop) app. For a windows store app this information is stored within "Package.appxmanifest" file. Visual studio provides an UI which helps in the process of editing it. The easiest way to connect your Windows Store Dashboard App to your desktop app is through Visual Studio menu **PROJECT -> Store -> Associate App With the Store ...** - then you should log into with your Windows Dev Center account credentials and select your application.

However for the sake of the example this application comes with a predefined package info (Windows8PushApp) owned by Telerik, so all you need is to set: "ms-app://s-1-15-2-3157833167-2319104520-3008724778-1960889256-2485977247-996848071-3039990472" as Package SID and "fIpx0SSm9Dbrnk4gmOkdjRCAGdrXiapc" as Client Secret within your Telerik Backend Services application. 

> Be aware that this application should be used only for testing purposes and Telerik could disable this Windows Store Application at any time.

The upper segment is used to send a toast push notification with a sample text. Just click "Register" button and device will be automatically registered within Telerik Backend Services. Next step is to fill the "Toast Message" field and click "Send Push Notification" button. It will send a toast notification with a template "ToastText01" and "Toast Message" will be the entered text. For a complete set of toast templates you can refer to [this article](http://msdn.microsoft.com/en-us/library/windows/apps/hh761494.aspx).

The second segment of the application shows how to pin, register and send a push notification to a secondary tile.
The workflow is similar pin a secondary tile by pressing the "Pin Second Tile" button and approve the action. Then register it within Telerik Backend Services, fill all required fields as text1, text2, text3, text4 and image1 and click "Send Push Second Tile". It will send a tile notification (secondary tiles can accept only tile and badge notifications) with template "TileSquarePeekImageAndText01" which requires an image (.png 150 x 150 pxls) and 4 text fields (first one is bold and bigger). For a complete set of tile templates you can refer to [this article](http://msdn.microsoft.com/en-us/library/windows/apps/hh761491.aspx).