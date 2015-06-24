#**Known Issues - Visual Studio 2015**
This article covers [known issues](../Readme.md#knownissues) specific to Visual Studio Tools for Apache Cordova 2015. 

----------
**Project structure change from CTP3/3.1:** Projects created in an earlier version of Visual Studio will need to be migrated to support the new Cordova CLI based project structure in VS 2015 that is more interoperable with 3rd party tools and CLIs. 

To migrate your previous projects to the new structure:

 1. Make a backup of your existing project (obligatory first step :))
 2. Create a new project using the JavaScript \ Apache Cordova Apps \
    Blank App template
	 * For TypeScript projects, you can use the TypeScript equivalent of this same project
 3. Copy the .jsproj and taco.json files created by this template into your own project's folder
 4. In your project, create a new folder named www
 5. Delete the following folders from your project's folder:
	 * bin
	 * bld
 8. Leave the following folders/files in your project directory:
	 * merges
	 * res
	 * plugins
	 * config.xml
 13. Copy all other files/folders into the www folder
 14. If you're using TypeScript, you'll need to add a tsconfig.json to
     your project folder and define config settings for your project –
     see more in the Configuring TypeScript section
 15. Now you can build and run your application

If you have errors, you may need to update file references to reflect the new folder structure. 

Lastly, you should add the following XML elements to your config.xml to ensure your icons and splash screens are picked up by right clicking on the file and selecting "View Code":

    <platformname="android">
        <iconsrc="res/icons/android/icon-36-ldpi.png"density="ldpi" />
        <iconsrc="res/icons/android/icon-48-mdpi.png"density="mdpi" />
        <iconsrc="res/icons/android/icon-72-hdpi.png"density="hdpi" />
        <iconsrc="res/icons/android/icon-96-xhdpi.png"density="xhdpi" />
      </platform>
      <platformname="ios">
        <iconsrc="res/icons/ios/icon-60-3x.png"width="180"height="180" />
        <iconsrc="res/icons/ios/icon-60.png"width="60"height="60" />
        <iconsrc="res/icons/ios/icon-60-2x.png"width="120"height="120" />
        <iconsrc="res/icons/ios/icon-76.png"width="76"height="76" />
        <iconsrc="res/icons/ios/icon-76-2x.png"width="152"height="152" />
        <iconsrc="res/icons/ios/icon-40.png"width="40"height="40" />
        <iconsrc="res/icons/ios/icon-40-2x.png"width="80"height="80" />
        <iconsrc="res/icons/ios/icon-57.png"width="57"height="57" />
        <iconsrc="res/icons/ios/icon-57-2x.png"width="114"height="114" />
        <iconsrc="res/icons/ios/icon-72.png"width="72"height="72" />
        <iconsrc="res/icons/ios/icon-72-2x.png"width="144"height="144" />
        <iconsrc="res/icons/ios/icon-small.png"width="29"height="29" />
        <iconsrc="res/icons/ios/icon-small-2x.png"width="58"height="58" />
        <iconsrc="res/icons/ios/icon-50.png"width="50"height="50" />
        <iconsrc="res/icons/ios/icon-50-2x.png"width="100"height="100" />
      </platform>
      <platformname="windows">
        <iconsrc="res/icons/windows/Square150x150Logo.scale-100.png"width="150"height="150" />
        <iconsrc="res/icons/windows/Square150x150Logo.scale-240.png"width="360"height="360" />
        <iconsrc="res/icons/windows/Square30x30Logo.scale-100.png"width="30"height="30" />
        <iconsrc="res/icons/windows/Square310x310Logo.scale-100.png"width=""height="" />
        <iconsrc="res/icons/windows/Square44x44Logo.scale-240.png"width="106"height="106" />
        <iconsrc="res/icons/windows/Square70x70Logo.scale-100.png"width="70"height="70" />
        <iconsrc="res/icons/windows/Square71x71Logo.scale-240.png"width="170"height="170" />
        <iconsrc="res/icons/windows/StoreLogo.scale-100.png"width="50"height="50" />
        <iconsrc="res/icons/windows/StoreLogo.scale-240.png"width="120"height="120" />
        <iconsrc="res/icons/windows/Wide310x150Logo.scale-100.png"width="310"height="150" />
        <iconsrc="res/icons/windows/Wide310x150Logo.scale-240.png"width="744"height="360" />
      </platform>
      <platformname="wp8">
        <iconsrc="res/icons/wp8/ApplicationIcon.png"width="62"height="62" />
        <iconsrc="res/icons/wp8/Background.png"width="173"height="173" />
      </platform>
      <platformname="android">
        <splashsrc="res/screens/android/screen-hdpi-landscape.png"density="land-hdpi" />
        <splashsrc="res/screens/android/screen-ldpi-landscape.png"density="land-ldpi" />
        <splashsrc="res/screens/android/screen-mdpi-landscape.png"density="land-mdpi" />
        <splashsrc="res/screens/android/screen-xhdpi-landscape.png"density="land-xhdpi" />
        <splashsrc="res/screens/android/screen-hdpi-portrait.png"density="port-hdpi" />
        <splashsrc="res/screens/android/screen-ldpi-portrait.png"density="port-ldpi" />
        <splashsrc="res/screens/android/screen-mdpi-portrait.png"density="port-mdpi" />
        <splashsrc="res/screens/android/screen-xhdpi-portrait.png"density="port-xhdpi" />
      </platform>
      <platformname="ios">
        <splashsrc="res/screens/ios/screen-iphone-portrait.png"width="320"height="480" />
        <splashsrc="res/screens/ios/screen-iphone-portrait-2x.png"width="640"height="960" />
        <splashsrc="res/screens/ios/screen-ipad-portrait.png"width="768"height="1024" />
        <splashsrc="res/screens/ios/screen-ipad-portrait-2x.png"width="1536"height="2048" />
        <splashsrc="res/screens/ios/screen-ipad-landscape.png"width="1024"height="768" />
        <splashsrc="res/screens/ios/screen-ipad-landscape-2x.png"width="2048"height="1536" />
        <splashsrc="res/screens/ios/screen-iphone-568h-2x.png"width="640"height="1136" />
        <splashsrc="res/screens/ios/screen-iphone-portrait-667h.png"width="750"height="1334" />
        <splashsrc="res/screens/ios/screen-iphone-portrait-736h.png"width="1242"height="2208" />
        <splashsrc="res/screens/ios/screen-iphone-landscape-736h.png"width="2208"height="1242" />
      </platform>
      <platformname="windows">
        <splashsrc="res/screens/windows/SplashScreen.scale-100.png"width="620"height="300" />
        <splashsrc="res/screens/windows/SplashScreen.scale-240.png"width="1152"height="1920" />
        <splashsrc="res/screens/windows/SplashScreenPhone.scale-240.png"width="1152"height="1920" />
      </platform>
      <platformname="wp8">
        <splashsrc="res/screens/wp8/SplashScreenImage.jpg"width="480"height="800" />
      </platform>

