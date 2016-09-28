# Creating the project

*Platform: OS X 10.10.4 iTerm2 3.0.10*

*Version of Cocos2d-x used: cocos2d-x-3.13.1*

```sh
droid@Yamz:~$ which cocos
/Users/droid/Software/Cocos2d-x/Cocos2d-x-3.13.1/tools/cocos2d-console/bin/cocos
```

Create a new project with the *cocos new* command.

```sh
droid@Yamz:~$ cocos new BasicCocos -p com.trdroid.basicgame -l cpp -d /Users/droid/onGit/Cocos2d-x-Templates
> Copy template into /Users/droid/onGit/Cocos2d-x-Templates/BasicCocos
> Copying Cocos2d-x files...
> Rename project name from 'HelloCpp' to 'BasicCocos'
> Replace the project name from 'HelloCpp' to 'BasicCocos'
> Replace the project package name from 'org.cocos2dx.hellocpp' to 'com.trdroid.basicgame'
> Replace the Mac bundle id from 'org.cocos2dx.hellocpp' to 'com.trdroid.basicgame'
> Replace the iOS bundle id from 'org.cocos2dx.hellocpp' to 'com.trdroid.basicgame'
```

### Project Structure

![](_misc/Project%20Structure.png)

### Building and Running from the console

```sh
droid@Yamz:~$ cocos run --help
usage: cocos run [-h] [-s SRC_DIR] [-q] [-p PLATFORM] [--list-platforms]
                 [--proj-dir PROJ_DIR] [-m MODE] [-b BROWSER] [--param PARAM]
                 [--port [SERVER_PORT]] [--host [SERVER_HOST]] [--no-console]
                 [--working-dir WORKING_DIR]

Compiles, deploy and run project on the target.

optional arguments:
  -h, --help            show this help message and exit
  -s SRC_DIR, --src SRC_DIR
                        Specify the path of the project.
  -q, --quiet           Less output
  -p PLATFORM, --platform PLATFORM
                        Specify the target platform.
  --list-platforms      List available platforms
  --proj-dir PROJ_DIR   Specify the directory for target platform.
  -m MODE, --mode MODE  Set the run mode, should be debug|release, default is
                        debug.

web project arguments:
  -b BROWSER, --browser BROWSER
                        Specify the browser to open the url. Use the system
                        default browser if not specified.
  --param PARAM         after Specify the browser to open the url, add the
                        browser param.
  --port [SERVER_PORT]  Set the port of the local web server, defualt is 8000
  --host [SERVER_HOST]  Set the host of the local web server, defualt is
                        127.0.0.1
  --no-console          Disable simulator console window (by passing command
                        line arguments '-console no' to simulator) for
                        Windows, Mac and Linux.
  --working-dir WORKING_DIR
                        Specify simulator working directory for Windows, Mac
                        and Linux (by passing command line arguments '-workdir
                        "<path>"' to simulator).
```

**Output from the Build and Run step** 

The output from the Build and Run step can be found at _misc/PROJECT_CONTENTS_ON_BUILD_AND_RUN.md

**Files created/modified on build and run step**

```sh
droid@Yamz:~/onGit/Cocos2d-x-Templates/BasicCocos$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	_misc/Screeshot of app on iPhone.png
	bin/
	cocos2d/build/build/
	proj.ios_mac/build/

nothing added to commit but untracked files present (use "git add" to track)
```

### Screenshot

![](_misc/Screeshot%20of%20app%20on%20iPhone.png)

### Building and Running from Xcode

Open the file "/Users/droid/onGit/Cocos2d-x-Templates/BasicCocos/proj.ios_mac/BasicCocos.xcodeproj", which opens the file in Xcode.

Click on Build & Run

![](_misc/Screenshot%20of%20app%20launched%20from%20Xcode.png)

**Files created/modified on build and run step**

```sh
droid@Yamz:~/onGit/Cocos2d-x-Templates/BasicCocos$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	cocos2d/build/cocos2d_libs.xcodeproj/xcuserdata/
	proj.ios_mac/BasicCocos.xcodeproj/project.xcworkspace/
	proj.ios_mac/BasicCocos.xcodeproj/xcuserdata/

nothing added to commit but untracked files present (use "git add" to track)
```
