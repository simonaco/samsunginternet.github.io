---
title: Progressive Web Apps
layout: page
image: /images/header-images/lighthouse-beacon.jpg
description: Samsung Internet support for PWA APIs
---
# Progressive Web Apps
 
Progressive Web Apps (PWAs) are regular mobile and desktop web applications that are 
accessible in any web browser. In browsers that support new open web standards - including 
[Samsung Internet for Android](/about) - they can provide additional capabilities including 
offline support and push notifications.
 
Having the ability to load from a cache means that PWAs can have great performance benefits, 
providing almost-instant loading times for return visitors.
 
You do not necessarily need to build a new PWA from scratch. The features can be added to your 
existing web properties using [Progressive Enhancement](https://www.smashingmagazine.com/2009/04/progressive-enhancement-what-it-is-and-how-to-use-it/).
 
## Service Workers
 
The most important web feature that enables PWAs is the *Service Worker*. A Service Worker is 
like a network proxy that runs in your browser. It can intercept requests to the network and 
depending on what you program it to do, it could return a response from a cache. This is what 
allows web apps to work offline.
 
If you have heard of AppCache, an earlier browser feature that also promised offline web apps, 
you can think of Service Workers as replacing and surpassing AppCache. AppCache had widely 
reported issues and limitations. Service Workers are designed to be much more programmable 
and powerful.
 
Service Workers are restricted to secure contexts, so for production you will need to use HTTPS.
They have been supported in Samsung Internet for Android since v4.
 
## Push Notifications
 
Service Workers are also used to deliver push notifications. Push notifications on the web are 
achieved using two APIs: the [Notification API](https://developer.mozilla.org/en-US/docs/Web/API/Notifications_API) 
and the [Push API](https://developer.mozilla.org/en-US/docs/Web/API/Push_API). The Notification 
API is used to display notifications. The Push API is used in a service worker to handle the 
push messages from the server. Because Service Workers are not tied to the lifetime of a browser 
tab, they can respond to push messages even when your web application is not currently open.
 
Samsung Internet for Android has supported the Notification API and Push API since v4. 
*Note:* The [“Web Notifications” API listed here on caniuse.com](http://caniuse.com/#feat=notifications) 
is marked as unsupported by Samsung Internet and Chrome for Android, but this refers to an earlier
specification. Notifications can be triggered via push messages in the service worker context.
  
## Web App Manifest
 
[Web App Manifests](https://developer.mozilla.org/en-US/docs/Web/Manifest) provide a standard 
way to describe how your web app should appear on the home screen and how it should launch. 
It consists of a simple JSON file that you reference via a meta tag. 
[Here is an example](https://samsunginter.net/bubble/manifest.json) from Diego Gonzalez’s 
[Bubble web app](https://samsunginter.net/bubble/).
 
In Samsung Internet for Android, the user can choose ‘Add shortcut on Home screen’ from the 
menu. If your manifest declares them appropriately, your chosen icon will appear on the home 
screen along with your chosen short name.
 
In the same way, in Samsung Internet running on Samsung DeX, web apps can be added to the 
desktop.
 
If you set the ‘display’ property to ‘standalone’, when the user taps on the icon, the web app 
will launch without the browser frame and URL bar.
 
Web App Manifest support arrived in Samsung Internet v4.
 
 
## Further Information
 
* Ada Rose Edwards has written a primer on PWAs for Smashing Magazine: 
[The Building Blocks of Progressive Web Apps](https://www.smashingmagazine.com/2016/09/the-building-blocks-of-progressive-web-apps/)
* Peter O’Shaughnessy has shared some lessons learned in 
[Things I learned making a Progressive Web App for “super selfies”](https://medium.com/samsung-internet-dev/things-i-learned-making-a-progressive-web-app-for-super-selfies-49e76d154e4f)
* We have collaborated with Google on their 
[Progressive Web Apps Training](https://developers.google.com/web/ilt/pwa/) materials.
 