##Visual Studio 2015 RC
----------
**VS 2015 RC and Cordova 5.x.x / Cordova Android 4.x.x:** See [Cordova 5.x.x known issues](known-issues-cordova5.md) for details on Android related issues that are specific to Cordova 5.0.0 and up.

----------
**Old versions of Cordova plugins due to Cordova plugin ID changes:** A significant change occurred with Cordova 5.0.0+ that also altered the IDs of many core Cordova plugins. The Visual Studio 2015 RC config.xml designer uses the old IDs (ex: org.apache.cordova.camera not cordova-plugin-camera) because Cordova 4.3.1 and below cannot access plugins using these new IDs and the default template uses 4.3.0. 

To install updated plugins, follow [this proceedure to install a npm sourced plugin](../tips-and-workarounds/general/README.md#plugin-npm). 

*Note that these updated plugins were tested on Cordova 5.0.0 or later and therefore may or may not work on earlier versions of Cordova.* We advise against updating your plugins when using older versions of Cordova unless you are attempting to solve a specific problem.

----------
**Building a Cordova project from source control results in Cordova plugin APIs not returning results:** The following four json files can cause this to occur if added to source control.

- plugins/android.json
- plugins/windows.json
- plugins/remote_ios.json
- plugins/wp8.json.

Remove these files from source control if you are not checking in the "platforms" folder (reccomended). For local copies, you can either fetch a fresh copy from source control or remove the above files along with platforms found in the "platforms" folder to resolve the issue. See [tips and workarounds](../tips-and-workarounds/general/README.md#l#missingexclude) for additional details.

----------
**Plugin with variables not working:** Due to a Cordova issue with Cordova 4.3.0 and a bug in VS 2015 RC, you can run into problems with plugin variables in Cordova < 5.0.0. Plugin variable information is lost if you install the "plugin" before the "platform" which can happen depending on your workflow. They do, however, function in Cordova 5.1.1 which you can use with VS 2015 RC. To update to 5.1.1 and use plugin variables, you will need to update your VS project and use the command line.

 1. Remove the plugins with the variables via the config designer.

 2. Update to Cordova 5.1.1 via the config designer (Platforms > Cordova CLI)

 3. From the command line:
	 1. Go to your project directory.
	 2. Type the following from substituting project path, plugin name, and variables for those that apply to you:
        
	    ~~~~~~~~~~~~~~
        cd <project path>
		npm install -g cordova@5.1.1 
        cordova plugin add nl.x-services.plugins.launchmyapp --variable URL_SCHEME=myscheme
	    ~~~~~~~~~~~~~~

##Visual Studio 2015 CTP6
----------
**Ant uninstalled when upgrading from CTP5 to CTP6:** When you upgrade from VS2015 CTP5 to CTP6, Apache Ant gets uninstalled. The workaround is to reinstall Ant. You can find manual instructions for installing and configuring Ant at [this location](https://msdn.microsoft.com/en-us/library/dn757054.aspx#InstallTools).

----------
## More Information
* [Read up on additional known issues, tips, tricks, and tutorials](../Readme.md)
* [Download samples from our Cordova Samples repository](http://github.com/Microsoft/cordova-samples)
* [Follow us on Twitter](https://twitter.com/VSCordovaTools)
* [Visit our site http://aka.ms/cordova](http://aka.ms/cordova)
* [Read MSDN docs on using Visual Studo Tools for Apache Cordova](http://go.microsoft.com/fwlink/?LinkID=533794)
* [Ask for help on StackOverflow](http://stackoverflow.com/questions/tagged/visual-studio-cordova)
* [Email us your questions](mailto://multidevicehybridapp@microsoft.com)