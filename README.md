# Vue-Parse-Guide

This documentation introduces how we should utilize Parse Objects to fulfill our apps' needs.

> We should update this documentation whenever we make changes to any Parse Objects, either add new properties or change existing ones, so that iOS and Android app are always synced.

## User
Use Parse's standard user object to manage sign in/ sign up. You may want to subclass it to add more properties


- `gender` **String**
	- "Male" or "Female", use this to save user's gender
- `emailVerified` **Boolean**
	- check if user has verified their email address
- `height` **Number**
	- save user's height, always in cm. Client should convert it to inches if necessary.
- `weight` **Number**
	- save user's weight, always in kg. Client should convert it to Pound if necessary
- `email` **String**
- `birthday` **Date**
- `devices` **Object**
	- this is a dictionary to save a list of devices taht this user has connected to. The key&value of this dictonary is `{"Mac address of the device": "User's custom name for this device"}`
