# Cordova/datastores task example

This is a modified version of the task tracking example that ships with the [Dropbox Datastore JavaScript SDK](https://www.dropbox.com/developers/datastore/sdks/js). This version has been modified to run in the context of a Cordova app.

Aside from UI changes to match the phone form factor, the two main modification were:

* Use the Cordova auth driver with `client.authDriver(new Dropbox.AuthDriver.Cordova());`
* Use the `deviceready` event instead of the standard document `ready` event with `document.addEventListener("deviceready", function () { ... }, false);` instead of `$(function () { ... })`.

## Run instructions

To run this, you need to create a Cordova project and include these files in the `www` directory of your project:

1. Create a Cordova app with `cordova create cordova_datastores` (or choose your own name).
2. Go into the directory you just created and run `cordova plugins add org.apache.cordova.inappbrowser`. The InAppBrowser is used by the Dropbox Datastore SDK to perform the OAuth authorization flow.
3. Remove everything in the `www` directory and clone this git repo into `www` to replace it.
4. Add platforms (`cordova platforms add ...`) and run (`cordova run ...`) as you would in any other Cordova project.
