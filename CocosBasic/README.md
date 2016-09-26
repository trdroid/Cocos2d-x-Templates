# Creating the project

*Version of Cocos2d-x used: cocos2d-x-3.13.1*

```sh
C:\Users\droid>cocos new --help
usage: cocos new [-h] [-p PACKAGE_NAME] [-d DIRECTORY] [-t TEMPLATE_NAME]
                 [--ios-bundleid IOS_BUNDLEID] [--mac-bundleid MAC_BUNDLEID]
                 [-e ENGINE_PATH] [--portrait] [--no-native] -l {cpp,lua,js}
                 [PROJECT_NAME]

Creates a new project.

positional arguments:
  PROJECT_NAME          Set the project name.

optional arguments:
  -h, --help            show this help message and exit
  -p PACKAGE_NAME, --package PACKAGE_NAME
                        Set a package name for project.
  -d DIRECTORY, --directory DIRECTORY
                        Set the path where to place the new project.
  -t TEMPLATE_NAME, --template TEMPLATE_NAME
                        Set the template name you want create from.
  --ios-bundleid IOS_BUNDLEID
                        Set a bundle id for iOS project.
  --mac-bundleid MAC_BUNDLEID
                        Set a bundle id for Mac project.
  -e ENGINE_PATH, --engine-path ENGINE_PATH
                        Set the path of engine.
  --portrait            Set the project be portrait.
  -l {cpp,lua,js}, --language {cpp,lua,js}
                        Major programming language you want to use, should be
                        [cpp | lua | js]

lua/js project arguments:
  --no-native           Create the project without native support.
```

Create a new project with the *cocos new* command.

```sh
C:\Users\droid>cocos new CocosBasic -p com.trdroid.basicgame -l cpp -d C:\Users\droid\onGit\cocos2d-x-templates
> Copy template into C:\Users\droid\onGit\cocos2d-x-templates
> Copying Cocos2d-x files...
> Rename project name from 'HelloCpp' to 'CocosBasic'
> Replace the project name from 'HelloCpp' to 'CocosBasic'
> Replace the project package name from 'org.cocos2dx.hellocpp' to 'com.trdroid.basicgame'
> Replace the Mac bundle id from 'org.cocos2dx.hellocpp' to 'com.trdroid.basicgame'
> Replace the iOS bundle id from 'org.cocos2dx.hellocpp' to 'com.trdroid.basicgame'
```

The parameters to the *cocos new* command are:

* **Project Name**: The name of the project is "CocosBasic"
* **Android Package Name**: The *-p* switch followed by the name of the package for the Android app which acts as the application ID in the Google Play Store
* **Programming Language**: The *-l* switch followed by the language to be used for the project
* **Project Location**: The *-d* switch followed by location where the project has to be generated. 

### Project Structure

![](_misc/Project%20Structure%20and%20Contents.PNG)
