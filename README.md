Cordova Mixpanel plugin
====================
# Overview #
mixpanel analytics

[android, ios] [crodova cli] [xdk]

Requires mixpanel account http://www.mixpanel.com/

Fix "error: use of undeclared identifier '_serialQueue'" xdk build error issue:
CORDOVA 3.X HYBRID MOBILE APP SETTINGS - Build Settings - set iOS Target Version: 6

This is open source cordova plugin.

You can see Plugins For Cordova in one page: http://cranberrygame.github.io?referrer=github

# Change log #
```c
```
# Install plugin #

## Cordova cli ##
```c
https://cordova.apache.org/docs/en/edge/guide_cli_index.md.html#The%20Command-Line%20Interface - npm install -g cordova@4.1.2

cordova plugin add com.cranberrygame.cordova.plugin.analytics.mixpanel
```

## Xdk ##
```c
https://software.intel.com/en-us/intel-xdk - Download XDK - XDK PORJECTS - [specific project] - CORDOVA 3.X HYBRID MOBILE APP SETTINGS - PLUGINS - Third Party Plugins - Add a Third Party Plugin - Get Plugin from the Web -

Name: mixpanel
Plugin ID: com.cranberrygame.cordova.plugin.analytics.mixpanel
[v] Plugin is located in the Apache Cordova Plugins Registry
```

## Cocoon ##
https://cocoon.io - Create project - [specific project] - Setting - Plugins - Search - cranberrygame - mixpanel

## Phonegap build service (config.xml) ##
```c
https://build.phonegap.com/ - Apps - [specific project] - Update code - Zip file including config.xml

<gap:plugin name="com.cranberrygame.cordova.plugin.analytics.mixpanel" source="plugins.cordova.io" />
```

## Construct2 ##

# Server setting #
```c
```

<img src="https://github.com/cranberrygame/cordova-plugin-analytics-mixpanel/blob/master/doc/token.png"><br>
<img src="https://github.com/cranberrygame/cordova-plugin-analytics-mixpanel/blob/master/doc/mixpanel_bookmark.png"><br>

# API #
```javascript
var token = "REPLACE_THIS_WITH_YOUR_TOKEN";
/*
var token;
//android
if (navigator.userAgent.match(/Android/i)) {
	token = "REPLACE_THIS_WITH_YOUR_TOKEN";
}
//ios
else if (navigator.userAgent.match(/iPhone/i) || navigator.userAgent.match(/iPad/i)) {
	token = "REPLACE_THIS_WITH_YOUR_TOKEN";
}
*/

document.addEventListener("deviceready", function(){
    window.mixpanel.setUp(token);
}, false);

//
window.mixpanel.trackEvent(eventName);
window.mixpanel.addEventProperty(propertyName, propertyValue);

//
window.mixpanel.identifyPeople(distinctId);
window.mixpanel.addPeopleProperty(propertyName, propertyValue);
window.mixpanel.changePeopleProperties();
window.mixpanel.incrementPeopleProperty(propertyName, propertyValue);
window.mixpanel.deletePeople();
			
```
# Examples #
<a href="https://github.com/cranberrygame/cordova-plugin-analytics-mixpanel/blob/master/example/basic/index.html">example/basic/index.html</a><br>

# Test #

You can also run following test apk.
https://dl.dropboxusercontent.com/u/186681453/pluginsforcordova/mixpanel/apk.html

# Useful links #

Plugins For Cordova<br>
http://cranberrygame.github.io?referrer=github

# Credits #

https://github.com/samzilverberg/cordova-mixpanel-plugin
