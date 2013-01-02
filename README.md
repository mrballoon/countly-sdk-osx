##What's Countly?

[Countly](http://count.ly) is an innovative, real-time, open source mobile and desktop analytics application. It collects data and visualizes this information to analyze application usage and end-user behavior. 
There are two parts of Countly: the server that collects and analyzes data, and SDK that sends this 
data (for iOS, Android, Windows Phone, Blackberry and OSX). Both parts are open source.

This repository includes the SDK for OSX. It's developed by [Pavel Guganov](mailto:mytinyship@gmail.com).

##Installing iOS SDK

Countly OSX SDK includes necessary tools to track your application. In order to integrate SDK to your application, follow these steps.

1. Download Countly OSX SDK.
2. Add these files to your project under Xcode: `Countly.h` `Countly.m` `Countly_OpenUDID.h` `Countly_OpenUDID.m`
3. import `Countly.h` and add the line;
`[[Countly sharedInstance] start:@"YOUR_APP_KEY" withHost:@"http://YOUR_API_HOST.com"];` where you want to start getting stats

**Note:** if you use Countly Cloud, you must set withHost parameter to http://cloud.count.ly for step 10.

It should finally look like this:

<pre class="prettyprint">
#import "Countly.h"  // newly added line
- (void) someYourFunc
{
[[Countly sharedInstance] start:@"TYPE_HERE_YOUR_APP_KEY_GENERATED_IN_COUNTLY_ADMIN_DASHBOARD" withHost:@"http://TYPE_HERE_URL_WHERE_API_IS_HOSTED"]; // newly added line
// your code
}
</pre>

Note: If your project uses automatic reference counting (ARC), you should disable it for the sources `Countly_OpenUDID.m` and `Countly.m`:

1. Select your project
2. Select the **Build Phases** tab
3. Open **Compile Sources** tab
4. Double click `Countly.m` and `Countly_OpenUDID.m` and add `-fno-objc-arc` flag

Note: Before upgrading to a new SDK, do not forget to remove the existing, older SDK from your project.


Check Countly Server source code here: 

- [Countly Server](https://github.com/Countly/countly-server)

There are also other Countly SDK repositories below:

- [Countly iOS SDK](https://github.com/Countly/countly-sdk-ios)
- [Countly Android SDK](https://github.com/Countly/countly-sdk-android)
- [Countly Windows Phone SDK](https://github.com/Countly/countly-sdk-windows-phone)
- [Countly Blackberry Webworks SDK](https://github.com/Countly/countly-sdk-blackberry-webworks)

##How can I help you with your efforts?
Glad you asked. We need ideas, feedbacks and constructive comments. All your suggestions will be taken care with upmost importance. 

We are on [Twitter](http://twitter.com/gocountly) and [Facebook](http://www.facebook.com/Countly) if you would like to keep up with our fast progress!

For community support page, see [http://support.count.ly](http://support.count.ly "Countly Support").
