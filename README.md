Getting Started
------------------------
This is a small productivity until program inspired by a #m2m project [Detect Phone](https://github.com/vlachoudis/DetectPhone)  that i found online . This solution was for linux and i could have written a C++ or XCode to work with OSX. However i too the easy route and  so i looked around and clubbed together a few tools and got it to work. For it to work you will need the following


* [Proximity Sensor](https://code.google.com/p/reduxcomputing-proximity)
*  Apple Scripts files found in this repo under compilled folder


How it works
------------------------
The concept is pretty simple. The Proximity scanner looks for your bluetooth device, and if it finds it within range trigger [Proximity Sensor](https://code.google.com/p/reduxcomputing-proximity) script and when its out of range it executes the [Proximity Sensor](https://code.google.com/p/reduxcomputing-proximity) script.

The scripts are pretty simple, all it does it sets the screensaver on and off.

Install
----------------
1.	Download the  [Proximity Sensor](https://code.google.com/p/reduxcomputing-proximity) and add it to your applications
2.	Download inrange.scpt and outofrange.scpt into a location
3.	Click on Change Device and make sure you point to the device/phone you want to tie too
4.	Add the inrange.scpt and outofrange.scpt to the Out of Range Script and In Range Script respectively 
5.	(Optional) Add [Proximity Sensor](https://code.google.com/p/reduxcomputing-proximity) to the user's login items so that it launches automatically.


Problem with Lion OSX
-------------------------
As a last work with Lion OSX its difficult to get ride of the password using Apple scripts, i tried a bunch of stuff but couldnt get it to work. Here are some the things i tried

###### Updating the ask for password option:
			
			defaults -currentHost write com.apple.screensaver askForPasswordDelay -int 0
###### Tried to Set system preference using AppleScripts, but that also didnt work

	tell application "System Events"
		tell security preferences
		set require password to wake to true
	end tell
if you are using this code then in outofrange make sure you set the password
	
	tell application "System Events"
		tell security preferences
			set require password to wake to true
		end tell
	end tell


