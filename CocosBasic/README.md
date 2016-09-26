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

### Build and Run

```sh
c:\Users\droid>cocos run --help
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

```sh
C:\Users\droid>cocos run -s c:\Users\droid\onGit\cocos2d-x-templates\CocosBasic -p android
Building mode: debug
Using Eclipse project : c:\Users\droid\onGit\cocos2d-x-templates\CocosBasic\proj.android
The directory 'android-13' can't be found in ANDROID_SDK_ROOT/platforms, please use --ap to set needed API level
```

The error indicates that "android-13" is not found in ANDROID_SDK_ROOT/platforms. Note that ANDROID_SDK_ROOT was set when the *cocos* command was first run, the information for which is in the Cocos2d-x-Examples repository. The ANDROID_SDK_ROOT was set to "C:\Software\Android\platforms" which contains "android-14 .. android-24" directories but not "android-13".

Explicitly specifying the Android API level to be "16"

```sh
C:\Users\droid>cocos run -s c:\Users\droid\onGit\cocos2d-x-templates\CocosBasic -p android --ap 16
Building mode: debug
Using Eclipse project : c:\Users\droid\onGit\cocos2d-x-templates\CocosBasic\proj.android
The directory '16' can't be found in ANDROID_SDK_ROOT/platforms, please use --ap to set needed API level
```

Do not specify just the number of the API level but the directory name itself.

Explicitly specifying the Android API level directory "android-16"

```sh
C:\Users\droid>cocos run -s c:\Users\droid\onGit\cocos2d-x-templates\CocosBasic -p android --ap android-16
Building mode: debug
Using Eclipse project : c:\Users\droid\onGit\cocos2d-x-templates\CocosBasic\proj.android
running: '"C:\Software\Android\tools\android" update project -t android-16 -p c:\Users\droid\onGit\cocos2d-x-templates\CocosBasic\proj.android'

Updated project.properties
Updated local.properties
Updated file c:\Users\droid\onGit\cocos2d-x-templates\CocosBasic\proj.android\proguard-project.txt
running: '"C:\Software\Android\tools\android" update lib-project -p c:\Users\droid\onGit\cocos2d-x-templates\CocosBasic\cocos2d\cocos\platform\android\java -t android-16'

Updated project.properties
Updated local.properties
Updated file c:\Users\droid\onGit\cocos2d-x-templates\CocosBasic\cocos2d\cocos\platform\android\java\proguard-project.txt
Building native...
NDK build mode: debug
running: '"C:\Software\Android NDK\android-ndk-r12b\ndk-build" -C c:\Users\droid\onGit\cocos2d-x-templates\CocosBasic\proj.android -j4 NDK_MODULE_PATH=c:\Users\droid\onGit\cocos2d-x-templates\CocosBasic\proj.android\../cocos2d;c:\Users\droid\onGit\cocos2d-x-templates\CocosBasic\proj.android\../cocos2d/cocos;c:\Users\droid\onGit\cocos2d-x-templates\CocosBasic\proj.android\../cocos2d/external NDK_TOOLCHAIN_VERSION=4.9 NDK_DEBUG=1'

'C:\Software\Android' is not recognized as an internal or external command,
operable program or batch file.
Error running command, return code: 1.
```

The problem occurred because of setting the "NDK_ROOT" to point to "C:\Software\Android NDK\android-ndk-r12b" which contains a space in its path, so change the name of the directory "Android NDK" to "Android-NDK" and update the modified path in the "environment variables" against the "NDK_ROOT" environment variable. 

NOTE: The environment variables ANDROID_SDK_ROOT, NDK_ROOT & ANT_ROOT were set when the *cocos* command was first run, the information about which can be found in Cocos2d-x-Examples repository.

```sh
C:\Users\droid>cocos run -s c:\Users\droid\onGit\cocos2d-x-templates\BasicX -p android --ap android-16
Building mode: debug
Using Eclipse project : c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android
running: '"C:\Software\Android\tools\android" update project -t android-16 -p c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android'

Updated project.properties
Updated local.properties
Updated file c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\proguard-project.txt
running: '"C:\Software\Android\tools\android" update lib-project -p c:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java -t android-16'

Updated project.properties
Updated local.properties
Updated file c:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\proguard-project.txt
Building native...
NDK build mode: debug
running: '"C:\Software\Android-NDK\android-ndk-r12b\ndk-build" -C c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android -j4 NDK_MODULE_PATH=c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\../cocos2d;c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\../cocos2d/cocos;c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\../cocos2d/external NDK_TOOLCHAIN_VERSION=4.9 NDK_DEBUG=1'

Android NDK: WARNING: APP_PLATFORM android-16 is larger than android:minSdkVersion 9 in ./AndroidManifest.xml
make: Entering directory `c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android'
[armeabi] Compile++ arm  : cocostudio_static <= WidgetReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= FlatBuffersSerialize.cpp
[armeabi] Compile++ arm  : cocostudio_static <= WidgetCallBackHandlerProtocol.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCComExtensionData.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CocoStudio.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UILayoutComponent.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UITabControl.cpp
[armeabi] Gdbserver      : [arm-linux-androideabi-4.9] libs/armeabi/gdbserver
[armeabi] Gdbsetup       : libs/armeabi/gdb.setup
[armeabi] Compile++ thumb: MyGame_shared <= main.cpp
[armeabi] Compile++ thumb: MyGame_shared <= AppDelegate.cpp
[armeabi] Compile++ thumb: MyGame_shared <= HelloWorldScene.cpp
[armeabi] StaticLibrary  : libcocos2d.a
[armeabi] Compile++ arm  : cocostudio_static <= CCActionFrame.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCActionFrameEasing.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCActionManagerEx.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCActionNode.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCActionObject.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCArmature.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCBone.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCArmatureAnimation.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCProcessBase.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCTween.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCDatas.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCBatchNode.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCDecorativeDisplay.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCDisplayFactory.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCDisplayManager.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCSkin.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCColliderDetector.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCArmatureDataManager.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCArmatureDefine.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCDataReaderHelper.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCSpriteFrameCacheHelper.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCTransformHelp.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCUtilMath.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCComAttribute.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCComAudio.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCComController.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCComRender.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCInputDelegate.cpp
[armeabi] Compile++ arm  : cocostudio_static <= DictionaryHelper.cpp
[armeabi] Compile++ arm  : cocostudio_static <= LocalizationManager.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCSGUIReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCSSceneReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= TriggerBase.cpp
[armeabi] Compile++ arm  : cocostudio_static <= TriggerMng.cpp
[armeabi] Compile++ arm  : cocostudio_static <= TriggerObj.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CocoLoader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= NodeReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= SingleNodeReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= SpriteReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= ParticleReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= GameMapReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= ProjectNodeReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= ComAudioReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= ButtonReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CheckBoxReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= ImageViewReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= LayoutReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= ListViewReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= LoadingBarReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= PageViewReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= ScrollViewReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= SliderReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= TextAtlasReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= TextBMFontReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= TextFieldReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= TextReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= Node3DReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= Sprite3DReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= UserCameraReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= Particle3DReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= BoneNodeReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= SkeletonNodeReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= GameNode3DReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= Light3DReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCActionTimelineCache.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCFrame.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCTimeLine.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCActionTimeline.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCActionTimelineNode.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CSLoader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCBoneNode.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCSkeletonNode.cpp
[armeabi] Compile++ arm  : cocostudio_static <= CCSkinNode.cpp
[armeabi] Compile++ arm  : cocostudio_static <= ArmatureNodeReader.cpp
[armeabi] Compile++ arm  : cocostudio_static <= TabControlReader.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCBAnimationManager.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCBFileLoader.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCBKeyframe.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCBReader.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCBSequence.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCBSequenceProperty.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCControlButtonLoader.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCControlLoader.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCLabelBMFontLoader.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCLabelTTFLoader.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCLayerColorLoader.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCLayerGradientLoader.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCLayerLoader.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCMenuItemImageLoader.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCMenuItemLoader.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCNode+CCBRelativePositioning.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCNodeLoader.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCNodeLoaderLibrary.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCParticleSystemQuadLoader.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCScale9SpriteLoader.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCScrollViewLoader.cpp
[armeabi] Compile++ arm  : cocosbuilder_static <= CCSpriteLoader.cpp
[armeabi] Compile++ arm  : cocos3d_static <= CCRay.cpp
[armeabi] Compile++ arm  : cocos3d_static <= CCAABB.cpp
[armeabi] Compile++ arm  : cocos3d_static <= CCOBB.cpp
[armeabi] Compile++ arm  : cocos3d_static <= CCAnimation3D.cpp
[armeabi] Compile++ arm  : cocos3d_static <= CCAnimate3D.cpp
[armeabi] Compile++ arm  : cocos3d_static <= CCAttachNode.cpp
[armeabi] Compile++ arm  : cocos3d_static <= CCBillBoard.cpp
[armeabi] Compile++ arm  : cocos3d_static <= CCBundle3D.cpp
[armeabi] Compile++ arm  : cocos3d_static <= CCBundleReader.cpp
[armeabi] Compile++ arm  : cocos3d_static <= CCMesh.cpp
[armeabi] Compile++ arm  : cocos3d_static <= CCMeshSkin.cpp
[armeabi] Compile++ arm  : cocos3d_static <= CCMeshVertexIndexData.cpp
[armeabi] Compile++ arm  : cocos3d_static <= CCMotionStreak3D.cpp
[armeabi] Compile++ arm  : cocos3d_static <= CCSprite3DMaterial.cpp
[armeabi] Compile++ arm  : cocos3d_static <= CCObjLoader.cpp
[armeabi] Compile++ arm  : cocos3d_static <= CCSkeleton3D.cpp
[armeabi] Compile++ arm  : cocos3d_static <= CCSprite3D.cpp
[armeabi] Compile++ arm  : cocos3d_static <= CCTerrain.cpp
[armeabi] Compile++ arm  : cocos3d_static <= CCSkybox.cpp
[armeabi] Compile arm    : spine_static <= Animation.c
[armeabi] Compile arm    : spine_static <= AnimationState.c
[armeabi] Compile arm    : spine_static <= AnimationStateData.c
[armeabi] Compile arm    : spine_static <= Atlas.c
[armeabi] Compile arm    : spine_static <= AtlasAttachmentLoader.c
[armeabi] Compile arm    : spine_static <= Attachment.c
[armeabi] Compile arm    : spine_static <= AttachmentLoader.c
[armeabi] Compile++ arm  : spine_static <= AttachmentVertices.cpp
[armeabi] Compile arm    : spine_static <= Bone.c
[armeabi] Compile arm    : spine_static <= BoneData.c
[armeabi] Compile arm    : spine_static <= BoundingBoxAttachment.c
[armeabi] Compile++ arm  : spine_static <= Cocos2dAttachmentLoader.cpp
[armeabi] Compile arm    : spine_static <= Event.c
[armeabi] Compile arm    : spine_static <= EventData.c
[armeabi] Compile arm    : spine_static <= IkConstraint.c
[armeabi] Compile arm    : spine_static <= IkConstraintData.c
[armeabi] Compile arm    : spine_static <= Json.c
[armeabi] Compile arm    : spine_static <= MeshAttachment.c
[armeabi] Compile arm    : spine_static <= PathAttachment.c
[armeabi] Compile arm    : spine_static <= PathConstraint.c
[armeabi] Compile arm    : spine_static <= PathConstraintData.c
[armeabi] Compile arm    : spine_static <= RegionAttachment.c
[armeabi] Compile arm    : spine_static <= Skeleton.c
[armeabi] Compile++ arm  : spine_static <= SkeletonAnimation.cpp
[armeabi] Compile++ arm  : spine_static <= SkeletonBatch.cpp
[armeabi] Compile arm    : spine_static <= SkeletonBounds.c
[armeabi] Compile arm    : spine_static <= SkeletonJson.c
[armeabi] Compile arm    : spine_static <= SkeletonData.c
[armeabi] Compile++ arm  : spine_static <= SkeletonRenderer.cpp
[armeabi] Compile arm    : spine_static <= Skin.c
[armeabi] Compile arm    : spine_static <= Slot.c
[armeabi] Compile arm    : spine_static <= SlotData.c
[armeabi] Compile arm    : spine_static <= TransformConstraint.c
[armeabi] Compile arm    : spine_static <= TransformConstraintData.c
[armeabi] Compile arm    : spine_static <= VertexAttachment.c
[armeabi] Compile arm    : spine_static <= extension.c
[armeabi] Compile++ arm  : spine_static <= spine-cocos2dx.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIWidget.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UILayout.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UILayoutParameter.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UILayoutManager.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= CocosGUI.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIHelper.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIListView.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIPageView.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIPageViewIndicator.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIScrollView.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIButton.cpp
[armeabi][armeabi] Compile++ arm  : Compile++ arm  : cocos_ui_static <= UIScrollViewBar.cpp cocos_ui_static <= UIAbstractCheckButton.cpp

[armeabi] Compile++ arm  : cocos_ui_static <= UICheckBox.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIRadioButton.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIImageView.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIText.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UITextAtlas.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UITextBMFont.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UILoadingBar.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UISlider.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UITextField.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIRichText.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIHBox.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIVBox.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIRelativeBox.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIVideoPlayer-android.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIDeprecated.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIScale9Sprite.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIWebView.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIWebViewImpl-android.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIEditBox.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIEditBoxImpl-android.cpp
[armeabi] Compile++ arm  : cocos_ui_static <= UIEditBoxImpl-common.cpp
[armeabi] Compile++ thumb: cocosdenshion_static <= cddSimpleAudioEngine.cpp
[armeabi] Compile++ thumb: cocosdenshion_static <= ccdandroidUtils.cpp
[armeabi] Compile++ thumb: cocosdenshion_static <= cddandroidAndroidJavaEngine.cpp
[armeabi] Compile++ arm  : cocos_flatbuffers_static <= flatc.cpp
[armeabi] Compile++ arm  : cocos_flatbuffers_static <= idl_gen_cpp.cpp
[armeabi] Compile++ arm  : cocos_flatbuffers_static <= idl_gen_fbs.cpp
[armeabi] Compile++ arm  : cocos_flatbuffers_static <= idl_gen_general.cpp
[armeabi] Compile++ arm  : cocos_flatbuffers_static <= idl_gen_go.cpp
[armeabi] Compile++ arm  : cocos_flatbuffers_static <= idl_gen_text.cpp
[armeabi] Compile++ arm  : cocos_flatbuffers_static <= idl_parser.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= AssetsManager.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= Manifest.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= AssetsManagerEx.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCEventAssetsManagerEx.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCEventListenerAssetsManagerEx.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCControl.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCControlButton.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCControlColourPicker.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCControlHuePicker.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCControlPotentiometer.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCControlSaturationBrightnessPicker.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCControlSlider.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCControlStepper.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCControlSwitch.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCControlUtils.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCInvocation.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCScrollView.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCTableView.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCTableViewCell.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPhysicsDebugNode.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPhysicsSprite.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCParticle3DAffector.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCParticle3DEmitter.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCParticle3DRender.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCParticleSystem3D.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUDynamicAttribute.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUDynamicAttributeTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUForceField.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUMaterialManager.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUMaterialTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUNoise.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUPlane.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPURendererTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUScriptCompiler.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUScriptLexer.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUScriptParser.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUScriptTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUSimpleSpline.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUSphere.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUTechniqueTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUTranslateManager.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUUtil.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUParticleSystem3D.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUParticleSystem3DTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUListener.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUAffector.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUAffectorManager.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUAffectorTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUAlignAffector.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUAlignAffectorTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUBaseCollider.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUBaseColliderTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUBaseForceAffector.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUBaseForceAffectorTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUBoxCollider.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUCollisionAvoidanceAffector.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUBoxColliderTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUCollisionAvoidanceAffectorTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUColorAffector.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUColorAffectorTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUFlockCenteringAffector.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUFlockCenteringAffectorTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUForceFieldAffector.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUForceFieldAffectorTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUGeometryRotator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUGeometryRotatorTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUGravityAffectorTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUGravityAffector.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUInterParticleCollider.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUInterParticleColliderTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUJetAffector.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUJetAffectorTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPULineAffector.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPULineAffectorTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPULinearForceAffector.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPULinearForceAffectorTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUParticleFollower.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUParticleFollowerTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUPathFollower.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUPathFollowerTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUPlaneCollider.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUPlaneColliderTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPURandomiser.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPURandomiserTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUScaleAffector.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUScaleAffectorTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUScaleVelocityAffector.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUScaleVelocityAffectorTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUSineForceAffector.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUSineForceAffectorTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUSphereCollider.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUSphereColliderTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUTextureAnimator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUTextureAnimatorTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUTextureRotator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUTextureRotatorTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUVelocityMatchingAffector.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUVelocityMatchingAffectorTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUVortexAffector.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUVortexAffectorTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUEmitter.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUEmitterTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUEmitterManager.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUBoxEmitter.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUBoxEmitterTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUCircleEmitter.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUCircleEmitterTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPULineEmitter.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPULineEmitterTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUMeshSurfaceEmitter.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUMeshSurfaceEmitterTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUPointEmitter.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUPointEmitterTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUPositionEmitter.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUPositionEmitterTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUSlaveEmitter.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUSphereSurfaceEmitter.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUSlaveEmitterTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUSphereSurfaceEmitterTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUVertexEmitter.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPURender.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUBeamRender.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUBillboardChain.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPURibbonTrail.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPURibbonTrailRender.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUDoAffectorEventHandler.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUDoAffectorEventHandlerTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUDoEnableComponentEventHandler.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUDoEnableComponentEventHandlerTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUDoExpireEventHandler.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUDoExpireEventHandlerTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUDoFreezeEventHandler.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUDoFreezeEventHandlerTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUDoPlacementParticleEventHandler.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUDoPlacementParticleEventHandlerTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUDoScaleEventHandler.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUDoScaleEventHandlerTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUDoStopSystemEventHandler.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUDoStopSystemEventHandlerTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUEventHandler.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUEventHandlerManager.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUEventHandlerTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUObserver.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUObserverManager.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUObserverTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnClearObserver.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnClearObserverTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnCollisionObserver.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnCollisionObserverTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnCountObserver.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnCountObserverTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnEmissionObserver.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnEmissionObserverTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnEventFlagObserver.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnEventFlagObserverTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnExpireObserver.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnExpireObserverTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnPositionObserver.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnPositionObserverTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnQuotaObserver.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnQuotaObserverTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnRandomObserver.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnRandomObserverTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnTimeObserver.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnTimeObserverTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnVelocityObserver.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUOnVelocityObserverTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUBehaviour.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUBehaviourManager.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUBehaviourTranslator.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUSlaveBehaviour.cpp
[armeabi] Compile++ arm  : cocos_extension_static <= CCPUSlaveBehaviourTranslator.cpp
[armeabi] Compile++ thumb: audioengine_static <= AudioEngine-inl.cpp
[armeabi] Compile++ thumb: audioengine_static <= AudioEngine.cpp
[armeabi] Compile++ thumb: audioengine_static <= CCThreadPool.cpp
[armeabi] Compile++ thumb: audioengine_static <= AssetFd.cpp
[armeabi] Compile++ thumb: audioengine_static <= AudioDecoder.cpp
In file included from c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/OpenSLHelper.h:27:0,
                 from c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/AudioPlayerProvider.h:28,
                 from c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/AudioEngine-inl.cpp:51:
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/AudioEngine-inl.cpp: In lambda function:
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/cutils/log.h:487:47: warning: format '%d' expects argument of type 'int', but argument 4 has type 'cocos2d::experimental::IAudioPlayer::State' [-Wformat=]
     __android_log_print(prio, tag, __VA_ARGS__)
                                               ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/cutils/log.h:459:5: note: in expansion of macro 'android_printLog'
     android_printLog(priority, tag, __VA_ARGS__)
     ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/cutils/log.h:451:5: note: in expansion of macro 'LOG_PRI'
     LOG_PRI(ANDROID_##priority, tag, __VA_ARGS__)
     ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/cutils/log.h:89:29: note: in expansion of macro 'ALOG'
 #define __ALOGV(...) ((void)ALOG(LOG_VERBOSE, LOG_TAG, __VA_ARGS__))
                             ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/cutils/log.h:93:20: note: in expansion of macro '__ALOGV'
 #define ALOGV(...) __ALOGV(__VA_ARGS__)
                    ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/AudioEngine-inl.cpp:222:21: note: in expansion of macro 'ALOGV'
                     ALOGV("Ignore state: %d", state);
                     ^
[armeabi] Compile++ thumb: audioengine_static <= AudioPlayerProvider.cpp
[armeabi] Compile++ thumb: audioengine_static <= AudioResampler.cpp
[armeabi] Compile++ thumb: audioengine_static <= AudioResamplerCubic.cpp
[armeabi] Compile++ thumb: audioengine_static <= PcmBufferProvider.cpp
[armeabi] Compile++ thumb: audioengine_static <= PcmAudioPlayer.cpp
[armeabi] Compile++ thumb: audioengine_static <= UrlAudioPlayer.cpp
[armeabi] Compile++ thumb: audioengine_static <= PcmData.cpp
In file included from c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/OpenSLHelper.h:27:0,
                 from c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/UrlAudioPlayer.h:28,
                 from c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/UrlAudioPlayer.cpp:27:
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/UrlAudioPlayer.cpp: In member function 'virtual void cocos2d::experimental::UrlAudioPlayer::stop()':
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/cutils/log.h:487:47: warning: format '%d' expects argument of type 'int', but argument 5 has type 'cocos2d::experimental::IAudioPlayer::State' [-Wformat=]
     __android_log_print(prio, tag, __VA_ARGS__)
                                               ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/cutils/log.h:459:5: note: in expansion of macro 'android_printLog'
     android_printLog(priority, tag, __VA_ARGS__)
     ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/cutils/log.h:451:5: note: in expansion of macro 'LOG_PRI'
     LOG_PRI(ANDROID_##priority, tag, __VA_ARGS__)
     ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/cutils/log.h:140:27: note: in expansion of macro 'ALOG'
 #define ALOGW(...) ((void)ALOG(LOG_WARN, LOG_TAG, __VA_ARGS__))
                           ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/UrlAudioPlayer.cpp:172:9: note: in expansion of macro 'ALOGW'
         ALOGW("UrlAudioPlayer (%p, state:%d) isn't playing or paused, could not invoke stop!", this, _state);
         ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/UrlAudioPlayer.cpp: In member function 'virtual void cocos2d::experimental::UrlAudioPlayer::pause()':
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/cutils/log.h:487:47: warning: format '%d' expects argument of type 'int', but argument 5 has type 'cocos2d::experimental::IAudioPlayer::State' [-Wformat=]
     __android_log_print(prio, tag, __VA_ARGS__)
                                               ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/cutils/log.h:459:5: note: in expansion of macro 'android_printLog'
     android_printLog(priority, tag, __VA_ARGS__)
     ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/cutils/log.h:451:5: note: in expansion of macro 'LOG_PRI'
     LOG_PRI(ANDROID_##priority, tag, __VA_ARGS__)
     ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/cutils/log.h:140:27: note: in expansion of macro 'ALOG'
 #define ALOGW(...) ((void)ALOG(LOG_WARN, LOG_TAG, __VA_ARGS__))
                           ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/UrlAudioPlayer.cpp:186:9: note: in expansion of macro 'ALOGW'
         ALOGW("UrlAudioPlayer (%p, state:%d) isn't playing, could not invoke pause!", this, _state);
         ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/UrlAudioPlayer.cpp: In member function 'virtual void cocos2d::experimental::UrlAudioPlayer::resume()':
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/cutils/log.h:487:47: warning: format '%d' expects argument of type 'int', but argument 5 has type 'cocos2d::experimental::IAudioPlayer::State' [-Wformat=]
     __android_log_print(prio, tag, __VA_ARGS__)
                                               ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/cutils/log.h:459:5: note: in expansion of macro 'android_printLog'
     android_printLog(priority, tag, __VA_ARGS__)
     ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/cutils/log.h:451:5: note: in expansion of macro 'LOG_PRI'
     LOG_PRI(ANDROID_##priority, tag, __VA_ARGS__)
     ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/cutils/log.h:140:27: note: in expansion of macro 'ALOG'
 #define ALOGW(...) ((void)ALOG(LOG_WARN, LOG_TAG, __VA_ARGS__))
                           ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/UrlAudioPlayer.cpp:200:9: note: in expansion of macro 'ALOGW'
         ALOGW("UrlAudioPlayer (%p, state:%d) isn't paused, could not invoke resume!", this, _state);
         ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/UrlAudioPlayer.cpp: In member function 'virtual void cocos2d::experimental::UrlAudioPlayer::play()':
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/cutils/log.h:487:47: warning: format '%d' expects argument of type 'int', but argument 5 has type 'cocos2d::experimental::IAudioPlayer::State' [-Wformat=]
     __android_log_print(prio, tag, __VA_ARGS__)
                                               ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/cutils/log.h:459:5: note: in expansion of macro 'android_printLog'
     android_printLog(priority, tag, __VA_ARGS__)
     ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/cutils/log.h:451:5: note: in expansion of macro 'LOG_PRI'
     LOG_PRI(ANDROID_##priority, tag, __VA_ARGS__)
     ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/../../audio/android/cutils/log.h:140:27: note: in expansion of macro 'ALOG'
 #define ALOGW(...) ((void)ALOG(LOG_WARN, LOG_TAG, __VA_ARGS__))
                           ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/audio/android/UrlAudioPlayer.cpp:214:9: note: in expansion of macro 'ALOGW'
         ALOGW("UrlAudioPlayer (%p, state:%d) isn't paused or initialized, could not invoke play!", this, _state);
         ^
[armeabi] Compile++ thumb: audioengine_static <= AudioMixer.cpp
[armeabi] Compile++ thumb: audioengine_static <= AudioMixerController.cpp
[armeabi] Compile++ thumb: audioengine_static <= PcmAudioService.cpp
[armeabi] Compile++ thumb: audioengine_static <= Track.cpp
[armeabi] Compile thumb  : audioengine_static <= format.c
[armeabi] Compile++ thumb: audioengine_static <= minifloat.cpp
[armeabi] Compile thumb  : audioengine_static <= primitives.c
[armeabi] Compile++ thumb: audioengine_static <= Utils.cpp
[armeabi] Compile++ arm  : box2d_static <= b2BroadPhase.cpp
[armeabi] Compile++ arm  : box2d_static <= b2CollideCircle.cpp
[armeabi] Compile++ arm  : box2d_static <= b2CollideEdge.cpp
[armeabi] Compile++ arm  : box2d_static <= b2CollidePolygon.cpp
[armeabi] Compile++ arm  : box2d_static <= b2Collision.cpp
[armeabi] Compile++ arm  : box2d_static <= b2Distance.cpp
[armeabi] Compile++ arm  : box2d_static <= b2DynamicTree.cpp
[armeabi] Compile++ arm  : box2d_static <= b2TimeOfImpact.cpp
[armeabi] Compile++ arm  : box2d_static <= b2ChainShape.cpp
[armeabi] Compile++ arm  : box2d_static <= b2CircleShape.cpp
[armeabi] Compile++ arm  : box2d_static <= b2EdgeShape.cpp
[armeabi][armeabi] Compile++ arm  : Compile++ arm  : box2d_static <= b2PolygonShape.cpp box2d_static <= b2Draw.cpp

[armeabi] Compile++ arm  : box2d_static <= b2BlockAllocator.cpp
[armeabi] Compile++ arm  : box2d_static <= b2Settings.cpp
[armeabi] Compile++ arm  : box2d_static <= b2Math.cpp
[armeabi] Compile++ arm  : box2d_static <= b2Timer.cpp
[armeabi] Compile++ arm  : box2d_static <= b2StackAllocator.cpp
[armeabi] Compile++ arm  : box2d_static <= b2ContactManager.cpp
[armeabi] Compile++ arm  : box2d_static <= b2Body.cpp
[armeabi][armeabi] Compile++ arm  : Compile++ arm  : box2d_static <= b2Fixture.cpp box2d_static <= b2Island.cpp

[armeabi] Compile++ arm  : box2d_static <= b2World.cpp
[armeabi] Compile++ arm  : box2d_static <= b2WorldCallbacks.cpp
[armeabi] Compile++ arm  : box2d_static <= b2ChainAndCircleContact.cpp
[armeabi] Compile++ arm  : box2d_static <= b2ChainAndPolygonContact.cpp
[armeabi] Compile++ arm  : box2d_static <= b2CircleContact.cpp
[armeabi] Compile++ arm  : box2d_static <= b2Contact.cpp
[armeabi] Compile++ arm  : box2d_static <= b2ContactSolver.cpp
[armeabi] Compile++ arm  : box2d_static <= b2EdgeAndCircleContact.cpp
[armeabi] Compile++ arm  : box2d_static <= b2EdgeAndPolygonContact.cpp
[armeabi][armeabi] Compile++ arm  : Compile++ arm  : box2d_static <= b2PolygonAndCircleContact.cpp
 box2d_static <= b2PolygonContact.cpp
[armeabi] Compile++ arm  : box2d_static <= b2DistanceJoint.cpp
[armeabi] Compile++ arm  : box2d_static <= b2FrictionJoint.cpp
[armeabi] Compile++ arm  : box2d_static <= b2GearJoint.cpp
[armeabi] Compile++ arm  : box2d_static <= b2MotorJoint.cpp
[armeabi] Compile++ arm  : box2d_static <= b2Joint.cpp
[armeabi][armeabi] Compile++ arm  : Compile++ arm  : box2d_static <= b2MouseJoint.cpp
 box2d_static <= b2PrismaticJoint.cpp
[armeabi] Compile++ arm  : box2d_static <= b2PulleyJoint.cpp
[armeabi] Compile++ arm  : box2d_static <= b2RevoluteJoint.cpp
[armeabi] Compile++ arm  : box2d_static <= b2RopeJoint.cpp
[armeabi] Compile++ arm  : box2d_static <= b2WeldJoint.cpp
[armeabi] Compile++ arm  : box2d_static <= b2WheelJoint.cpp
[armeabi] Compile++ arm  : box2d_static <= b2Rope.cpp
[armeabi] Compile++ arm  : cocos_network_static <= HttpClient-android.cpp
[armeabi][armeabi] Compile++ arm  : Compile++ arm  : cocos_network_static <= CCDownloader.cpp cocos_network_static <= SocketIO.cpp

[armeabi] Compile++ arm  : cocos_network_static <= WebSocket.cpp
[armeabi] Compile++ arm  : cocos_network_static <= CCDownloader-android.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= cocos2d.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCAction.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCActionCamera.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCActionCatmullRom.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCActionEase.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCActionGrid.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCActionGrid3D.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCActionInstant.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCActionInterval.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCActionManager.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCActionPageTurn3D.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCActionProgressTimer.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCActionTiledGrid.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCActionTween.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCAnimation.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCAnimationCache.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCAtlasNode.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCCamera.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCCameraBackgroundBrush.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCClippingNode.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCClippingRectangleNode.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCComponent.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCComponentContainer.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCDrawNode.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCDrawingPrimitives.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCFastTMXLayer.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCFastTMXTiledMap.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCFont.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCFontAtlas.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCFontAtlasCache.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCFontCharMap.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCFontFNT.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCFontFreeType.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCGLBufferedNode.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCGrabber.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCGrid.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCLabel.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCLabelAtlas.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCLabelBMFont.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCLabelTTF.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCLabelTextFormatter.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCLayer.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCLight.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCMenu.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCMenuItem.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCMotionStreak.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCNode.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCNodeGrid.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCParallaxNode.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCParticleBatchNode.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCParticleExamples.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCParticleSystem.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCParticleSystemQuad.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCProgressTimer.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCProtectedNode.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCRenderTexture.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCScene.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCSprite.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCSpriteBatchNode.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCSpriteFrame.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCSpriteFrameCache.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCTMXLayer.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCTMXObjectGroup.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCTMXTiledMap.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCTMXXMLParser.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCTextFieldTTF.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCTileMapAtlas.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCTransition.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCTransitionPageTurn.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCTransitionProgress.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCTweenFunction.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCAutoPolygon.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCFrustum.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCPlane.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCFileUtils.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCImage.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCGLView.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCSAXParser.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCThread.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= MathUtil.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCAffineTransform.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCGeometry.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCVertex.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= Mat4.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= Quaternion.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= TransformUtils.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= Vec2.cpp
[armeabi][armeabi] Compile++ arm  : Compile++ arm  : cocos2dx_internal_static <= Vec4.cpp cocos2dx_internal_static <= Vec3.cpp

[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCNinePatchImageParser.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCStencilStateManager.cpp
[armeabi][armeabi] Compile++ arm  : Compile++ arm  : cocos2dx_internal_static <= CCAsyncTaskPool.cpp cocos2dx_internal_static <= CCAutoreleasePool.cpp

[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCConfiguration.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCConsole.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCController-android.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCController.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCData.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCDataVisitor.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCDirector.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCEvent.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCEventAcceleration.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCEventController.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCEventCustom.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCEventDispatcher.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCEventFocus.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCEventKeyboard.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCEventListener.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCEventListenerAcceleration.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCEventListenerController.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCEventListenerCustom.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCEventListenerFocus.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCEventListenerKeyboard.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCEventListenerMouse.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCEventListenerTouch.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCEventMouse.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCEventTouch.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCIMEDispatcher.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCNS.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCProfiling.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCProperties.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCRef.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCScheduler.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCScriptSupport.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCTouch.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCUserDefault-android.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCUserDefault.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCValue.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= ObjectFactory.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= TGAlib.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= ZipUtils.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCAllocatorDiagnostics.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCAllocatorGlobal.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCAllocatorGlobalNewDelete.cpp
[armeabi] Compile++ arm  :[armeabi] Compile++ arm  : cocos2dx_internal_static <= base64.cpp
 cocos2dx_internal_static <= atitc.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= ccCArray.cpp
[armeabi] Compile arm    : cocos2dx_internal_static <= ccFPSImages.c
[armeabi] Compile++ arm  : cocos2dx_internal_static <= ccRandom.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= ccTypes.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= ccUTF8.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= etc1.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= ccUtils.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= pvr.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= s3tc.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCBatchCommand.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCCustomCommand.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCGLProgramCache.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCGLProgram.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCGLProgramState.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCGLProgramStateCache.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCGroupCommand.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCMaterial.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCMeshCommand.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCPass.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCPrimitive.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCPrimitiveCommand.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCQuadCommand.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCRenderCommand.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCRenderState.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCRenderer.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCTechnique.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCTexture2D.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCTextureAtlas.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCTextureCache.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCTextureCube.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCTrianglesCommand.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCVertexAttribBinding.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCVertexIndexBuffer.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCVertexIndexData.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= ccGLStateCache.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCFrameBuffer.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= ccShaders.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCVRDistortion.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCVRDistortionMesh.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCVRGenericRenderer.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCVRGenericHeadTracker.cpp
[armeabi] Compile++ arm  :[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCArray.cpp
 cocos2dx_internal_static <= CCDeprecated.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCDictionary.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCNotificationCenter.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCSet.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCString.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCPhysicsBody.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCPhysicsContact.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCPhysicsJoint.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCPhysicsShape.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCPhysicsWorld.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCPhysics3D.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCPhysics3DWorld.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCPhysics3DComponent.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCPhysics3DDebugDrawer.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCPhysics3DObject.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCPhysics3DShape.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCPhysicsSprite3D.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCPhysics3DConstraint.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCNavMesh.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCNavMeshAgent.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCNavMeshDebugDraw.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCNavMeshObstacle.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= CCNavMeshUtils.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= ConvertUTFWrapper.cpp
[armeabi] Compile arm    : cocos2dx_internal_static <= ConvertUTF.c
[armeabi] Compile++ arm  : cocos2dx_internal_static <= tinyxml2.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= ioapi_mem.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= ioapi.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= unzip.cpp
[armeabi] Compile++ arm  : cocos2dx_internal_static <= edtaa3func.cpp
[armeabi] Compile arm    : cocos2dx_internal_static <= xxhash.c
[armeabi] Compile++ arm  : cocos2dx_internal_static <= shapes.cc
[armeabi] Compile++ arm  : cocos2dx_internal_static <= advancing_front.cc
[armeabi] Compile++ arm  : cocos2dx_internal_static <= cdt.cc
[armeabi] Compile++ arm  : cocos2dx_internal_static <= sweep_context.cc
[armeabi] Compile++ arm  : cocos2dx_internal_static <= sweep.cc
[armeabi] Compile++ arm  : cocos2dx_internal_static <= clipper.cpp
[armeabi] Compile++ arm  : recast_static <= DebugDraw.cpp
[armeabi] Compile++ arm  : recast_static <= DetourDebugDraw.cpp
[armeabi] Compile++ arm  : recast_static <= DetourAlloc.cpp
[armeabi] Compile++ arm  : recast_static <= DetourCommon.cpp
[armeabi] Compile++ arm  : recast_static <= DetourNavMesh.cpp
[armeabi] Compile++ arm  : recast_static <= DetourNavMeshBuilder.cpp
[armeabi] Compile++ arm  : recast_static <= DetourNavMeshQuery.cpp
[armeabi] Compile++ arm  : recast_static <= DetourNode.cpp
[armeabi] Compile++ arm  : recast_static <= DetourCrowd.cpp
[armeabi] Compile++ arm  : recast_static <= DetourLocalBoundary.cpp
[armeabi] Compile++ arm  : recast_static <= DetourObstacleAvoidance.cpp
[armeabi] Compile++ arm  : recast_static <= DetourPathCorridor.cpp
[armeabi] Compile++ arm  : recast_static <= DetourPathQueue.cpp
[armeabi] Compile++ arm  : recast_static <= DetourProximityGrid.cpp
[armeabi] Compile++ arm  : recast_static <= DetourTileCache.cpp
[armeabi] Compile++ arm  : recast_static <= DetourTileCacheBuilder.cpp
[armeabi] Compile arm    : recast_static <= fastlz.c
[armeabi] Compile++ arm  : bullet_static <= btAxisSweep3.cpp
[armeabi] Compile++ arm  : bullet_static <= btBroadphaseProxy.cpp
[armeabi] Compile++ arm  : bullet_static <= btCollisionAlgorithm.cpp
[armeabi] Compile++ arm  : bullet_static <= btDbvt.cpp
[armeabi] Compile++ arm  : bullet_static <= btDbvtBroadphase.cpp
[armeabi] Compile++ arm  : bullet_static <= btDispatcher.cpp
[armeabi] Compile++ arm  : bullet_static <= btMultiSapBroadphase.cpp
[armeabi] Compile++ arm  : bullet_static <= btQuantizedBvh.cpp
[armeabi] Compile++ arm  : bullet_static <= btOverlappingPairCache.cpp
[armeabi] Compile++ arm  : bullet_static <= btSimpleBroadphase.cpp
[armeabi] Compile++ arm  : bullet_static <= btActivatingCollisionAlgorithm.cpp
[armeabi] Compile++ arm  : bullet_static <= btBoxBoxCollisionAlgorithm.cpp
[armeabi] Compile++ arm  : bullet_static <= btBox2dBox2dCollisionAlgorithm.cpp
[armeabi] Compile++ arm  : bullet_static <= btBoxBoxDetector.cpp
[armeabi] Compile++ arm  : bullet_static <= btCollisionDispatcher.cpp
[armeabi] Compile++ arm  : bullet_static <= btCollisionObject.cpp
[armeabi] Compile++ arm  : bullet_static <= btCollisionWorld.cpp
[armeabi] Compile++ arm  : bullet_static <= btCompoundCollisionAlgorithm.cpp
[armeabi] Compile++ arm  : bullet_static <= btConvexConcaveCollisionAlgorithm.cpp
[armeabi] Compile++ arm  : bullet_static <= btCompoundCompoundCollisionAlgorithm.cpp
[armeabi] Compile++ arm  : bullet_static <= btConvexConvexAlgorithm.cpp
[armeabi] Compile++ arm  : bullet_static <= btConvexPlaneCollisionAlgorithm.cpp
[armeabi] Compile++ arm  : bullet_static <= btConvex2dConvex2dAlgorithm.cpp
[armeabi] Compile++ arm  : bullet_static <= btDefaultCollisionConfiguration.cpp
[armeabi] Compile++ arm  : bullet_static <= btEmptyCollisionAlgorithm.cpp
[armeabi] Compile++ arm  : bullet_static <= btHashedSimplePairCache.cpp
[armeabi] Compile++ arm  : bullet_static <= btGhostObject.cpp
[armeabi] Compile++ arm  : bullet_static <= btInternalEdgeUtility.cpp
[armeabi] Compile++ arm  : bullet_static <= btManifoldResult.cpp
[armeabi] Compile++ arm  : bullet_static <= btSimulationIslandManager.cpp
[armeabi] Compile++ arm  : bullet_static <= btSphereBoxCollisionAlgorithm.cpp
[armeabi] Compile++ arm  : bullet_static <= btSphereSphereCollisionAlgorithm.cpp
[armeabi] Compile++ arm  : bullet_static <= btSphereTriangleCollisionAlgorithm.cpp
[armeabi] Compile++ arm  : bullet_static <= btUnionFind.cpp
[armeabi] Compile++ arm  : bullet_static <= SphereTriangleDetector.cpp
[armeabi] Compile++ arm  : bullet_static <= btBoxShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btBox2dShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btBvhTriangleMeshShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btCapsuleShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btCollisionShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btCompoundShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btConeShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btConcaveShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btConvexHullShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btConvexInternalShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btConvexPointCloudShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btConvexPolyhedron.cpp
[armeabi] Compile++ arm  : bullet_static <= btConvexShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btConvex2dShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btConvexTriangleMeshShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btCylinderShape.cpp
[armeabi][armeabi] Compile++ arm  : Compile++ arm  : bullet_static <= btHeightfieldTerrainShape.cpp bullet_static <= btEmptyShape.cpp

[armeabi] Compile++ arm  : bullet_static <= btMinkowskiSumShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btMultimaterialTriangleMeshShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btMultiSphereShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btOptimizedBvh.cpp
[armeabi] Compile++ arm  : bullet_static <= btPolyhedralConvexShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btScaledBvhTriangleMeshShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btShapeHull.cpp
[armeabi] Compile++ arm  : bullet_static <= btSphereShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btStaticPlaneShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btStridingMeshInterface.cpp
[armeabi] Compile++ arm  : bullet_static <= btTetrahedronShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btTriangleBuffer.cpp
[armeabi] Compile++ arm  : bullet_static <= btTriangleCallback.cpp
[armeabi] Compile++ arm  : bullet_static <= btTriangleIndexVertexArray.cpp
[armeabi] Compile++ arm  :[armeabi] bullet_static <= btTriangleIndexVertexMaterialArray.cpp Compile++ arm  : bullet_static <= btTriangleMesh.cpp

[armeabi] Compile++ arm  : bullet_static <= btTriangleMeshShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btUniformScalingShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btContactProcessing.cpp
[armeabi] Compile++ arm  : bullet_static <= btGenericPoolAllocator.cpp
[armeabi] Compile++ arm  : bullet_static <= btGImpactBvh.cpp
[armeabi] Compile++ arm  : bullet_static <= btGImpactCollisionAlgorithm.cpp
[armeabi] Compile++ arm  : bullet_static <= btGImpactQuantizedBvh.cpp
[armeabi] Compile++ arm  : bullet_static <= btGImpactShape.cpp
[armeabi] Compile++ arm  : bullet_static <= btTriangleShapeEx.cpp
[armeabi] Compile++ arm  : bullet_static <= gim_box_set.cpp
[armeabi] Compile++ arm  : bullet_static <= gim_contact.cpp
[armeabi] Compile++ arm  : bullet_static <= gim_memory.cpp
[armeabi] Compile++ arm  : bullet_static <= gim_tri_collision.cpp
[armeabi] Compile++ arm  : bullet_static <= btContinuousConvexCollision.cpp
[armeabi] Compile++ arm  : bullet_static <= btConvexCast.cpp
[armeabi] Compile++ arm  : bullet_static <= btGjkConvexCast.cpp
[armeabi] Compile++ arm  : bullet_static <= btGjkEpa2.cpp
[armeabi] Compile++ arm  : bullet_static <= btGjkEpaPenetrationDepthSolver.cpp
[armeabi] Compile++ arm  : bullet_static <= btGjkPairDetector.cpp
[armeabi] Compile++ arm  : bullet_static <= btMinkowskiPenetrationDepthSolver.cpp
[armeabi] Compile++ arm  : bullet_static <= btPersistentManifold.cpp
[armeabi] Compile++ arm  : bullet_static <= btRaycastCallback.cpp
[armeabi] Compile++ arm  : bullet_static <= btSubSimplexConvexCast.cpp
[armeabi] Compile++ arm  : bullet_static <= btVoronoiSimplexSolver.cpp
[armeabi] Compile++ arm  : bullet_static <= btPolyhedralContactClipping.cpp
[armeabi] Compile++ arm  : bullet_static <= btKinematicCharacterController.cpp
[armeabi] Compile++ arm  : bullet_static <= btConeTwistConstraint.cpp
[armeabi] Compile++ arm  : bullet_static <= btContactConstraint.cpp
[armeabi] Compile++ arm  : bullet_static <= btFixedConstraint.cpp
[armeabi] Compile++ arm  : bullet_static <= btGearConstraint.cpp
[armeabi] Compile++ arm  : bullet_static <= btGeneric6DofConstraint.cpp
[armeabi] Compile++ arm  : bullet_static <= btGeneric6DofSpringConstraint.cpp
[armeabi] Compile++ arm  : bullet_static <= btHinge2Constraint.cpp
[armeabi] Compile++ arm  : bullet_static <= btHingeConstraint.cpp
[armeabi] Compile++ arm  : bullet_static <= btPoint2PointConstraint.cpp
[armeabi] Compile++ arm  : bullet_static <= btSequentialImpulseConstraintSolver.cpp
[armeabi] Compile++ arm  : bullet_static <= btSliderConstraint.cpp
[armeabi] Compile++ arm  : bullet_static <= btSolve2LinearConstraint.cpp
[armeabi] Compile++ arm  : bullet_static <= btTypedConstraint.cpp
[armeabi] Compile++ arm  : bullet_static <= btUniversalConstraint.cpp
[armeabi] Compile++ arm  : bullet_static <= btDiscreteDynamicsWorld.cpp
[armeabi] Compile++ arm  : bullet_static <= btRigidBody.cpp
[armeabi] Compile++ arm  : bullet_static <= btSimpleDynamicsWorld.cpp
[armeabi] Compile++ arm  : bullet_static <= btRaycastVehicle.cpp
[armeabi] Compile++ arm  : bullet_static <= btWheelInfo.cpp
[armeabi] Compile++ arm  : bullet_static <= btMultiBody.cpp
[armeabi] Compile++ arm  : bullet_static <= btMultiBodyDynamicsWorld.cpp
[armeabi] Compile++ arm  : bullet_static <= btMultiBodyConstraintSolver.cpp
[armeabi] Compile++ arm  : bullet_static <= btMultiBodyJointLimitConstraint.cpp
[armeabi] Compile++ arm  : bullet_static <= btMultiBodyConstraint.cpp
[armeabi] Compile++ arm  : bullet_static <= btMultiBodyPoint2Point.cpp
[armeabi] Compile++ arm  : bullet_static <= btMultiBodyJointMotor.cpp
[armeabi] Compile++ arm  : bullet_static <= btDantzigLCP.cpp
[armeabi] Compile++ arm  : bullet_static <= btMLCPSolver.cpp
[armeabi] Compile++ arm  : bullet_static <= btGpu3DGridBroadphase.cpp
[armeabi] Compile++ arm  : bullet_static <= btParallelConstraintSolver.cpp
[armeabi] Compile++ arm  : bullet_static <= btThreadSupportInterface.cpp
[armeabi] Compile++ arm  : bullet_static <= PosixThreadSupport.cpp
[armeabi] Compile++ arm  : bullet_static <= SequentialThreadSupport.cpp
[armeabi] Compile++ arm  : bullet_static <= SpuCollisionObjectWrapper.cpp
[armeabi] Compile++ arm  :[armeabi] bullet_static <= SpuContactManifoldCollisionAlgorithm.cpp Compile++ arm  :
 bullet_static <= SpuCollisionTaskProcess.cpp
[armeabi] Compile++ arm  : bullet_static <= SpuFakeDma.cpp
[armeabi] Compile++ arm  : bullet_static <= SpuGatheringCollisionDispatcher.cpp
[armeabi] Compile++ arm  : bullet_static <= SpuLibspe2Support.cpp
[armeabi] Compile++ arm  : bullet_static <= SpuSampleTaskProcess.cpp
[armeabi] Compile++ arm  : bullet_static <= boxBoxDistance.cpp
[armeabi] Compile++ arm  : bullet_static <= SpuCollisionShapes.cpp
[armeabi] Compile++ arm  : bullet_static <= SpuContactResult.cpp
[armeabi] Compile++ arm  : bullet_static <= SpuGatheringCollisionTask.cpp
[armeabi] Compile++ arm  : bullet_static <= SpuMinkowskiPenetrationDepthSolver.cpp
[armeabi] Compile++ arm  : bullet_static <= SpuSampleTask.cpp
[armeabi] Compile++ arm  : bullet_static <= btAlignedAllocator.cpp
[armeabi] Compile++ arm  : bullet_static <= btConvexHull.cpp
[armeabi] Compile++ arm  : bullet_static <= btConvexHullComputer.cpp
[armeabi] Compile++ arm  : bullet_static <= btGeometryUtil.cpp
[armeabi] Compile++ arm  : bullet_static <= btPolarDecomposition.cpp
[armeabi] Compile++ arm  : bullet_static <= btQuickprof.cpp
[armeabi] Compile++ arm  : bullet_static <= btSerializer.cpp
[armeabi] Compile++ arm  : bullet_static <= btVector3.cpp
[armeabi] Compile++ arm  : bullet_static <= MiniCLTask.cpp
[armeabi] Compile++ arm  : bullet_static <= MiniCL.cpp
[armeabi] Compile++ arm  : bullet_static <= MiniCLTaskScheduler.cpp
[armeabi] Compile++ thumb: cocos2dxandroid_static <= CCApplication-android.cpp
[armeabi] Compile++ thumb: cocos2dxandroid_static <= CCCommon-android.cpp
[armeabi] Compile++ thumb: cocos2dxandroid_static <= CCDevice-android.cpp
[armeabi] Compile++ thumb: cocos2dxandroid_static <= CCGLViewImpl-android.cpp
[armeabi] Compile++ thumb: cocos2dxandroid_static <= CCFileUtils-android.cpp
[armeabi] Compile++ thumb: cocos2dxandroid_static <= javaactivity-android.cpp
[armeabi] Compile++ thumb: cocos2dxandroid_static <= CCEnhanceAPI-android.cpp
[armeabi] Compile++ thumb: cocos2dxandroid_static <= Java_org_cocos2dx_lib_Cocos2dxAccelerometer.cpp
[armeabi] Compile++ thumb: cocos2dxandroid_static <= Java_org_cocos2dx_lib_Cocos2dxBitmap.cpp
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/platform/android/javaactivity-android.cpp: In function 'void Java_org_cocos2dx_lib_Cocos2dxRenderer_nativeInit(JNIEnv*, jobject, jint, jint)':
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/platform/android/javaactivity-android.cpp:101:34: warning: 'void cocos2d::DrawPrimitives::init()' is deprecated (declared at c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/platform/android/../../2d/CCDrawingPrimitives.h:88) [-Wdeprecated-declarations]
         cocos2d::DrawPrimitives::init();
                                  ^
c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/platform/android/javaactivity-android.cpp:101:39: warning: 'void cocos2d::DrawPrimitives::init()' is deprecated (declared at c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android/../cocos2d/cocos/platform/android/../../2d/CCDrawingPrimitives.h:88) [-Wdeprecated-declarations]
         cocos2d::DrawPrimitives::init();
                                       ^
[armeabi] Compile++ thumb: cocos2dxandroid_static <= Java_org_cocos2dx_lib_Cocos2dxHelper.cpp
[armeabi] Compile++ thumb: cocos2dxandroid_static <= Java_org_cocos2dx_lib_Cocos2dxRenderer.cpp
[armeabi] Compile++ thumb: cocos2dxandroid_static <= JniHelper.cpp
[armeabi] Compile++ thumb: cocos2dxandroid_static <= TouchesJni.cpp
[armeabi] Compile thumb  : cpufeatures <= cpu-features.c
[armeabi] StaticLibrary  : libcocostudio.a
[armeabi] StaticLibrary  : libcocosbuilder.a
[armeabi] StaticLibrary  : libcocos3d.a
[armeabi] StaticLibrary  : libspine.a
[armeabi] StaticLibrary  : libui.a
[armeabi] StaticLibrary  : libcocosdenshion.a
[armeabi] StaticLibrary  : flatbuffers.a
[armeabi] StaticLibrary  : libextension.a
[armeabi] StaticLibrary  : libaudioengine.a
[armeabi] StaticLibrary  : libbox2d.a
[armeabi] StaticLibrary  : libnetwork.a
[armeabi] StaticLibrary  : libcocos2dxinternal.a
[armeabi] StaticLibrary  : librecast.a
[armeabi] StaticLibrary  : libbullet.a
[armeabi] StaticLibrary  : libcocos2dandroid.a
[armeabi] StaticLibrary  : libcpufeatures.a
[armeabi] SharedLibrary  : libMyGame.so
[armeabi] Install        : libMyGame.so => libs/armeabi/libMyGame.so
make: Leaving directory `c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android'
Building apk...
running: '"C:\Software\Apache-Ant\apache-ant-1.9.7\bin\ant" clean debug -f c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\build.xml -Dsdk.dir="C:\Software\Android"'

Unable to locate tools.jar. Expected to find it in C:\Software\Java\jre1.8.0_91\lib\tools.jar
Buildfile: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\build.xml

-check-env:
 [checkenv] Android SDK Tools Revision 25.1.7
 [checkenv] Installed at C:\Software\Android

-setup:
     [echo] Project Name: BasicX
  [gettype] Project Type: Application

-pre-clean:

clean:
[getlibpath] Library dependencies:
[getlibpath]
[getlibpath] ------------------
[getlibpath] Ordered libraries:

nodeps:

-check-env:
 [checkenv] Android SDK Tools Revision 25.1.7
 [checkenv] Installed at C:\Software\Android

-setup:
     [echo] Project Name: cocos2dxandroid
  [gettype] Project Type: Android Library

-pre-clean:

clean:

-set-mode-check:

-set-debug-files:

-check-env:
 [checkenv] Android SDK Tools Revision 25.1.7
 [checkenv] Installed at C:\Software\Android

-setup:
     [echo] Project Name: BasicX
  [gettype] Project Type: Application

-set-debug-mode:

-debug-obfuscation-check:

-pre-build:

-build-setup:
[getbuildtools] Using latest Build Tools: 24.0.0
     [echo] Resolving Build Target for BasicX...
[gettarget] Project Target:   Android 4.1.2
[gettarget] API level:        16
     [echo] ----------
     [echo] Creating output directories if needed...
    [mkdir] Created dir: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin
    [mkdir] Created dir: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\res
    [mkdir] Created dir: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\rsObj
    [mkdir] Created dir: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\rsLibs
    [mkdir] Created dir: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\gen
    [mkdir] Created dir: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\classes
    [mkdir] Created dir: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\dexedLibs
     [echo] ----------
     [echo] Resolving Dependencies for BasicX...
[dependency] Ordered libraries:
[dependency] C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java
[dependency]
[dependency] ------------------
     [echo] ----------
     [echo] Building Libraries with 'debug'...

nodeps:

-set-mode-check:

-set-debug-files:

-check-env:
 [checkenv] Android SDK Tools Revision 25.1.7
 [checkenv] Installed at C:\Software\Android

-setup:
     [echo] Project Name: cocos2dxandroid
  [gettype] Project Type: Android Library

-set-debug-mode:

-debug-obfuscation-check:

-pre-build:

-build-setup:
[getbuildtools] Using latest Build Tools: 24.0.0
     [echo] Resolving Build Target for cocos2dxandroid...
[gettarget] Project Target:   Android 4.1.2
[gettarget] API level:        16
     [echo] ----------
     [echo] Creating output directories if needed...
    [mkdir] Created dir: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\res
    [mkdir] Created dir: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin
    [mkdir] Created dir: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin\res
    [mkdir] Created dir: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin\rsObj
    [mkdir] Created dir: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin\rsLibs
    [mkdir] Created dir: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\gen
    [mkdir] Created dir: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin\classes
    [mkdir] Created dir: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin\dexedLibs
     [echo] ----------
     [echo] Resolving Dependencies for cocos2dxandroid...
[dependency] Library dependencies:
[dependency] No Libraries
[dependency]
[dependency] ------------------

-code-gen:
[mergemanifest] Merging AndroidManifest files into one.
[mergemanifest] Manifest merger disabled. Using project manifest only.
     [echo] Handling aidl files...
     [aidl] Found 1 AIDL files.
     [aidl] Compiling 1 AIDL files.
     [echo] ----------
     [echo] Handling RenderScript files...
     [echo] ----------
     [echo] Handling Resources...
     [aapt] Generating resource IDs...
     [echo] ----------
     [echo] Handling BuildConfig class...
[buildconfig] Generating BuildConfig class.

-pre-compile:

-compile:

BUILD FAILED
C:\Software\Android\tools\ant\build.xml:597: The following error occurred while executing this line:
C:\Software\Android\tools\ant\build.xml:716: The following error occurred while executing this line:
C:\Software\Android\tools\ant\build.xml:730: Unable to find a javac compiler;
com.sun.tools.javac.Main is not on the classpath.
Perhaps JAVA_HOME does not point to the JDK.
It is currently set to "C:\Software\Java\jre1.8.0_91"

Total time: 2 seconds
Error running command, return code: 1.
```

Set JAVA_HOME environment variable C:\Software\Java\jdk1.8.0_92 and re-run

```sh
C:\Users\droid>cocos run -s c:\Users\droid\onGit\cocos2d-x-templates\BasicX -p android --ap android-16
Building mode: debug
Using Eclipse project : c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android
running: '"C:\Software\Android\tools\android" update project -t android-16 -p c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android'

Updated project.properties
Updated local.properties
Updated file c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\proguard-project.txt
running: '"C:\Software\Android\tools\android" update lib-project -p c:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java -t android-16'

                                                                                                                                                                                                  Updated project.properties
Updated local.properties
Updated file c:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\proguard-project.txt
Building native...
NDK build mode: debug
running: '"C:\Software\Android-NDK\android-ndk-r12b\ndk-build" -C c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android -j4 NDK_MODULE_PATH=c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\../cocos2d;c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\../cocos2d/cocos;c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\../cocos2d/external NDK_TOOLCHAIN_VERSION=4.9 NDK_DEBUG=1'

Android NDK: WARNING: APP_PLATFORM android-16 is larger than android:minSdkVersion 9 in ./AndroidManifest.xml
make: Entering directory `c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android'
[armeabi] StaticLibrary  : libcocos2d.a
[armeabi] StaticLibrary  : libcocostudio.a
[armeabi] StaticLibrary  : libcocosbuilder.a
[armeabi] StaticLibrary  : libcocos3d.a
[armeabi] StaticLibrary  : libspine.a
[armeabi] StaticLibrary  : libui.a
[armeabi] StaticLibrary  : libcocosdenshion.a
[armeabi] StaticLibrary  : flatbuffers.a
[armeabi] StaticLibrary  : libextension.a
[armeabi] StaticLibrary  : libaudioengine.a
[armeabi] StaticLibrary  : libbox2d.a
[armeabi] StaticLibrary  : libnetwork.a
[armeabi] StaticLibrary  : libcocos2dxinternal.a
[armeabi] StaticLibrary  : librecast.a
[armeabi] StaticLibrary  : libbullet.a
[armeabi] StaticLibrary  : libcocos2dandroid.a
[armeabi] StaticLibrary  : libcpufeatures.a
[armeabi] Gdbserver      : [arm-linux-androideabi-4.9] libs/armeabi/gdbserver
[armeabi] Gdbsetup       : libs/armeabi/gdb.setup
[armeabi] SharedLibrary  : libMyGame.so
[armeabi] Install        : libMyGame.so => libs/armeabi/libMyGame.so
make: Leaving directory `c:/Users/droid/onGit/cocos2d-x-templates/BasicX/proj.android'
Building apk...
running: '"C:\Software\Apache-Ant\apache-ant-1.9.7\bin\ant" clean debug -f c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\build.xml -Dsdk.dir="C:\Software\Android"'

Buildfile: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\build.xml

-check-env:
 [checkenv] Android SDK Tools Revision 25.1.7
 [checkenv] Installed at C:\Software\Android

-setup:
     [echo] Project Name: BasicX
  [gettype] Project Type: Application

-pre-clean:

clean:
   [delete] Deleting directory c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin
   [delete] Deleting directory c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\gen
[getlibpath] Library dependencies:
[getlibpath]
[getlibpath] ------------------
[getlibpath] Ordered libraries:

nodeps:

-check-env:
 [checkenv] Android SDK Tools Revision 25.1.7
 [checkenv] Installed at C:\Software\Android

-setup:
     [echo] Project Name: cocos2dxandroid
  [gettype] Project Type: Android Library

-pre-clean:

clean:
   [delete] Deleting directory C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin
   [delete] Deleting directory C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\gen

-set-mode-check:

-set-debug-files:

-check-env:
 [checkenv] Android SDK Tools Revision 25.1.7
 [checkenv] Installed at C:\Software\Android

-setup:
     [echo] Project Name: BasicX
  [gettype] Project Type: Application

-set-debug-mode:

-debug-obfuscation-check:

-pre-build:

-build-setup:
[getbuildtools] Using latest Build Tools: 24.0.0
     [echo] Resolving Build Target for BasicX...
[gettarget] Project Target:   Android 4.1.2
[gettarget] API level:        16
     [echo] ----------
     [echo] Creating output directories if needed...
    [mkdir] Created dir: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin
    [mkdir] Created dir: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\res
    [mkdir] Created dir: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\rsObj
    [mkdir] Created dir: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\rsLibs
    [mkdir] Created dir: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\gen
    [mkdir] Created dir: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\classes
    [mkdir] Created dir: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\dexedLibs
     [echo] ----------
     [echo] Resolving Dependencies for BasicX...
[dependency] Ordered libraries:
[dependency] C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java
[dependency]
[dependency] ------------------
     [echo] ----------
     [echo] Building Libraries with 'debug'...

nodeps:

-set-mode-check:

-set-debug-files:

-check-env:
 [checkenv] Android SDK Tools Revision 25.1.7
 [checkenv] Installed at C:\Software\Android

-setup:
     [echo] Project Name: cocos2dxandroid
  [gettype] Project Type: Android Library

-set-debug-mode:

-debug-obfuscation-check:

-pre-build:

-build-setup:
[getbuildtools] Using latest Build Tools: 24.0.0
     [echo] Resolving Build Target for cocos2dxandroid...
[gettarget] Project Target:   Android 4.1.2
[gettarget] API level:        16
     [echo] ----------
     [echo] Creating output directories if needed...
    [mkdir] Created dir: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin
    [mkdir] Created dir: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin\res
    [mkdir] Created dir: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin\rsObj
    [mkdir] Created dir: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin\rsLibs
    [mkdir] Created dir: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\gen
    [mkdir] Created dir: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin\classes
    [mkdir] Created dir: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin\dexedLibs
     [echo] ----------
     [echo] Resolving Dependencies for cocos2dxandroid...
[dependency] Library dependencies:
[dependency] No Libraries
[dependency]
[dependency] ------------------

-code-gen:
[mergemanifest] Merging AndroidManifest files into one.
[mergemanifest] Manifest merger disabled. Using project manifest only.
     [echo] Handling aidl files...
     [aidl] Found 1 AIDL files.
     [aidl] Compiling 1 AIDL files.
     [echo] ----------
     [echo] Handling RenderScript files...
     [echo] ----------
     [echo] Handling Resources...
     [aapt] Generating resource IDs...
     [echo] ----------
     [echo] Handling BuildConfig class...
[buildconfig] Generating BuildConfig class.

-pre-compile:

-compile:
    [javac] Compiling 29 source files to C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin\classes
    [javac] warning: [options] source value 1.5 is obsolete and will be removed in a future release
    [javac] warning: [options] target value 1.5 is obsolete and will be removed in a future release
    [javac] warning: [options] To suppress warnings about obsolete options, use -Xlint:-options.
    [javac] Note: Some input files use or override a deprecated API.
    [javac] Note: Recompile with -Xlint:deprecation for details.
    [javac] Note: Some input files use unchecked or unsafe operations.
    [javac] Note: Recompile with -Xlint:unchecked for details.
    [javac] 3 warnings
     [echo] Creating library output jar file...
      [jar] Building jar: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin\classes.jar

-post-compile:

-obfuscate:

-dex:
     [echo] Library project: do not convert bytecode...

-crunch:
   [crunch] Crunching PNG Files in source dir: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\res
   [crunch] To destination dir: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin\res
   [crunch] Crunched 0 PNG files to update cache

-package-resources:
     [echo] Library project: do not package resources...

-package:
     [echo] Library project: do not package apk...

-post-package:

-do-debug:
     [echo] Library project: do not create apk...
[propertyfile] Creating new property file: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin\build.prop
[propertyfile] Updating property file: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin\build.prop
[propertyfile] Updating property file: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin\build.prop
[propertyfile] Updating property file: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin\build.prop

-post-build:

debug:

-code-gen:
[mergemanifest] Merging AndroidManifest files into one.
[mergemanifest] Manifest merger disabled. Using project manifest only.
     [echo] Handling aidl files...
     [aidl] No AIDL files to compile.
     [echo] ----------
     [echo] Handling RenderScript files...
     [echo] ----------
     [echo] Handling Resources...
     [aapt] Generating resource IDs...
     [echo] ----------
     [echo] Handling BuildConfig class...
[buildconfig] Generating BuildConfig class.

-pre-compile:

-compile:
    [javac] Compiling 3 source files to c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\classes
    [javac] warning: [options] source value 1.5 is obsolete and will be removed in a future release
    [javac] warning: [options] target value 1.5 is obsolete and will be removed in a future release
    [javac] warning: [options] To suppress warnings about obsolete options, use -Xlint:-options.
    [javac] 3 warnings

-post-compile:

-obfuscate:

-dex:
      [dex] input: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\classes
      [dex] input: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin\classes.jar
      [dex] input: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\libs\com.android.vending.expansion.zipfile.jar
      [dex] input: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\libs\httpclient-4.4.1.1.jar
      [dex] input: C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\libs\android-async-http-1.4.9.jar
      [dex] Pre-Dexing C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\bin\classes.jar -> classes-64b4e7c2cf4a276d5d34b19f74415afe.jar
      [dex] Pre-Dexing C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\libs\com.android.vending.expansion.zipfile.jar -> com.android.vending.expansion.zipfile-e13a52bd7f9b391a02b5d4b5bd0f00f7.jar
      [dex] Pre-Dexing C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\libs\httpclient-4.4.1.1.jar -> httpclient-4.4.1.1-2ea5eb16173a0f936d7d09c3d0d81887.jar
      [dex] Pre-Dexing C:\Users\droid\onGit\cocos2d-x-templates\BasicX\cocos2d\cocos\platform\android\java\libs\android-async-http-1.4.9.jar -> android-async-http-1.4.9-2db3499ffe8182c2f48f368b2f807fbf.jar
      [dex] Converting compiled files and external libraries into c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\classes.dex...
       [dx] Merged dex #1 (6 defs/1.6KiB)
       [dx] Merged dex #2 (61 defs/106.4KiB)
       [dx] Merged dex #3 (124 defs/140.3KiB)
       [dx] Merged dex #4 (4 defs/15.8KiB)
       [dx] Merged dex #5 (797 defs/844.3KiB)
       [dx] Result is 992 defs/1371.2KiB. Took 0.3s

-crunch:
   [crunch] Crunching PNG Files in source dir: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\res
   [crunch] To destination dir: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\res
   [crunch] Processing image to cache: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\res\drawable-hdpi\icon.png => c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\res\drawable-hdpi\icon.png
   [crunch]   (processed image to cache entry c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\res\drawable-hdpi\icon.png: 67% size of source)
   [crunch] Processing image to cache: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\res\drawable-ldpi\icon.png => c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\res\drawable-ldpi\icon.png
   [crunch]   (processed image to cache entry c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\res\drawable-ldpi\icon.png: 0% size of source)
   [crunch] Processing image to cache: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\res\drawable-mdpi\icon.png => c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\res\drawable-mdpi\icon.png
   [crunch]   (processed image to cache entry c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\res\drawable-mdpi\icon.png: 53% size of source)
   [crunch] Crunched 3 PNG files to update cache

-package-resources:
     [aapt] Creating full resource package...
     [aapt]     (skipping file '.gitkeep' due to ANDROID_AAPT_IGNORE pattern '.*')

-package:
[apkbuilder] Current build type is different than previous build: forced apkbuilder run.
[apkbuilder] Creating BasicX-debug-unaligned.apk and signing it with a debug key...

-post-package:

-do-debug:
 [zipalign] Running zip align on final apk...
     [echo] Debug Package: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\BasicX-debug.apk
[propertyfile] Creating new property file: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\build.prop
[propertyfile] Updating property file: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\build.prop
[propertyfile] Updating property file: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\build.prop
[propertyfile] Updating property file: c:\Users\droid\onGit\cocos2d-x-templates\BasicX\proj.android\bin\build.prop

-post-build:

debug:

BUILD SUCCESSFUL
Total time: 17 seconds
Move apk to c:\Users\droid\onGit\cocos2d-x-templates\BasicX\bin\debug\android
Build succeed.
Deploying mode: debug
Installing on device
running: '"C:\Software\Android\platform-tools\adb" uninstall com.trdroid.basicgame'

adb server version (32) doesn't match this client (36); killing...
* daemon started successfully *
error: no devices/emulators found
Error running command, return code: 1.
```

```sh
C:\Users\droid>cd c:\Users\droid\onGit\cocos2d-x-templates\BasicX\bin\debug\android

c:\Users\droid\onGit\cocos2d-x-templates\BasicX\bin\debug\android>adb -d install -r BasicX-debug.apk
'adb' is not recognized as an internal or external command,
operable program or batch file.
```

Create the following environment variables

* ANDROID_HOME: C:\Software\Android
* ANDROID_PLATFORM_TOOLS: %ANDROID_HOME%\platform-tools
 
Add %ANDROID_PLATFORM_TOOLS% to the PATH environment variable.

```sh
c:\Users\droid\onGit\cocos2d-x-templates\BasicX\bin\debug\android>adb -d install -r BasicX-debug.apk
[100%] /data/local/tmp/BasicX-debug.apk
        pkg: /data/local/tmp/BasicX-debug.apk
Success
```

### Project Contents

```
C:\Users\droid\onGit\cocos2d-x-templates\CocosBasic>tree /f
Folder PATH listing for volume OS
Volume serial number is 00000027 266E:E77F
C:.
│   .cocos-project.json
│   CMakeLists.txt
│   README.md
│
├───Classes
│       AppDelegate.cpp
│       AppDelegate.h
│       HelloWorldScene.cpp
│       HelloWorldScene.h
│
├───cocos2d
│   │   AUTHORS
│   │   CHANGELOG
│   │   CMakeLists.txt
│   │   CONTRIBUTING.md
│   │   download-deps.py
│   │   issue_template.md
│   │   README.cmake
│   │   README.md
│   │
│   ├───build
│   │   │   android-build.py
│   │   │   cocos2d-win10.sln
│   │   │   cocos2d-win32.sln
│   │   │   cocos2d-win8.1-universal.sln
│   │   │   install-deps-linux.sh
│   │   │   win32-msvc-2013-x86.cmd
│   │   │
│   │   ├───cocos2d_libs.xcodeproj
│   │   │       project.pbxproj
│   │   │
│   │   ├───cocos2d_tests.xcodeproj
│   │   │       project.pbxproj
│   │   │
│   │   └───tizen
│   │           .cproject
│   │           .exportMap
│   │           .project
│   │           .tproject
│   │
│   ├───cmake
│   │   │   android.toolchain.cmake
│   │   │   AndroidNdkGdb.cmake
│   │   │   AndroidNdkModules.cmake
│   │   │   BuildHelpers.CMakeLists.txt
│   │   │   ios.toolchain.cmake
│   │   │
│   │   └───Modules
│   │           BuildModules.cmake
│   │           CMakeParseArguments.cmake
│   │           CocosBuildHelpers.cmake
│   │           CocosUsePrebuiltLibs.cmake
│   │           FindChipmunk.cmake
│   │           FindCURL.cmake
│   │           Findflatbuffers.cmake
│   │           FindFMOD.cmake
│   │           FindFontconfig.cmake
│   │           FindFreetype.cmake
│   │           FindGLFW3.cmake
│   │           FindGTK3.cmake
│   │           FindJPEG.cmake
│   │           FindMINIZIP.cmake
│   │           FindMPG123.cmake
│   │           FindOgg.cmake
│   │           FindPackageHandleStandardArgs.cmake
│   │           FindPackageMessage.cmake
│   │           FindPkgConfig.cmake
│   │           FindPNG.cmake
│   │           FindRecast.cmake
│   │           FindSQLite3.cmake
│   │           FindTIFF.cmake
│   │           FindTinyXML2.cmake
│   │           FindVorbis.cmake
│   │           FindWebP.cmake
│   │           FindWEBSOCKETS.cmake
│   │           Findxxhash.cmake
│   │           SelectLibraryConfigurations.cmake
│   │           SelectModule.cmake
│   │           SetCompilerOptions.cmake
│   │
│   ├───cocos
│   │   │   Android.mk
│   │   │   cc_dummy.c
│   │   │   CMakeLists.txt
│   │   │   cocos2d.cpp
│   │   │   cocos2d.h
│   │   │
│   │   ├───2d
│   │   │   │   CCAction.cpp
│   │   │   │   CCAction.h
│   │   │   │   CCActionCamera.cpp
│   │   │   │   CCActionCamera.h
│   │   │   │   CCActionCatmullRom.cpp
│   │   │   │   CCActionCatmullRom.h
│   │   │   │   CCActionEase.cpp
│   │   │   │   CCActionEase.h
│   │   │   │   CCActionGrid.cpp
│   │   │   │   CCActionGrid.h
│   │   │   │   CCActionGrid3D.cpp
│   │   │   │   CCActionGrid3D.h
│   │   │   │   CCActionInstant.cpp
│   │   │   │   CCActionInstant.h
│   │   │   │   CCActionInterval.cpp
│   │   │   │   CCActionInterval.h
│   │   │   │   CCActionManager.cpp
│   │   │   │   CCActionManager.h
│   │   │   │   CCActionPageTurn3D.cpp
│   │   │   │   CCActionPageTurn3D.h
│   │   │   │   CCActionProgressTimer.cpp
│   │   │   │   CCActionProgressTimer.h
│   │   │   │   CCActionTiledGrid.cpp
│   │   │   │   CCActionTiledGrid.h
│   │   │   │   CCActionTween.cpp
│   │   │   │   CCActionTween.h
│   │   │   │   CCAnimation.cpp
│   │   │   │   CCAnimation.h
│   │   │   │   CCAnimationCache.cpp
│   │   │   │   CCAnimationCache.h
│   │   │   │   CCAtlasNode.cpp
│   │   │   │   CCAtlasNode.h
│   │   │   │   CCAutoPolygon.cpp
│   │   │   │   CCAutoPolygon.h
│   │   │   │   CCCamera.cpp
│   │   │   │   CCCamera.h
│   │   │   │   CCCameraBackgroundBrush.cpp
│   │   │   │   CCCameraBackgroundBrush.h
│   │   │   │   CCClippingNode.cpp
│   │   │   │   CCClippingNode.h
│   │   │   │   CCClippingRectangleNode.cpp
│   │   │   │   CCClippingRectangleNode.h
│   │   │   │   CCComponent.cpp
│   │   │   │   CCComponent.h
│   │   │   │   CCComponentContainer.cpp
│   │   │   │   CCComponentContainer.h
│   │   │   │   CCDrawingPrimitives.cpp
│   │   │   │   CCDrawingPrimitives.h
│   │   │   │   CCDrawNode.cpp
│   │   │   │   CCDrawNode.h
│   │   │   │   CCFastTMXLayer.cpp
│   │   │   │   CCFastTMXLayer.h
│   │   │   │   CCFastTMXTiledMap.cpp
│   │   │   │   CCFastTMXTiledMap.h
│   │   │   │   CCFont.cpp
│   │   │   │   CCFont.h
│   │   │   │   CCFontAtlas.cpp
│   │   │   │   CCFontAtlas.h
│   │   │   │   CCFontAtlasCache.cpp
│   │   │   │   CCFontAtlasCache.h
│   │   │   │   CCFontCharMap.cpp
│   │   │   │   CCFontCharMap.h
│   │   │   │   CCFontFNT.cpp
│   │   │   │   CCFontFNT.h
│   │   │   │   CCFontFreeType.cpp
│   │   │   │   CCFontFreeType.h
│   │   │   │   CCGLBufferedNode.cpp
│   │   │   │   CCGLBufferedNode.h
│   │   │   │   CCGrabber.cpp
│   │   │   │   CCGrabber.h
│   │   │   │   CCGrid.cpp
│   │   │   │   CCGrid.h
│   │   │   │   CCLabel.cpp
│   │   │   │   CCLabel.h
│   │   │   │   CCLabelAtlas.cpp
│   │   │   │   CCLabelAtlas.h
│   │   │   │   CCLabelBMFont.cpp
│   │   │   │   CCLabelBMFont.h
│   │   │   │   CCLabelTextFormatter.cpp
│   │   │   │   CCLabelTextFormatter.h
│   │   │   │   CCLabelTTF.cpp
│   │   │   │   CCLabelTTF.h
│   │   │   │   CCLayer.cpp
│   │   │   │   CCLayer.h
│   │   │   │   CCLight.cpp
│   │   │   │   CCLight.h
│   │   │   │   CCMenu.cpp
│   │   │   │   CCMenu.h
│   │   │   │   CCMenuItem.cpp
│   │   │   │   CCMenuItem.h
│   │   │   │   CCMotionStreak.cpp
│   │   │   │   CCMotionStreak.h
│   │   │   │   CCNode.cpp
│   │   │   │   CCNode.h
│   │   │   │   CCNodeGrid.cpp
│   │   │   │   CCNodeGrid.h
│   │   │   │   CCParallaxNode.cpp
│   │   │   │   CCParallaxNode.h
│   │   │   │   CCParticleBatchNode.cpp
│   │   │   │   CCParticleBatchNode.h
│   │   │   │   CCParticleExamples.cpp
│   │   │   │   CCParticleExamples.h
│   │   │   │   CCParticleSystem.cpp
│   │   │   │   CCParticleSystem.h
│   │   │   │   CCParticleSystemQuad.cpp
│   │   │   │   CCParticleSystemQuad.h
│   │   │   │   CCProgressTimer.cpp
│   │   │   │   CCProgressTimer.h
│   │   │   │   CCProtectedNode.cpp
│   │   │   │   CCProtectedNode.h
│   │   │   │   CCRenderTexture.cpp
│   │   │   │   CCRenderTexture.h
│   │   │   │   CCScene.cpp
│   │   │   │   CCScene.h
│   │   │   │   CCSprite.cpp
│   │   │   │   CCSprite.h
│   │   │   │   CCSpriteBatchNode.cpp
│   │   │   │   CCSpriteBatchNode.h
│   │   │   │   CCSpriteFrame.cpp
│   │   │   │   CCSpriteFrame.h
│   │   │   │   CCSpriteFrameCache.cpp
│   │   │   │   CCSpriteFrameCache.h
│   │   │   │   CCTextFieldTTF.cpp
│   │   │   │   CCTextFieldTTF.h
│   │   │   │   CCTileMapAtlas.cpp
│   │   │   │   CCTileMapAtlas.h
│   │   │   │   CCTMXLayer.cpp
│   │   │   │   CCTMXLayer.h
│   │   │   │   CCTMXObjectGroup.cpp
│   │   │   │   CCTMXObjectGroup.h
│   │   │   │   CCTMXTiledMap.cpp
│   │   │   │   CCTMXTiledMap.h
│   │   │   │   CCTMXXMLParser.cpp
│   │   │   │   CCTMXXMLParser.h
│   │   │   │   CCTransition.cpp
│   │   │   │   CCTransition.h
│   │   │   │   CCTransitionPageTurn.cpp
│   │   │   │   CCTransitionPageTurn.h
│   │   │   │   CCTransitionProgress.cpp
│   │   │   │   CCTransitionProgress.h
│   │   │   │   CCTweenFunction.cpp
│   │   │   │   CCTweenFunction.h
│   │   │   │   CMakeLists.txt
│   │   │   │   cocos2d.def
│   │   │   │   cocos2dx.props
│   │   │   │   cocos2d_headers.props
│   │   │   │   libcocos2d.vcxproj
│   │   │   │   libcocos2d.vcxproj.filters
│   │   │   │
│   │   │   ├───libcocos2d_8_1
│   │   │   │   │   libcocos2d_8_1.sln
│   │   │   │   │
│   │   │   │   └───libcocos2d_8_1
│   │   │   │       ├───libcocos2d_8_1.Shared
│   │   │   │       │       libcocos2d_8_1.Shared.vcxitems
│   │   │   │       │       libcocos2d_8_1.Shared.vcxitems.filters
│   │   │   │       │       targetver.h
│   │   │   │       │
│   │   │   │       ├───libcocos2d_8_1.Windows
│   │   │   │       │       libcocos2d_8_1.Windows.vcxproj
│   │   │   │       │       libcocos2d_8_1.Windows.vcxproj.filters
│   │   │   │       │
│   │   │   │       └───libcocos2d_8_1.WindowsPhone
│   │   │   │               libcocos2d_8_1.WindowsPhone.vcxproj
│   │   │   │               libcocos2d_8_1.WindowsPhone.vcxproj.filters
│   │   │   │
│   │   │   ├───libcocos2d_win10
│   │   │   │       libcocos2d.vcxproj
│   │   │   │       libcocos2d.vcxproj.filters
│   │   │   │
│   │   │   ├───win10_props
│   │   │   │       cocos2d_win10.props
│   │   │   │       cocos2d_win10_app.props
│   │   │   │       cocos2d_win10_platform.props
│   │   │   │
│   │   │   ├───winrt_8.1_props
│   │   │   │       cocos2d_winrt_8.1.props
│   │   │   │       cocos2d_winrt_8.1_app.props
│   │   │   │       cocos2d_winrt_8.1_platform.props
│   │   │   │
│   │   │   └───wp_8.1_props
│   │   │           cocos2d_wp_8.1_platform.props
│   │   │
│   │   ├───3d
│   │   │       Android.mk
│   │   │       CCAABB.cpp
│   │   │       CCAABB.h
│   │   │       CCAnimate3D.cpp
│   │   │       CCAnimate3D.h
│   │   │       CCAnimation3D.cpp
│   │   │       CCAnimation3D.h
│   │   │       CCAnimationCurve.h
│   │   │       CCAnimationCurve.inl
│   │   │       CCAttachNode.cpp
│   │   │       CCAttachNode.h
│   │   │       CCBillBoard.cpp
│   │   │       CCBillBoard.h
│   │   │       CCBundle3D.cpp
│   │   │       CCBundle3D.h
│   │   │       CCBundle3DData.h
│   │   │       CCBundleReader.cpp
│   │   │       CCBundleReader.h
│   │   │       CCFrustum.cpp
│   │   │       CCFrustum.h
│   │   │       CCMesh.cpp
│   │   │       CCMesh.h
│   │   │       CCMeshSkin.cpp
│   │   │       CCMeshSkin.h
│   │   │       CCMeshVertexIndexData.cpp
│   │   │       CCMeshVertexIndexData.h
│   │   │       CCMotionStreak3D.cpp
│   │   │       CCMotionStreak3D.h
│   │   │       CCOBB.cpp
│   │   │       CCOBB.h
│   │   │       CCObjLoader.cpp
│   │   │       CCObjLoader.h
│   │   │       CCPlane.cpp
│   │   │       CCPlane.h
│   │   │       CCRay.cpp
│   │   │       CCRay.h
│   │   │       CCSkeleton3D.cpp
│   │   │       CCSkeleton3D.h
│   │   │       CCSkybox.cpp
│   │   │       CCSkybox.h
│   │   │       CCSprite3D.cpp
│   │   │       CCSprite3D.h
│   │   │       CCSprite3DMaterial.cpp
│   │   │       CCSprite3DMaterial.h
│   │   │       CCTerrain.cpp
│   │   │       CCTerrain.h
│   │   │       CMakeLists.txt
│   │   │       cocos3d.h
│   │   │
│   │   ├───audio
│   │   │   │   AudioEngine.cpp
│   │   │   │   CMakeLists.txt
│   │   │   │
│   │   │   ├───android
│   │   │   │   │   Android.mk
│   │   │   │   │   AssetFd.cpp
│   │   │   │   │   AssetFd.h
│   │   │   │   │   audio.h
│   │   │   │   │   AudioBufferProvider.h
│   │   │   │   │   AudioDecoder.cpp
│   │   │   │   │   AudioDecoder.h
│   │   │   │   │   AudioEngine-inl.cpp
│   │   │   │   │   AudioEngine-inl.h
│   │   │   │   │   AudioMixer.cpp
│   │   │   │   │   AudioMixer.h
│   │   │   │   │   AudioMixerController.cpp
│   │   │   │   │   AudioMixerController.h
│   │   │   │   │   AudioMixerOps.h
│   │   │   │   │   AudioPlayerProvider.cpp
│   │   │   │   │   AudioPlayerProvider.h
│   │   │   │   │   AudioResampler.cpp
│   │   │   │   │   AudioResampler.h
│   │   │   │   │   AudioResamplerCubic.cpp
│   │   │   │   │   AudioResamplerCubic.h
│   │   │   │   │   AudioResamplerPublic.h
│   │   │   │   │   ccdandroidUtils.cpp
│   │   │   │   │   ccdandroidUtils.h
│   │   │   │   │   CCThreadPool.cpp
│   │   │   │   │   CCThreadPool.h
│   │   │   │   │   cddSimpleAudioEngine.cpp
│   │   │   │   │   IAudioPlayer.h
│   │   │   │   │   ICallerThreadUtils.h
│   │   │   │   │   IVolumeProvider.h
│   │   │   │   │   OpenSLHelper.h
│   │   │   │   │   PcmAudioPlayer.cpp
│   │   │   │   │   PcmAudioPlayer.h
│   │   │   │   │   PcmAudioService.cpp
│   │   │   │   │   PcmAudioService.h
│   │   │   │   │   PcmBufferProvider.cpp
│   │   │   │   │   PcmBufferProvider.h
│   │   │   │   │   PcmData.cpp
│   │   │   │   │   PcmData.h
│   │   │   │   │   Track.cpp
│   │   │   │   │   Track.h
│   │   │   │   │   UrlAudioPlayer.cpp
│   │   │   │   │   UrlAudioPlayer.h
│   │   │   │   │
│   │   │   │   ├───audio_utils
│   │   │   │   │   │   format.c
│   │   │   │   │   │   minifloat.cpp
│   │   │   │   │   │   primitives.c
│   │   │   │   │   │
│   │   │   │   │   ├───include
│   │   │   │   │   │   └───audio_utils
│   │   │   │   │   │           format.h
│   │   │   │   │   │           minifloat.h
│   │   │   │   │   │           primitives.h
│   │   │   │   │   │
│   │   │   │   │   └───private
│   │   │   │   │           private.h
│   │   │   │   │
│   │   │   │   ├───cutils
│   │   │   │   │       bitops.h
│   │   │   │   │       log.h
│   │   │   │   │
│   │   │   │   ├───jni
│   │   │   │   │       cddandroidAndroidJavaEngine.cpp
│   │   │   │   │       cddandroidAndroidJavaEngine.h
│   │   │   │   │
│   │   │   │   └───utils
│   │   │   │           Compat.h
│   │   │   │           Errors.h
│   │   │   │           Utils.cpp
│   │   │   │           Utils.h
│   │   │   │
│   │   │   ├───apple
│   │   │   │       AudioCache.h
│   │   │   │       AudioCache.mm
│   │   │   │       AudioEngine-inl.h
│   │   │   │       AudioEngine-inl.mm
│   │   │   │       AudioPlayer.h
│   │   │   │       AudioPlayer.mm
│   │   │   │
│   │   │   ├───include
│   │   │   │       AudioEngine.h
│   │   │   │       Export.h
│   │   │   │       SimpleAudioEngine.h
│   │   │   │
│   │   │   ├───ios
│   │   │   │       CDAudioManager.h
│   │   │   │       CDAudioManager.m
│   │   │   │       CDConfig.h
│   │   │   │       CDOpenALSupport.h
│   │   │   │       CDOpenALSupport.m
│   │   │   │       CocosDenshion.h
│   │   │   │       CocosDenshion.m
│   │   │   │       SimpleAudioEngine.mm
│   │   │   │       SimpleAudioEngine_objc.h
│   │   │   │       SimpleAudioEngine_objc.m
│   │   │   │
│   │   │   ├───linux
│   │   │   │       AudioEngine-linux.cpp
│   │   │   │       AudioEngine-linux.h
│   │   │   │       SimpleAudioEngine.cpp
│   │   │   │
│   │   │   ├───mac
│   │   │   │       CDAudioManager.h
│   │   │   │       CDAudioManager.m
│   │   │   │       CDConfig.h
│   │   │   │       CDOpenALSupport.h
│   │   │   │       CDOpenALSupport.m
│   │   │   │       CDXMacOSXSupport.h
│   │   │   │       CDXMacOSXSupport.mm
│   │   │   │       CocosDenshion.h
│   │   │   │       CocosDenshion.m
│   │   │   │       SimpleAudioEngine.mm
│   │   │   │       SimpleAudioEngine_objc.h
│   │   │   │       SimpleAudioEngine_objc.m
│   │   │   │
│   │   │   ├───tizen
│   │   │   │       AudioEngine-tizen.cpp
│   │   │   │       AudioEngine-tizen.h
│   │   │   │       SimpleAudioEngineTizen.cpp
│   │   │   │
│   │   │   ├───win32
│   │   │   │       AudioCache.cpp
│   │   │   │       AudioCache.h
│   │   │   │       AudioEngine-win32.cpp
│   │   │   │       AudioEngine-win32.h
│   │   │   │       AudioPlayer.cpp
│   │   │   │       AudioPlayer.h
│   │   │   │       MciPlayer.cpp
│   │   │   │       MciPlayer.h
│   │   │   │       SimpleAudioEngine.cpp
│   │   │   │
│   │   │   └───winrt
│   │   │           Audio.cpp
│   │   │           Audio.h
│   │   │           AudioCachePlayer.cpp
│   │   │           AudioCachePlayer.h
│   │   │           AudioEngine-winrt.cpp
│   │   │           AudioEngine-winrt.h
│   │   │           AudioSourceReader.cpp
│   │   │           AudioSourceReader.h
│   │   │           MediaStreamer.cpp
│   │   │           MediaStreamer.h
│   │   │           SimpleAudioEngine.cpp
│   │   │
│   │   ├───base
│   │   │   │   atitc.cpp
│   │   │   │   atitc.h
│   │   │   │   base64.cpp
│   │   │   │   base64.h
│   │   │   │   CCAsyncTaskPool.cpp
│   │   │   │   CCAsyncTaskPool.h
│   │   │   │   CCAutoreleasePool.cpp
│   │   │   │   CCAutoreleasePool.h
│   │   │   │   ccCArray.cpp
│   │   │   │   ccCArray.h
│   │   │   │   ccConfig.h
│   │   │   │   CCConfiguration.cpp
│   │   │   │   CCConfiguration.h
│   │   │   │   CCConsole.cpp
│   │   │   │   CCConsole.h
│   │   │   │   CCController-android.cpp
│   │   │   │   CCController-iOS.mm
│   │   │   │   CCController.cpp
│   │   │   │   CCController.h
│   │   │   │   CCData.cpp
│   │   │   │   CCData.h
│   │   │   │   CCDataVisitor.cpp
│   │   │   │   CCDataVisitor.h
│   │   │   │   CCDirector.cpp
│   │   │   │   CCDirector.h
│   │   │   │   CCEvent.cpp
│   │   │   │   CCEvent.h
│   │   │   │   CCEventAcceleration.cpp
│   │   │   │   CCEventAcceleration.h
│   │   │   │   CCEventController.cpp
│   │   │   │   CCEventController.h
│   │   │   │   CCEventCustom.cpp
│   │   │   │   CCEventCustom.h
│   │   │   │   CCEventDispatcher.cpp
│   │   │   │   CCEventDispatcher.h
│   │   │   │   CCEventFocus.cpp
│   │   │   │   CCEventFocus.h
│   │   │   │   CCEventKeyboard.cpp
│   │   │   │   CCEventKeyboard.h
│   │   │   │   CCEventListener.cpp
│   │   │   │   CCEventListener.h
│   │   │   │   CCEventListenerAcceleration.cpp
│   │   │   │   CCEventListenerAcceleration.h
│   │   │   │   CCEventListenerController.cpp
│   │   │   │   CCEventListenerController.h
│   │   │   │   CCEventListenerCustom.cpp
│   │   │   │   CCEventListenerCustom.h
│   │   │   │   CCEventListenerFocus.cpp
│   │   │   │   CCEventListenerFocus.h
│   │   │   │   CCEventListenerKeyboard.cpp
│   │   │   │   CCEventListenerKeyboard.h
│   │   │   │   CCEventListenerMouse.cpp
│   │   │   │   CCEventListenerMouse.h
│   │   │   │   CCEventListenerTouch.cpp
│   │   │   │   CCEventListenerTouch.h
│   │   │   │   CCEventMouse.cpp
│   │   │   │   CCEventMouse.h
│   │   │   │   CCEventTouch.cpp
│   │   │   │   CCEventTouch.h
│   │   │   │   CCEventType.h
│   │   │   │   ccFPSImages.c
│   │   │   │   ccFPSImages.h
│   │   │   │   CCGameController.h
│   │   │   │   CCIMEDelegate.h
│   │   │   │   CCIMEDispatcher.cpp
│   │   │   │   CCIMEDispatcher.h
│   │   │   │   ccMacros.h
│   │   │   │   CCMap.h
│   │   │   │   CCNinePatchImageParser.cpp
│   │   │   │   CCNinePatchImageParser.h
│   │   │   │   CCNS.cpp
│   │   │   │   CCNS.h
│   │   │   │   CCProfiling.cpp
│   │   │   │   CCProfiling.h
│   │   │   │   CCProperties.cpp
│   │   │   │   CCProperties.h
│   │   │   │   CCProtocols.h
│   │   │   │   ccRandom.cpp
│   │   │   │   ccRandom.h
│   │   │   │   CCRef.cpp
│   │   │   │   CCRef.h
│   │   │   │   CCRefPtr.h
│   │   │   │   CCScheduler.cpp
│   │   │   │   CCScheduler.h
│   │   │   │   CCScriptSupport.cpp
│   │   │   │   CCScriptSupport.h
│   │   │   │   CCStencilStateManager.cpp
│   │   │   │   CCStencilStateManager.hpp
│   │   │   │   CCTouch.cpp
│   │   │   │   CCTouch.h
│   │   │   │   ccTypes.cpp
│   │   │   │   ccTypes.h
│   │   │   │   CCUserDefault-android.cpp
│   │   │   │   CCUserDefault-apple.mm
│   │   │   │   CCUserDefault-winrt.cpp
│   │   │   │   CCUserDefault.cpp
│   │   │   │   CCUserDefault.h
│   │   │   │   ccUTF8.cpp
│   │   │   │   ccUTF8.h
│   │   │   │   ccUtils.cpp
│   │   │   │   ccUtils.h
│   │   │   │   CCValue.cpp
│   │   │   │   CCValue.h
│   │   │   │   CCVector.h
│   │   │   │   CMakeLists.txt
│   │   │   │   etc1.cpp
│   │   │   │   etc1.h
│   │   │   │   firePngData.h
│   │   │   │   ObjectFactory.cpp
│   │   │   │   ObjectFactory.h
│   │   │   │   pvr.cpp
│   │   │   │   pvr.h
│   │   │   │   s3tc.cpp
│   │   │   │   s3tc.h
│   │   │   │   TGAlib.cpp
│   │   │   │   TGAlib.h
│   │   │   │   uthash.h
│   │   │   │   utlist.h
│   │   │   │   ZipUtils.cpp
│   │   │   │   ZipUtils.h
│   │   │   │
│   │   │   └───allocator
│   │   │           CCAllocatorBase.h
│   │   │           CCAllocatorDiagnostics.cpp
│   │   │           CCAllocatorDiagnostics.h
│   │   │           CCAllocatorGlobal.cpp
│   │   │           CCAllocatorGlobal.h
│   │   │           CCAllocatorGlobalNewDelete.cpp
│   │   │           CCAllocatorMacros.h
│   │   │           CCAllocatorMutex.h
│   │   │           CCAllocatorStrategyDefault.h
│   │   │           CCAllocatorStrategyFixedBlock.h
│   │   │           CCAllocatorStrategyGlobalSmallBlock.h
│   │   │           CCAllocatorStrategyPool.h
│   │   │
│   │   ├───deprecated
│   │   │       CCArray.cpp
│   │   │       CCArray.h
│   │   │       CCBool.h
│   │   │       CCDeprecated.cpp
│   │   │       CCDeprecated.h
│   │   │       CCDictionary.cpp
│   │   │       CCDictionary.h
│   │   │       CCDouble.h
│   │   │       CCFloat.h
│   │   │       CCInteger.h
│   │   │       CCNotificationCenter.cpp
│   │   │       CCNotificationCenter.h
│   │   │       CCSet.cpp
│   │   │       CCSet.h
│   │   │       CCString.cpp
│   │   │       CCString.h
│   │   │       CMakeLists.txt
│   │   │
│   │   ├───editor-support
│   │   │   ├───cocosbuilder
│   │   │   │       Android.mk
│   │   │   │       CCBAnimationManager.cpp
│   │   │   │       CCBAnimationManager.h
│   │   │   │       CCBFileLoader.cpp
│   │   │   │       CCBFileLoader.h
│   │   │   │       CCBKeyframe.cpp
│   │   │   │       CCBKeyframe.h
│   │   │   │       CCBMemberVariableAssigner.h
│   │   │   │       CCBReader.cpp
│   │   │   │       CCBReader.h
│   │   │   │       CCBSelectorResolver.h
│   │   │   │       CCBSequence.cpp
│   │   │   │       CCBSequence.h
│   │   │   │       CCBSequenceProperty.cpp
│   │   │   │       CCBSequenceProperty.h
│   │   │   │       CCControlButtonLoader.cpp
│   │   │   │       CCControlButtonLoader.h
│   │   │   │       CCControlLoader.cpp
│   │   │   │       CCControlLoader.h
│   │   │   │       CCLabelBMFontLoader.cpp
│   │   │   │       CCLabelBMFontLoader.h
│   │   │   │       CCLabelTTFLoader.cpp
│   │   │   │       CCLabelTTFLoader.h
│   │   │   │       CCLayerColorLoader.cpp
│   │   │   │       CCLayerColorLoader.h
│   │   │   │       CCLayerGradientLoader.cpp
│   │   │   │       CCLayerGradientLoader.h
│   │   │   │       CCLayerLoader.cpp
│   │   │   │       CCLayerLoader.h
│   │   │   │       CCMenuItemImageLoader.cpp
│   │   │   │       CCMenuItemImageLoader.h
│   │   │   │       CCMenuItemLoader.cpp
│   │   │   │       CCMenuItemLoader.h
│   │   │   │       CCMenuLoader.h
│   │   │   │       CCNode+CCBRelativePositioning.cpp
│   │   │   │       CCNode+CCBRelativePositioning.h
│   │   │   │       CCNodeLoader.cpp
│   │   │   │       CCNodeLoader.h
│   │   │   │       CCNodeLoaderLibrary.cpp
│   │   │   │       CCNodeLoaderLibrary.h
│   │   │   │       CCNodeLoaderListener.h
│   │   │   │       CCParticleSystemQuadLoader.cpp
│   │   │   │       CCParticleSystemQuadLoader.h
│   │   │   │       CCScale9SpriteLoader.cpp
│   │   │   │       CCScale9SpriteLoader.h
│   │   │   │       CCScrollViewLoader.cpp
│   │   │   │       CCScrollViewLoader.h
│   │   │   │       CCSpriteLoader.cpp
│   │   │   │       CCSpriteLoader.h
│   │   │   │       CMakeLists.txt
│   │   │   │       CocosBuilder.h
│   │   │   │
│   │   │   ├───cocostudio
│   │   │   │   │   Android.mk
│   │   │   │   │   CCActionFrame.cpp
│   │   │   │   │   CCActionFrame.h
│   │   │   │   │   CCActionFrameEasing.cpp
│   │   │   │   │   CCActionFrameEasing.h
│   │   │   │   │   CCActionManagerEx.cpp
│   │   │   │   │   CCActionManagerEx.h
│   │   │   │   │   CCActionNode.cpp
│   │   │   │   │   CCActionNode.h
│   │   │   │   │   CCActionObject.cpp
│   │   │   │   │   CCActionObject.h
│   │   │   │   │   CCArmature.cpp
│   │   │   │   │   CCArmature.h
│   │   │   │   │   CCArmatureAnimation.cpp
│   │   │   │   │   CCArmatureAnimation.h
│   │   │   │   │   CCArmatureDataManager.cpp
│   │   │   │   │   CCArmatureDataManager.h
│   │   │   │   │   CCArmatureDefine.cpp
│   │   │   │   │   CCArmatureDefine.h
│   │   │   │   │   CCBatchNode.cpp
│   │   │   │   │   CCBatchNode.h
│   │   │   │   │   CCBone.cpp
│   │   │   │   │   CCBone.h
│   │   │   │   │   CCColliderDetector.cpp
│   │   │   │   │   CCColliderDetector.h
│   │   │   │   │   CCComAttribute.cpp
│   │   │   │   │   CCComAttribute.h
│   │   │   │   │   CCComAudio.cpp
│   │   │   │   │   CCComAudio.h
│   │   │   │   │   CCComBase.h
│   │   │   │   │   CCComController.cpp
│   │   │   │   │   CCComController.h
│   │   │   │   │   CCComExtensionData.cpp
│   │   │   │   │   CCComExtensionData.h
│   │   │   │   │   CCComRender.cpp
│   │   │   │   │   CCComRender.h
│   │   │   │   │   CCDataReaderHelper.cpp
│   │   │   │   │   CCDataReaderHelper.h
│   │   │   │   │   CCDatas.cpp
│   │   │   │   │   CCDatas.h
│   │   │   │   │   CCDecorativeDisplay.cpp
│   │   │   │   │   CCDecorativeDisplay.h
│   │   │   │   │   CCDisplayFactory.cpp
│   │   │   │   │   CCDisplayFactory.h
│   │   │   │   │   CCDisplayManager.cpp
│   │   │   │   │   CCDisplayManager.h
│   │   │   │   │   CCInputDelegate.cpp
│   │   │   │   │   CCInputDelegate.h
│   │   │   │   │   CCProcessBase.cpp
│   │   │   │   │   CCProcessBase.h
│   │   │   │   │   CCSGUIReader.cpp
│   │   │   │   │   CCSGUIReader.h
│   │   │   │   │   CCSkin.cpp
│   │   │   │   │   CCSkin.h
│   │   │   │   │   CCSpriteFrameCacheHelper.cpp
│   │   │   │   │   CCSpriteFrameCacheHelper.h
│   │   │   │   │   CCSSceneReader.cpp
│   │   │   │   │   CCSSceneReader.h
│   │   │   │   │   CCTransformHelp.cpp
│   │   │   │   │   CCTransformHelp.h
│   │   │   │   │   CCTween.cpp
│   │   │   │   │   CCTween.h
│   │   │   │   │   CCUtilMath.cpp
│   │   │   │   │   CCUtilMath.h
│   │   │   │   │   CMakeLists.txt
│   │   │   │   │   CocoLoader.cpp
│   │   │   │   │   CocoLoader.h
│   │   │   │   │   CocosStudioExport.h
│   │   │   │   │   CocosStudioExtension.cpp
│   │   │   │   │   CocosStudioExtension.h
│   │   │   │   │   CocoStudio.cpp
│   │   │   │   │   CocoStudio.h
│   │   │   │   │   CSLanguageDataBinary_generated.h
│   │   │   │   │   CSParse3DBinary_generated.h
│   │   │   │   │   CSParseBinary_generated.h
│   │   │   │   │   DictionaryHelper.cpp
│   │   │   │   │   DictionaryHelper.h
│   │   │   │   │   FlatBuffersSerialize.cpp
│   │   │   │   │   FlatBuffersSerialize.h
│   │   │   │   │   LocalizationManager.cpp
│   │   │   │   │   LocalizationManager.h
│   │   │   │   │   TriggerBase.cpp
│   │   │   │   │   TriggerBase.h
│   │   │   │   │   TriggerMng.cpp
│   │   │   │   │   TriggerMng.h
│   │   │   │   │   TriggerObj.cpp
│   │   │   │   │   TriggerObj.h
│   │   │   │   │   WidgetCallBackHandlerProtocol.cpp
│   │   │   │   │   WidgetCallBackHandlerProtocol.h
│   │   │   │   │
│   │   │   │   ├───ActionTimeline
│   │   │   │   │       CCActionTimeline.cpp
│   │   │   │   │       CCActionTimeline.h
│   │   │   │   │       CCActionTimelineCache.cpp
│   │   │   │   │       CCActionTimelineCache.h
│   │   │   │   │       CCActionTimelineNode.cpp
│   │   │   │   │       CCActionTimelineNode.h
│   │   │   │   │       CCBoneNode.cpp
│   │   │   │   │       CCBoneNode.h
│   │   │   │   │       CCFrame.cpp
│   │   │   │   │       CCFrame.h
│   │   │   │   │       CCSkeletonNode.cpp
│   │   │   │   │       CCSkeletonNode.h
│   │   │   │   │       CCSkinNode.cpp
│   │   │   │   │       CCSkinNode.h
│   │   │   │   │       CCTimeLine.cpp
│   │   │   │   │       CCTimeLine.h
│   │   │   │   │       CCTimelineMacro.h
│   │   │   │   │       CSLoader.cpp
│   │   │   │   │       CSLoader.h
│   │   │   │   │
│   │   │   │   └───WidgetReader
│   │   │   │       │   NodeReaderDefine.cpp
│   │   │   │       │   NodeReaderDefine.h
│   │   │   │       │   NodeReaderProtocol.cpp
│   │   │   │       │   NodeReaderProtocol.h
│   │   │   │       │   WidgetReader.cpp
│   │   │   │       │   WidgetReader.h
│   │   │   │       │   WidgetReaderProtocol.h
│   │   │   │       │
│   │   │   │       ├───ArmatureNodeReader
│   │   │   │       │       ArmatureNodeReader.cpp
│   │   │   │       │       ArmatureNodeReader.h
│   │   │   │       │       CSArmatureNode_generated.h
│   │   │   │       │
│   │   │   │       ├───ButtonReader
│   │   │   │       │       ButtonReader.cpp
│   │   │   │       │       ButtonReader.h
│   │   │   │       │
│   │   │   │       ├───CheckBoxReader
│   │   │   │       │       CheckBoxReader.cpp
│   │   │   │       │       CheckBoxReader.h
│   │   │   │       │
│   │   │   │       ├───ComAudioReader
│   │   │   │       │       ComAudioReader.cpp
│   │   │   │       │       ComAudioReader.h
│   │   │   │       │
│   │   │   │       ├───GameMapReader
│   │   │   │       │       GameMapReader.cpp
│   │   │   │       │       GameMapReader.h
│   │   │   │       │
│   │   │   │       ├───GameNode3DReader
│   │   │   │       │       GameNode3DReader.cpp
│   │   │   │       │       GameNode3DReader.h
│   │   │   │       │
│   │   │   │       ├───ImageViewReader
│   │   │   │       │       ImageViewReader.cpp
│   │   │   │       │       ImageViewReader.h
│   │   │   │       │
│   │   │   │       ├───LayoutReader
│   │   │   │       │       LayoutReader.cpp
│   │   │   │       │       LayoutReader.h
│   │   │   │       │
│   │   │   │       ├───Light3DReader
│   │   │   │       │       Light3DReader.cpp
│   │   │   │       │       Light3DReader.h
│   │   │   │       │
│   │   │   │       ├───ListViewReader
│   │   │   │       │       ListViewReader.cpp
│   │   │   │       │       ListViewReader.h
│   │   │   │       │
│   │   │   │       ├───LoadingBarReader
│   │   │   │       │       LoadingBarReader.cpp
│   │   │   │       │       LoadingBarReader.h
│   │   │   │       │
│   │   │   │       ├───Node3DReader
│   │   │   │       │       Node3DReader.cpp
│   │   │   │       │       Node3DReader.h
│   │   │   │       │
│   │   │   │       ├───NodeReader
│   │   │   │       │       NodeReader.cpp
│   │   │   │       │       NodeReader.h
│   │   │   │       │
│   │   │   │       ├───PageViewReader
│   │   │   │       │       PageViewReader.cpp
│   │   │   │       │       PageViewReader.h
│   │   │   │       │
│   │   │   │       ├───Particle3DReader
│   │   │   │       │       Particle3DReader.cpp
│   │   │   │       │       Particle3DReader.h
│   │   │   │       │
│   │   │   │       ├───ParticleReader
│   │   │   │       │       ParticleReader.cpp
│   │   │   │       │       ParticleReader.h
│   │   │   │       │
│   │   │   │       ├───ProjectNodeReader
│   │   │   │       │       ProjectNodeReader.cpp
│   │   │   │       │       ProjectNodeReader.h
│   │   │   │       │
│   │   │   │       ├───ScrollViewReader
│   │   │   │       │       ScrollViewReader.cpp
│   │   │   │       │       ScrollViewReader.h
│   │   │   │       │
│   │   │   │       ├───SingleNodeReader
│   │   │   │       │       SingleNodeReader.cpp
│   │   │   │       │       SingleNodeReader.h
│   │   │   │       │
│   │   │   │       ├───SkeletonReader
│   │   │   │       │       BoneNodeReader.cpp
│   │   │   │       │       BoneNodeReader.h
│   │   │   │       │       CSBoneBinary_generated.h
│   │   │   │       │       SkeletonNodeReader.cpp
│   │   │   │       │       SkeletonNodeReader.h
│   │   │   │       │
│   │   │   │       ├───SliderReader
│   │   │   │       │       SliderReader.cpp
│   │   │   │       │       SliderReader.h
│   │   │   │       │
│   │   │   │       ├───Sprite3DReader
│   │   │   │       │       Sprite3DReader.cpp
│   │   │   │       │       Sprite3DReader.h
│   │   │   │       │
│   │   │   │       ├───SpriteReader
│   │   │   │       │       SpriteReader.cpp
│   │   │   │       │       SpriteReader.h
│   │   │   │       │
│   │   │   │       ├───TabControlReader
│   │   │   │       │       CSTabControl_generated.h
│   │   │   │       │       TabControlReader.cpp
│   │   │   │       │       TabControlReader.h
│   │   │   │       │
│   │   │   │       ├───TextAtlasReader
│   │   │   │       │       TextAtlasReader.cpp
│   │   │   │       │       TextAtlasReader.h
│   │   │   │       │
│   │   │   │       ├───TextBMFontReader
│   │   │   │       │       TextBMFontReader.cpp
│   │   │   │       │       TextBMFontReader.h
│   │   │   │       │
│   │   │   │       ├───TextFieldReader
│   │   │   │       │       TextFieldReader.cpp
│   │   │   │       │       TextFieldReader.h
│   │   │   │       │
│   │   │   │       ├───TextReader
│   │   │   │       │       TextReader.cpp
│   │   │   │       │       TextReader.h
│   │   │   │       │
│   │   │   │       └───UserCameraReader
│   │   │   │               UserCameraReader.cpp
│   │   │   │               UserCameraReader.h
│   │   │   │
│   │   │   └───spine
│   │   │       │   Android.mk
│   │   │       │   Animation.c
│   │   │       │   Animation.h
│   │   │       │   AnimationState.c
│   │   │       │   AnimationState.h
│   │   │       │   AnimationStateData.c
│   │   │       │   AnimationStateData.h
│   │   │       │   Atlas.c
│   │   │       │   Atlas.h
│   │   │       │   AtlasAttachmentLoader.c
│   │   │       │   AtlasAttachmentLoader.h
│   │   │       │   Attachment.c
│   │   │       │   Attachment.h
│   │   │       │   AttachmentLoader.c
│   │   │       │   AttachmentLoader.h
│   │   │       │   AttachmentVertices.cpp
│   │   │       │   AttachmentVertices.h
│   │   │       │   Bone.c
│   │   │       │   Bone.h
│   │   │       │   BoneData.c
│   │   │       │   BoneData.h
│   │   │       │   BoundingBoxAttachment.c
│   │   │       │   BoundingBoxAttachment.h
│   │   │       │   CMakeLists.txt
│   │   │       │   Cocos2dAttachmentLoader.cpp
│   │   │       │   Cocos2dAttachmentLoader.h
│   │   │       │   Event.c
│   │   │       │   Event.h
│   │   │       │   EventData.c
│   │   │       │   EventData.h
│   │   │       │   extension.c
│   │   │       │   extension.h
│   │   │       │   IkConstraint.c
│   │   │       │   IkConstraint.h
│   │   │       │   IkConstraintData.c
│   │   │       │   IkConstraintData.h
│   │   │       │   Json.c
│   │   │       │   Json.h
│   │   │       │   MeshAttachment.c
│   │   │       │   MeshAttachment.h
│   │   │       │   PathAttachment.c
│   │   │       │   PathAttachment.h
│   │   │       │   PathConstraint.c
│   │   │       │   PathConstraint.h
│   │   │       │   PathConstraintData.c
│   │   │       │   PathConstraintData.h
│   │   │       │   RegionAttachment.c
│   │   │       │   RegionAttachment.h
│   │   │       │   Skeleton.c
│   │   │       │   Skeleton.h
│   │   │       │   SkeletonAnimation.cpp
│   │   │       │   SkeletonAnimation.h
│   │   │       │   SkeletonBatch.cpp
│   │   │       │   SkeletonBatch.h
│   │   │       │   SkeletonBounds.c
│   │   │       │   SkeletonBounds.h
│   │   │       │   SkeletonData.c
│   │   │       │   SkeletonData.h
│   │   │       │   SkeletonJson.c
│   │   │       │   SkeletonJson.h
│   │   │       │   SkeletonRenderer.cpp
│   │   │       │   SkeletonRenderer.h
│   │   │       │   Skin.c
│   │   │       │   Skin.h
│   │   │       │   Slot.c
│   │   │       │   Slot.h
│   │   │       │   SlotData.c
│   │   │       │   SlotData.h
│   │   │       │   spine-cocos2dx.cpp
│   │   │       │   spine-cocos2dx.h
│   │   │       │   spine.h
│   │   │       │   TransformConstraint.c
│   │   │       │   TransformConstraint.h
│   │   │       │   TransformConstraintData.c
│   │   │       │   TransformConstraintData.h
│   │   │       │   VertexAttachment.c
│   │   │       │   VertexAttachment.h
│   │   │       │
│   │   │       ├───proj.win10
│   │   │       │       libSpine.vcxproj
│   │   │       │
│   │   │       ├───proj.win32
│   │   │       │       libSpine.vcxproj
│   │   │       │       libSpine.vcxproj.filters
│   │   │       │
│   │   │       └───proj.win8.1-universal
│   │   │           ├───libSpine.Shared
│   │   │           │       libSpine.Shared.vcxitems
│   │   │           │       libSpine.Shared.vcxitems.filters
│   │   │           │
│   │   │           ├───libSpine.Windows
│   │   │           │       libSpine.Windows.vcxproj
│   │   │           │       libSpine.Windows.vcxproj.filters
│   │   │           │
│   │   │           └───libSpine.WindowsPhone
│   │   │                   libSpine.WindowsPhone.vcxproj
│   │   │                   libSpine.WindowsPhone.vcxproj.filters
│   │   │
│   │   ├───math
│   │   │       CCAffineTransform.cpp
│   │   │       CCAffineTransform.h
│   │   │       CCGeometry.cpp
│   │   │       CCGeometry.h
│   │   │       CCMath.h
│   │   │       CCMathBase.h
│   │   │       CCVertex.cpp
│   │   │       CCVertex.h
│   │   │       CMakeLists.txt
│   │   │       Mat4.cpp
│   │   │       Mat4.h
│   │   │       Mat4.inl
│   │   │       MathUtil.cpp
│   │   │       MathUtil.h
│   │   │       MathUtil.inl
│   │   │       MathUtilNeon.inl
│   │   │       MathUtilNeon64.inl
│   │   │       MathUtilSSE.inl
│   │   │       Quaternion.cpp
│   │   │       Quaternion.h
│   │   │       Quaternion.inl
│   │   │       TransformUtils.cpp
│   │   │       TransformUtils.h
│   │   │       Vec2.cpp
│   │   │       Vec2.h
│   │   │       Vec2.inl
│   │   │       Vec3.cpp
│   │   │       Vec3.h
│   │   │       Vec3.inl
│   │   │       Vec4.cpp
│   │   │       Vec4.h
│   │   │       Vec4.inl
│   │   │
│   │   ├───navmesh
│   │   │       CCNavMesh.cpp
│   │   │       CCNavMesh.h
│   │   │       CCNavMeshAgent.cpp
│   │   │       CCNavMeshAgent.h
│   │   │       CCNavMeshDebugDraw.cpp
│   │   │       CCNavMeshDebugDraw.h
│   │   │       CCNavMeshObstacle.cpp
│   │   │       CCNavMeshObstacle.h
│   │   │       CCNavMeshUtils.cpp
│   │   │       CCNavMeshUtils.h
│   │   │       CMakeLists.txt
│   │   │
│   │   ├───network
│   │   │       Android.mk
│   │   │       CCDownloader-android.cpp
│   │   │       CCDownloader-android.h
│   │   │       CCDownloader-apple.h
│   │   │       CCDownloader-apple.mm
│   │   │       CCDownloader-curl.cpp
│   │   │       CCDownloader-curl.h
│   │   │       CCDownloader.cpp
│   │   │       CCDownloader.h
│   │   │       CCIDownloaderImpl.h
│   │   │       CMakeLists.txt
│   │   │       HttpAsynConnection-apple.h
│   │   │       HttpAsynConnection-apple.m
│   │   │       HttpClient-android.cpp
│   │   │       HttpClient-apple.mm
│   │   │       HttpClient-winrt.cpp
│   │   │       HttpClient.cpp
│   │   │       HttpClient.h
│   │   │       HttpConnection-winrt.cpp
│   │   │       HttpConnection-winrt.h
│   │   │       HttpCookie.cpp
│   │   │       HttpCookie.h
│   │   │       HttpRequest.h
│   │   │       HttpResponse.h
│   │   │       SocketIO.cpp
│   │   │       SocketIO.h
│   │   │       WebSocket.cpp
│   │   │       WebSocket.h
│   │   │
│   │   ├───physics
│   │   │       CCPhysicsBody.cpp
│   │   │       CCPhysicsBody.h
│   │   │       CCPhysicsContact.cpp
│   │   │       CCPhysicsContact.h
│   │   │       CCPhysicsHelper.h
│   │   │       CCPhysicsJoint.cpp
│   │   │       CCPhysicsJoint.h
│   │   │       CCPhysicsShape.cpp
│   │   │       CCPhysicsShape.h
│   │   │       CCPhysicsWorld.cpp
│   │   │       CCPhysicsWorld.h
│   │   │       CMakeLists.txt
│   │   │       cpCompat62.h
│   │   │
│   │   ├───physics3d
│   │   │       CCPhysics3D.cpp
│   │   │       CCPhysics3D.h
│   │   │       CCPhysics3DComponent.cpp
│   │   │       CCPhysics3DComponent.h
│   │   │       CCPhysics3DConstraint.cpp
│   │   │       CCPhysics3DConstraint.h
│   │   │       CCPhysics3DDebugDrawer.cpp
│   │   │       CCPhysics3DDebugDrawer.h
│   │   │       CCPhysics3DObject.cpp
│   │   │       CCPhysics3DObject.h
│   │   │       CCPhysics3DShape.cpp
│   │   │       CCPhysics3DShape.h
│   │   │       CCPhysics3DWorld.cpp
│   │   │       CCPhysics3DWorld.h
│   │   │       CCPhysicsSprite3D.cpp
│   │   │       CCPhysicsSprite3D.h
│   │   │       CMakeLists.txt
│   │   │
│   │   ├───platform
│   │   │   │   CCApplication.h
│   │   │   │   CCApplicationProtocol.h
│   │   │   │   CCCommon.h
│   │   │   │   CCDevice.h
│   │   │   │   CCFileUtils.cpp
│   │   │   │   CCFileUtils.h
│   │   │   │   CCGL.h
│   │   │   │   CCGLView.cpp
│   │   │   │   CCGLView.h
│   │   │   │   CCImage.cpp
│   │   │   │   CCImage.h
│   │   │   │   CCPlatformConfig.h
│   │   │   │   CCPlatformDefine.h
│   │   │   │   CCPlatformMacros.h
│   │   │   │   CCSAXParser.cpp
│   │   │   │   CCSAXParser.h
│   │   │   │   CCStdC.h
│   │   │   │   CCThread.cpp
│   │   │   │   CCThread.h
│   │   │   │   CMakeLists.txt
│   │   │   │
│   │   │   ├───android
│   │   │   │   │   Android.mk
│   │   │   │   │   CCApplication-android.cpp
│   │   │   │   │   CCApplication-android.h
│   │   │   │   │   CCCommon-android.cpp
│   │   │   │   │   CCDevice-android.cpp
│   │   │   │   │   CCEnhanceAPI-android.cpp
│   │   │   │   │   CCEnhanceAPI-android.h
│   │   │   │   │   CCFileUtils-android.cpp
│   │   │   │   │   CCFileUtils-android.h
│   │   │   │   │   CCGL-android.h
│   │   │   │   │   CCGLViewImpl-android.cpp
│   │   │   │   │   CCGLViewImpl-android.h
│   │   │   │   │   CCPlatformDefine-android.h
│   │   │   │   │   CCStdC-android.h
│   │   │   │   │   javaactivity-android.cpp
│   │   │   │   │
│   │   │   │   ├───ControllerManualAdapter
│   │   │   │   │   │   .classpath
│   │   │   │   │   │   .project
│   │   │   │   │   │   AndroidManifest.xml
│   │   │   │   │   │   ant.properties
│   │   │   │   │   │   build.xml
│   │   │   │   │   │   lint.xml
│   │   │   │   │   │   proguard-project.txt
│   │   │   │   │   │   project.properties
│   │   │   │   │   │
│   │   │   │   │   ├───.settings
│   │   │   │   │   │       org.eclipse.jdt.core.prefs
│   │   │   │   │   │
│   │   │   │   │   ├───libs
│   │   │   │   │   │       com.bda.controller.jar
│   │   │   │   │   │       nibiru_lib.jar
│   │   │   │   │   │       ouya-sdk.jar
│   │   │   │   │   │
│   │   │   │   │   └───src
│   │   │   │   │       └───org
│   │   │   │   │           └───cocos2dx
│   │   │   │   │               └───lib
│   │   │   │   │                   │   GameControllerActivity.java
│   │   │   │   │                   │   GameControllerHelper.java
│   │   │   │   │                   │   GameControllerMoga.java
│   │   │   │   │                   │   GameControllerNibiru.java
│   │   │   │   │                   │   GameControllerOuya.java
│   │   │   │   │                   │
│   │   │   │   │                   └───inputmanagercompat
│   │   │   │   │                           InputManagerCompat.java
│   │   │   │   │                           InputManagerV16.java
│   │   │   │   │                           InputManagerV9.java
│   │   │   │   │
│   │   │   │   ├───java
│   │   │   │   │   │   .classpath
│   │   │   │   │   │   .project
│   │   │   │   │   │   AndroidManifest.xml
│   │   │   │   │   │   ant.properties
│   │   │   │   │   │   build.xml
│   │   │   │   │   │   lint.xml
│   │   │   │   │   │   proguard-project.txt
│   │   │   │   │   │   project.properties
│   │   │   │   │   │
│   │   │   │   │   ├───.settings
│   │   │   │   │   │       org.eclipse.jdt.core.prefs
│   │   │   │   │   │
│   │   │   │   │   ├───libs
│   │   │   │   │   │       android-async-http-1.4.9.jar
│   │   │   │   │   │       com.android.vending.expansion.zipfile.jar
│   │   │   │   │   │       httpclient-4.4.1.1.jar
│   │   │   │   │   │
│   │   │   │   │   └───src
│   │   │   │   │       ├───com
│   │   │   │   │       │   └───enhance
│   │   │   │   │       │       └───gameservice
│   │   │   │   │       │               IGameTuningService.aidl
│   │   │   │   │       │
│   │   │   │   │       └───org
│   │   │   │   │           └───cocos2dx
│   │   │   │   │               └───lib
│   │   │   │   │                       Cocos2dxAccelerometer.java
│   │   │   │   │                       Cocos2dxActivity.java
│   │   │   │   │                       Cocos2dxBitmap.java
│   │   │   │   │                       Cocos2dxDownloader.java
│   │   │   │   │                       Cocos2dxEditBox.java
│   │   │   │   │                       Cocos2dxEditBoxHelper.java
│   │   │   │   │                       Cocos2dxGLSurfaceView.java
│   │   │   │   │                       Cocos2dxHandler.java
│   │   │   │   │                       Cocos2dxHelper.java
│   │   │   │   │                       Cocos2dxHttpURLConnection.java
│   │   │   │   │                       Cocos2dxJavascriptJavaBridge.java
│   │   │   │   │                       Cocos2dxLocalStorage.java
│   │   │   │   │                       Cocos2dxLuaJavaBridge.java
│   │   │   │   │                       Cocos2dxMusic.java
│   │   │   │   │                       Cocos2dxReflectionHelper.java
│   │   │   │   │                       Cocos2dxRenderer.java
│   │   │   │   │                       Cocos2dxSound.java
│   │   │   │   │                       Cocos2dxTextInputWrapper.java
│   │   │   │   │                       Cocos2dxTypefaces.java
│   │   │   │   │                       Cocos2dxVideoHelper.java
│   │   │   │   │                       Cocos2dxVideoView.java
│   │   │   │   │                       Cocos2dxWebView.java
│   │   │   │   │                       Cocos2dxWebViewHelper.java
│   │   │   │   │                       GameControllerAdapter.java
│   │   │   │   │                       GameControllerDelegate.java
│   │   │   │   │                       GameControllerUtils.java
│   │   │   │   │                       ResizeLayout.java
│   │   │   │   │
│   │   │   │   ├───jni
│   │   │   │   │       Java_org_cocos2dx_lib_Cocos2dxAccelerometer.cpp
│   │   │   │   │       Java_org_cocos2dx_lib_Cocos2dxBitmap.cpp
│   │   │   │   │       Java_org_cocos2dx_lib_Cocos2dxBitmap.h
│   │   │   │   │       Java_org_cocos2dx_lib_Cocos2dxHelper.cpp
│   │   │   │   │       Java_org_cocos2dx_lib_Cocos2dxHelper.h
│   │   │   │   │       Java_org_cocos2dx_lib_Cocos2dxRenderer.cpp
│   │   │   │   │       JniHelper.cpp
│   │   │   │   │       JniHelper.h
│   │   │   │   │       TouchesJni.cpp
│   │   │   │   │
│   │   │   │   ├───libcocos2dx
│   │   │   │   │       AndroidManifest.xml
│   │   │   │   │       build.gradle
│   │   │   │   │       proguard-rules.pro
│   │   │   │   │
│   │   │   │   └───libcocos2dx-with-controller
│   │   │   │           AndroidManifest.xml
│   │   │   │           build.gradle
│   │   │   │           proguard-rules.pro
│   │   │   │
│   │   │   ├───apple
│   │   │   │       CCDevice-apple.h
│   │   │   │       CCDevice-apple.mm
│   │   │   │       CCFileUtils-apple.h
│   │   │   │       CCFileUtils-apple.mm
│   │   │   │       CCLock-apple.cpp
│   │   │   │       CCLock-apple.h
│   │   │   │       CCThread-apple.mm
│   │   │   │
│   │   │   ├───desktop
│   │   │   │       CCGLViewImpl-desktop.cpp
│   │   │   │       CCGLViewImpl-desktop.h
│   │   │   │
│   │   │   ├───ios
│   │   │   │       CCApplication-ios.h
│   │   │   │       CCApplication-ios.mm
│   │   │   │       CCCommon-ios.mm
│   │   │   │       CCDevice-ios.mm
│   │   │   │       CCDirectorCaller-ios.h
│   │   │   │       CCDirectorCaller-ios.mm
│   │   │   │       CCEAGLView-ios.h
│   │   │   │       CCEAGLView-ios.mm
│   │   │   │       CCES2Renderer-ios.h
│   │   │   │       CCES2Renderer-ios.m
│   │   │   │       CCESRenderer-ios.h
│   │   │   │       CCGL-ios.h
│   │   │   │       CCGLViewImpl-ios.h
│   │   │   │       CCGLViewImpl-ios.mm
│   │   │   │       CCImage-ios.mm
│   │   │   │       CCPlatformDefine-ios.h
│   │   │   │       CCStdC-ios.h
│   │   │   │       cocos2d-prefix.pch
│   │   │   │       OpenGL_Internal-ios.h
│   │   │   │
│   │   │   ├───linux
│   │   │   │       CCApplication-linux.cpp
│   │   │   │       CCApplication-linux.h
│   │   │   │       CCCommon-linux.cpp
│   │   │   │       CCDevice-linux.cpp
│   │   │   │       CCFileUtils-linux.cpp
│   │   │   │       CCFileUtils-linux.h
│   │   │   │       CCGL-linux.h
│   │   │   │       CCPlatformDefine-linux.h
│   │   │   │       CCStdC-linux.cpp
│   │   │   │       CCStdC-linux.h
│   │   │   │
│   │   │   ├───mac
│   │   │   │       CCApplication-mac.h
│   │   │   │       CCApplication-mac.mm
│   │   │   │       CCCommon-mac.mm
│   │   │   │       CCDevice-mac.mm
│   │   │   │       CCGL-mac.h
│   │   │   │       CCPlatformDefine-mac.h
│   │   │   │       CCStdC-mac.h
│   │   │   │       cocos2d-prefix.pch
│   │   │   │
│   │   │   ├───tizen
│   │   │   │       CCApplication-tizen.cpp
│   │   │   │       CCApplication-tizen.h
│   │   │   │       CCCommon-tizen.cpp
│   │   │   │       CCDevice-tizen.cpp
│   │   │   │       CCFileUtils-tizen.cpp
│   │   │   │       CCFileUtils-tizen.h
│   │   │   │       CCGL-tizen.h
│   │   │   │       CCGLViewImpl-tizen.cpp
│   │   │   │       CCGLViewImpl-tizen.h
│   │   │   │       CCPlatformDefine-tizen.h
│   │   │   │       CCStdC-tizen.cpp
│   │   │   │       CCStdC-tizen.h
│   │   │   │
│   │   │   ├───win32
│   │   │   │   │   CCApplication-win32.cpp
│   │   │   │   │   CCApplication-win32.h
│   │   │   │   │   CCCommon-win32.cpp
│   │   │   │   │   CCDevice-win32.cpp
│   │   │   │   │   CCFileUtils-win32.cpp
│   │   │   │   │   CCFileUtils-win32.h
│   │   │   │   │   CCGL-win32.h
│   │   │   │   │   CCPlatformDefine-win32.h
│   │   │   │   │   CCStdC-win32.cpp
│   │   │   │   │   CCStdC-win32.h
│   │   │   │   │   CCUtils-win32.cpp
│   │   │   │   │   CCUtils-win32.h
│   │   │   │   │   inet_pton_mingw.cpp
│   │   │   │   │   inet_pton_mingw.h
│   │   │   │   │
│   │   │   │   └───compat
│   │   │   │           stdint.h
│   │   │   │
│   │   │   ├───win8.1-universal
│   │   │   │   │   Cocos2dRenderer.cpp
│   │   │   │   │   Cocos2dRenderer.h
│   │   │   │   │   OpenGLES.cpp
│   │   │   │   │   OpenGLES.h
│   │   │   │   │   OpenGLESPage.xaml
│   │   │   │   │   OpenGLESPage.xaml.cpp
│   │   │   │   │   OpenGLESPage.xaml.h
│   │   │   │   │   pch.cpp
│   │   │   │   │   pch.h
│   │   │   │   │
│   │   │   │   └───cocos2d-js
│   │   │   │           pch.h
│   │   │   │
│   │   │   └───winrt
│   │   │       │   CCApplication.cpp
│   │   │       │   CCApplication.h
│   │   │       │   CCCommon.cpp
│   │   │       │   CCDevice.cpp
│   │   │       │   CCFileUtilsWinRT.cpp
│   │   │       │   CCFileUtilsWinRT.h
│   │   │       │   CCFreeTypeFont.cpp
│   │   │       │   CCFreeTypeFont.h
│   │   │       │   CCGL.h
│   │   │       │   CCGLViewImpl-winrt.cpp
│   │   │       │   CCGLViewImpl-winrt.h
│   │   │       │   CCGLViewImpl.cpp
│   │   │       │   CCGLViewImpl.h
│   │   │       │   CCPlatformDefine-winrt.h
│   │   │       │   CCPrecompiledShaders.cpp
│   │   │       │   CCPrecompiledShaders.h
│   │   │       │   CCPThreadWinRT.cpp
│   │   │       │   CCPThreadWinRT.h
│   │   │       │   CCStdC.cpp
│   │   │       │   CCStdC.h
│   │   │       │   CCWinRTUtils.cpp
│   │   │       │   CCWinRTUtils.h
│   │   │       │   inet_ntop_winrt.cpp
│   │   │       │   inet_ntop_winrt.h
│   │   │       │   inet_pton_winrt.cpp
│   │   │       │   inet_pton_winrt.h
│   │   │       │   InputEvent.cpp
│   │   │       │   InputEvent.h
│   │   │       │   InputEventTypes.h
│   │   │       │   Keyboard-winrt.cpp
│   │   │       │   Keyboard-winrt.h
│   │   │       │   pch.cpp
│   │   │       │   pch.h
│   │   │       │   sha1.cpp
│   │   │       │   sha1.h
│   │   │       │   targetver.h
│   │   │       │   WICImageLoader-winrt.cpp
│   │   │       │   WICImageLoader-winrt.h
│   │   │       │
│   │   │       └───shaders
│   │   │               precompiledshaders.h
│   │   │
│   │   ├───renderer
│   │   │       CCBatchCommand.cpp
│   │   │       CCBatchCommand.h
│   │   │       CCCustomCommand.cpp
│   │   │       CCCustomCommand.h
│   │   │       CCFrameBuffer.cpp
│   │   │       CCFrameBuffer.h
│   │   │       CCGLProgram.cpp
│   │   │       CCGLProgram.h
│   │   │       CCGLProgramCache.cpp
│   │   │       CCGLProgramCache.h
│   │   │       CCGLProgramState.cpp
│   │   │       CCGLProgramState.h
│   │   │       CCGLProgramStateCache.cpp
│   │   │       CCGLProgramStateCache.h
│   │   │       ccGLStateCache.cpp
│   │   │       ccGLStateCache.h
│   │   │       CCGroupCommand.cpp
│   │   │       CCGroupCommand.h
│   │   │       CCMaterial.cpp
│   │   │       CCMaterial.h
│   │   │       CCMeshCommand.cpp
│   │   │       CCMeshCommand.h
│   │   │       CCPass.cpp
│   │   │       CCPass.h
│   │   │       CCPrimitive.cpp
│   │   │       CCPrimitive.h
│   │   │       CCPrimitiveCommand.cpp
│   │   │       CCPrimitiveCommand.h
│   │   │       CCQuadCommand.cpp
│   │   │       CCQuadCommand.h
│   │   │       CCRenderCommand.cpp
│   │   │       CCRenderCommand.h
│   │   │       CCRenderCommandPool.h
│   │   │       CCRenderer.cpp
│   │   │       CCRenderer.h
│   │   │       CCRenderState.cpp
│   │   │       CCRenderState.h
│   │   │       ccShaders.cpp
│   │   │       ccShaders.h
│   │   │       ccShader_3D_Color.frag
│   │   │       ccShader_3D_ColorNormal.frag
│   │   │       ccShader_3D_ColorNormalTex.frag
│   │   │       ccShader_3D_ColorTex.frag
│   │   │       ccShader_3D_Particle.frag
│   │   │       ccShader_3D_Particle.vert
│   │   │       ccShader_3D_PositionNormalTex.vert
│   │   │       ccShader_3D_PositionTex.vert
│   │   │       ccShader_3D_Skybox.frag
│   │   │       ccShader_3D_Skybox.vert
│   │   │       ccShader_3D_Terrain.frag
│   │   │       ccShader_3D_Terrain.vert
│   │   │       ccShader_CameraClear.frag
│   │   │       ccShader_CameraClear.vert
│   │   │       ccShader_ETC1AS_PositionTextureColor.frag
│   │   │       ccShader_ETC1AS_PositionTextureGray.frag
│   │   │       ccShader_Label.vert
│   │   │       ccShader_Label_df.frag
│   │   │       ccShader_Label_df_glow.frag
│   │   │       ccShader_Label_normal.frag
│   │   │       ccShader_Label_outline.frag
│   │   │       ccShader_PositionColor.frag
│   │   │       ccShader_PositionColor.vert
│   │   │       ccShader_PositionColorLengthTexture.frag
│   │   │       ccShader_PositionColorLengthTexture.vert
│   │   │       ccShader_PositionColorTextureAsPointsize.vert
│   │   │       ccShader_PositionTexture.frag
│   │   │       ccShader_PositionTexture.vert
│   │   │       ccShader_PositionTextureA8Color.frag
│   │   │       ccShader_PositionTextureA8Color.vert
│   │   │       ccShader_PositionTextureColor.frag
│   │   │       ccShader_PositionTextureColor.vert
│   │   │       ccShader_PositionTextureColorAlphaTest.frag
│   │   │       ccShader_PositionTextureColor_noMVP.frag
│   │   │       ccShader_PositionTextureColor_noMVP.vert
│   │   │       ccShader_PositionTexture_uColor.frag
│   │   │       ccShader_PositionTexture_uColor.vert
│   │   │       ccShader_Position_uColor.frag
│   │   │       ccShader_Position_uColor.vert
│   │   │       ccShader_UI_Gray.frag
│   │   │       CCTechnique.cpp
│   │   │       CCTechnique.h
│   │   │       CCTexture2D.cpp
│   │   │       CCTexture2D.h
│   │   │       CCTextureAtlas.cpp
│   │   │       CCTextureAtlas.h
│   │   │       CCTextureCache.cpp
│   │   │       CCTextureCache.h
│   │   │       CCTextureCube.cpp
│   │   │       CCTextureCube.h
│   │   │       CCTrianglesCommand.cpp
│   │   │       CCTrianglesCommand.h
│   │   │       CCVertexAttribBinding.cpp
│   │   │       CCVertexAttribBinding.h
│   │   │       CCVertexIndexBuffer.cpp
│   │   │       CCVertexIndexBuffer.h
│   │   │       CCVertexIndexData.cpp
│   │   │       CCVertexIndexData.h
│   │   │       CMakeLists.txt
│   │   │
│   │   ├───storage
│   │   │   │   CMakeLists.txt
│   │   │   │
│   │   │   └───local-storage
│   │   │           Android.mk
│   │   │           LocalStorage-android.cpp
│   │   │           LocalStorage.cpp
│   │   │           LocalStorage.h
│   │   │
│   │   ├───ui
│   │   │   │   Android.mk
│   │   │   │   CMakeLists.txt
│   │   │   │   CocosGUI.cpp
│   │   │   │   CocosGUI.h
│   │   │   │   GUIDefine.h
│   │   │   │   GUIExport.h
│   │   │   │   UIAbstractCheckButton.cpp
│   │   │   │   UIAbstractCheckButton.h
│   │   │   │   UIButton.cpp
│   │   │   │   UIButton.h
│   │   │   │   UICheckBox.cpp
│   │   │   │   UICheckBox.h
│   │   │   │   UIDeprecated.cpp
│   │   │   │   UIDeprecated.h
│   │   │   │   UIHBox.cpp
│   │   │   │   UIHBox.h
│   │   │   │   UIHelper.cpp
│   │   │   │   UIHelper.h
│   │   │   │   UIImageView.cpp
│   │   │   │   UIImageView.h
│   │   │   │   UILayout.cpp
│   │   │   │   UILayout.h
│   │   │   │   UILayoutComponent.cpp
│   │   │   │   UILayoutComponent.h
│   │   │   │   UILayoutManager.cpp
│   │   │   │   UILayoutManager.h
│   │   │   │   UILayoutParameter.cpp
│   │   │   │   UILayoutParameter.h
│   │   │   │   UIListView.cpp
│   │   │   │   UIListView.h
│   │   │   │   UILoadingBar.cpp
│   │   │   │   UILoadingBar.h
│   │   │   │   UIPageView.cpp
│   │   │   │   UIPageView.h
│   │   │   │   UIPageViewIndicator.cpp
│   │   │   │   UIPageViewIndicator.h
│   │   │   │   UIRadioButton.cpp
│   │   │   │   UIRadioButton.h
│   │   │   │   UIRelativeBox.cpp
│   │   │   │   UIRelativeBox.h
│   │   │   │   UIRichText.cpp
│   │   │   │   UIRichText.h
│   │   │   │   UIScale9Sprite.cpp
│   │   │   │   UIScale9Sprite.h
│   │   │   │   UIScrollView.cpp
│   │   │   │   UIScrollView.h
│   │   │   │   UIScrollViewBar.cpp
│   │   │   │   UIScrollViewBar.h
│   │   │   │   UISlider.cpp
│   │   │   │   UISlider.h
│   │   │   │   UITabControl.cpp
│   │   │   │   UITabControl.h
│   │   │   │   UIText.cpp
│   │   │   │   UIText.h
│   │   │   │   UITextAtlas.cpp
│   │   │   │   UITextAtlas.h
│   │   │   │   UITextBMFont.cpp
│   │   │   │   UITextBMFont.h
│   │   │   │   UITextField.cpp
│   │   │   │   UITextField.h
│   │   │   │   UIVBox.cpp
│   │   │   │   UIVBox.h
│   │   │   │   UIVideoPlayer-android.cpp
│   │   │   │   UIVideoPlayer-ios.mm
│   │   │   │   UIVideoPlayer-tizen.cpp
│   │   │   │   UIVideoPlayer.h
│   │   │   │   UIWebView-inl.h
│   │   │   │   UIWebView.cpp
│   │   │   │   UIWebView.h
│   │   │   │   UIWebView.mm
│   │   │   │   UIWebViewImpl-android.cpp
│   │   │   │   UIWebViewImpl-android.h
│   │   │   │   UIWebViewImpl-ios.h
│   │   │   │   UIWebViewImpl-ios.mm
│   │   │   │   UIWebViewImpl-tizen.cpp
│   │   │   │   UIWebViewImpl-tizen.h
│   │   │   │   UIWidget.cpp
│   │   │   │   UIWidget.h
│   │   │   │
│   │   │   ├───proj.win32
│   │   │   │       libui.vcxproj
│   │   │   │       libui.vcxproj.filters
│   │   │   │
│   │   │   └───UIEditBox
│   │   │       │   UIEditBox.cpp
│   │   │       │   UIEditBox.h
│   │   │       │   UIEditBoxImpl-android.cpp
│   │   │       │   UIEditBoxImpl-android.h
│   │   │       │   UIEditBoxImpl-common.cpp
│   │   │       │   UIEditBoxImpl-common.h
│   │   │       │   UIEditBoxImpl-ios.h
│   │   │       │   UIEditBoxImpl-ios.mm
│   │   │       │   UIEditBoxImpl-linux.cpp
│   │   │       │   UIEditBoxImpl-linux.h
│   │   │       │   UIEditBoxImpl-mac.h
│   │   │       │   UIEditBoxImpl-mac.mm
│   │   │       │   UIEditBoxImpl-stub.cpp
│   │   │       │   UIEditBoxImpl-tizen.cpp
│   │   │       │   UIEditBoxImpl-tizen.h
│   │   │       │   UIEditBoxImpl-win32.cpp
│   │   │       │   UIEditBoxImpl-win32.h
│   │   │       │   UIEditBoxImpl-winrt.cpp
│   │   │       │   UIEditBoxImpl-winrt.h
│   │   │       │   UIEditBoxImpl.h
│   │   │       │
│   │   │       ├───iOS
│   │   │       │       CCUIEditBoxIOS.h
│   │   │       │       CCUIEditBoxIOS.mm
│   │   │       │       CCUIMultilineTextField.h
│   │   │       │       CCUIMultilineTextField.mm
│   │   │       │       CCUISingleLineTextField.h
│   │   │       │       CCUISingleLineTextField.mm
│   │   │       │       CCUITextInput.h
│   │   │       │       UITextField+CCUITextInput.h
│   │   │       │       UITextField+CCUITextInput.mm
│   │   │       │       UITextView+CCUITextInput.h
│   │   │       │       UITextView+CCUITextInput.mm
│   │   │       │
│   │   │       └───Mac
│   │   │               CCUIEditBoxMac.h
│   │   │               CCUIEditBoxMac.mm
│   │   │               CCUIMultilineTextField.h
│   │   │               CCUIMultilineTextField.m
│   │   │               CCUIPasswordTextField.h
│   │   │               CCUIPasswordTextField.m
│   │   │               CCUISingleLineTextField.h
│   │   │               CCUISingleLineTextField.m
│   │   │               CCUITextFieldFormatter.h
│   │   │               CCUITextFieldFormatter.m
│   │   │               CCUITextInput.h
│   │   │
│   │   └───vr
│   │           CCVRDistortion.cpp
│   │           CCVRDistortion.h
│   │           CCVRDistortionMesh.cpp
│   │           CCVRDistortionMesh.h
│   │           CCVRGenericHeadTracker.cpp
│   │           CCVRGenericHeadTracker.h
│   │           CCVRGenericRenderer.cpp
│   │           CCVRGenericRenderer.h
│   │           CCVRProtocol.h
│   │           CMakeLists.txt
│   │
│   ├───docs
│   │       cocos2dx_portrait.png
│   │       CODING_STYLE.md
│   │       doxygen.config
│   │       doxygen_white_book.config
│   │       framework_architecture.jpg
│   │       Groups.h
│   │       img-cocos.jpg
│   │       MainPage.h
│   │       MainPageWhiteBook.h
│   │       RELEASE_ENGINEERING.md
│   │       RELEASE_NOTES.md
│   │       RELEASE_NOTES_CN.md
│   │
│   ├───extensions
│   │   │   Android.mk
│   │   │   CMakeLists.txt
│   │   │   cocos-ext.h
│   │   │   ExtensionDeprecated.cpp
│   │   │   ExtensionDeprecated.h
│   │   │   ExtensionExport.h
│   │   │   ExtensionMacros.h
│   │   │
│   │   ├───assets-manager
│   │   │       AssetsManager.cpp
│   │   │       AssetsManager.h
│   │   │       AssetsManagerEx.cpp
│   │   │       AssetsManagerEx.h
│   │   │       CCEventAssetsManagerEx.cpp
│   │   │       CCEventAssetsManagerEx.h
│   │   │       CCEventListenerAssetsManagerEx.cpp
│   │   │       CCEventListenerAssetsManagerEx.h
│   │   │       Manifest.cpp
│   │   │       Manifest.h
│   │   │
│   │   ├───GUI
│   │   │   ├───CCControlExtension
│   │   │   │       CCControl.cpp
│   │   │   │       CCControl.h
│   │   │   │       CCControlButton.cpp
│   │   │   │       CCControlButton.h
│   │   │   │       CCControlColourPicker.cpp
│   │   │   │       CCControlColourPicker.h
│   │   │   │       CCControlExtensions.h
│   │   │   │       CCControlHuePicker.cpp
│   │   │   │       CCControlHuePicker.h
│   │   │   │       CCControlPotentiometer.cpp
│   │   │   │       CCControlPotentiometer.h
│   │   │   │       CCControlSaturationBrightnessPicker.cpp
│   │   │   │       CCControlSaturationBrightnessPicker.h
│   │   │   │       CCControlSlider.cpp
│   │   │   │       CCControlSlider.h
│   │   │   │       CCControlStepper.cpp
│   │   │   │       CCControlStepper.h
│   │   │   │       CCControlSwitch.cpp
│   │   │   │       CCControlSwitch.h
│   │   │   │       CCControlUtils.cpp
│   │   │   │       CCControlUtils.h
│   │   │   │       CCInvocation.cpp
│   │   │   │       CCInvocation.h
│   │   │   │
│   │   │   └───CCScrollView
│   │   │           CCScrollView.cpp
│   │   │           CCScrollView.h
│   │   │           CCTableView.cpp
│   │   │           CCTableView.h
│   │   │           CCTableViewCell.cpp
│   │   │           CCTableViewCell.h
│   │   │
│   │   ├───Particle3D
│   │   │   │   CCParticle3DAffector.cpp
│   │   │   │   CCParticle3DAffector.h
│   │   │   │   CCParticle3DEmitter.cpp
│   │   │   │   CCParticle3DEmitter.h
│   │   │   │   CCParticle3DRender.cpp
│   │   │   │   CCParticle3DRender.h
│   │   │   │   CCParticleSystem3D.cpp
│   │   │   │   CCParticleSystem3D.h
│   │   │   │
│   │   │   └───PU
│   │   │           CCPUAffector.cpp
│   │   │           CCPUAffector.h
│   │   │           CCPUAffectorManager.cpp
│   │   │           CCPUAffectorManager.h
│   │   │           CCPUAffectorTranslator.cpp
│   │   │           CCPUAffectorTranslator.h
│   │   │           CCPUAlignAffector.cpp
│   │   │           CCPUAlignAffector.h
│   │   │           CCPUAlignAffectorTranslator.cpp
│   │   │           CCPUAlignAffectorTranslator.h
│   │   │           CCPUBaseCollider.cpp
│   │   │           CCPUBaseCollider.h
│   │   │           CCPUBaseColliderTranslator.cpp
│   │   │           CCPUBaseColliderTranslator.h
│   │   │           CCPUBaseForceAffector.cpp
│   │   │           CCPUBaseForceAffector.h
│   │   │           CCPUBaseForceAffectorTranslator.cpp
│   │   │           CCPUBaseForceAffectorTranslator.h
│   │   │           CCPUBeamRender.cpp
│   │   │           CCPUBeamRender.h
│   │   │           CCPUBehaviour.cpp
│   │   │           CCPUBehaviour.h
│   │   │           CCPUBehaviourManager.cpp
│   │   │           CCPUBehaviourManager.h
│   │   │           CCPUBehaviourTranslator.cpp
│   │   │           CCPUBehaviourTranslator.h
│   │   │           CCPUBillboardChain.cpp
│   │   │           CCPUBillboardChain.h
│   │   │           CCPUBoxCollider.cpp
│   │   │           CCPUBoxCollider.h
│   │   │           CCPUBoxColliderTranslator.cpp
│   │   │           CCPUBoxColliderTranslator.h
│   │   │           CCPUBoxEmitter.cpp
│   │   │           CCPUBoxEmitter.h
│   │   │           CCPUBoxEmitterTranslator.cpp
│   │   │           CCPUBoxEmitterTranslator.h
│   │   │           CCPUCircleEmitter.cpp
│   │   │           CCPUCircleEmitter.h
│   │   │           CCPUCircleEmitterTranslator.cpp
│   │   │           CCPUCircleEmitterTranslator.h
│   │   │           CCPUCollisionAvoidanceAffector.cpp
│   │   │           CCPUCollisionAvoidanceAffector.h
│   │   │           CCPUCollisionAvoidanceAffectorTranslator.cpp
│   │   │           CCPUCollisionAvoidanceAffectorTranslator.h
│   │   │           CCPUColorAffector.cpp
│   │   │           CCPUColorAffector.h
│   │   │           CCPUColorAffectorTranslator.cpp
│   │   │           CCPUColorAffectorTranslator.h
│   │   │           CCPUDoAffectorEventHandler.cpp
│   │   │           CCPUDoAffectorEventHandler.h
│   │   │           CCPUDoAffectorEventHandlerTranslator.cpp
│   │   │           CCPUDoAffectorEventHandlerTranslator.h
│   │   │           CCPUDoEnableComponentEventHandler.cpp
│   │   │           CCPUDoEnableComponentEventHandler.h
│   │   │           CCPUDoEnableComponentEventHandlerTranslator.cpp
│   │   │           CCPUDoEnableComponentEventHandlerTranslator.h
│   │   │           CCPUDoExpireEventHandler.cpp
│   │   │           CCPUDoExpireEventHandler.h
│   │   │           CCPUDoExpireEventHandlerTranslator.cpp
│   │   │           CCPUDoExpireEventHandlerTranslator.h
│   │   │           CCPUDoFreezeEventHandler.cpp
│   │   │           CCPUDoFreezeEventHandler.h
│   │   │           CCPUDoFreezeEventHandlerTranslator.cpp
│   │   │           CCPUDoFreezeEventHandlerTranslator.h
│   │   │           CCPUDoPlacementParticleEventHandler.cpp
│   │   │           CCPUDoPlacementParticleEventHandler.h
│   │   │           CCPUDoPlacementParticleEventHandlerTranslator.cpp
│   │   │           CCPUDoPlacementParticleEventHandlerTranslator.h
│   │   │           CCPUDoScaleEventHandler.cpp
│   │   │           CCPUDoScaleEventHandler.h
│   │   │           CCPUDoScaleEventHandlerTranslator.cpp
│   │   │           CCPUDoScaleEventHandlerTranslator.h
│   │   │           CCPUDoStopSystemEventHandler.cpp
│   │   │           CCPUDoStopSystemEventHandler.h
│   │   │           CCPUDoStopSystemEventHandlerTranslator.cpp
│   │   │           CCPUDoStopSystemEventHandlerTranslator.h
│   │   │           CCPUDynamicAttribute.cpp
│   │   │           CCPUDynamicAttribute.h
│   │   │           CCPUDynamicAttributeTranslator.cpp
│   │   │           CCPUDynamicAttributeTranslator.h
│   │   │           CCPUEmitter.cpp
│   │   │           CCPUEmitter.h
│   │   │           CCPUEmitterManager.cpp
│   │   │           CCPUEmitterManager.h
│   │   │           CCPUEmitterTranslator.cpp
│   │   │           CCPUEmitterTranslator.h
│   │   │           CCPUEventHandler.cpp
│   │   │           CCPUEventHandler.h
│   │   │           CCPUEventHandlerManager.cpp
│   │   │           CCPUEventHandlerManager.h
│   │   │           CCPUEventHandlerTranslator.cpp
│   │   │           CCPUEventHandlerTranslator.h
│   │   │           CCPUFlockCenteringAffector.cpp
│   │   │           CCPUFlockCenteringAffector.h
│   │   │           CCPUFlockCenteringAffectorTranslator.cpp
│   │   │           CCPUFlockCenteringAffectorTranslator.h
│   │   │           CCPUForceField.cpp
│   │   │           CCPUForceField.h
│   │   │           CCPUForceFieldAffector.cpp
│   │   │           CCPUForceFieldAffector.h
│   │   │           CCPUForceFieldAffectorTranslator.cpp
│   │   │           CCPUForceFieldAffectorTranslator.h
│   │   │           CCPUGeometryRotator.cpp
│   │   │           CCPUGeometryRotator.h
│   │   │           CCPUGeometryRotatorTranslator.cpp
│   │   │           CCPUGeometryRotatorTranslator.h
│   │   │           CCPUGravityAffector.cpp
│   │   │           CCPUGravityAffector.h
│   │   │           CCPUGravityAffectorTranslator.cpp
│   │   │           CCPUGravityAffectorTranslator.h
│   │   │           CCPUInterParticleCollider.cpp
│   │   │           CCPUInterParticleCollider.h
│   │   │           CCPUInterParticleColliderTranslator.cpp
│   │   │           CCPUInterParticleColliderTranslator.h
│   │   │           CCPUJetAffector.cpp
│   │   │           CCPUJetAffector.h
│   │   │           CCPUJetAffectorTranslator.cpp
│   │   │           CCPUJetAffectorTranslator.h
│   │   │           CCPULineAffector.cpp
│   │   │           CCPULineAffector.h
│   │   │           CCPULineAffectorTranslator.cpp
│   │   │           CCPULineAffectorTranslator.h
│   │   │           CCPULinearForceAffector.cpp
│   │   │           CCPULinearForceAffector.h
│   │   │           CCPULinearForceAffectorTranslator.cpp
│   │   │           CCPULinearForceAffectorTranslator.h
│   │   │           CCPULineEmitter.cpp
│   │   │           CCPULineEmitter.h
│   │   │           CCPULineEmitterTranslator.cpp
│   │   │           CCPULineEmitterTranslator.h
│   │   │           CCPUListener.cpp
│   │   │           CCPUListener.h
│   │   │           CCPUMaterialManager.cpp
│   │   │           CCPUMaterialManager.h
│   │   │           CCPUMaterialTranslator.cpp
│   │   │           CCPUMaterialTranslator.h
│   │   │           CCPUMeshSurfaceEmitter.cpp
│   │   │           CCPUMeshSurfaceEmitter.h
│   │   │           CCPUMeshSurfaceEmitterTranslator.cpp
│   │   │           CCPUMeshSurfaceEmitterTranslator.h
│   │   │           CCPUNoise.cpp
│   │   │           CCPUNoise.h
│   │   │           CCPUObserver.cpp
│   │   │           CCPUObserver.h
│   │   │           CCPUObserverManager.cpp
│   │   │           CCPUObserverManager.h
│   │   │           CCPUObserverTranslator.cpp
│   │   │           CCPUObserverTranslator.h
│   │   │           CCPUOnClearObserver.cpp
│   │   │           CCPUOnClearObserver.h
│   │   │           CCPUOnClearObserverTranslator.cpp
│   │   │           CCPUOnClearObserverTranslator.h
│   │   │           CCPUOnCollisionObserver.cpp
│   │   │           CCPUOnCollisionObserver.h
│   │   │           CCPUOnCollisionObserverTranslator.cpp
│   │   │           CCPUOnCollisionObserverTranslator.h
│   │   │           CCPUOnCountObserver.cpp
│   │   │           CCPUOnCountObserver.h
│   │   │           CCPUOnCountObserverTranslator.cpp
│   │   │           CCPUOnCountObserverTranslator.h
│   │   │           CCPUOnEmissionObserver.cpp
│   │   │           CCPUOnEmissionObserver.h
│   │   │           CCPUOnEmissionObserverTranslator.cpp
│   │   │           CCPUOnEmissionObserverTranslator.h
│   │   │           CCPUOnEventFlagObserver.cpp
│   │   │           CCPUOnEventFlagObserver.h
│   │   │           CCPUOnEventFlagObserverTranslator.cpp
│   │   │           CCPUOnEventFlagObserverTranslator.h
│   │   │           CCPUOnExpireObserver.cpp
│   │   │           CCPUOnExpireObserver.h
│   │   │           CCPUOnExpireObserverTranslator.cpp
│   │   │           CCPUOnExpireObserverTranslator.h
│   │   │           CCPUOnPositionObserver.cpp
│   │   │           CCPUOnPositionObserver.h
│   │   │           CCPUOnPositionObserverTranslator.cpp
│   │   │           CCPUOnPositionObserverTranslator.h
│   │   │           CCPUOnQuotaObserver.cpp
│   │   │           CCPUOnQuotaObserver.h
│   │   │           CCPUOnQuotaObserverTranslator.cpp
│   │   │           CCPUOnQuotaObserverTranslator.h
│   │   │           CCPUOnRandomObserver.cpp
│   │   │           CCPUOnRandomObserver.h
│   │   │           CCPUOnRandomObserverTranslator.cpp
│   │   │           CCPUOnRandomObserverTranslator.h
│   │   │           CCPUOnTimeObserver.cpp
│   │   │           CCPUOnTimeObserver.h
│   │   │           CCPUOnTimeObserverTranslator.cpp
│   │   │           CCPUOnTimeObserverTranslator.h
│   │   │           CCPUOnVelocityObserver.cpp
│   │   │           CCPUOnVelocityObserver.h
│   │   │           CCPUOnVelocityObserverTranslator.cpp
│   │   │           CCPUOnVelocityObserverTranslator.h
│   │   │           CCPUParticleFollower.cpp
│   │   │           CCPUParticleFollower.h
│   │   │           CCPUParticleFollowerTranslator.cpp
│   │   │           CCPUParticleFollowerTranslator.h
│   │   │           CCPUParticleSystem3D.cpp
│   │   │           CCPUParticleSystem3D.h
│   │   │           CCPUParticleSystem3DTranslator.cpp
│   │   │           CCPUParticleSystem3DTranslator.h
│   │   │           CCPUPathFollower.cpp
│   │   │           CCPUPathFollower.h
│   │   │           CCPUPathFollowerTranslator.cpp
│   │   │           CCPUPathFollowerTranslator.h
│   │   │           CCPUPlane.cpp
│   │   │           CCPUPlane.h
│   │   │           CCPUPlaneCollider.cpp
│   │   │           CCPUPlaneCollider.h
│   │   │           CCPUPlaneColliderTranslator.cpp
│   │   │           CCPUPlaneColliderTranslator.h
│   │   │           CCPUPointEmitter.cpp
│   │   │           CCPUPointEmitter.h
│   │   │           CCPUPointEmitterTranslator.cpp
│   │   │           CCPUPointEmitterTranslator.h
│   │   │           CCPUPositionEmitter.cpp
│   │   │           CCPUPositionEmitter.h
│   │   │           CCPUPositionEmitterTranslator.cpp
│   │   │           CCPUPositionEmitterTranslator.h
│   │   │           CCPURandomiser.cpp
│   │   │           CCPURandomiser.h
│   │   │           CCPURandomiserTranslator.cpp
│   │   │           CCPURandomiserTranslator.h
│   │   │           CCPURender.cpp
│   │   │           CCPURender.h
│   │   │           CCPURendererTranslator.cpp
│   │   │           CCPURendererTranslator.h
│   │   │           CCPURibbonTrail.cpp
│   │   │           CCPURibbonTrail.h
│   │   │           CCPURibbonTrailRender.cpp
│   │   │           CCPURibbonTrailRender.h
│   │   │           CCPUScaleAffector.cpp
│   │   │           CCPUScaleAffector.h
│   │   │           CCPUScaleAffectorTranslator.cpp
│   │   │           CCPUScaleAffectorTranslator.h
│   │   │           CCPUScaleVelocityAffector.cpp
│   │   │           CCPUScaleVelocityAffector.h
│   │   │           CCPUScaleVelocityAffectorTranslator.cpp
│   │   │           CCPUScaleVelocityAffectorTranslator.h
│   │   │           CCPUScriptCompiler.cpp
│   │   │           CCPUScriptCompiler.h
│   │   │           CCPUScriptLexer.cpp
│   │   │           CCPUScriptLexer.h
│   │   │           CCPUScriptParser.cpp
│   │   │           CCPUScriptParser.h
│   │   │           CCPUScriptTranslator.cpp
│   │   │           CCPUScriptTranslator.h
│   │   │           CCPUSimpleSpline.cpp
│   │   │           CCPUSimpleSpline.h
│   │   │           CCPUSineForceAffector.cpp
│   │   │           CCPUSineForceAffector.h
│   │   │           CCPUSineForceAffectorTranslator.cpp
│   │   │           CCPUSineForceAffectorTranslator.h
│   │   │           CCPUSlaveBehaviour.cpp
│   │   │           CCPUSlaveBehaviour.h
│   │   │           CCPUSlaveBehaviourTranslator.cpp
│   │   │           CCPUSlaveBehaviourTranslator.h
│   │   │           CCPUSlaveEmitter.cpp
│   │   │           CCPUSlaveEmitter.h
│   │   │           CCPUSlaveEmitterTranslator.cpp
│   │   │           CCPUSlaveEmitterTranslator.h
│   │   │           CCPUSphere.cpp
│   │   │           CCPUSphere.h
│   │   │           CCPUSphereCollider.cpp
│   │   │           CCPUSphereCollider.h
│   │   │           CCPUSphereColliderTranslator.cpp
│   │   │           CCPUSphereColliderTranslator.h
│   │   │           CCPUSphereSurfaceEmitter.cpp
│   │   │           CCPUSphereSurfaceEmitter.h
│   │   │           CCPUSphereSurfaceEmitterTranslator.cpp
│   │   │           CCPUSphereSurfaceEmitterTranslator.h
│   │   │           CCPUTechniqueTranslator.cpp
│   │   │           CCPUTechniqueTranslator.h
│   │   │           CCPUTextureAnimator.cpp
│   │   │           CCPUTextureAnimator.h
│   │   │           CCPUTextureAnimatorTranslator.cpp
│   │   │           CCPUTextureAnimatorTranslator.h
│   │   │           CCPUTextureRotator.cpp
│   │   │           CCPUTextureRotator.h
│   │   │           CCPUTextureRotatorTranslator.cpp
│   │   │           CCPUTextureRotatorTranslator.h
│   │   │           CCPUTranslateManager.cpp
│   │   │           CCPUTranslateManager.h
│   │   │           CCPUUtil.cpp
│   │   │           CCPUUtil.h
│   │   │           CCPUVelocityMatchingAffector.cpp
│   │   │           CCPUVelocityMatchingAffector.h
│   │   │           CCPUVelocityMatchingAffectorTranslator.cpp
│   │   │           CCPUVelocityMatchingAffectorTranslator.h
│   │   │           CCPUVertexEmitter.cpp
│   │   │           CCPUVertexEmitter.h
│   │   │           CCPUVortexAffector.cpp
│   │   │           CCPUVortexAffector.h
│   │   │           CCPUVortexAffectorTranslator.cpp
│   │   │           CCPUVortexAffectorTranslator.h
│   │   │
│   │   └───physics-nodes
│   │           CCPhysicsDebugNode.cpp
│   │           CCPhysicsDebugNode.h
│   │           CCPhysicsSprite.cpp
│   │           CCPhysicsSprite.h
│   │
│   ├───external
│   │   │   config.json
│   │   │   version.json
│   │   │
│   │   ├───Box2D
│   │   │   │   Android.mk
│   │   │   │   Box2D.h
│   │   │   │   CMakeLists.txt
│   │   │   │
│   │   │   ├───Collision
│   │   │   │   │   b2BroadPhase.cpp
│   │   │   │   │   b2BroadPhase.h
│   │   │   │   │   b2CollideCircle.cpp
│   │   │   │   │   b2CollideEdge.cpp
│   │   │   │   │   b2CollidePolygon.cpp
│   │   │   │   │   b2Collision.cpp
│   │   │   │   │   b2Collision.h
│   │   │   │   │   b2Distance.cpp
│   │   │   │   │   b2Distance.h
│   │   │   │   │   b2DynamicTree.cpp
│   │   │   │   │   b2DynamicTree.h
│   │   │   │   │   b2TimeOfImpact.cpp
│   │   │   │   │   b2TimeOfImpact.h
│   │   │   │   │
│   │   │   │   └───Shapes
│   │   │   │           b2ChainShape.cpp
│   │   │   │           b2ChainShape.h
│   │   │   │           b2CircleShape.cpp
│   │   │   │           b2CircleShape.h
│   │   │   │           b2EdgeShape.cpp
│   │   │   │           b2EdgeShape.h
│   │   │   │           b2PolygonShape.cpp
│   │   │   │           b2PolygonShape.h
│   │   │   │           b2Shape.h
│   │   │   │
│   │   │   ├───Common
│   │   │   │       b2BlockAllocator.cpp
│   │   │   │       b2BlockAllocator.h
│   │   │   │       b2Draw.cpp
│   │   │   │       b2Draw.h
│   │   │   │       b2GrowableStack.h
│   │   │   │       b2Math.cpp
│   │   │   │       b2Math.h
│   │   │   │       b2Settings.cpp
│   │   │   │       b2Settings.h
│   │   │   │       b2StackAllocator.cpp
│   │   │   │       b2StackAllocator.h
│   │   │   │       b2Timer.cpp
│   │   │   │       b2Timer.h
│   │   │   │
│   │   │   ├───Dynamics
│   │   │   │   │   b2Body.cpp
│   │   │   │   │   b2Body.h
│   │   │   │   │   b2ContactManager.cpp
│   │   │   │   │   b2ContactManager.h
│   │   │   │   │   b2Fixture.cpp
│   │   │   │   │   b2Fixture.h
│   │   │   │   │   b2Island.cpp
│   │   │   │   │   b2Island.h
│   │   │   │   │   b2TimeStep.h
│   │   │   │   │   b2World.cpp
│   │   │   │   │   b2World.h
│   │   │   │   │   b2WorldCallbacks.cpp
│   │   │   │   │   b2WorldCallbacks.h
│   │   │   │   │
│   │   │   │   ├───Contacts
│   │   │   │   │       b2ChainAndCircleContact.cpp
│   │   │   │   │       b2ChainAndCircleContact.h
│   │   │   │   │       b2ChainAndPolygonContact.cpp
│   │   │   │   │       b2ChainAndPolygonContact.h
│   │   │   │   │       b2CircleContact.cpp
│   │   │   │   │       b2CircleContact.h
│   │   │   │   │       b2Contact.cpp
│   │   │   │   │       b2Contact.h
│   │   │   │   │       b2ContactSolver.cpp
│   │   │   │   │       b2ContactSolver.h
│   │   │   │   │       b2EdgeAndCircleContact.cpp
│   │   │   │   │       b2EdgeAndCircleContact.h
│   │   │   │   │       b2EdgeAndPolygonContact.cpp
│   │   │   │   │       b2EdgeAndPolygonContact.h
│   │   │   │   │       b2PolygonAndCircleContact.cpp
│   │   │   │   │       b2PolygonAndCircleContact.h
│   │   │   │   │       b2PolygonContact.cpp
│   │   │   │   │       b2PolygonContact.h
│   │   │   │   │
│   │   │   │   └───Joints
│   │   │   │           b2DistanceJoint.cpp
│   │   │   │           b2DistanceJoint.h
│   │   │   │           b2FrictionJoint.cpp
│   │   │   │           b2FrictionJoint.h
│   │   │   │           b2GearJoint.cpp
│   │   │   │           b2GearJoint.h
│   │   │   │           b2Joint.cpp
│   │   │   │           b2Joint.h
│   │   │   │           b2MotorJoint.cpp
│   │   │   │           b2MotorJoint.h
│   │   │   │           b2MouseJoint.cpp
│   │   │   │           b2MouseJoint.h
│   │   │   │           b2PrismaticJoint.cpp
│   │   │   │           b2PrismaticJoint.h
│   │   │   │           b2PulleyJoint.cpp
│   │   │   │           b2PulleyJoint.h
│   │   │   │           b2RevoluteJoint.cpp
│   │   │   │           b2RevoluteJoint.h
│   │   │   │           b2RopeJoint.cpp
│   │   │   │           b2RopeJoint.h
│   │   │   │           b2WeldJoint.cpp
│   │   │   │           b2WeldJoint.h
│   │   │   │           b2WheelJoint.cpp
│   │   │   │           b2WheelJoint.h
│   │   │   │
│   │   │   ├───proj-win10
│   │   │   │       libbox2d.vcxproj
│   │   │   │       libbox2d.vcxproj.filters
│   │   │   │
│   │   │   ├───proj.win32
│   │   │   │       libbox2d.vcxproj
│   │   │   │       libbox2d.vcxproj.filters
│   │   │   │
│   │   │   ├───proj.win8.1-universal
│   │   │   │   ├───libbox2d.Shared
│   │   │   │   │       libbox2d.Shared.vcxitems
│   │   │   │   │       libbox2d.Shared.vcxitems.filters
│   │   │   │   │
│   │   │   │   ├───libbox2d.Windows
│   │   │   │   │       libbox2d.Windows.vcxproj
│   │   │   │   │       libbox2d.Windows.vcxproj.filters
│   │   │   │   │
│   │   │   │   └───libbox2d.WindowsPhone
│   │   │   │           libbox2d.WindowsPhone.vcxproj
│   │   │   │           libbox2d.WindowsPhone.vcxproj.filters
│   │   │   │
│   │   │   └───Rope
│   │   │           b2Rope.cpp
│   │   │           b2Rope.h
│   │   │
│   │   ├───bullet
│   │   │   │   Android.mk
│   │   │   │   btBulletCollisionCommon.h
│   │   │   │   btBulletDynamicsCommon.h
│   │   │   │   Bullet-C-Api.h
│   │   │   │   CMakeLists.txt
│   │   │   │
│   │   │   ├───BulletCollision
│   │   │   │   ├───BroadphaseCollision
│   │   │   │   │       btAxisSweep3.cpp
│   │   │   │   │       btAxisSweep3.h
│   │   │   │   │       btBroadphaseInterface.h
│   │   │   │   │       btBroadphaseProxy.cpp
│   │   │   │   │       btBroadphaseProxy.h
│   │   │   │   │       btCollisionAlgorithm.cpp
│   │   │   │   │       btCollisionAlgorithm.h
│   │   │   │   │       btDbvt.cpp
│   │   │   │   │       btDbvt.h
│   │   │   │   │       btDbvtBroadphase.cpp
│   │   │   │   │       btDbvtBroadphase.h
│   │   │   │   │       btDispatcher.cpp
│   │   │   │   │       btDispatcher.h
│   │   │   │   │       btMultiSapBroadphase.cpp
│   │   │   │   │       btMultiSapBroadphase.h
│   │   │   │   │       btOverlappingPairCache.cpp
│   │   │   │   │       btOverlappingPairCache.h
│   │   │   │   │       btOverlappingPairCallback.h
│   │   │   │   │       btQuantizedBvh.cpp
│   │   │   │   │       btQuantizedBvh.h
│   │   │   │   │       btSimpleBroadphase.cpp
│   │   │   │   │       btSimpleBroadphase.h
│   │   │   │   │
│   │   │   │   ├───CollisionDispatch
│   │   │   │   │       btActivatingCollisionAlgorithm.cpp
│   │   │   │   │       btActivatingCollisionAlgorithm.h
│   │   │   │   │       btBox2dBox2dCollisionAlgorithm.cpp
│   │   │   │   │       btBox2dBox2dCollisionAlgorithm.h
│   │   │   │   │       btBoxBoxCollisionAlgorithm.cpp
│   │   │   │   │       btBoxBoxCollisionAlgorithm.h
│   │   │   │   │       btBoxBoxDetector.cpp
│   │   │   │   │       btBoxBoxDetector.h
│   │   │   │   │       btCollisionConfiguration.h
│   │   │   │   │       btCollisionCreateFunc.h
│   │   │   │   │       btCollisionDispatcher.cpp
│   │   │   │   │       btCollisionDispatcher.h
│   │   │   │   │       btCollisionObject.cpp
│   │   │   │   │       btCollisionObject.h
│   │   │   │   │       btCollisionObjectWrapper.h
│   │   │   │   │       btCollisionWorld.cpp
│   │   │   │   │       btCollisionWorld.h
│   │   │   │   │       btCompoundCollisionAlgorithm.cpp
│   │   │   │   │       btCompoundCollisionAlgorithm.h
│   │   │   │   │       btCompoundCompoundCollisionAlgorithm.cpp
│   │   │   │   │       btCompoundCompoundCollisionAlgorithm.h
│   │   │   │   │       btConvex2dConvex2dAlgorithm.cpp
│   │   │   │   │       btConvex2dConvex2dAlgorithm.h
│   │   │   │   │       btConvexConcaveCollisionAlgorithm.cpp
│   │   │   │   │       btConvexConcaveCollisionAlgorithm.h
│   │   │   │   │       btConvexConvexAlgorithm.cpp
│   │   │   │   │       btConvexConvexAlgorithm.h
│   │   │   │   │       btConvexPlaneCollisionAlgorithm.cpp
│   │   │   │   │       btConvexPlaneCollisionAlgorithm.h
│   │   │   │   │       btDefaultCollisionConfiguration.cpp
│   │   │   │   │       btDefaultCollisionConfiguration.h
│   │   │   │   │       btEmptyCollisionAlgorithm.cpp
│   │   │   │   │       btEmptyCollisionAlgorithm.h
│   │   │   │   │       btGhostObject.cpp
│   │   │   │   │       btGhostObject.h
│   │   │   │   │       btHashedSimplePairCache.cpp
│   │   │   │   │       btHashedSimplePairCache.h
│   │   │   │   │       btInternalEdgeUtility.cpp
│   │   │   │   │       btInternalEdgeUtility.h
│   │   │   │   │       btManifoldResult.cpp
│   │   │   │   │       btManifoldResult.h
│   │   │   │   │       btSimulationIslandManager.cpp
│   │   │   │   │       btSimulationIslandManager.h
│   │   │   │   │       btSphereBoxCollisionAlgorithm.cpp
│   │   │   │   │       btSphereBoxCollisionAlgorithm.h
│   │   │   │   │       btSphereSphereCollisionAlgorithm.cpp
│   │   │   │   │       btSphereSphereCollisionAlgorithm.h
│   │   │   │   │       btSphereTriangleCollisionAlgorithm.cpp
│   │   │   │   │       btSphereTriangleCollisionAlgorithm.h
│   │   │   │   │       btUnionFind.cpp
│   │   │   │   │       btUnionFind.h
│   │   │   │   │       SphereTriangleDetector.cpp
│   │   │   │   │       SphereTriangleDetector.h
│   │   │   │   │
│   │   │   │   ├───CollisionShapes
│   │   │   │   │       btBox2dShape.cpp
│   │   │   │   │       btBox2dShape.h
│   │   │   │   │       btBoxShape.cpp
│   │   │   │   │       btBoxShape.h
│   │   │   │   │       btBvhTriangleMeshShape.cpp
│   │   │   │   │       btBvhTriangleMeshShape.h
│   │   │   │   │       btCapsuleShape.cpp
│   │   │   │   │       btCapsuleShape.h
│   │   │   │   │       btCollisionMargin.h
│   │   │   │   │       btCollisionShape.cpp
│   │   │   │   │       btCollisionShape.h
│   │   │   │   │       btCompoundShape.cpp
│   │   │   │   │       btCompoundShape.h
│   │   │   │   │       btConcaveShape.cpp
│   │   │   │   │       btConcaveShape.h
│   │   │   │   │       btConeShape.cpp
│   │   │   │   │       btConeShape.h
│   │   │   │   │       btConvex2dShape.cpp
│   │   │   │   │       btConvex2dShape.h
│   │   │   │   │       btConvexHullShape.cpp
│   │   │   │   │       btConvexHullShape.h
│   │   │   │   │       btConvexInternalShape.cpp
│   │   │   │   │       btConvexInternalShape.h
│   │   │   │   │       btConvexPointCloudShape.cpp
│   │   │   │   │       btConvexPointCloudShape.h
│   │   │   │   │       btConvexPolyhedron.cpp
│   │   │   │   │       btConvexPolyhedron.h
│   │   │   │   │       btConvexShape.cpp
│   │   │   │   │       btConvexShape.h
│   │   │   │   │       btConvexTriangleMeshShape.cpp
│   │   │   │   │       btConvexTriangleMeshShape.h
│   │   │   │   │       btCylinderShape.cpp
│   │   │   │   │       btCylinderShape.h
│   │   │   │   │       btEmptyShape.cpp
│   │   │   │   │       btEmptyShape.h
│   │   │   │   │       btHeightfieldTerrainShape.cpp
│   │   │   │   │       btHeightfieldTerrainShape.h
│   │   │   │   │       btMaterial.h
│   │   │   │   │       btMinkowskiSumShape.cpp
│   │   │   │   │       btMinkowskiSumShape.h
│   │   │   │   │       btMultimaterialTriangleMeshShape.cpp
│   │   │   │   │       btMultimaterialTriangleMeshShape.h
│   │   │   │   │       btMultiSphereShape.cpp
│   │   │   │   │       btMultiSphereShape.h
│   │   │   │   │       btOptimizedBvh.cpp
│   │   │   │   │       btOptimizedBvh.h
│   │   │   │   │       btPolyhedralConvexShape.cpp
│   │   │   │   │       btPolyhedralConvexShape.h
│   │   │   │   │       btScaledBvhTriangleMeshShape.cpp
│   │   │   │   │       btScaledBvhTriangleMeshShape.h
│   │   │   │   │       btShapeHull.cpp
│   │   │   │   │       btShapeHull.h
│   │   │   │   │       btSphereShape.cpp
│   │   │   │   │       btSphereShape.h
│   │   │   │   │       btStaticPlaneShape.cpp
│   │   │   │   │       btStaticPlaneShape.h
│   │   │   │   │       btStridingMeshInterface.cpp
│   │   │   │   │       btStridingMeshInterface.h
│   │   │   │   │       btTetrahedronShape.cpp
│   │   │   │   │       btTetrahedronShape.h
│   │   │   │   │       btTriangleBuffer.cpp
│   │   │   │   │       btTriangleBuffer.h
│   │   │   │   │       btTriangleCallback.cpp
│   │   │   │   │       btTriangleCallback.h
│   │   │   │   │       btTriangleIndexVertexArray.cpp
│   │   │   │   │       btTriangleIndexVertexArray.h
│   │   │   │   │       btTriangleIndexVertexMaterialArray.cpp
│   │   │   │   │       btTriangleIndexVertexMaterialArray.h
│   │   │   │   │       btTriangleInfoMap.h
│   │   │   │   │       btTriangleMesh.cpp
│   │   │   │   │       btTriangleMesh.h
│   │   │   │   │       btTriangleMeshShape.cpp
│   │   │   │   │       btTriangleMeshShape.h
│   │   │   │   │       btTriangleShape.h
│   │   │   │   │       btUniformScalingShape.cpp
│   │   │   │   │       btUniformScalingShape.h
│   │   │   │   │
│   │   │   │   ├───Gimpact
│   │   │   │   │       btBoxCollision.h
│   │   │   │   │       btClipPolygon.h
│   │   │   │   │       btCompoundFromGimpact.h
│   │   │   │   │       btContactProcessing.cpp
│   │   │   │   │       btContactProcessing.h
│   │   │   │   │       btGenericPoolAllocator.cpp
│   │   │   │   │       btGenericPoolAllocator.h
│   │   │   │   │       btGeometryOperations.h
│   │   │   │   │       btGImpactBvh.cpp
│   │   │   │   │       btGImpactBvh.h
│   │   │   │   │       btGImpactCollisionAlgorithm.cpp
│   │   │   │   │       btGImpactCollisionAlgorithm.h
│   │   │   │   │       btGImpactMassUtil.h
│   │   │   │   │       btGImpactQuantizedBvh.cpp
│   │   │   │   │       btGImpactQuantizedBvh.h
│   │   │   │   │       btGImpactShape.cpp
│   │   │   │   │       btGImpactShape.h
│   │   │   │   │       btQuantization.h
│   │   │   │   │       btTriangleShapeEx.cpp
│   │   │   │   │       btTriangleShapeEx.h
│   │   │   │   │       gim_array.h
│   │   │   │   │       gim_basic_geometry_operations.h
│   │   │   │   │       gim_bitset.h
│   │   │   │   │       gim_box_collision.h
│   │   │   │   │       gim_box_set.cpp
│   │   │   │   │       gim_box_set.h
│   │   │   │   │       gim_clip_polygon.h
│   │   │   │   │       gim_contact.cpp
│   │   │   │   │       gim_contact.h
│   │   │   │   │       gim_geometry.h
│   │   │   │   │       gim_geom_types.h
│   │   │   │   │       gim_hash_table.h
│   │   │   │   │       gim_linear_math.h
│   │   │   │   │       gim_math.h
│   │   │   │   │       gim_memory.cpp
│   │   │   │   │       gim_memory.h
│   │   │   │   │       gim_radixsort.h
│   │   │   │   │       gim_tri_collision.cpp
│   │   │   │   │       gim_tri_collision.h
│   │   │   │   │
│   │   │   │   └───NarrowPhaseCollision
│   │   │   │           btContinuousConvexCollision.cpp
│   │   │   │           btContinuousConvexCollision.h
│   │   │   │           btConvexCast.cpp
│   │   │   │           btConvexCast.h
│   │   │   │           btConvexPenetrationDepthSolver.h
│   │   │   │           btDiscreteCollisionDetectorInterface.h
│   │   │   │           btGjkConvexCast.cpp
│   │   │   │           btGjkConvexCast.h
│   │   │   │           btGjkEpa2.cpp
│   │   │   │           btGjkEpa2.h
│   │   │   │           btGjkEpaPenetrationDepthSolver.cpp
│   │   │   │           btGjkEpaPenetrationDepthSolver.h
│   │   │   │           btGjkPairDetector.cpp
│   │   │   │           btGjkPairDetector.h
│   │   │   │           btManifoldPoint.h
│   │   │   │           btMinkowskiPenetrationDepthSolver.cpp
│   │   │   │           btMinkowskiPenetrationDepthSolver.h
│   │   │   │           btPersistentManifold.cpp
│   │   │   │           btPersistentManifold.h
│   │   │   │           btPointCollector.h
│   │   │   │           btPolyhedralContactClipping.cpp
│   │   │   │           btPolyhedralContactClipping.h
│   │   │   │           btRaycastCallback.cpp
│   │   │   │           btRaycastCallback.h
│   │   │   │           btSimplexSolverInterface.h
│   │   │   │           btSubSimplexConvexCast.cpp
│   │   │   │           btSubSimplexConvexCast.h
│   │   │   │           btVoronoiSimplexSolver.cpp
│   │   │   │           btVoronoiSimplexSolver.h
│   │   │   │
│   │   │   ├───BulletDynamics
│   │   │   │   ├───Character
│   │   │   │   │       btCharacterControllerInterface.h
│   │   │   │   │       btKinematicCharacterController.cpp
│   │   │   │   │       btKinematicCharacterController.h
│   │   │   │   │
│   │   │   │   ├───ConstraintSolver
│   │   │   │   │       btConeTwistConstraint.cpp
│   │   │   │   │       btConeTwistConstraint.h
│   │   │   │   │       btConstraintSolver.h
│   │   │   │   │       btContactConstraint.cpp
│   │   │   │   │       btContactConstraint.h
│   │   │   │   │       btContactSolverInfo.h
│   │   │   │   │       btFixedConstraint.cpp
│   │   │   │   │       btFixedConstraint.h
│   │   │   │   │       btGearConstraint.cpp
│   │   │   │   │       btGearConstraint.h
│   │   │   │   │       btGeneric6DofConstraint.cpp
│   │   │   │   │       btGeneric6DofConstraint.h
│   │   │   │   │       btGeneric6DofSpringConstraint.cpp
│   │   │   │   │       btGeneric6DofSpringConstraint.h
│   │   │   │   │       btHinge2Constraint.cpp
│   │   │   │   │       btHinge2Constraint.h
│   │   │   │   │       btHingeConstraint.cpp
│   │   │   │   │       btHingeConstraint.h
│   │   │   │   │       btJacobianEntry.h
│   │   │   │   │       btPoint2PointConstraint.cpp
│   │   │   │   │       btPoint2PointConstraint.h
│   │   │   │   │       btSequentialImpulseConstraintSolver.cpp
│   │   │   │   │       btSequentialImpulseConstraintSolver.h
│   │   │   │   │       btSliderConstraint.cpp
│   │   │   │   │       btSliderConstraint.h
│   │   │   │   │       btSolve2LinearConstraint.cpp
│   │   │   │   │       btSolve2LinearConstraint.h
│   │   │   │   │       btSolverBody.h
│   │   │   │   │       btSolverConstraint.h
│   │   │   │   │       btTypedConstraint.cpp
│   │   │   │   │       btTypedConstraint.h
│   │   │   │   │       btUniversalConstraint.cpp
│   │   │   │   │       btUniversalConstraint.h
│   │   │   │   │
│   │   │   │   ├───Dynamics
│   │   │   │   │       btActionInterface.h
│   │   │   │   │       btDiscreteDynamicsWorld.cpp
│   │   │   │   │       btDiscreteDynamicsWorld.h
│   │   │   │   │       btDynamicsWorld.h
│   │   │   │   │       btRigidBody.cpp
│   │   │   │   │       btRigidBody.h
│   │   │   │   │       btSimpleDynamicsWorld.cpp
│   │   │   │   │       btSimpleDynamicsWorld.h
│   │   │   │   │       Bullet-C-API.cpp
│   │   │   │   │
│   │   │   │   ├───Featherstone
│   │   │   │   │       btMultiBody.cpp
│   │   │   │   │       btMultiBody.h
│   │   │   │   │       btMultiBodyConstraint.cpp
│   │   │   │   │       btMultiBodyConstraint.h
│   │   │   │   │       btMultiBodyConstraintSolver.cpp
│   │   │   │   │       btMultiBodyConstraintSolver.h
│   │   │   │   │       btMultiBodyDynamicsWorld.cpp
│   │   │   │   │       btMultiBodyDynamicsWorld.h
│   │   │   │   │       btMultiBodyJointLimitConstraint.cpp
│   │   │   │   │       btMultiBodyJointLimitConstraint.h
│   │   │   │   │       btMultiBodyJointMotor.cpp
│   │   │   │   │       btMultiBodyJointMotor.h
│   │   │   │   │       btMultiBodyLink.h
│   │   │   │   │       btMultiBodyLinkCollider.h
│   │   │   │   │       btMultiBodyPoint2Point.cpp
│   │   │   │   │       btMultiBodyPoint2Point.h
│   │   │   │   │       btMultiBodySolverConstraint.h
│   │   │   │   │
│   │   │   │   ├───MLCPSolvers
│   │   │   │   │       btDantzigLCP.cpp
│   │   │   │   │       btDantzigLCP.h
│   │   │   │   │       btDantzigSolver.h
│   │   │   │   │       btMLCPSolver.cpp
│   │   │   │   │       btMLCPSolver.h
│   │   │   │   │       btMLCPSolverInterface.h
│   │   │   │   │       btPATHSolver.h
│   │   │   │   │       btSolveProjectedGaussSeidel.h
│   │   │   │   │
│   │   │   │   └───Vehicle
│   │   │   │           btRaycastVehicle.cpp
│   │   │   │           btRaycastVehicle.h
│   │   │   │           btVehicleRaycaster.h
│   │   │   │           btWheelInfo.cpp
│   │   │   │           btWheelInfo.h
│   │   │   │
│   │   │   ├───BulletMultiThreaded
│   │   │   │   │   btGpu3DGridBroadphase.cpp
│   │   │   │   │   btGpu3DGridBroadphase.h
│   │   │   │   │   btGpu3DGridBroadphaseSharedCode.h
│   │   │   │   │   btGpu3DGridBroadphaseSharedDefs.h
│   │   │   │   │   btGpu3DGridBroadphaseSharedTypes.h
│   │   │   │   │   btGpuDefines.h
│   │   │   │   │   btGpuUtilsSharedCode.h
│   │   │   │   │   btGpuUtilsSharedDefs.h
│   │   │   │   │   btParallelConstraintSolver.cpp
│   │   │   │   │   btParallelConstraintSolver.h
│   │   │   │   │   btThreadSupportInterface.cpp
│   │   │   │   │   btThreadSupportInterface.h
│   │   │   │   │   HeapManager.h
│   │   │   │   │   PlatformDefinitions.h
│   │   │   │   │   PosixThreadSupport.cpp
│   │   │   │   │   PosixThreadSupport.h
│   │   │   │   │   PpuAddressSpace.h
│   │   │   │   │   SequentialThreadSupport.cpp
│   │   │   │   │   SequentialThreadSupport.h
│   │   │   │   │   SpuCollisionObjectWrapper.cpp
│   │   │   │   │   SpuCollisionObjectWrapper.h
│   │   │   │   │   SpuCollisionTaskProcess.cpp
│   │   │   │   │   SpuCollisionTaskProcess.h
│   │   │   │   │   SpuContactManifoldCollisionAlgorithm.cpp
│   │   │   │   │   SpuContactManifoldCollisionAlgorithm.h
│   │   │   │   │   SpuDoubleBuffer.h
│   │   │   │   │   SpuFakeDma.cpp
│   │   │   │   │   SpuFakeDma.h
│   │   │   │   │   SpuGatheringCollisionDispatcher.cpp
│   │   │   │   │   SpuGatheringCollisionDispatcher.h
│   │   │   │   │   SpuLibspe2Support.cpp
│   │   │   │   │   SpuLibspe2Support.h
│   │   │   │   │   SpuSampleTaskProcess.cpp
│   │   │   │   │   SpuSampleTaskProcess.h
│   │   │   │   │   SpuSync.h
│   │   │   │   │   TrbDynBody.h
│   │   │   │   │   TrbStateVec.h
│   │   │   │   │   vectormath2bullet.h
│   │   │   │   │   Win32ThreadSupport.cpp
│   │   │   │   │   Win32ThreadSupport.h
│   │   │   │   │
│   │   │   │   ├───GpuSoftBodySolvers
│   │   │   │   │   ├───DX11
│   │   │   │   │   │   │   btSoftBodySolverBuffer_DX11.h
│   │   │   │   │   │   │   btSoftBodySolverLinkData_DX11.h
│   │   │   │   │   │   │   btSoftBodySolverLinkData_DX11SIMDAware.h
│   │   │   │   │   │   │   btSoftBodySolverTriangleData_DX11.h
│   │   │   │   │   │   │   btSoftBodySolverVertexBuffer_DX11.h
│   │   │   │   │   │   │   btSoftBodySolverVertexData_DX11.h
│   │   │   │   │   │   │   btSoftBodySolver_DX11.cpp
│   │   │   │   │   │   │   btSoftBodySolver_DX11.h
│   │   │   │   │   │   │   btSoftBodySolver_DX11SIMDAware.cpp
│   │   │   │   │   │   │   btSoftBodySolver_DX11SIMDAware.h
│   │   │   │   │   │   │
│   │   │   │   │   │   └───HLSL
│   │   │   │   │   │           ApplyForces.hlsl
│   │   │   │   │   │           ComputeBounds.hlsl
│   │   │   │   │   │           Integrate.hlsl
│   │   │   │   │   │           OutputToVertexArray.hlsl
│   │   │   │   │   │           PrepareLinks.hlsl
│   │   │   │   │   │           solveCollisionsAndUpdateVelocities.hlsl
│   │   │   │   │   │           solveCollisionsAndUpdateVelocitiesSIMDBatched.hlsl
│   │   │   │   │   │           SolvePositions.hlsl
│   │   │   │   │   │           SolvePositionsSIMDBatched.hlsl
│   │   │   │   │   │           UpdateConstants.hlsl
│   │   │   │   │   │           UpdateNodes.hlsl
│   │   │   │   │   │           UpdateNormals.hlsl
│   │   │   │   │   │           UpdatePositions.hlsl
│   │   │   │   │   │           UpdatePositionsFromVelocities.hlsl
│   │   │   │   │   │           VSolveLinks.hlsl
│   │   │   │   │   │
│   │   │   │   │   ├───OpenCL
│   │   │   │   │   │   │   btSoftBodySolverBuffer_OpenCL.h
│   │   │   │   │   │   │   btSoftBodySolverLinkData_OpenCL.h
│   │   │   │   │   │   │   btSoftBodySolverLinkData_OpenCLSIMDAware.h
│   │   │   │   │   │   │   btSoftBodySolverOutputCLtoGL.cpp
│   │   │   │   │   │   │   btSoftBodySolverOutputCLtoGL.h
│   │   │   │   │   │   │   btSoftBodySolverTriangleData_OpenCL.h
│   │   │   │   │   │   │   btSoftBodySolverVertexBuffer_OpenGL.h
│   │   │   │   │   │   │   btSoftBodySolverVertexData_OpenCL.h
│   │   │   │   │   │   │   btSoftBodySolver_OpenCL.cpp
│   │   │   │   │   │   │   btSoftBodySolver_OpenCL.h
│   │   │   │   │   │   │   btSoftBodySolver_OpenCLSIMDAware.cpp
│   │   │   │   │   │   │   btSoftBodySolver_OpenCLSIMDAware.h
│   │   │   │   │   │   │
│   │   │   │   │   │   ├───MiniCL
│   │   │   │   │   │   │       MiniCLTaskWrap.cpp
│   │   │   │   │   │   │
│   │   │   │   │   │   └───OpenCLC10
│   │   │   │   │   │           ApplyForces.cl
│   │   │   │   │   │           ComputeBounds.cl
│   │   │   │   │   │           Integrate.cl
│   │   │   │   │   │           OutputToVertexArray.cl
│   │   │   │   │   │           PrepareLinks.cl
│   │   │   │   │   │           SolveCollisionsAndUpdateVelocities.cl
│   │   │   │   │   │           SolveCollisionsAndUpdateVelocitiesSIMDBatched.cl
│   │   │   │   │   │           SolvePositions.cl
│   │   │   │   │   │           SolvePositionsSIMDBatched.cl
│   │   │   │   │   │           UpdateConstants.cl
│   │   │   │   │   │           UpdateFixedVertexPositions.cl
│   │   │   │   │   │           UpdateNodes.cl
│   │   │   │   │   │           UpdateNormals.cl
│   │   │   │   │   │           UpdatePositions.cl
│   │   │   │   │   │           UpdatePositionsFromVelocities.cl
│   │   │   │   │   │           VSolveLinks.cl
│   │   │   │   │   │
│   │   │   │   │   └───Shared
│   │   │   │   │           btSoftBodySolverData.h
│   │   │   │   │
│   │   │   │   ├───SpuNarrowPhaseCollisionTask
│   │   │   │   │       Box.h
│   │   │   │   │       boxBoxDistance.cpp
│   │   │   │   │       boxBoxDistance.h
│   │   │   │   │       SpuCollisionShapes.cpp
│   │   │   │   │       SpuCollisionShapes.h
│   │   │   │   │       SpuContactResult.cpp
│   │   │   │   │       SpuContactResult.h
│   │   │   │   │       SpuConvexPenetrationDepthSolver.h
│   │   │   │   │       SpuGatheringCollisionTask.cpp
│   │   │   │   │       SpuGatheringCollisionTask.h
│   │   │   │   │       SpuLocalSupport.h
│   │   │   │   │       SpuMinkowskiPenetrationDepthSolver.cpp
│   │   │   │   │       SpuMinkowskiPenetrationDepthSolver.h
│   │   │   │   │       SpuPreferredPenetrationDirections.h
│   │   │   │   │
│   │   │   │   └───SpuSampleTask
│   │   │   │           SpuSampleTask.cpp
│   │   │   │           SpuSampleTask.h
│   │   │   │
│   │   │   ├───BulletSoftBody
│   │   │   │       btDefaultSoftBodySolver.cpp
│   │   │   │       btDefaultSoftBodySolver.h
│   │   │   │       btSoftBody.cpp
│   │   │   │       btSoftBody.h
│   │   │   │       btSoftBodyConcaveCollisionAlgorithm.cpp
│   │   │   │       btSoftBodyConcaveCollisionAlgorithm.h
│   │   │   │       btSoftBodyData.h
│   │   │   │       btSoftBodyHelpers.cpp
│   │   │   │       btSoftBodyHelpers.h
│   │   │   │       btSoftBodyInternals.h
│   │   │   │       btSoftBodyRigidBodyCollisionConfiguration.cpp
│   │   │   │       btSoftBodyRigidBodyCollisionConfiguration.h
│   │   │   │       btSoftBodySolvers.h
│   │   │   │       btSoftBodySolverVertexBuffer.h
│   │   │   │       btSoftRigidCollisionAlgorithm.cpp
│   │   │   │       btSoftRigidCollisionAlgorithm.h
│   │   │   │       btSoftRigidDynamicsWorld.cpp
│   │   │   │       btSoftRigidDynamicsWorld.h
│   │   │   │       btSoftSoftCollisionAlgorithm.cpp
│   │   │   │       btSoftSoftCollisionAlgorithm.h
│   │   │   │       btSparseSDF.h
│   │   │   │
│   │   │   ├───LinearMath
│   │   │   │       btAabbUtil2.h
│   │   │   │       btAlignedAllocator.cpp
│   │   │   │       btAlignedAllocator.h
│   │   │   │       btAlignedObjectArray.h
│   │   │   │       btConvexHull.cpp
│   │   │   │       btConvexHull.h
│   │   │   │       btConvexHullComputer.cpp
│   │   │   │       btConvexHullComputer.h
│   │   │   │       btDefaultMotionState.h
│   │   │   │       btGeometryUtil.cpp
│   │   │   │       btGeometryUtil.h
│   │   │   │       btGrahamScan2dConvexHull.h
│   │   │   │       btHashMap.h
│   │   │   │       btIDebugDraw.h
│   │   │   │       btList.h
│   │   │   │       btMatrix3x3.h
│   │   │   │       btMatrixX.h
│   │   │   │       btMinMax.h
│   │   │   │       btMotionState.h
│   │   │   │       btPolarDecomposition.cpp
│   │   │   │       btPolarDecomposition.h
│   │   │   │       btPoolAllocator.h
│   │   │   │       btQuadWord.h
│   │   │   │       btQuaternion.h
│   │   │   │       btQuickprof.cpp
│   │   │   │       btQuickprof.h
│   │   │   │       btRandom.h
│   │   │   │       btScalar.h
│   │   │   │       btSerializer.cpp
│   │   │   │       btSerializer.h
│   │   │   │       btStackAlloc.h
│   │   │   │       btTransform.h
│   │   │   │       btTransformUtil.h
│   │   │   │       btVector3.cpp
│   │   │   │       btVector3.h
│   │   │   │
│   │   │   ├───MiniCL
│   │   │   │   │   cl.h
│   │   │   │   │   cl_gl.h
│   │   │   │   │   cl_MiniCL_Defs.h
│   │   │   │   │   cl_platform.h
│   │   │   │   │   MiniCL.cpp
│   │   │   │   │   MiniCLTaskScheduler.cpp
│   │   │   │   │   MiniCLTaskScheduler.h
│   │   │   │   │
│   │   │   │   └───MiniCLTask
│   │   │   │           MiniCLTask.cpp
│   │   │   │           MiniCLTask.h
│   │   │   │
│   │   │   ├───proj.win10
│   │   │   │       libbullet.vcxproj
│   │   │   │       libbullet.vcxproj.filters
│   │   │   │
│   │   │   ├───proj.win32
│   │   │   │       libbullet.vcxproj
│   │   │   │       libbullet.vcxproj.filters
│   │   │   │
│   │   │   ├───proj.win8.1-universal
│   │   │   │   ├───libbullet.Shared
│   │   │   │   │       libbullet.Shared.vcxitems
│   │   │   │   │       libbullet.Shared.vcxitems.filters
│   │   │   │   │
│   │   │   │   ├───libbullet.Windows
│   │   │   │   │       libbullet.Windows.vcxproj
│   │   │   │   │       libbullet.Windows.vcxproj.filters
│   │   │   │   │
│   │   │   │   └───libbullet.WindowsPhone
│   │   │   │           libbullet.WindowsPhone.vcxproj
│   │   │   │           libbullet.WindowsPhone.vcxproj.filters
│   │   │   │
│   │   │   └───vectormath
│   │   │       │   vmInclude.h
│   │   │       │
│   │   │       ├───neon
│   │   │       │       boolInVec.h
│   │   │       │       floatInVec.h
│   │   │       │       mat_aos.h
│   │   │       │       quat_aos.h
│   │   │       │       vectormath_aos.h
│   │   │       │       vec_aos.h
│   │   │       │
│   │   │       ├───scalar
│   │   │       │       boolInVec.h
│   │   │       │       floatInVec.h
│   │   │       │       mat_aos.h
│   │   │       │       quat_aos.h
│   │   │       │       vectormath_aos.h
│   │   │       │       vec_aos.h
│   │   │       │
│   │   │       └───sse
│   │   │               boolInVec.h
│   │   │               floatInVec.h
│   │   │               mat_aos.h
│   │   │               quat_aos.h
│   │   │               vecidx_aos.h
│   │   │               vectormath_aos.h
│   │   │               vec_aos.h
│   │   │
│   │   ├───chipmunk
│   │   │   ├───include
│   │   │   │   └───chipmunk
│   │   │   │           chipmunk.h
│   │   │   │           chipmunk_ffi.h
│   │   │   │           chipmunk_private.h
│   │   │   │           chipmunk_types.h
│   │   │   │           chipmunk_unsafe.h
│   │   │   │           cpArbiter.h
│   │   │   │           cpBB.h
│   │   │   │           cpBody.h
│   │   │   │           cpConstraint.h
│   │   │   │           cpDampedRotarySpring.h
│   │   │   │           cpDampedSpring.h
│   │   │   │           cpGearJoint.h
│   │   │   │           cpGrooveJoint.h
│   │   │   │           cpHastySpace.h
│   │   │   │           cpMarch.h
│   │   │   │           cpPinJoint.h
│   │   │   │           cpPivotJoint.h
│   │   │   │           cpPolyline.h
│   │   │   │           cpPolyShape.h
│   │   │   │           cpRatchetJoint.h
│   │   │   │           cpRobust.h
│   │   │   │           cpRotaryLimitJoint.h
│   │   │   │           cpShape.h
│   │   │   │           cpSimpleMotor.h
│   │   │   │           cpSlideJoint.h
│   │   │   │           cpSpace.h
│   │   │   │           cpSpatialIndex.h
│   │   │   │           cpTransform.h
│   │   │   │           cpVect.h
│   │   │   │
│   │   │   └───prebuilt
│   │   │       ├───android
│   │   │       │   │   Android.mk
│   │   │       │   │
│   │   │       │   ├───arm64-v8a
│   │   │       │   │       libchipmunk.a
│   │   │       │   │
│   │   │       │   ├───armeabi
│   │   │       │   │       libchipmunk.a
│   │   │       │   │
│   │   │       │   ├───armeabi-v7a
│   │   │       │   │       libchipmunk.a
│   │   │       │   │
│   │   │       │   └───x86
│   │   │       │           libchipmunk.a
│   │   │       │
│   │   │       ├───ios
│   │   │       │       libchipmunk.a
│   │   │       │
│   │   │       ├───linux
│   │   │       │   └───64-bit
│   │   │       │           libchipmunk.a
│   │   │       │
│   │   │       ├───mac
│   │   │       │       libchipmunk.a
│   │   │       │
│   │   │       ├───tizen
│   │   │       │   ├───arm
│   │   │       │   │       libchipmunk.a
│   │   │       │   │
│   │   │       │   └───x86
│   │   │       │           libchipmunk.a
│   │   │       │
│   │   │       ├───win10
│   │   │       │   ├───arm
│   │   │       │   │       chipmunk.lib
│   │   │       │   │
│   │   │       │   ├───win32
│   │   │       │   │       chipmunk.lib
│   │   │       │   │
│   │   │       │   └───x64
│   │   │       │           chipmunk.lib
│   │   │       │
│   │   │       ├───win32
│   │   │       │   ├───debug-lib
│   │   │       │   │       libchipmunk-2015.lib
│   │   │       │   │       libchipmunk.lib
│   │   │       │   │
│   │   │       │   └───release-lib
│   │   │       │           libchipmunk-2015.lib
│   │   │       │           libchipmunk.lib
│   │   │       │
│   │   │       ├───winrt_8.1
│   │   │       │   ├───arm
│   │   │       │   │       chipmunk.lib
│   │   │       │   │
│   │   │       │   └───win32
│   │   │       │           chipmunk.lib
│   │   │       │
│   │   │       └───wp_8.1
│   │   │           ├───arm
│   │   │           │       chipmunk.lib
│   │   │           │
│   │   │           └───win32
│   │   │                   chipmunk.lib
│   │   │
│   │   ├───clipper
│   │   │       clipper.cpp
│   │   │       clipper.hpp
│   │   │
│   │   ├───ConvertUTF
│   │   │       ConvertUTF.c
│   │   │       ConvertUTF.h
│   │   │       ConvertUTFWrapper.cpp
│   │   │
│   │   ├───curl
│   │   │   ├───include
│   │   │   │   ├───android
│   │   │   │   │   └───curl
│   │   │   │   │           curl.h
│   │   │   │   │           curlbuild-32.h
│   │   │   │   │           curlbuild-64.h
│   │   │   │   │           curlbuild.h
│   │   │   │   │           curlrules.h
│   │   │   │   │           curlver.h
│   │   │   │   │           easy.h
│   │   │   │   │           mprintf.h
│   │   │   │   │           multi.h
│   │   │   │   │           stdcheaders.h
│   │   │   │   │           typecheck-gcc.h
│   │   │   │   │
│   │   │   │   ├───ios
│   │   │   │   │   └───curl
│   │   │   │   │           curl.h
│   │   │   │   │           curlbuild-32.h
│   │   │   │   │           curlbuild-64.h
│   │   │   │   │           curlbuild.h
│   │   │   │   │           curlrules.h
│   │   │   │   │           curlver.h
│   │   │   │   │           easy.h
│   │   │   │   │           mprintf.h
│   │   │   │   │           multi.h
│   │   │   │   │           stdcheaders.h
│   │   │   │   │           typecheck-gcc.h
│   │   │   │   │
│   │   │   │   ├───mac
│   │   │   │   │   └───curl
│   │   │   │   │           curl.h
│   │   │   │   │           curlbuild.h
│   │   │   │   │           curlrules.h
│   │   │   │   │           curlver.h
│   │   │   │   │           easy.h
│   │   │   │   │           mprintf.h
│   │   │   │   │           multi.h
│   │   │   │   │           stdcheaders.h
│   │   │   │   │           typecheck-gcc.h
│   │   │   │   │
│   │   │   │   ├───win10
│   │   │   │   │   └───curl
│   │   │   │   │           curl.h
│   │   │   │   │           curlbuild.h
│   │   │   │   │           curlrules.h
│   │   │   │   │           curlver.h
│   │   │   │   │           easy.h
│   │   │   │   │           mprintf.h
│   │   │   │   │           multi.h
│   │   │   │   │           stdcheaders.h
│   │   │   │   │           typecheck-gcc.h
│   │   │   │   │
│   │   │   │   ├───win32
│   │   │   │   │   └───curl
│   │   │   │   │           curl.h
│   │   │   │   │           curlbuild.h
│   │   │   │   │           curlrules.h
│   │   │   │   │           curlver.h
│   │   │   │   │           easy.h
│   │   │   │   │           mprintf.h
│   │   │   │   │           multi.h
│   │   │   │   │           stdcheaders.h
│   │   │   │   │           typecheck-gcc.h
│   │   │   │   │
│   │   │   │   ├───winrt_8.1
│   │   │   │   │   └───curl
│   │   │   │   │           curl.h
│   │   │   │   │           curlbuild.h
│   │   │   │   │           curlrules.h
│   │   │   │   │           curlver.h
│   │   │   │   │           easy.h
│   │   │   │   │           mprintf.h
│   │   │   │   │           multi.h
│   │   │   │   │           stdcheaders.h
│   │   │   │   │           typecheck-gcc.h
│   │   │   │   │
│   │   │   │   └───wp_8.1
│   │   │   │       └───curl
│   │   │   │               curl.h
│   │   │   │               curlbuild.h
│   │   │   │               curlrules.h
│   │   │   │               curlver.h
│   │   │   │               easy.h
│   │   │   │               mprintf.h
│   │   │   │               multi.h
│   │   │   │               stdcheaders.h
│   │   │   │               typecheck-gcc.h
│   │   │   │
│   │   │   └───prebuilt
│   │   │       ├───android
│   │   │       │   │   Android.mk
│   │   │       │   │
│   │   │       │   ├───arm64-v8a
│   │   │       │   │       libcrypto.a
│   │   │       │   │       libcurl.a
│   │   │       │   │       libssl.a
│   │   │       │   │
│   │   │       │   ├───armeabi
│   │   │       │   │       libcrypto.a
│   │   │       │   │       libcurl.a
│   │   │       │   │       libssl.a
│   │   │       │   │
│   │   │       │   ├───armeabi-v7a
│   │   │       │   │       libcrypto.a
│   │   │       │   │       libcurl.a
│   │   │       │   │       libssl.a
│   │   │       │   │
│   │   │       │   └───x86
│   │   │       │           libcrypto.a
│   │   │       │           libcurl.a
│   │   │       │           libssl.a
│   │   │       │
│   │   │       ├───ios
│   │   │       │       libcrypto.a
│   │   │       │       libcurl.a
│   │   │       │       libssl.a
│   │   │       │
│   │   │       ├───mac
│   │   │       │       libcrypto.a
│   │   │       │       libcurl.a
│   │   │       │       libssl.a
│   │   │       │
│   │   │       ├───win10
│   │   │       │   ├───arm
│   │   │       │   │       libcurl.dll
│   │   │       │   │       libcurl.lib
│   │   │       │   │       libeay32.dll
│   │   │       │   │       ssleay32.dll
│   │   │       │   │
│   │   │       │   ├───win32
│   │   │       │   │       libcurl.dll
│   │   │       │   │       libcurl.lib
│   │   │       │   │       libeay32.dll
│   │   │       │   │       ssleay32.dll
│   │   │       │   │
│   │   │       │   └───x64
│   │   │       │           libcurl.dll
│   │   │       │           libcurl.lib
│   │   │       │           libeay32.dll
│   │   │       │           ssleay32.dll
│   │   │       │
│   │   │       ├───win32
│   │   │       │       libcurl.dll
│   │   │       │       libcurl_imp.lib
│   │   │       │       libeay32.lib
│   │   │       │       ssleay32.lib
│   │   │       │
│   │   │       ├───winrt_8.1
│   │   │       │   ├───arm
│   │   │       │   │       libcurl.dll
│   │   │       │   │       libcurl.lib
│   │   │       │   │       libeay32.dll
│   │   │       │   │       ssleay32.dll
│   │   │       │   │
│   │   │       │   └───win32
│   │   │       │           libcurl.dll
│   │   │       │           libcurl.lib
│   │   │       │           libeay32.dll
│   │   │       │           ssleay32.dll
│   │   │       │
│   │   │       └───wp_8.1
│   │   │           ├───arm
│   │   │           │       libcurl.dll
│   │   │           │       libcurl.lib
│   │   │           │       libeay32.dll
│   │   │           │       libeay32.lib
│   │   │           │       ssleay32.dll
│   │   │           │       ssleay32.lib
│   │   │           │
│   │   │           └───win32
│   │   │                   libcurl.dll
│   │   │                   libcurl.lib
│   │   │                   libeay32.dll
│   │   │                   libeay32.lib
│   │   │                   ssleay32.dll
│   │   │                   ssleay32.lib
│   │   │
│   │   ├───edtaa3func
│   │   │       edtaa3func.cpp
│   │   │       edtaa3func.h
│   │   │
│   │   ├───flatbuffers
│   │   │       Android.mk
│   │   │       CMakeLists.txt
│   │   │       flatbuffers.h
│   │   │       flatc.cpp
│   │   │       idl.h
│   │   │       idl_gen_cpp.cpp
│   │   │       idl_gen_fbs.cpp
│   │   │       idl_gen_general.cpp
│   │   │       idl_gen_go.cpp
│   │   │       idl_gen_text.cpp
│   │   │       idl_parser.cpp
│   │   │       util.h
│   │   │
│   │   ├───freetype2
│   │   │   ├───include
│   │   │   │   ├───android
│   │   │   │   │   └───freetype2
│   │   │   │   │       │   freetype.h
│   │   │   │   │       │   ft2build.h
│   │   │   │   │       │   ftadvanc.h
│   │   │   │   │       │   ftautoh.h
│   │   │   │   │       │   ftbbox.h
│   │   │   │   │       │   ftbdf.h
│   │   │   │   │       │   ftbitmap.h
│   │   │   │   │       │   ftbzip2.h
│   │   │   │   │       │   ftcache.h
│   │   │   │   │       │   ftcffdrv.h
│   │   │   │   │       │   ftchapters.h
│   │   │   │   │       │   ftcid.h
│   │   │   │   │       │   fterrdef.h
│   │   │   │   │       │   fterrors.h
│   │   │   │   │       │   ftgasp.h
│   │   │   │   │       │   ftglyph.h
│   │   │   │   │       │   ftgxval.h
│   │   │   │   │       │   ftgzip.h
│   │   │   │   │       │   ftimage.h
│   │   │   │   │       │   ftincrem.h
│   │   │   │   │       │   ftlcdfil.h
│   │   │   │   │       │   ftlist.h
│   │   │   │   │       │   ftlzw.h
│   │   │   │   │       │   ftmac.h
│   │   │   │   │       │   ftmm.h
│   │   │   │   │       │   ftmodapi.h
│   │   │   │   │       │   ftmoderr.h
│   │   │   │   │       │   ftotval.h
│   │   │   │   │       │   ftoutln.h
│   │   │   │   │       │   ftpfr.h
│   │   │   │   │       │   ftrender.h
│   │   │   │   │       │   ftsizes.h
│   │   │   │   │       │   ftsnames.h
│   │   │   │   │       │   ftstroke.h
│   │   │   │   │       │   ftsynth.h
│   │   │   │   │       │   ftsystem.h
│   │   │   │   │       │   fttrigon.h
│   │   │   │   │       │   ftttdrv.h
│   │   │   │   │       │   fttypes.h
│   │   │   │   │       │   ftwinfnt.h
│   │   │   │   │       │   ftxf86.h
│   │   │   │   │       │   t1tables.h
│   │   │   │   │       │   ttnameid.h
│   │   │   │   │       │   tttables.h
│   │   │   │   │       │   tttags.h
│   │   │   │   │       │   ttunpat.h
│   │   │   │   │       │
│   │   │   │   │       └───config
│   │   │   │   │               ftconfig.h
│   │   │   │   │               ftheader.h
│   │   │   │   │               ftmodule.h
│   │   │   │   │               ftoption.h
│   │   │   │   │               ftstdlib.h
│   │   │   │   │
│   │   │   │   ├───ios
│   │   │   │   │   └───freetype2
│   │   │   │   │       │   freetype.h
│   │   │   │   │       │   ft2build.h
│   │   │   │   │       │   ftadvanc.h
│   │   │   │   │       │   ftautoh.h
│   │   │   │   │       │   ftbbox.h
│   │   │   │   │       │   ftbdf.h
│   │   │   │   │       │   ftbitmap.h
│   │   │   │   │       │   ftbzip2.h
│   │   │   │   │       │   ftcache.h
│   │   │   │   │       │   ftcffdrv.h
│   │   │   │   │       │   ftchapters.h
│   │   │   │   │       │   ftcid.h
│   │   │   │   │       │   fterrdef.h
│   │   │   │   │       │   fterrors.h
│   │   │   │   │       │   ftgasp.h
│   │   │   │   │       │   ftglyph.h
│   │   │   │   │       │   ftgxval.h
│   │   │   │   │       │   ftgzip.h
│   │   │   │   │       │   ftimage.h
│   │   │   │   │       │   ftincrem.h
│   │   │   │   │       │   ftlcdfil.h
│   │   │   │   │       │   ftlist.h
│   │   │   │   │       │   ftlzw.h
│   │   │   │   │       │   ftmac.h
│   │   │   │   │       │   ftmm.h
│   │   │   │   │       │   ftmodapi.h
│   │   │   │   │       │   ftmoderr.h
│   │   │   │   │       │   ftotval.h
│   │   │   │   │       │   ftoutln.h
│   │   │   │   │       │   ftpfr.h
│   │   │   │   │       │   ftrender.h
│   │   │   │   │       │   ftsizes.h
│   │   │   │   │       │   ftsnames.h
│   │   │   │   │       │   ftstroke.h
│   │   │   │   │       │   ftsynth.h
│   │   │   │   │       │   ftsystem.h
│   │   │   │   │       │   fttrigon.h
│   │   │   │   │       │   ftttdrv.h
│   │   │   │   │       │   fttypes.h
│   │   │   │   │       │   ftwinfnt.h
│   │   │   │   │       │   ftxf86.h
│   │   │   │   │       │   t1tables.h
│   │   │   │   │       │   ttnameid.h
│   │   │   │   │       │   tttables.h
│   │   │   │   │       │   tttags.h
│   │   │   │   │       │   ttunpat.h
│   │   │   │   │       │
│   │   │   │   │       └───config
│   │   │   │   │               ftconfig.h
│   │   │   │   │               ftheader.h
│   │   │   │   │               ftmodule.h
│   │   │   │   │               ftoption.h
│   │   │   │   │               ftstdlib.h
│   │   │   │   │
│   │   │   │   ├───linux
│   │   │   │   │   │   ft2build.h
│   │   │   │   │   │
│   │   │   │   │   └───freetype
│   │   │   │   │       │   freetype.h
│   │   │   │   │       │   ftadvanc.h
│   │   │   │   │       │   ftautoh.h
│   │   │   │   │       │   ftbbox.h
│   │   │   │   │       │   ftbdf.h
│   │   │   │   │       │   ftbitmap.h
│   │   │   │   │       │   ftbzip2.h
│   │   │   │   │       │   ftcache.h
│   │   │   │   │       │   ftcffdrv.h
│   │   │   │   │       │   ftchapters.h
│   │   │   │   │       │   ftcid.h
│   │   │   │   │       │   fterrdef.h
│   │   │   │   │       │   fterrors.h
│   │   │   │   │       │   ftgasp.h
│   │   │   │   │       │   ftglyph.h
│   │   │   │   │       │   ftgxval.h
│   │   │   │   │       │   ftgzip.h
│   │   │   │   │       │   ftimage.h
│   │   │   │   │       │   ftincrem.h
│   │   │   │   │       │   ftlcdfil.h
│   │   │   │   │       │   ftlist.h
│   │   │   │   │       │   ftlzw.h
│   │   │   │   │       │   ftmac.h
│   │   │   │   │       │   ftmm.h
│   │   │   │   │       │   ftmodapi.h
│   │   │   │   │       │   ftmoderr.h
│   │   │   │   │       │   ftotval.h
│   │   │   │   │       │   ftoutln.h
│   │   │   │   │       │   ftpfr.h
│   │   │   │   │       │   ftrender.h
│   │   │   │   │       │   ftsizes.h
│   │   │   │   │       │   ftsnames.h
│   │   │   │   │       │   ftstroke.h
│   │   │   │   │       │   ftsynth.h
│   │   │   │   │       │   ftsystem.h
│   │   │   │   │       │   fttrigon.h
│   │   │   │   │       │   ftttdrv.h
│   │   │   │   │       │   fttypes.h
│   │   │   │   │       │   ftwinfnt.h
│   │   │   │   │       │   ftxf86.h
│   │   │   │   │       │   t1tables.h
│   │   │   │   │       │   ttnameid.h
│   │   │   │   │       │   tttables.h
│   │   │   │   │       │   tttags.h
│   │   │   │   │       │   ttunpat.h
│   │   │   │   │       │
│   │   │   │   │       └───config
│   │   │   │   │               ftconfig.h
│   │   │   │   │               ftheader.h
│   │   │   │   │               ftmodule.h
│   │   │   │   │               ftoption.h
│   │   │   │   │               ftstdlib.h
│   │   │   │   │
│   │   │   │   ├───mac
│   │   │   │   │   └───freetype2
│   │   │   │   │       │   freetype.h
│   │   │   │   │       │   ft2build.h
│   │   │   │   │       │   ftadvanc.h
│   │   │   │   │       │   ftautoh.h
│   │   │   │   │       │   ftbbox.h
│   │   │   │   │       │   ftbdf.h
│   │   │   │   │       │   ftbitmap.h
│   │   │   │   │       │   ftbzip2.h
│   │   │   │   │       │   ftcache.h
│   │   │   │   │       │   ftcffdrv.h
│   │   │   │   │       │   ftchapters.h
│   │   │   │   │       │   ftcid.h
│   │   │   │   │       │   fterrdef.h
│   │   │   │   │       │   fterrors.h
│   │   │   │   │       │   ftgasp.h
│   │   │   │   │       │   ftglyph.h
│   │   │   │   │       │   ftgxval.h
│   │   │   │   │       │   ftgzip.h
│   │   │   │   │       │   ftimage.h
│   │   │   │   │       │   ftincrem.h
│   │   │   │   │       │   ftlcdfil.h
│   │   │   │   │       │   ftlist.h
│   │   │   │   │       │   ftlzw.h
│   │   │   │   │       │   ftmac.h
│   │   │   │   │       │   ftmm.h
│   │   │   │   │       │   ftmodapi.h
│   │   │   │   │       │   ftmoderr.h
│   │   │   │   │       │   ftotval.h
│   │   │   │   │       │   ftoutln.h
│   │   │   │   │       │   ftpfr.h
│   │   │   │   │       │   ftrender.h
│   │   │   │   │       │   ftsizes.h
│   │   │   │   │       │   ftsnames.h
│   │   │   │   │       │   ftstroke.h
│   │   │   │   │       │   ftsynth.h
│   │   │   │   │       │   ftsystem.h
│   │   │   │   │       │   fttrigon.h
│   │   │   │   │       │   ftttdrv.h
│   │   │   │   │       │   fttypes.h
│   │   │   │   │       │   ftwinfnt.h
│   │   │   │   │       │   ftxf86.h
│   │   │   │   │       │   t1tables.h
│   │   │   │   │       │   ttnameid.h
│   │   │   │   │       │   tttables.h
│   │   │   │   │       │   tttags.h
│   │   │   │   │       │   ttunpat.h
│   │   │   │   │       │
│   │   │   │   │       └───config
│   │   │   │   │               ftconfig.h
│   │   │   │   │               ftheader.h
│   │   │   │   │               ftmodule.h
│   │   │   │   │               ftoption.h
│   │   │   │   │               ftstdlib.h
│   │   │   │   │
│   │   │   │   ├───win10
│   │   │   │   │   └───freetype2
│   │   │   │   │       │   freetype.h
│   │   │   │   │       │   ft2build.h
│   │   │   │   │       │   ftadvanc.h
│   │   │   │   │       │   ftautoh.h
│   │   │   │   │       │   ftbbox.h
│   │   │   │   │       │   ftbdf.h
│   │   │   │   │       │   ftbitmap.h
│   │   │   │   │       │   ftbzip2.h
│   │   │   │   │       │   ftcache.h
│   │   │   │   │       │   ftcffdrv.h
│   │   │   │   │       │   ftchapters.h
│   │   │   │   │       │   ftcid.h
│   │   │   │   │       │   fterrdef.h
│   │   │   │   │       │   fterrors.h
│   │   │   │   │       │   ftgasp.h
│   │   │   │   │       │   ftglyph.h
│   │   │   │   │       │   ftgxval.h
│   │   │   │   │       │   ftgzip.h
│   │   │   │   │       │   ftimage.h
│   │   │   │   │       │   ftincrem.h
│   │   │   │   │       │   ftlcdfil.h
│   │   │   │   │       │   ftlist.h
│   │   │   │   │       │   ftlzw.h
│   │   │   │   │       │   ftmac.h
│   │   │   │   │       │   ftmm.h
│   │   │   │   │       │   ftmodapi.h
│   │   │   │   │       │   ftmoderr.h
│   │   │   │   │       │   ftotval.h
│   │   │   │   │       │   ftoutln.h
│   │   │   │   │       │   ftpfr.h
│   │   │   │   │       │   ftrender.h
│   │   │   │   │       │   ftsizes.h
│   │   │   │   │       │   ftsnames.h
│   │   │   │   │       │   ftstroke.h
│   │   │   │   │       │   ftsynth.h
│   │   │   │   │       │   ftsystem.h
│   │   │   │   │       │   fttrigon.h
│   │   │   │   │       │   ftttdrv.h
│   │   │   │   │       │   fttypes.h
│   │   │   │   │       │   ftwinfnt.h
│   │   │   │   │       │   ftxf86.h
│   │   │   │   │       │   t1tables.h
│   │   │   │   │       │   ttnameid.h
│   │   │   │   │       │   tttables.h
│   │   │   │   │       │   tttags.h
│   │   │   │   │       │   ttunpat.h
│   │   │   │   │       │
│   │   │   │   │       └───config
│   │   │   │   │               ftconfig.h
│   │   │   │   │               ftheader.h
│   │   │   │   │               ftmodule.h
│   │   │   │   │               ftoption.h
│   │   │   │   │               ftstdlib.h
│   │   │   │   │
│   │   │   │   ├───win32
│   │   │   │   │   └───freetype2
│   │   │   │   │       │   freetype.h
│   │   │   │   │       │   ft2build.h
│   │   │   │   │       │   ftadvanc.h
│   │   │   │   │       │   ftautoh.h
│   │   │   │   │       │   ftbbox.h
│   │   │   │   │       │   ftbdf.h
│   │   │   │   │       │   ftbitmap.h
│   │   │   │   │       │   ftbzip2.h
│   │   │   │   │       │   ftcache.h
│   │   │   │   │       │   ftcffdrv.h
│   │   │   │   │       │   ftchapters.h
│   │   │   │   │       │   ftcid.h
│   │   │   │   │       │   fterrdef.h
│   │   │   │   │       │   fterrors.h
│   │   │   │   │       │   ftgasp.h
│   │   │   │   │       │   ftglyph.h
│   │   │   │   │       │   ftgxval.h
│   │   │   │   │       │   ftgzip.h
│   │   │   │   │       │   ftimage.h
│   │   │   │   │       │   ftincrem.h
│   │   │   │   │       │   ftlcdfil.h
│   │   │   │   │       │   ftlist.h
│   │   │   │   │       │   ftlzw.h
│   │   │   │   │       │   ftmac.h
│   │   │   │   │       │   ftmm.h
│   │   │   │   │       │   ftmodapi.h
│   │   │   │   │       │   ftmoderr.h
│   │   │   │   │       │   ftotval.h
│   │   │   │   │       │   ftoutln.h
│   │   │   │   │       │   ftpfr.h
│   │   │   │   │       │   ftrender.h
│   │   │   │   │       │   ftsizes.h
│   │   │   │   │       │   ftsnames.h
│   │   │   │   │       │   ftstroke.h
│   │   │   │   │       │   ftsynth.h
│   │   │   │   │       │   ftsystem.h
│   │   │   │   │       │   fttrigon.h
│   │   │   │   │       │   ftttdrv.h
│   │   │   │   │       │   fttypes.h
│   │   │   │   │       │   ftwinfnt.h
│   │   │   │   │       │   ftxf86.h
│   │   │   │   │       │   t1tables.h
│   │   │   │   │       │   ttnameid.h
│   │   │   │   │       │   tttables.h
│   │   │   │   │       │   tttags.h
│   │   │   │   │       │   ttunpat.h
│   │   │   │   │       │
│   │   │   │   │       ├───config
│   │   │   │   │       │       ftconfig.h
│   │   │   │   │       │       ftheader.h
│   │   │   │   │       │       ftmodule.h
│   │   │   │   │       │       ftoption.h
│   │   │   │   │       │       ftstdlib.h
│   │   │   │   │       │
│   │   │   │   │       └───internal
│   │   │   │   │           │   autohint.h
│   │   │   │   │           │   ftcalc.h
│   │   │   │   │           │   ftdebug.h
│   │   │   │   │           │   ftdriver.h
│   │   │   │   │           │   ftgloadr.h
│   │   │   │   │           │   ftmemory.h
│   │   │   │   │           │   ftobjs.h
│   │   │   │   │           │   ftpic.h
│   │   │   │   │           │   ftrfork.h
│   │   │   │   │           │   ftserv.h
│   │   │   │   │           │   ftstream.h
│   │   │   │   │           │   fttrace.h
│   │   │   │   │           │   ftvalid.h
│   │   │   │   │           │   internal.h
│   │   │   │   │           │   psaux.h
│   │   │   │   │           │   pshints.h
│   │   │   │   │           │   sfnt.h
│   │   │   │   │           │   t1types.h
│   │   │   │   │           │   tttypes.h
│   │   │   │   │           │
│   │   │   │   │           └───services
│   │   │   │   │                   svbdf.h
│   │   │   │   │                   svcid.h
│   │   │   │   │                   svgldict.h
│   │   │   │   │                   svgxval.h
│   │   │   │   │                   svkern.h
│   │   │   │   │                   svmm.h
│   │   │   │   │                   svotval.h
│   │   │   │   │                   svpfr.h
│   │   │   │   │                   svpostnm.h
│   │   │   │   │                   svprop.h
│   │   │   │   │                   svpscmap.h
│   │   │   │   │                   svpsinfo.h
│   │   │   │   │                   svsfnt.h
│   │   │   │   │                   svttcmap.h
│   │   │   │   │                   svtteng.h
│   │   │   │   │                   svttglyf.h
│   │   │   │   │                   svwinfnt.h
│   │   │   │   │                   svxf86nm.h
│   │   │   │   │
│   │   │   │   ├───winrt_8.1
│   │   │   │   │   └───freetype2
│   │   │   │   │       │   freetype.h
│   │   │   │   │       │   ft2build.h
│   │   │   │   │       │   ftadvanc.h
│   │   │   │   │       │   ftautoh.h
│   │   │   │   │       │   ftbbox.h
│   │   │   │   │       │   ftbdf.h
│   │   │   │   │       │   ftbitmap.h
│   │   │   │   │       │   ftbzip2.h
│   │   │   │   │       │   ftcache.h
│   │   │   │   │       │   ftcffdrv.h
│   │   │   │   │       │   ftchapters.h
│   │   │   │   │       │   ftcid.h
│   │   │   │   │       │   fterrdef.h
│   │   │   │   │       │   fterrors.h
│   │   │   │   │       │   ftgasp.h
│   │   │   │   │       │   ftglyph.h
│   │   │   │   │       │   ftgxval.h
│   │   │   │   │       │   ftgzip.h
│   │   │   │   │       │   ftimage.h
│   │   │   │   │       │   ftincrem.h
│   │   │   │   │       │   ftlcdfil.h
│   │   │   │   │       │   ftlist.h
│   │   │   │   │       │   ftlzw.h
│   │   │   │   │       │   ftmac.h
│   │   │   │   │       │   ftmm.h
│   │   │   │   │       │   ftmodapi.h
│   │   │   │   │       │   ftmoderr.h
│   │   │   │   │       │   ftotval.h
│   │   │   │   │       │   ftoutln.h
│   │   │   │   │       │   ftpfr.h
│   │   │   │   │       │   ftrender.h
│   │   │   │   │       │   ftsizes.h
│   │   │   │   │       │   ftsnames.h
│   │   │   │   │       │   ftstroke.h
│   │   │   │   │       │   ftsynth.h
│   │   │   │   │       │   ftsystem.h
│   │   │   │   │       │   fttrigon.h
│   │   │   │   │       │   ftttdrv.h
│   │   │   │   │       │   fttypes.h
│   │   │   │   │       │   ftwinfnt.h
│   │   │   │   │       │   ftxf86.h
│   │   │   │   │       │   t1tables.h
│   │   │   │   │       │   ttnameid.h
│   │   │   │   │       │   tttables.h
│   │   │   │   │       │   tttags.h
│   │   │   │   │       │   ttunpat.h
│   │   │   │   │       │
│   │   │   │   │       └───config
│   │   │   │   │               ftconfig.h
│   │   │   │   │               ftheader.h
│   │   │   │   │               ftmodule.h
│   │   │   │   │               ftoption.h
│   │   │   │   │               ftstdlib.h
│   │   │   │   │
│   │   │   │   └───wp_8.1
│   │   │   │       └───freetype2
│   │   │   │           │   freetype.h
│   │   │   │           │   ft2build.h
│   │   │   │           │   ftadvanc.h
│   │   │   │           │   ftautoh.h
│   │   │   │           │   ftbbox.h
│   │   │   │           │   ftbdf.h
│   │   │   │           │   ftbitmap.h
│   │   │   │           │   ftbzip2.h
│   │   │   │           │   ftcache.h
│   │   │   │           │   ftcffdrv.h
│   │   │   │           │   ftchapters.h
│   │   │   │           │   ftcid.h
│   │   │   │           │   fterrdef.h
│   │   │   │           │   fterrors.h
│   │   │   │           │   ftgasp.h
│   │   │   │           │   ftglyph.h
│   │   │   │           │   ftgxval.h
│   │   │   │           │   ftgzip.h
│   │   │   │           │   ftimage.h
│   │   │   │           │   ftincrem.h
│   │   │   │           │   ftlcdfil.h
│   │   │   │           │   ftlist.h
│   │   │   │           │   ftlzw.h
│   │   │   │           │   ftmac.h
│   │   │   │           │   ftmm.h
│   │   │   │           │   ftmodapi.h
│   │   │   │           │   ftmoderr.h
│   │   │   │           │   ftotval.h
│   │   │   │           │   ftoutln.h
│   │   │   │           │   ftpfr.h
│   │   │   │           │   ftrender.h
│   │   │   │           │   ftsizes.h
│   │   │   │           │   ftsnames.h
│   │   │   │           │   ftstroke.h
│   │   │   │           │   ftsynth.h
│   │   │   │           │   ftsystem.h
│   │   │   │           │   fttrigon.h
│   │   │   │           │   ftttdrv.h
│   │   │   │           │   fttypes.h
│   │   │   │           │   ftwinfnt.h
│   │   │   │           │   ftxf86.h
│   │   │   │           │   t1tables.h
│   │   │   │           │   ttnameid.h
│   │   │   │           │   tttables.h
│   │   │   │           │   tttags.h
│   │   │   │           │   ttunpat.h
│   │   │   │           │
│   │   │   │           └───config
│   │   │   │                   ftconfig.h
│   │   │   │                   ftheader.h
│   │   │   │                   ftmodule.h
│   │   │   │                   ftoption.h
│   │   │   │                   ftstdlib.h
│   │   │   │
│   │   │   └───prebuilt
│   │   │       ├───android
│   │   │       │   │   Android.mk
│   │   │       │   │
│   │   │       │   ├───arm64-v8a
│   │   │       │   │       libfreetype.a
│   │   │       │   │
│   │   │       │   ├───armeabi
│   │   │       │   │       libfreetype.a
│   │   │       │   │
│   │   │       │   ├───armeabi-v7a
│   │   │       │   │       libfreetype.a
│   │   │       │   │
│   │   │       │   └───x86
│   │   │       │           libfreetype.a
│   │   │       │
│   │   │       ├───ios
│   │   │       │       libfreetype.a
│   │   │       │
│   │   │       ├───linux
│   │   │       │   ├───32-bit
│   │   │       │   │       libfreetype.a
│   │   │       │   │
│   │   │       │   └───64-bit
│   │   │       │           libfreetype.a
│   │   │       │
│   │   │       ├───mac
│   │   │       │       libfreetype.a
│   │   │       │
│   │   │       ├───win10
│   │   │       │   ├───arm
│   │   │       │   │       freetype.lib
│   │   │       │   │
│   │   │       │   ├───win32
│   │   │       │   │       freetype.lib
│   │   │       │   │
│   │   │       │   └───x64
│   │   │       │           freetype.lib
│   │   │       │
│   │   │       ├───win32
│   │   │       │       freetype.lib
│   │   │       │
│   │   │       ├───winrt_8.1
│   │   │       │   ├───arm
│   │   │       │   │       freetype.lib
│   │   │       │   │
│   │   │       │   └───win32
│   │   │       │           freetype.lib
│   │   │       │
│   │   │       └───wp_8.1
│   │   │           ├───arm
│   │   │           │       freetype.lib
│   │   │           │
│   │   │           └───win32
│   │   │                   freetype.lib
│   │   │
│   │   ├───glfw3
│   │   │   ├───include
│   │   │   │   ├───mac
│   │   │   │   │       glfw3.h
│   │   │   │   │       glfw3native.h
│   │   │   │   │
│   │   │   │   └───win32
│   │   │   │           glfw3.h
│   │   │   │           glfw3native.h
│   │   │   │
│   │   │   └───prebuilt
│   │   │       ├───mac
│   │   │       │       libglfw3.a
│   │   │       │
│   │   │       └───win32
│   │   │               glfw3-2015.lib
│   │   │               glfw3.lib
│   │   │
│   │   ├───jpeg
│   │   │   │   CMakeLists.txt
│   │   │   │
│   │   │   ├───include
│   │   │   │   ├───android
│   │   │   │   │       jconfig.h
│   │   │   │   │       jerror.h
│   │   │   │   │       jmorecfg.h
│   │   │   │   │       jpeglib.h
│   │   │   │   │
│   │   │   │   ├───ios
│   │   │   │   │       jconfig.h
│   │   │   │   │       jerror.h
│   │   │   │   │       jmorecfg.h
│   │   │   │   │       jpeglib.h
│   │   │   │   │
│   │   │   │   ├───linux
│   │   │   │   │       jconfig.h
│   │   │   │   │       jmorecfg.h
│   │   │   │   │       jpeglib.h
│   │   │   │   │
│   │   │   │   ├───mac
│   │   │   │   │       jconfig.h
│   │   │   │   │       jmorecfg.h
│   │   │   │   │       jpeglib.h
│   │   │   │   │
│   │   │   │   ├───tizen
│   │   │   │   │       jconfig.h
│   │   │   │   │       jmorecfg.h
│   │   │   │   │       jpeglib.h
│   │   │   │   │
│   │   │   │   └───win32
│   │   │   │           jconfig.h
│   │   │   │           jmorecfg.h
│   │   │   │           jpeglib.h
│   │   │   │
│   │   │   └───prebuilt
│   │   │       ├───android
│   │   │       │   │   Android.mk
│   │   │       │   │
│   │   │       │   ├───arm64-v8a
│   │   │       │   │       libjpeg.a
│   │   │       │   │
│   │   │       │   ├───armeabi
│   │   │       │   │       libjpeg.a
│   │   │       │   │
│   │   │       │   ├───armeabi-v7a
│   │   │       │   │       libjpeg.a
│   │   │       │   │
│   │   │       │   └───x86
│   │   │       │           libjpeg.a
│   │   │       │
│   │   │       ├───ios
│   │   │       │       libjpeg.a
│   │   │       │
│   │   │       ├───linux
│   │   │       │   ├───32-bit
│   │   │       │   │       libjpeg.a
│   │   │       │   │
│   │   │       │   └───64-bit
│   │   │       │           libjpeg.a
│   │   │       │
│   │   │       ├───mac
│   │   │       │       libjpeg.a
│   │   │       │
│   │   │       ├───tizen
│   │   │       │   ├───arm
│   │   │       │   │       libjpeg.a
│   │   │       │   │
│   │   │       │   └───x86
│   │   │       │           libjpeg.a
│   │   │       │
│   │   │       └───win32
│   │   │               libjpeg-2015.lib
│   │   │               libjpeg.lib
│   │   │
│   │   ├───json
│   │   │   │   allocators.h
│   │   │   │   document.h
│   │   │   │   encodedstream.h
│   │   │   │   encodings.h
│   │   │   │   filereadstream.h
│   │   │   │   filestream.h
│   │   │   │   filewritestream.h
│   │   │   │   memorybuffer.h
│   │   │   │   memorystream.h
│   │   │   │   prettywriter.h
│   │   │   │   rapidjson.h
│   │   │   │   reader.h
│   │   │   │   stringbuffer.h
│   │   │   │   writer.h
│   │   │   │
│   │   │   ├───error
│   │   │   │       en.h
│   │   │   │       error.h
│   │   │   │
│   │   │   ├───internal
│   │   │   │       biginteger.h
│   │   │   │       diyfp.h
│   │   │   │       dtoa.h
│   │   │   │       ieee754.h
│   │   │   │       itoa.h
│   │   │   │       meta.h
│   │   │   │       pow10.h
│   │   │   │       stack.h
│   │   │   │       strfunc.h
│   │   │   │       strtod.h
│   │   │   │
│   │   │   └───msinttypes
│   │   │           inttypes.h
│   │   │           stdint.h
│   │   │
│   │   ├───linux-specific
│   │   │   └───fmod
│   │   │       ├───include
│   │   │       │       fmod.h
│   │   │       │       fmod.hpp
│   │   │       │       fmod_codec.h
│   │   │       │       fmod_common.h
│   │   │       │       fmod_dsp.h
│   │   │       │       fmod_dsp_effects.h
│   │   │       │       fmod_errors.h
│   │   │       │       fmod_output.h
│   │   │       │
│   │   │       └───prebuilt
│   │   │           ├───32-bit
│   │   │           │       libfmod.so
│   │   │           │       libfmodL.so
│   │   │           │
│   │   │           └───64-bit
│   │   │                   libfmod.so
│   │   │                   libfmodL.so
│   │   │
│   │   ├───png
│   │   │   ├───include
│   │   │   │   ├───android
│   │   │   │   │       png.h
│   │   │   │   │       pngconf.h
│   │   │   │   │       pnglibconf.h
│   │   │   │   │
│   │   │   │   ├───ios
│   │   │   │   │       png.h
│   │   │   │   │       pngconf.h
│   │   │   │   │       pnglibconf.h
│   │   │   │   │
│   │   │   │   ├───mac
│   │   │   │   │       png.h
│   │   │   │   │       pngconf.h
│   │   │   │   │       pnglibconf.h
│   │   │   │   │
│   │   │   │   ├───tizen
│   │   │   │   │       png.h
│   │   │   │   │       pngconf.h
│   │   │   │   │       pnglibconf.h
│   │   │   │   │
│   │   │   │   └───win32
│   │   │   │           png.h
│   │   │   │           pngconf.h
│   │   │   │           pnglibconf.h
│   │   │   │
│   │   │   └───prebuilt
│   │   │       ├───android
│   │   │       │   │   Android.mk
│   │   │       │   │
│   │   │       │   ├───arm64-v8a
│   │   │       │   │       libpng.a
│   │   │       │   │
│   │   │       │   ├───armeabi
│   │   │       │   │       libpng.a
│   │   │       │   │
│   │   │       │   ├───armeabi-v7a
│   │   │       │   │       libpng.a
│   │   │       │   │
│   │   │       │   └───x86
│   │   │       │           libpng.a
│   │   │       │
│   │   │       ├───ios
│   │   │       │       libpng.a
│   │   │       │
│   │   │       ├───mac
│   │   │       │       libpng.a
│   │   │       │
│   │   │       ├───tizen
│   │   │       │   ├───arm
│   │   │       │   │       libpng.a
│   │   │       │   │
│   │   │       │   └───x86
│   │   │       │           libpng.a
│   │   │       │
│   │   │       └───win32
│   │   │               libpng-2015.lib
│   │   │               libpng.lib
│   │   │
│   │   ├───poly2tri
│   │   │   │   poly2tri.h
│   │   │   │
│   │   │   ├───common
│   │   │   │       shapes.cc
│   │   │   │       shapes.h
│   │   │   │       utils.h
│   │   │   │
│   │   │   └───sweep
│   │   │           advancing_front.cc
│   │   │           advancing_front.h
│   │   │           cdt.cc
│   │   │           cdt.h
│   │   │           sweep.cc
│   │   │           sweep.h
│   │   │           sweep_context.cc
│   │   │           sweep_context.h
│   │   │
│   │   ├───recast
│   │   │   │   Android.mk
│   │   │   │   CMakeLists.txt
│   │   │   │
│   │   │   ├───DebugUtils
│   │   │   │       DebugDraw.cpp
│   │   │   │       DebugDraw.h
│   │   │   │       DetourDebugDraw.cpp
│   │   │   │       DetourDebugDraw.h
│   │   │   │       RecastDebugDraw.cpp
│   │   │   │       RecastDebugDraw.h
│   │   │   │       RecastDump.cpp
│   │   │   │       RecastDump.h
│   │   │   │
│   │   │   ├───Detour
│   │   │   │       DetourAlloc.cpp
│   │   │   │       DetourAlloc.h
│   │   │   │       DetourAssert.h
│   │   │   │       DetourCommon.cpp
│   │   │   │       DetourCommon.h
│   │   │   │       DetourMath.h
│   │   │   │       DetourNavMesh.cpp
│   │   │   │       DetourNavMesh.h
│   │   │   │       DetourNavMeshBuilder.cpp
│   │   │   │       DetourNavMeshBuilder.h
│   │   │   │       DetourNavMeshQuery.cpp
│   │   │   │       DetourNavMeshQuery.h
│   │   │   │       DetourNode.cpp
│   │   │   │       DetourNode.h
│   │   │   │       DetourStatus.h
│   │   │   │
│   │   │   ├───DetourCrowd
│   │   │   │       DetourCrowd.cpp
│   │   │   │       DetourCrowd.h
│   │   │   │       DetourLocalBoundary.cpp
│   │   │   │       DetourLocalBoundary.h
│   │   │   │       DetourObstacleAvoidance.cpp
│   │   │   │       DetourObstacleAvoidance.h
│   │   │   │       DetourPathCorridor.cpp
│   │   │   │       DetourPathCorridor.h
│   │   │   │       DetourPathQueue.cpp
│   │   │   │       DetourPathQueue.h
│   │   │   │       DetourProximityGrid.cpp
│   │   │   │       DetourProximityGrid.h
│   │   │   │
│   │   │   ├───DetourTileCache
│   │   │   │       DetourTileCache.cpp
│   │   │   │       DetourTileCache.h
│   │   │   │       DetourTileCacheBuilder.cpp
│   │   │   │       DetourTileCacheBuilder.h
│   │   │   │
│   │   │   ├───fastlz
│   │   │   │       fastlz.c
│   │   │   │       fastlz.h
│   │   │   │
│   │   │   ├───proj.win10
│   │   │   │       librecast.vcxproj
│   │   │   │       librecast.vcxproj.filters
│   │   │   │
│   │   │   ├───proj.win32
│   │   │   │       librecast.vcxproj
│   │   │   │       librecast.vcxproj.filters
│   │   │   │
│   │   │   ├───proj.win8.1-universal
│   │   │   │   ├───librecast.Shared
│   │   │   │   │       librecast.Shared.vcxitems
│   │   │   │   │       librecast.Shared.vcxitems.filters
│   │   │   │   │
│   │   │   │   ├───librecast.Windows
│   │   │   │   │       librecast.Windows.vcxproj
│   │   │   │   │       librecast.Windows.vcxproj.filters
│   │   │   │   │
│   │   │   │   └───librecast.WindowsPhone
│   │   │   │           librecast.WindowsPhone.vcxproj
│   │   │   │           librecast.WindowsPhone.vcxproj.filters
│   │   │   │
│   │   │   └───Recast
│   │   │           Recast.cpp
│   │   │           Recast.h
│   │   │           RecastAlloc.cpp
│   │   │           RecastAlloc.h
│   │   │           RecastArea.cpp
│   │   │           RecastAssert.h
│   │   │           RecastContour.cpp
│   │   │           RecastFilter.cpp
│   │   │           RecastLayers.cpp
│   │   │           RecastMesh.cpp
│   │   │           RecastMeshDetail.cpp
│   │   │           RecastRasterization.cpp
│   │   │           RecastRegion.cpp
│   │   │
│   │   ├───sqlite3
│   │   │   │   Android.mk
│   │   │   │
│   │   │   ├───include
│   │   │   │       sqlite3.h
│   │   │   │       sqlite3ext.h
│   │   │   │
│   │   │   └───libraries
│   │   │       ├───win10
│   │   │       │   ├───arm
│   │   │       │   │       sqlite3.dll
│   │   │       │   │       sqlite3.lib
│   │   │       │   │
│   │   │       │   ├───win32
│   │   │       │   │       sqlite3.dll
│   │   │       │   │       sqlite3.lib
│   │   │       │   │
│   │   │       │   └───x64
│   │   │       │           sqlite3.dll
│   │   │       │           sqlite3.lib
│   │   │       │
│   │   │       ├───win32
│   │   │       │       sqlite3.dll
│   │   │       │       sqlite3.lib
│   │   │       │
│   │   │       ├───winrt_8.1
│   │   │       │   ├───arm
│   │   │       │   │       sqlite3.dll
│   │   │       │   │       sqlite3.lib
│   │   │       │   │
│   │   │       │   └───win32
│   │   │       │           sqlite3.dll
│   │   │       │           sqlite3.lib
│   │   │       │
│   │   │       └───wp_8.1
│   │   │           ├───arm
│   │   │           │       sqlite3.dll
│   │   │           │       sqlite3.lib
│   │   │           │
│   │   │           └───win32
│   │   │                   sqlite3.dll
│   │   │                   sqlite3.lib
│   │   │
│   │   ├───tiff
│   │   │   │   CMakeLists.txt
│   │   │   │
│   │   │   ├───include
│   │   │   │   ├───android
│   │   │   │   │       tiff.h
│   │   │   │   │       tiffconf.h
│   │   │   │   │       tiffio.h
│   │   │   │   │       tiffvers.h
│   │   │   │   │
│   │   │   │   ├───ios
│   │   │   │   │       tiff.h
│   │   │   │   │       tiffconf-32.h
│   │   │   │   │       tiffconf-64.h
│   │   │   │   │       tiffconf.h
│   │   │   │   │       tiffio.h
│   │   │   │   │       tiffvers.h
│   │   │   │   │
│   │   │   │   ├───linux
│   │   │   │   │       tiff.h
│   │   │   │   │       tiffconf.h
│   │   │   │   │       tiffio.h
│   │   │   │   │       tiffvers.h
│   │   │   │   │
│   │   │   │   ├───mac
│   │   │   │   │       tiff.h
│   │   │   │   │       tiffconf-32.h
│   │   │   │   │       tiffconf-64.h
│   │   │   │   │       tiffconf.h
│   │   │   │   │       tiffio.h
│   │   │   │   │       tiffvers.h
│   │   │   │   │
│   │   │   │   ├───tizen
│   │   │   │   │       tiff.h
│   │   │   │   │       tiffconf.h
│   │   │   │   │       tiffio.h
│   │   │   │   │       tiffvers.h
│   │   │   │   │
│   │   │   │   └───win32
│   │   │   │           tiff.h
│   │   │   │           tiffconf.h
│   │   │   │           tiffio.h
│   │   │   │           tiffvers.h
│   │   │   │
│   │   │   └───prebuilt
│   │   │       ├───android
│   │   │       │   │   Android.mk
│   │   │       │   │
│   │   │       │   ├───arm64-v8a
│   │   │       │   │       libtiff.a
│   │   │       │   │
│   │   │       │   ├───armeabi
│   │   │       │   │       libtiff.a
│   │   │       │   │
│   │   │       │   ├───armeabi-v7a
│   │   │       │   │       libtiff.a
│   │   │       │   │
│   │   │       │   └───x86
│   │   │       │           libtiff.a
│   │   │       │
│   │   │       ├───ios
│   │   │       │       libtiff.a
│   │   │       │
│   │   │       ├───linux
│   │   │       │   ├───32-bit
│   │   │       │   │       libtiff.a
│   │   │       │   │
│   │   │       │   └───64-bit
│   │   │       │           libtiff.a
│   │   │       │
│   │   │       ├───mac
│   │   │       │       libtiff.a
│   │   │       │
│   │   │       ├───tizen
│   │   │       │   ├───arm
│   │   │       │   │       libtiff.a
│   │   │       │   │
│   │   │       │   └───x86
│   │   │       │           libtiff.a
│   │   │       │
│   │   │       └───win32
│   │   │               libtiff-2015.lib
│   │   │               libtiff.dll
│   │   │               libtiff.lib
│   │   │
│   │   ├───tinyxml2
│   │   │       CMakeLists.txt
│   │   │       tinyxml2.cpp
│   │   │       tinyxml2.h
│   │   │
│   │   ├───unzip
│   │   │       CMakeLists.txt
│   │   │       crypt.h
│   │   │       ioapi.cpp
│   │   │       ioapi.h
│   │   │       ioapi_mem.cpp
│   │   │       ioapi_mem.h
│   │   │       unzip.cpp
│   │   │       unzip.h
│   │   │
│   │   ├───webp
│   │   │   │   CMakeLists.txt
│   │   │   │
│   │   │   ├───include
│   │   │   │   ├───android
│   │   │   │   │       decode.h
│   │   │   │   │       encode.h
│   │   │   │   │       types.h
│   │   │   │   │
│   │   │   │   ├───ios
│   │   │   │   │       decode.h
│   │   │   │   │       encode.h
│   │   │   │   │       types.h
│   │   │   │   │
│   │   │   │   ├───linux
│   │   │   │   │       decode.h
│   │   │   │   │       encode.h
│   │   │   │   │       types.h
│   │   │   │   │
│   │   │   │   ├───mac
│   │   │   │   │       decode.h
│   │   │   │   │       encode.h
│   │   │   │   │       types.h
│   │   │   │   │
│   │   │   │   ├───tizen
│   │   │   │   │       decode.h
│   │   │   │   │       encode.h
│   │   │   │   │       types.h
│   │   │   │   │
│   │   │   │   └───win32
│   │   │   │           decode.h
│   │   │   │           encode.h
│   │   │   │           types.h
│   │   │   │
│   │   │   └───prebuilt
│   │   │       ├───android
│   │   │       │   │   Android.mk
│   │   │       │   │
│   │   │       │   ├───arm64-v8a
│   │   │       │   │       libwebp.a
│   │   │       │   │
│   │   │       │   ├───armeabi
│   │   │       │   │       libwebp.a
│   │   │       │   │
│   │   │       │   ├───armeabi-v7a
│   │   │       │   │       libwebp.a
│   │   │       │   │
│   │   │       │   └───x86
│   │   │       │           libwebp.a
│   │   │       │
│   │   │       ├───ios
│   │   │       │       libwebp.a
│   │   │       │
│   │   │       ├───linux
│   │   │       │   ├───32-bit
│   │   │       │   │       libwebp.a
│   │   │       │   │
│   │   │       │   └───64-bit
│   │   │       │           libwebp.a
│   │   │       │
│   │   │       ├───mac
│   │   │       │       libwebp.a
│   │   │       │
│   │   │       ├───tizen
│   │   │       │   ├───arm
│   │   │       │   │       libwebp.a
│   │   │       │   │
│   │   │       │   └───x86
│   │   │       │           libwebp.a
│   │   │       │
│   │   │       └───win32
│   │   │               libwebp.lib
│   │   │
│   │   ├───websockets
│   │   │   ├───include
│   │   │   │   ├───android
│   │   │   │   │       libwebsockets.h
│   │   │   │   │       lws_config.h
│   │   │   │   │
│   │   │   │   ├───ios
│   │   │   │   │       libwebsockets.h
│   │   │   │   │       lws_config.h
│   │   │   │   │
│   │   │   │   ├───linux
│   │   │   │   │       libwebsockets.h
│   │   │   │   │       lws_config.h
│   │   │   │   │
│   │   │   │   ├───mac
│   │   │   │   │       libwebsockets.h
│   │   │   │   │       lws_config.h
│   │   │   │   │
│   │   │   │   ├───tizen
│   │   │   │   │       libwebsockets.h
│   │   │   │   │       lws_config.h
│   │   │   │   │
│   │   │   │   ├───win10
│   │   │   │   │       libwebsockets.h
│   │   │   │   │       lws_config.h
│   │   │   │   │       private-libwebsockets.h
│   │   │   │   │
│   │   │   │   ├───win32
│   │   │   │   │   │   libwebsockets.h
│   │   │   │   │   │   lws_config.h
│   │   │   │   │   │
│   │   │   │   │   └───win32helpers
│   │   │   │   │           getopt.h
│   │   │   │   │           gettimeofday.h
│   │   │   │   │           websock-w32.h
│   │   │   │   │
│   │   │   │   ├───winrt_8.1
│   │   │   │   │       libwebsockets.h
│   │   │   │   │       lws_config.h
│   │   │   │   │       private-libwebsockets.h
│   │   │   │   │
│   │   │   │   └───wp_8.1
│   │   │   │           libwebsockets.h
│   │   │   │           lws_config.h
│   │   │   │           private-libwebsockets.h
│   │   │   │
│   │   │   └───prebuilt
│   │   │       ├───android
│   │   │       │   │   Android.mk
│   │   │       │   │
│   │   │       │   ├───arm64-v8a
│   │   │       │   │       libwebsockets.a
│   │   │       │   │
│   │   │       │   ├───armeabi
│   │   │       │   │       libwebsockets.a
│   │   │       │   │
│   │   │       │   ├───armeabi-v7a
│   │   │       │   │       libwebsockets.a
│   │   │       │   │
│   │   │       │   └───x86
│   │   │       │           libwebsockets.a
│   │   │       │
│   │   │       ├───ios
│   │   │       │       libwebsockets.a
│   │   │       │
│   │   │       ├───linux
│   │   │       │   ├───32-bit
│   │   │       │   │       libwebsockets.a
│   │   │       │   │
│   │   │       │   └───64-bit
│   │   │       │           libwebsockets.a
│   │   │       │
│   │   │       ├───mac
│   │   │       │       libwebsockets.a
│   │   │       │
│   │   │       ├───tizen
│   │   │       │   ├───arm
│   │   │       │   │       libwebsockets.a
│   │   │       │   │
│   │   │       │   └───x86
│   │   │       │           libwebsockets.a
│   │   │       │
│   │   │       ├───win10
│   │   │       │   ├───arm
│   │   │       │   │       libwebsockets.lib
│   │   │       │   │
│   │   │       │   ├───win32
│   │   │       │   │       libwebsockets.lib
│   │   │       │   │
│   │   │       │   └───x64
│   │   │       │           libwebsockets.lib
│   │   │       │
│   │   │       ├───win32
│   │   │       │       websockets.lib
│   │   │       │
│   │   │       ├───winrt_8.1
│   │   │       │   ├───arm
│   │   │       │   │       libwebsockets.lib
│   │   │       │   │
│   │   │       │   └───win32
│   │   │       │           libwebsockets.lib
│   │   │       │
│   │   │       └───wp_8.1
│   │   │           ├───arm
│   │   │           │       libwebsockets.lib
│   │   │           │
│   │   │           └───win32
│   │   │                   libwebsockets.lib
│   │   │
│   │   ├───win10-specific
│   │   │   ├───angle
│   │   │   │   ├───include
│   │   │   │   │   │   angle_windowsstore.h
│   │   │   │   │   │
│   │   │   │   │   ├───EGL
│   │   │   │   │   │       egl.h
│   │   │   │   │   │       eglext.h
│   │   │   │   │   │       eglplatform.h
│   │   │   │   │   │
│   │   │   │   │   ├───GLES2
│   │   │   │   │   │       gl2.h
│   │   │   │   │   │       gl2ext.h
│   │   │   │   │   │       gl2platform.h
│   │   │   │   │   │
│   │   │   │   │   ├───GLES3
│   │   │   │   │   │       gl3.h
│   │   │   │   │   │       gl31.h
│   │   │   │   │   │       gl32.h
│   │   │   │   │   │       gl3platform.h
│   │   │   │   │   │
│   │   │   │   │   └───KHR
│   │   │   │   │           khrplatform.h
│   │   │   │   │
│   │   │   │   └───prebuilt
│   │   │   │       ├───arm
│   │   │   │       │       libEGL.dll
│   │   │   │       │       libEGL.lib
│   │   │   │       │       libGLESv2.dll
│   │   │   │       │       libGLESv2.lib
│   │   │   │       │
│   │   │   │       ├───win32
│   │   │   │       │       libEGL.dll
│   │   │   │       │       libEGL.lib
│   │   │   │       │       libGLESv2.dll
│   │   │   │       │       libGLESv2.lib
│   │   │   │       │
│   │   │   │       └───x64
│   │   │   │               libEGL.dll
│   │   │   │               libEGL.lib
│   │   │   │               libGLESv2.dll
│   │   │   │               libGLESv2.lib
│   │   │   │
│   │   │   ├───OggDecoder
│   │   │   │   ├───include
│   │   │   │   │   ├───ogg
│   │   │   │   │   │       ogg.h
│   │   │   │   │   │       os_types.h
│   │   │   │   │   │
│   │   │   │   │   └───vorbis
│   │   │   │   │           codec.h
│   │   │   │   │           vorbisenc.h
│   │   │   │   │           vorbisfile.h
│   │   │   │   │
│   │   │   │   └───prebuilt
│   │   │   │       ├───arm
│   │   │   │       │       libogg.dll
│   │   │   │       │       libogg.lib
│   │   │   │       │       libvorbis.dll
│   │   │   │       │       libvorbis.lib
│   │   │   │       │       libvorbisfile.dll
│   │   │   │       │       libvorbisfile.lib
│   │   │   │       │
│   │   │   │       ├───win32
│   │   │   │       │       libogg.dll
│   │   │   │       │       libogg.lib
│   │   │   │       │       libvorbis.dll
│   │   │   │       │       libvorbis.lib
│   │   │   │       │       libvorbisfile.dll
│   │   │   │       │       libvorbisfile.lib
│   │   │   │       │
│   │   │   │       └───x64
│   │   │   │               libogg.dll
│   │   │   │               libogg.lib
│   │   │   │               libvorbis.dll
│   │   │   │               libvorbis.lib
│   │   │   │               libvorbisfile.dll
│   │   │   │               libvorbisfile.lib
│   │   │   │
│   │   │   └───zlib
│   │   │       ├───include
│   │   │       │       zconf.h
│   │   │       │       zlib.h
│   │   │       │
│   │   │       └───prebuilt
│   │   │           ├───arm
│   │   │           │       zlib.dll
│   │   │           │       zlib.lib
│   │   │           │       zlibstatic.lib
│   │   │           │
│   │   │           ├───win32
│   │   │           │       zlib.dll
│   │   │           │       zlib.lib
│   │   │           │       zlibstatic.lib
│   │   │           │
│   │   │           └───x64
│   │   │                   zlib.dll
│   │   │                   zlib.lib
│   │   │                   zlibstatic.lib
│   │   │
│   │   ├───win32-specific
│   │   │   ├───gles
│   │   │   │   ├───include
│   │   │   │   │   └───OGLES
│   │   │   │   │       └───GL
│   │   │   │   │               glew.h
│   │   │   │   │               glxew.h
│   │   │   │   │               wglew.h
│   │   │   │   │
│   │   │   │   └───prebuilt
│   │   │   │           glew32.dll
│   │   │   │           glew32.lib
│   │   │   │
│   │   │   ├───icon
│   │   │   │   ├───include
│   │   │   │   │       iconv.h
│   │   │   │   │
│   │   │   │   └───prebuilt
│   │   │   │           iconv.dll
│   │   │   │           libiconv.lib
│   │   │   │
│   │   │   ├───MP3Decoder
│   │   │   │   ├───include
│   │   │   │   │       mpg123.h
│   │   │   │   │
│   │   │   │   └───prebuilt
│   │   │   │           libmpg123.dll
│   │   │   │           libmpg123.lib
│   │   │   │
│   │   │   ├───OggDecoder
│   │   │   │   ├───include
│   │   │   │   │   ├───ogg
│   │   │   │   │   │       ogg.h
│   │   │   │   │   │       os_types.h
│   │   │   │   │   │
│   │   │   │   │   └───vorbis
│   │   │   │   │           codec.h
│   │   │   │   │           vorbisenc.h
│   │   │   │   │           vorbisfile.h
│   │   │   │   │
│   │   │   │   └───prebuilt
│   │   │   │           libogg.dll
│   │   │   │           libogg.lib
│   │   │   │           libvorbis.dll
│   │   │   │           libvorbis.lib
│   │   │   │           libvorbisfile.dll
│   │   │   │           libvorbisfile.lib
│   │   │   │
│   │   │   ├───OpenalSoft
│   │   │   │   ├───include
│   │   │   │   │   └───AL
│   │   │   │   │           al.h
│   │   │   │   │           alc.h
│   │   │   │   │           alext.h
│   │   │   │   │           efx-creative.h
│   │   │   │   │           efx-presets.h
│   │   │   │   │           efx.h
│   │   │   │   │
│   │   │   │   └───prebuilt
│   │   │   │           OpenAL32.dll
│   │   │   │           OpenAL32.lib
│   │   │   │
│   │   │   └───zlib
│   │   │       ├───include
│   │   │       │       zconf.h
│   │   │       │       zlib.h
│   │   │       │
│   │   │       └───prebuilt
│   │   │               libzlib.lib
│   │   │               zlib1.dll
│   │   │
│   │   ├───winrt_8.1-specific
│   │   │   ├───angle
│   │   │   │   ├───include
│   │   │   │   │   │   angle_windowsstore.h
│   │   │   │   │   │
│   │   │   │   │   ├───EGL
│   │   │   │   │   │       egl.h
│   │   │   │   │   │       eglext.h
│   │   │   │   │   │       eglplatform.h
│   │   │   │   │   │
│   │   │   │   │   ├───GLES2
│   │   │   │   │   │       gl2.h
│   │   │   │   │   │       gl2ext.h
│   │   │   │   │   │       gl2platform.h
│   │   │   │   │   │
│   │   │   │   │   ├───GLES3
│   │   │   │   │   │       gl3.h
│   │   │   │   │   │       gl31.h
│   │   │   │   │   │       gl32.h
│   │   │   │   │   │       gl3platform.h
│   │   │   │   │   │
│   │   │   │   │   └───KHR
│   │   │   │   │           khrplatform.h
│   │   │   │   │
│   │   │   │   └───prebuilt
│   │   │   │       ├───arm
│   │   │   │       │       libEGL.dll
│   │   │   │       │       libEGL.lib
│   │   │   │       │       libGLESv2.dll
│   │   │   │       │       libGLESv2.lib
│   │   │   │       │
│   │   │   │       └───win32
│   │   │   │               libEGL.dll
│   │   │   │               libEGL.lib
│   │   │   │               libGLESv2.dll
│   │   │   │               libGLESv2.lib
│   │   │   │
│   │   │   ├───OggDecoder
│   │   │   │   ├───include
│   │   │   │   │   ├───ogg
│   │   │   │   │   │       ogg.h
│   │   │   │   │   │       os_types.h
│   │   │   │   │   │
│   │   │   │   │   └───vorbis
│   │   │   │   │           codec.h
│   │   │   │   │           vorbisenc.h
│   │   │   │   │           vorbisfile.h
│   │   │   │   │
│   │   │   │   └───prebuilt
│   │   │   │       ├───arm
│   │   │   │       │       libogg.dll
│   │   │   │       │       libogg.lib
│   │   │   │       │       libvorbis.dll
│   │   │   │       │       libvorbis.lib
│   │   │   │       │       libvorbisfile.dll
│   │   │   │       │       libvorbisfile.lib
│   │   │   │       │
│   │   │   │       └───win32
│   │   │   │               libogg.dll
│   │   │   │               libogg.lib
│   │   │   │               libvorbis.dll
│   │   │   │               libvorbis.lib
│   │   │   │               libvorbisfile.dll
│   │   │   │               libvorbisfile.lib
│   │   │   │
│   │   │   └───zlib
│   │   │       ├───include
│   │   │       │       zconf.h
│   │   │       │       zlib.h
│   │   │       │
│   │   │       └───prebuilt
│   │   │           ├───arm
│   │   │           │       zlib.dll
│   │   │           │       zlib.lib
│   │   │           │       zlibstatic.lib
│   │   │           │
│   │   │           └───win32
│   │   │                   zlib.dll
│   │   │                   zlib.lib
│   │   │                   zlibstatic.lib
│   │   │
│   │   ├───wp_8.1-specific
│   │   │   ├───angle
│   │   │   │   ├───include
│   │   │   │   │   │   angle_windowsstore.h
│   │   │   │   │   │
│   │   │   │   │   ├───EGL
│   │   │   │   │   │       egl.h
│   │   │   │   │   │       eglext.h
│   │   │   │   │   │       eglplatform.h
│   │   │   │   │   │
│   │   │   │   │   ├───GLES2
│   │   │   │   │   │       gl2.h
│   │   │   │   │   │       gl2ext.h
│   │   │   │   │   │       gl2platform.h
│   │   │   │   │   │
│   │   │   │   │   ├───GLES3
│   │   │   │   │   │       gl3.h
│   │   │   │   │   │       gl31.h
│   │   │   │   │   │       gl32.h
│   │   │   │   │   │       gl3platform.h
│   │   │   │   │   │
│   │   │   │   │   └───KHR
│   │   │   │   │           khrplatform.h
│   │   │   │   │
│   │   │   │   └───prebuilt
│   │   │   │       ├───arm
│   │   │   │       │       libEGL.dll
│   │   │   │       │       libEGL.lib
│   │   │   │       │       libGLESv2.dll
│   │   │   │       │       libGLESv2.lib
│   │   │   │       │
│   │   │   │       └───win32
│   │   │   │               libEGL.dll
│   │   │   │               libEGL.lib
│   │   │   │               libGLESv2.dll
│   │   │   │               libGLESv2.lib
│   │   │   │
│   │   │   ├───OggDecoder
│   │   │   │   ├───include
│   │   │   │   │   ├───ogg
│   │   │   │   │   │       ogg.h
│   │   │   │   │   │       os_types.h
│   │   │   │   │   │
│   │   │   │   │   └───vorbis
│   │   │   │   │           codec.h
│   │   │   │   │           vorbisenc.h
│   │   │   │   │           vorbisfile.h
│   │   │   │   │
│   │   │   │   └───prebuilt
│   │   │   │       ├───arm
│   │   │   │       │       libogg.dll
│   │   │   │       │       libogg.lib
│   │   │   │       │       libvorbis.dll
│   │   │   │       │       libvorbis.lib
│   │   │   │       │       libvorbisfile.dll
│   │   │   │       │       libvorbisfile.lib
│   │   │   │       │
│   │   │   │       └───win32
│   │   │   │               libogg.dll
│   │   │   │               libogg.lib
│   │   │   │               libvorbis.dll
│   │   │   │               libvorbis.lib
│   │   │   │               libvorbisfile.dll
│   │   │   │               libvorbisfile.lib
│   │   │   │
│   │   │   └───zlib
│   │   │       ├───include
│   │   │       │       zconf.h
│   │   │       │       zlib.h
│   │   │       │
│   │   │       └───prebuilt
│   │   │           ├───arm
│   │   │           │       zlib.dll
│   │   │           │       zlib.lib
│   │   │           │       zlibstatic.lib
│   │   │           │
│   │   │           └───win32
│   │   │                   zlib.dll
│   │   │                   zlib.lib
│   │   │                   zlibstatic.lib
│   │   │
│   │   ├───xxhash
│   │   │       CMakeLists.txt
│   │   │       xxhash.c
│   │   │       xxhash.h
│   │   │
│   │   ├───xxtea
│   │   │       xxtea.cpp
│   │   │       xxtea.h
│   │   │
│   │   └───zlib
│   │       ├───include
│   │       │       zconf.h
│   │       │       zlib.h
│   │       │
│   │       └───prebuilt
│   │           ├───android
│   │           │   │   Android.mk
│   │           │   │
│   │           │   ├───arm64-v8a
│   │           │   │       libz.a
│   │           │   │
│   │           │   ├───armeabi
│   │           │   │       libz.a
│   │           │   │
│   │           │   ├───armeabi-v7a
│   │           │   │       libz.a
│   │           │   │
│   │           │   └───x86
│   │           │           libz.a
│   │           │
│   │           └───mac
│   │                   libz.a
│   │
│   ├───licenses
│   │       LICENSE_AA-EDT.txt
│   │       LICENSE_artwork.txt
│   │       LICENSE_box2d.txt
│   │       LICENSE_CCBReader.txt
│   │       LICENSE_CCControlExtension.txt
│   │       LICENSE_chipmunk.txt
│   │       LICENSE_cocos2d-iphone.txt
│   │       LICENSE_cocos2d-x.txt
│   │       LICENSE_cocosdenshion.txt
│   │       LICENSE_com.android.vending.expansion.zipfile.txt
│   │       LICENSE_curl.txt
│   │       LICENSE_js.txt
│   │       LICENSE_JSON4Lua.txt
│   │       LICENSE_jsoncpp.txt
│   │       LICENSE_Kazmath.txt
│   │       LICENSE_libjpeg.txt
│   │       LICENSE_libpng.txt
│   │       LICENSE_libtiff.txt
│   │       LICENSE_libwebsockets.txt
│   │       LICENSE_libxml2.txt
│   │       LICENSE_llvm.txt
│   │       LICENSE_lua.txt
│   │       LICENSE_LuaSocket.txt
│   │       LICENSE_ogg_vorbis.txt
│   │       LICENSE_Poly2Tri.txt
│   │       LICENSE_SpiderMonkey.txt
│   │       LICENSE_spine.txt
│   │       LICENSE_tolua++.txt
│   │       LICENSE_unicode.txt
│   │       LICENSE_zlib.txt
│   │
│   ├───plugin
│   │   │   AUTHORS
│   │   │   README.md
│   │   │
│   │   ├───jsbindings
│   │   │   │   Android.mk
│   │   │   │
│   │   │   ├───auto
│   │   │   │   │   jsb_cocos2dx_pluginx_auto.cpp
│   │   │   │   │   jsb_cocos2dx_pluginx_auto.hpp
│   │   │   │   │
│   │   │   │   └───api
│   │   │   │           jsb_cocos2dx_pluginx_auto_api.js
│   │   │   │
│   │   │   ├───manual
│   │   │   │       jsb_pluginx_basic_conversions.cpp
│   │   │   │       jsb_pluginx_basic_conversions.h
│   │   │   │       jsb_pluginx_extension_registration.cpp
│   │   │   │       jsb_pluginx_extension_registration.h
│   │   │   │       jsb_pluginx_manual_callback.cpp
│   │   │   │       jsb_pluginx_manual_callback.h
│   │   │   │       jsb_pluginx_manual_protocols.cpp
│   │   │   │       jsb_pluginx_manual_protocols.h
│   │   │   │       jsb_pluginx_spidermonkey_specifics.cpp
│   │   │   │       jsb_pluginx_spidermonkey_specifics.h
│   │   │   │       pluginxUTF8.cpp
│   │   │   │       pluginxUTF8.h
│   │   │   │       uthash.h
│   │   │   │
│   │   │   └───script
│   │   │           jsb_pluginx.js
│   │   │
│   │   ├───luabindings
│   │   │   ├───auto
│   │   │   │   │   lua_cocos2dx_pluginx_auto.cpp
│   │   │   │   │   lua_cocos2dx_pluginx_auto.hpp
│   │   │   │   │
│   │   │   │   └───api
│   │   │   │           AgentManager.lua
│   │   │   │           FacebookAgent.lua
│   │   │   │           lua_cocos2dx_pluginx_auto_api.lua
│   │   │   │           PluginManager.lua
│   │   │   │           PluginProtocol.lua
│   │   │   │           ProtocolAds.lua
│   │   │   │           ProtocolAnalytics.lua
│   │   │   │           ProtocolIAP.lua
│   │   │   │           ProtocolShare.lua
│   │   │   │           ProtocolSocial.lua
│   │   │   │           ProtocolUser.lua
│   │   │   │
│   │   │   ├───manual
│   │   │   │       lua_pluginx_basic_conversions.cpp
│   │   │   │       lua_pluginx_basic_conversions.h
│   │   │   │       lua_pluginx_manual_callback.cpp
│   │   │   │       lua_pluginx_manual_callback.h
│   │   │   │       lua_pluginx_manual_protocols.cpp
│   │   │   │       lua_pluginx_manual_protocols.h
│   │   │   │
│   │   │   └───script
│   │   │           lua_plugin.lua
│   │   │
│   │   ├───plugins
│   │   │   ├───admob
│   │   │   │   ├───proj.android
│   │   │   │   │   │   .classpath
│   │   │   │   │   │   .project
│   │   │   │   │   │   AndroidManifest.xml
│   │   │   │   │   │   build.xml
│   │   │   │   │   │   ForManifest.xml
│   │   │   │   │   │   project.properties
│   │   │   │   │   │
│   │   │   │   │   ├───sdk
│   │   │   │   │   │       GoogleAdMobAdsSdk.jar
│   │   │   │   │   │
│   │   │   │   │   └───src
│   │   │   │   │       └───org
│   │   │   │   │           └───cocos2dx
│   │   │   │   │               └───plugin
│   │   │   │   │                       AdsAdmob.java
│   │   │   │   │
│   │   │   │   └───proj.ios
│   │   │   │       │   AdsAdmob.h
│   │   │   │       │   AdsAdmob.m
│   │   │   │       │   PluginAdmob-Prefix.pch
│   │   │   │       │
│   │   │   │       ├───Admob
│   │   │   │       │       GADAdMobExtras.h
│   │   │   │       │       GADAdNetworkExtras.h
│   │   │   │       │       GADAdSize.h
│   │   │   │       │       GADBannerView.h
│   │   │   │       │       GADBannerViewDelegate.h
│   │   │   │       │       GADInAppPurchase.h
│   │   │   │       │       GADInAppPurchaseDelegate.h
│   │   │   │       │       GADInterstitial.h
│   │   │   │       │       GADInterstitialDelegate.h
│   │   │   │       │       GADModules.h
│   │   │   │       │       GADRequest.h
│   │   │   │       │       GADRequestError.h
│   │   │   │       │       libGoogleAdMobAds.a
│   │   │   │       │
│   │   │   │       └───PluginAdmob.xcodeproj
│   │   │   │               project.pbxproj
│   │   │   │
│   │   │   ├───alipay
│   │   │   │   └───proj.android
│   │   │   │       │   .classpath
│   │   │   │       │   .project
│   │   │   │       │   AndroidManifest.xml
│   │   │   │       │   build.xml
│   │   │   │       │   ForManifest.xml
│   │   │   │       │   project.properties
│   │   │   │       │
│   │   │   │       ├───ForAssets
│   │   │   │       │       alipay_plugin.apk
│   │   │   │       │
│   │   │   │       ├───sdk
│   │   │   │       │       alipay_plugin.jar
│   │   │   │       │
│   │   │   │       └───src
│   │   │   │           └───org
│   │   │   │               └───cocos2dx
│   │   │   │                   └───plugin
│   │   │   │                           AlixId.java
│   │   │   │                           Base64.java
│   │   │   │                           BaseHelper.java
│   │   │   │                           IAPAlipay.java
│   │   │   │                           MobileSecurePayer.java
│   │   │   │                           MobileSecurePayHelper.java
│   │   │   │                           NetworkManager.java
│   │   │   │                           PartnerConfig.java
│   │   │   │                           ResultChecker.java
│   │   │   │                           Rsa.java
│   │   │   │
│   │   │   ├───facebook
│   │   │   │   ├───proj.android
│   │   │   │   │   │   .classpath
│   │   │   │   │   │   .project
│   │   │   │   │   │   AndroidManifest.xml
│   │   │   │   │   │   build.xml
│   │   │   │   │   │   ForManifest.xml
│   │   │   │   │   │   proguard-project.txt
│   │   │   │   │   │   project.properties
│   │   │   │   │   │
│   │   │   │   │   ├───DependProject
│   │   │   │   │   │   │   .classpath
│   │   │   │   │   │   │   .project
│   │   │   │   │   │   │   AndroidManifest.xml
│   │   │   │   │   │   │   build.xml
│   │   │   │   │   │   │   project.properties
│   │   │   │   │   │   │
│   │   │   │   │   │   └───res
│   │   │   │   │   │       ├───drawable
│   │   │   │   │   │       │       com_facebook_button_blue.xml
│   │   │   │   │   │       │       com_facebook_button_blue_focused.9.png
│   │   │   │   │   │       │       com_facebook_button_blue_normal.9.png
│   │   │   │   │   │       │       com_facebook_button_blue_pressed.9.png
│   │   │   │   │   │       │       com_facebook_button_check.xml
│   │   │   │   │   │       │       com_facebook_button_check_off.png
│   │   │   │   │   │       │       com_facebook_button_check_on.png
│   │   │   │   │   │       │       com_facebook_button_grey_focused.9.png
│   │   │   │   │   │       │       com_facebook_button_grey_normal.9.png
│   │   │   │   │   │       │       com_facebook_button_grey_pressed.9.png
│   │   │   │   │   │       │       com_facebook_close.png
│   │   │   │   │   │       │       com_facebook_inverse_icon.png
│   │   │   │   │   │       │       com_facebook_list_divider.9.png
│   │   │   │   │   │       │       com_facebook_list_section_header_background.9.png
│   │   │   │   │   │       │       com_facebook_loginbutton_silver.xml
│   │   │   │   │   │       │       com_facebook_logo.png
│   │   │   │   │   │       │       com_facebook_picker_item_background.xml
│   │   │   │   │   │       │       com_facebook_picker_list_focused.9.png
│   │   │   │   │   │       │       com_facebook_picker_list_longpressed.9.png
│   │   │   │   │   │       │       com_facebook_picker_list_pressed.9.png
│   │   │   │   │   │       │       com_facebook_picker_list_selector.xml
│   │   │   │   │   │       │       com_facebook_picker_list_selector_background_transition.xml
│   │   │   │   │   │       │       com_facebook_picker_list_selector_disabled.9.png
│   │   │   │   │   │       │       com_facebook_picker_top_button.xml
│   │   │   │   │   │       │       com_facebook_place_default_icon.png
│   │   │   │   │   │       │       com_facebook_profile_default_icon.png
│   │   │   │   │   │       │       com_facebook_profile_picture_blank_portrait.png
│   │   │   │   │   │       │       com_facebook_profile_picture_blank_square.png
│   │   │   │   │   │       │       com_facebook_top_background.xml
│   │   │   │   │   │       │       com_facebook_top_button.xml
│   │   │   │   │   │       │       com_facebook_usersettingsfragment_background_gradient.xml
│   │   │   │   │   │       │
│   │   │   │   │   │       ├───drawable-hdpi
│   │   │   │   │   │       │       com_facebook_button_blue_focused.9.png
│   │   │   │   │   │       │       com_facebook_button_blue_normal.9.png
│   │   │   │   │   │       │       com_facebook_button_blue_pressed.9.png
│   │   │   │   │   │       │       com_facebook_button_grey_focused.9.png
│   │   │   │   │   │       │       com_facebook_button_grey_normal.9.png
│   │   │   │   │   │       │       com_facebook_button_grey_pressed.9.png
│   │   │   │   │   │       │       com_facebook_close.png
│   │   │   │   │   │       │       com_facebook_inverse_icon.png
│   │   │   │   │   │       │       com_facebook_logo.png
│   │   │   │   │   │       │       com_facebook_picker_magnifier.png
│   │   │   │   │   │       │       com_facebook_tooltip_black_background.9.png
│   │   │   │   │   │       │       com_facebook_tooltip_black_bottomnub.png
│   │   │   │   │   │       │       com_facebook_tooltip_black_topnub.png
│   │   │   │   │   │       │       com_facebook_tooltip_black_xout.png
│   │   │   │   │   │       │       com_facebook_tooltip_blue_background.9.png
│   │   │   │   │   │       │       com_facebook_tooltip_blue_bottomnub.png
│   │   │   │   │   │       │       com_facebook_tooltip_blue_topnub.png
│   │   │   │   │   │       │       com_facebook_tooltip_blue_xout.png
│   │   │   │   │   │       │
│   │   │   │   │   │       ├───drawable-ldpi
│   │   │   │   │   │       │       com_facebook_close.png
│   │   │   │   │   │       │
│   │   │   │   │   │       ├───drawable-mdpi
│   │   │   │   │   │       │       com_facebook_button_blue_focused.9.png
│   │   │   │   │   │       │       com_facebook_button_blue_normal.9.png
│   │   │   │   │   │       │       com_facebook_button_blue_pressed.9.png
│   │   │   │   │   │       │       com_facebook_inverse_icon.png
│   │   │   │   │   │       │       com_facebook_picker_magnifier.png
│   │   │   │   │   │       │       com_facebook_tooltip_black_background.9.png
│   │   │   │   │   │       │       com_facebook_tooltip_black_bottomnub.png
│   │   │   │   │   │       │       com_facebook_tooltip_black_topnub.png
│   │   │   │   │   │       │       com_facebook_tooltip_black_xout.png
│   │   │   │   │   │       │       com_facebook_tooltip_blue_background.9.png
│   │   │   │   │   │       │       com_facebook_tooltip_blue_bottomnub.png
│   │   │   │   │   │       │       com_facebook_tooltip_blue_topnub.png
│   │   │   │   │   │       │       com_facebook_tooltip_blue_xout.png
│   │   │   │   │   │       │
│   │   │   │   │   │       ├───drawable-xhdpi
│   │   │   │   │   │       │       com_facebook_button_blue_focused.9.png
│   │   │   │   │   │       │       com_facebook_button_blue_normal.9.png
│   │   │   │   │   │       │       com_facebook_button_blue_pressed.9.png
│   │   │   │   │   │       │       com_facebook_button_grey_focused.9.png
│   │   │   │   │   │       │       com_facebook_button_grey_normal.9.png
│   │   │   │   │   │       │       com_facebook_button_grey_pressed.9.png
│   │   │   │   │   │       │       com_facebook_close.png
│   │   │   │   │   │       │       com_facebook_inverse_icon.png
│   │   │   │   │   │       │       com_facebook_logo.png
│   │   │   │   │   │       │       com_facebook_picker_magnifier.png
│   │   │   │   │   │       │       com_facebook_tooltip_black_background.9.png
│   │   │   │   │   │       │       com_facebook_tooltip_black_bottomnub.png
│   │   │   │   │   │       │       com_facebook_tooltip_black_topnub.png
│   │   │   │   │   │       │       com_facebook_tooltip_black_xout.png
│   │   │   │   │   │       │       com_facebook_tooltip_blue_background.9.png
│   │   │   │   │   │       │       com_facebook_tooltip_blue_bottomnub.png
│   │   │   │   │   │       │       com_facebook_tooltip_blue_topnub.png
│   │   │   │   │   │       │       com_facebook_tooltip_blue_xout.png
│   │   │   │   │   │       │
│   │   │   │   │   │       ├───layout
│   │   │   │   │   │       │       com_facebook_friendpickerfragment.xml
│   │   │   │   │   │       │       com_facebook_login_activity_layout.xml
│   │   │   │   │   │       │       com_facebook_picker_activity_circle_row.xml
│   │   │   │   │   │       │       com_facebook_picker_checkbox.xml
│   │   │   │   │   │       │       com_facebook_picker_image.xml
│   │   │   │   │   │       │       com_facebook_picker_list_row.xml
│   │   │   │   │   │       │       com_facebook_picker_list_section_header.xml
│   │   │   │   │   │       │       com_facebook_picker_search_box.xml
│   │   │   │   │   │       │       com_facebook_picker_title_bar.xml
│   │   │   │   │   │       │       com_facebook_picker_title_bar_stub.xml
│   │   │   │   │   │       │       com_facebook_placepickerfragment.xml
│   │   │   │   │   │       │       com_facebook_placepickerfragment_list_row.xml
│   │   │   │   │   │       │       com_facebook_search_bar_layout.xml
│   │   │   │   │   │       │       com_facebook_tooltip_bubble.xml
│   │   │   │   │   │       │       com_facebook_usersettingsfragment.xml
│   │   │   │   │   │       │
│   │   │   │   │   │       ├───values
│   │   │   │   │   │       │       attrs.xml
│   │   │   │   │   │       │       colors.xml
│   │   │   │   │   │       │       drawables.xml
│   │   │   │   │   │       │       strings.xml
│   │   │   │   │   │       │       styles.xml
│   │   │   │   │   │       │
│   │   │   │   │   │       ├───values-es
│   │   │   │   │   │       │       strings.xml
│   │   │   │   │   │       │
│   │   │   │   │   │       ├───values-hdpi
│   │   │   │   │   │       │       dimens.xml
│   │   │   │   │   │       │
│   │   │   │   │   │       ├───values-he
│   │   │   │   │   │       │       strings.xml
│   │   │   │   │   │       │
│   │   │   │   │   │       ├───values-iw
│   │   │   │   │   │       │       strings.xml
│   │   │   │   │   │       │
│   │   │   │   │   │       ├───values-ldpi
│   │   │   │   │   │       │       dimens.xml
│   │   │   │   │   │       │
│   │   │   │   │   │       ├───values-mdpi
│   │   │   │   │   │       │       dimens.xml
│   │   │   │   │   │       │
│   │   │   │   │   │       └───values-xhdpi
│   │   │   │   │   │               dimens.xml
│   │   │   │   │   │
│   │   │   │   │   ├───sdk
│   │   │   │   │   │       android-support-v4.jar
│   │   │   │   │   │       bolts.jar
│   │   │   │   │   │       facebooksdk.jar
│   │   │   │   │   │
│   │   │   │   │   └───src
│   │   │   │   │       └───org
│   │   │   │   │           └───cocos2dx
│   │   │   │   │               └───plugin
│   │   │   │   │                       FacebookWrapper.java
│   │   │   │   │                       ShareFacebook.java
│   │   │   │   │                       UserFacebook.java
│   │   │   │   │
│   │   │   │   └───proj.ios
│   │   │   │       ├───FacebookSDK.framework
│   │   │   │       │   │   FacebookSDK
│   │   │   │       │   │
│   │   │   │       │   ├───Headers
│   │   │   │       │   │       FacebookSDK.h
│   │   │   │       │   │       FBAccessTokenData.h
│   │   │   │       │   │       FBAppCall.h
│   │   │   │       │   │       FBAppEvents.h
│   │   │   │       │   │       FBAppLinkData.h
│   │   │   │       │   │       FBAppLinkResolver.h
│   │   │   │       │   │       FBCacheDescriptor.h
│   │   │   │       │   │       FBColor.h
│   │   │   │       │   │       FBDialogs.h
│   │   │   │       │   │       FBDialogsData.h
│   │   │   │       │   │       FBDialogsParams.h
│   │   │   │       │   │       FBError.h
│   │   │   │       │   │       FBErrorUtility.h
│   │   │   │       │   │       FBFrictionlessRecipientCache.h
│   │   │   │       │   │       FBFriendPickerViewController.h
│   │   │   │       │   │       FBGraphLocation.h
│   │   │   │       │   │       FBGraphObject.h
│   │   │   │       │   │       FBGraphObjectPickerViewController.h
│   │   │   │       │   │       FBGraphPerson.h
│   │   │   │       │   │       FBGraphPlace.h
│   │   │   │       │   │       FBGraphUser.h
│   │   │   │       │   │       FBInsights.h
│   │   │   │       │   │       FBLikeControl.h
│   │   │   │       │   │       FBLinkShareParams.h
│   │   │   │       │   │       FBLoginTooltipView.h
│   │   │   │       │   │       FBLoginView.h
│   │   │   │       │   │       FBNativeDialogs.h
│   │   │   │       │   │       FBOpenGraphAction.h
│   │   │   │       │   │       FBOpenGraphActionParams.h
│   │   │   │       │   │       FBOpenGraphActionShareDialogParams.h
│   │   │   │       │   │       FBOpenGraphObject.h
│   │   │   │       │   │       FBPeoplePickerViewController.h
│   │   │   │       │   │       FBPhotoParams.h
│   │   │   │       │   │       FBPlacePickerViewController.h
│   │   │   │       │   │       FBProfilePictureView.h
│   │   │   │       │   │       FBRequest.h
│   │   │   │       │   │       FBRequestConnection.h
│   │   │   │       │   │       FBSDKMacros.h
│   │   │   │       │   │       FBSession.h
│   │   │   │       │   │       FBSessionTokenCachingStrategy.h
│   │   │   │       │   │       FBSettings.h
│   │   │   │       │   │       FBShareDialogParams.h
│   │   │   │       │   │       FBShareDialogPhotoParams.h
│   │   │   │       │   │       FBTaggableFriendPickerViewController.h
│   │   │   │       │   │       FBTestSession.h
│   │   │   │       │   │       FBTooltipView.h
│   │   │   │       │   │       FBUserSettingsViewController.h
│   │   │   │       │   │       FBViewController.h
│   │   │   │       │   │       FBWebDialogs.h
│   │   │   │       │   │       NSError+FBError.h
│   │   │   │       │   │
│   │   │   │       │   ├───Resources
│   │   │   │       │   │   │   FacebookSDKResources.bundle.README
│   │   │   │       │   │   │   Info.plist
│   │   │   │       │   │   │
│   │   │   │       │   │   └───FBUserSettingsViewResources.bundle
│   │   │   │       │   │       ├───Contents
│   │   │   │       │   │       │   └───Resources
│   │   │   │       │   │       │       ├───en.lproj
│   │   │   │       │   │       │       │       Localizable.strings
│   │   │   │       │   │       │       │
│   │   │   │       │   │       │       └───he.lproj
│   │   │   │       │   │       │               Localizable.strings
│   │   │   │       │   │       │
│   │   │   │       │   │       └───images
│   │   │   │       │   │               facebook-logo.png
│   │   │   │       │   │               facebook-logo@2x.png
│   │   │   │       │   │               loginBackgroundIPadLandscape.jpg
│   │   │   │       │   │               loginBackgroundIPadLandscape@2x.jpg
│   │   │   │       │   │               loginBackgroundIPadPortrait.jpg
│   │   │   │       │   │               loginBackgroundIPadPortrait@2x.jpg
│   │   │   │       │   │               loginBackgroundIPhonePortrait.jpg
│   │   │   │       │   │               loginBackgroundIPhonePortrait@2x.jpg
│   │   │   │       │   │               silver-button-normal.png
│   │   │   │       │   │               silver-button-normal@2x.png
│   │   │   │       │   │               silver-button-pressed.png
│   │   │   │       │   │               silver-button-pressed@2x.png
│   │   │   │       │   │
│   │   │   │       │   └───Versions
│   │   │   │       │       ├───A
│   │   │   │       │       │   │   FacebookSDK
│   │   │   │       │       │   │
│   │   │   │       │       │   ├───DeprecatedHeaders
│   │   │   │       │       │   │       Facebook.h
│   │   │   │       │       │   │       FacebookSDK.h
│   │   │   │       │       │   │       FBAccessTokenData.h
│   │   │   │       │       │   │       FBAppCall.h
│   │   │   │       │       │   │       FBAppEvents.h
│   │   │   │       │       │   │       FBAppLinkData.h
│   │   │   │       │       │   │       FBAppLinkResolver.h
│   │   │   │       │       │   │       FBCacheDescriptor.h
│   │   │   │       │       │   │       FBColor.h
│   │   │   │       │       │   │       FBConnect.h
│   │   │   │       │       │   │       FBDialog.h
│   │   │   │       │       │   │       FBDialogs.h
│   │   │   │       │       │   │       FBDialogsData.h
│   │   │   │       │       │   │       FBDialogsParams.h
│   │   │   │       │       │   │       FBError.h
│   │   │   │       │       │   │       FBErrorUtility.h
│   │   │   │       │       │   │       FBFrictionlessRecipientCache.h
│   │   │   │       │       │   │       FBFrictionlessRequestSettings.h
│   │   │   │       │       │   │       FBFriendPickerViewController.h
│   │   │   │       │       │   │       FBGraphLocation.h
│   │   │   │       │       │   │       FBGraphObject.h
│   │   │   │       │       │   │       FBGraphObjectPickerViewController.h
│   │   │   │       │       │   │       FBGraphPerson.h
│   │   │   │       │       │   │       FBGraphPlace.h
│   │   │   │       │       │   │       FBGraphUser.h
│   │   │   │       │       │   │       FBInsights.h
│   │   │   │       │       │   │       FBLikeControl.h
│   │   │   │       │       │   │       FBLinkShareParams.h
│   │   │   │       │       │   │       FBLoginDialog.h
│   │   │   │       │       │   │       FBLoginTooltipView.h
│   │   │   │       │       │   │       FBLoginView.h
│   │   │   │       │       │   │       FBNativeDialogs.h
│   │   │   │       │       │   │       FBOpenGraphAction.h
│   │   │   │       │       │   │       FBOpenGraphActionParams.h
│   │   │   │       │       │   │       FBOpenGraphActionShareDialogParams.h
│   │   │   │       │       │   │       FBOpenGraphObject.h
│   │   │   │       │       │   │       FBPeoplePickerViewController.h
│   │   │   │       │       │   │       FBPhotoParams.h
│   │   │   │       │       │   │       FBPlacePickerViewController.h
│   │   │   │       │       │   │       FBProfilePictureView.h
│   │   │   │       │       │   │       FBRequest.h
│   │   │   │       │       │   │       FBRequestConnection.h
│   │   │   │       │       │   │       FBSDKMacros.h
│   │   │   │       │       │   │       FBSession.h
│   │   │   │       │       │   │       FBSessionManualTokenCachingStrategy.h
│   │   │   │       │       │   │       FBSessionTokenCachingStrategy.h
│   │   │   │       │       │   │       FBSettings.h
│   │   │   │       │       │   │       FBShareDialogParams.h
│   │   │   │       │       │   │       FBShareDialogPhotoParams.h
│   │   │   │       │       │   │       FBTaggableFriendPickerViewController.h
│   │   │   │       │       │   │       FBTestSession.h
│   │   │   │       │       │   │       FBTooltipView.h
│   │   │   │       │       │   │       FBUserSettingsViewController.h
│   │   │   │       │       │   │       FBViewController.h
│   │   │   │       │       │   │       FBWebDialogs.h
│   │   │   │       │       │   │       NSError+FBError.h
│   │   │   │       │       │   │
│   │   │   │       │       │   ├───Headers
│   │   │   │       │       │   │       FacebookSDK.h
│   │   │   │       │       │   │       FBAccessTokenData.h
│   │   │   │       │       │   │       FBAppCall.h
│   │   │   │       │       │   │       FBAppEvents.h
│   │   │   │       │       │   │       FBAppLinkData.h
│   │   │   │       │       │   │       FBAppLinkResolver.h
│   │   │   │       │       │   │       FBCacheDescriptor.h
│   │   │   │       │       │   │       FBColor.h
│   │   │   │       │       │   │       FBDialogs.h
│   │   │   │       │       │   │       FBDialogsData.h
│   │   │   │       │       │   │       FBDialogsParams.h
│   │   │   │       │       │   │       FBError.h
│   │   │   │       │       │   │       FBErrorUtility.h
│   │   │   │       │       │   │       FBFrictionlessRecipientCache.h
│   │   │   │       │       │   │       FBFriendPickerViewController.h
│   │   │   │       │       │   │       FBGraphLocation.h
│   │   │   │       │       │   │       FBGraphObject.h
│   │   │   │       │       │   │       FBGraphObjectPickerViewController.h
│   │   │   │       │       │   │       FBGraphPerson.h
│   │   │   │       │       │   │       FBGraphPlace.h
│   │   │   │       │       │   │       FBGraphUser.h
│   │   │   │       │       │   │       FBInsights.h
│   │   │   │       │       │   │       FBLikeControl.h
│   │   │   │       │       │   │       FBLinkShareParams.h
│   │   │   │       │       │   │       FBLoginTooltipView.h
│   │   │   │       │       │   │       FBLoginView.h
│   │   │   │       │       │   │       FBNativeDialogs.h
│   │   │   │       │       │   │       FBOpenGraphAction.h
│   │   │   │       │       │   │       FBOpenGraphActionParams.h
│   │   │   │       │       │   │       FBOpenGraphActionShareDialogParams.h
│   │   │   │       │       │   │       FBOpenGraphObject.h
│   │   │   │       │       │   │       FBPeoplePickerViewController.h
│   │   │   │       │       │   │       FBPhotoParams.h
│   │   │   │       │       │   │       FBPlacePickerViewController.h
│   │   │   │       │       │   │       FBProfilePictureView.h
│   │   │   │       │       │   │       FBRequest.h
│   │   │   │       │       │   │       FBRequestConnection.h
│   │   │   │       │       │   │       FBSDKMacros.h
│   │   │   │       │       │   │       FBSession.h
│   │   │   │       │       │   │       FBSessionTokenCachingStrategy.h
│   │   │   │       │       │   │       FBSettings.h
│   │   │   │       │       │   │       FBShareDialogParams.h
│   │   │   │       │       │   │       FBShareDialogPhotoParams.h
│   │   │   │       │       │   │       FBTaggableFriendPickerViewController.h
│   │   │   │       │       │   │       FBTestSession.h
│   │   │   │       │       │   │       FBTooltipView.h
│   │   │   │       │       │   │       FBUserSettingsViewController.h
│   │   │   │       │       │   │       FBViewController.h
│   │   │   │       │       │   │       FBWebDialogs.h
│   │   │   │       │       │   │       NSError+FBError.h
│   │   │   │       │       │   │
│   │   │   │       │       │   └───Resources
│   │   │   │       │       │       │   FacebookSDKResources.bundle.README
│   │   │   │       │       │       │   Info.plist
│   │   │   │       │       │       │
│   │   │   │       │       │       └───FBUserSettingsViewResources.bundle
│   │   │   │       │       │           ├───Contents
│   │   │   │       │       │           │   └───Resources
│   │   │   │       │       │           │       ├───en.lproj
│   │   │   │       │       │           │       │       Localizable.strings
│   │   │   │       │       │           │       │
│   │   │   │       │       │           │       └───he.lproj
│   │   │   │       │       │           │               Localizable.strings
│   │   │   │       │       │           │
│   │   │   │       │       │           └───images
│   │   │   │       │       │                   facebook-logo.png
│   │   │   │       │       │                   facebook-logo@2x.png
│   │   │   │       │       │                   loginBackgroundIPadLandscape.jpg
│   │   │   │       │       │                   loginBackgroundIPadLandscape@2x.jpg
│   │   │   │       │       │                   loginBackgroundIPadPortrait.jpg
│   │   │   │       │       │                   loginBackgroundIPadPortrait@2x.jpg
│   │   │   │       │       │                   loginBackgroundIPhonePortrait.jpg
│   │   │   │       │       │                   loginBackgroundIPhonePortrait@2x.jpg
│   │   │   │       │       │                   silver-button-normal.png
│   │   │   │       │       │                   silver-button-normal@2x.png
│   │   │   │       │       │                   silver-button-pressed.png
│   │   │   │       │       │                   silver-button-pressed@2x.png
│   │   │   │       │       │
│   │   │   │       │       └───Current
│   │   │   │       │           │   FacebookSDK
│   │   │   │       │           │
│   │   │   │       │           ├───DeprecatedHeaders
│   │   │   │       │           │       Facebook.h
│   │   │   │       │           │       FacebookSDK.h
│   │   │   │       │           │       FBAccessTokenData.h
│   │   │   │       │           │       FBAppCall.h
│   │   │   │       │           │       FBAppEvents.h
│   │   │   │       │           │       FBAppLinkData.h
│   │   │   │       │           │       FBAppLinkResolver.h
│   │   │   │       │           │       FBCacheDescriptor.h
│   │   │   │       │           │       FBColor.h
│   │   │   │       │           │       FBConnect.h
│   │   │   │       │           │       FBDialog.h
│   │   │   │       │           │       FBDialogs.h
│   │   │   │       │           │       FBDialogsData.h
│   │   │   │       │           │       FBDialogsParams.h
│   │   │   │       │           │       FBError.h
│   │   │   │       │           │       FBErrorUtility.h
│   │   │   │       │           │       FBFrictionlessRecipientCache.h
│   │   │   │       │           │       FBFrictionlessRequestSettings.h
│   │   │   │       │           │       FBFriendPickerViewController.h
│   │   │   │       │           │       FBGraphLocation.h
│   │   │   │       │           │       FBGraphObject.h
│   │   │   │       │           │       FBGraphObjectPickerViewController.h
│   │   │   │       │           │       FBGraphPerson.h
│   │   │   │       │           │       FBGraphPlace.h
│   │   │   │       │           │       FBGraphUser.h
│   │   │   │       │           │       FBInsights.h
│   │   │   │       │           │       FBLikeControl.h
│   │   │   │       │           │       FBLinkShareParams.h
│   │   │   │       │           │       FBLoginDialog.h
│   │   │   │       │           │       FBLoginTooltipView.h
│   │   │   │       │           │       FBLoginView.h
│   │   │   │       │           │       FBNativeDialogs.h
│   │   │   │       │           │       FBOpenGraphAction.h
│   │   │   │       │           │       FBOpenGraphActionParams.h
│   │   │   │       │           │       FBOpenGraphActionShareDialogParams.h
│   │   │   │       │           │       FBOpenGraphObject.h
│   │   │   │       │           │       FBPeoplePickerViewController.h
│   │   │   │       │           │       FBPhotoParams.h
│   │   │   │       │           │       FBPlacePickerViewController.h
│   │   │   │       │           │       FBProfilePictureView.h
│   │   │   │       │           │       FBRequest.h
│   │   │   │       │           │       FBRequestConnection.h
│   │   │   │       │           │       FBSDKMacros.h
│   │   │   │       │           │       FBSession.h
│   │   │   │       │           │       FBSessionManualTokenCachingStrategy.h
│   │   │   │       │           │       FBSessionTokenCachingStrategy.h
│   │   │   │       │           │       FBSettings.h
│   │   │   │       │           │       FBShareDialogParams.h
│   │   │   │       │           │       FBShareDialogPhotoParams.h
│   │   │   │       │           │       FBTaggableFriendPickerViewController.h
│   │   │   │       │           │       FBTestSession.h
│   │   │   │       │           │       FBTooltipView.h
│   │   │   │       │           │       FBUserSettingsViewController.h
│   │   │   │       │           │       FBViewController.h
│   │   │   │       │           │       FBWebDialogs.h
│   │   │   │       │           │       NSError+FBError.h
│   │   │   │       │           │
│   │   │   │       │           ├───Headers
│   │   │   │       │           │       FacebookSDK.h
│   │   │   │       │           │       FBAccessTokenData.h
│   │   │   │       │           │       FBAppCall.h
│   │   │   │       │           │       FBAppEvents.h
│   │   │   │       │           │       FBAppLinkData.h
│   │   │   │       │           │       FBAppLinkResolver.h
│   │   │   │       │           │       FBCacheDescriptor.h
│   │   │   │       │           │       FBColor.h
│   │   │   │       │           │       FBDialogs.h
│   │   │   │       │           │       FBDialogsData.h
│   │   │   │       │           │       FBDialogsParams.h
│   │   │   │       │           │       FBError.h
│   │   │   │       │           │       FBErrorUtility.h
│   │   │   │       │           │       FBFrictionlessRecipientCache.h
│   │   │   │       │           │       FBFriendPickerViewController.h
│   │   │   │       │           │       FBGraphLocation.h
│   │   │   │       │           │       FBGraphObject.h
│   │   │   │       │           │       FBGraphObjectPickerViewController.h
│   │   │   │       │           │       FBGraphPerson.h
│   │   │   │       │           │       FBGraphPlace.h
│   │   │   │       │           │       FBGraphUser.h
│   │   │   │       │           │       FBInsights.h
│   │   │   │       │           │       FBLikeControl.h
│   │   │   │       │           │       FBLinkShareParams.h
│   │   │   │       │           │       FBLoginTooltipView.h
│   │   │   │       │           │       FBLoginView.h
│   │   │   │       │           │       FBNativeDialogs.h
│   │   │   │       │           │       FBOpenGraphAction.h
│   │   │   │       │           │       FBOpenGraphActionParams.h
│   │   │   │       │           │       FBOpenGraphActionShareDialogParams.h
│   │   │   │       │           │       FBOpenGraphObject.h
│   │   │   │       │           │       FBPeoplePickerViewController.h
│   │   │   │       │           │       FBPhotoParams.h
│   │   │   │       │           │       FBPlacePickerViewController.h
│   │   │   │       │           │       FBProfilePictureView.h
│   │   │   │       │           │       FBRequest.h
│   │   │   │       │           │       FBRequestConnection.h
│   │   │   │       │           │       FBSDKMacros.h
│   │   │   │       │           │       FBSession.h
│   │   │   │       │           │       FBSessionTokenCachingStrategy.h
│   │   │   │       │           │       FBSettings.h
│   │   │   │       │           │       FBShareDialogParams.h
│   │   │   │       │           │       FBShareDialogPhotoParams.h
│   │   │   │       │           │       FBTaggableFriendPickerViewController.h
│   │   │   │       │           │       FBTestSession.h
│   │   │   │       │           │       FBTooltipView.h
│   │   │   │       │           │       FBUserSettingsViewController.h
│   │   │   │       │           │       FBViewController.h
│   │   │   │       │           │       FBWebDialogs.h
│   │   │   │       │           │       NSError+FBError.h
│   │   │   │       │           │
│   │   │   │       │           └───Resources
│   │   │   │       │               │   FacebookSDKResources.bundle.README
│   │   │   │       │               │   Info.plist
│   │   │   │       │               │
│   │   │   │       │               └───FBUserSettingsViewResources.bundle
│   │   │   │       │                   ├───Contents
│   │   │   │       │                   │   └───Resources
│   │   │   │       │                   │       ├───en.lproj
│   │   │   │       │                   │       │       Localizable.strings
│   │   │   │       │                   │       │
│   │   │   │       │                   │       └───he.lproj
│   │   │   │       │                   │               Localizable.strings
│   │   │   │       │                   │
│   │   │   │       │                   └───images
│   │   │   │       │                           facebook-logo.png
│   │   │   │       │                           facebook-logo@2x.png
│   │   │   │       │                           loginBackgroundIPadLandscape.jpg
│   │   │   │       │                           loginBackgroundIPadLandscape@2x.jpg
│   │   │   │       │                           loginBackgroundIPadPortrait.jpg
│   │   │   │       │                           loginBackgroundIPadPortrait@2x.jpg
│   │   │   │       │                           loginBackgroundIPhonePortrait.jpg
│   │   │   │       │                           loginBackgroundIPhonePortrait@2x.jpg
│   │   │   │       │                           silver-button-normal.png
│   │   │   │       │                           silver-button-normal@2x.png
│   │   │   │       │                           silver-button-pressed.png
│   │   │   │       │                           silver-button-pressed@2x.png
│   │   │   │       │
│   │   │   │       ├───PluginFacebook
│   │   │   │       │       PluginFacebook-Prefix.pch
│   │   │   │       │       ShareFacebook.h
│   │   │   │       │       ShareFacebook.m
│   │   │   │       │       UserFacebook.h
│   │   │   │       │       UserFacebook.m
│   │   │   │       │
│   │   │   │       └───PluginFacebook.xcodeproj
│   │   │   │               project.pbxproj
│   │   │   │
│   │   │   ├───facebookads
│   │   │   │   ├───proj.android
│   │   │   │   │   │   .classpath
│   │   │   │   │   │   .project
│   │   │   │   │   │   AndroidManifest.xml
│   │   │   │   │   │   build.xml
│   │   │   │   │   │   ForManifest.xml
│   │   │   │   │   │   proguard-project.txt
│   │   │   │   │   │   project.properties
│   │   │   │   │   │
│   │   │   │   │   ├───res
│   │   │   │   │   │   ├───values
│   │   │   │   │   │   │       layouts.xml
│   │   │   │   │   │   │
│   │   │   │   │   │   ├───values-large
│   │   │   │   │   │   │       layout.xml
│   │   │   │   │   │   │
│   │   │   │   │   │   └───values-sw600dp
│   │   │   │   │   │           layout.xml
│   │   │   │   │   │
│   │   │   │   │   ├───sdk
│   │   │   │   │   │       android-support-v4.jar
│   │   │   │   │   │       AudienceNetwork.jar
│   │   │   │   │   │
│   │   │   │   │   └───src
│   │   │   │   │       └───org
│   │   │   │   │           └───cocos2dx
│   │   │   │   │               └───plugin
│   │   │   │   │                       AdsFacebook.java
│   │   │   │   │
│   │   │   │   └───proj.ios
│   │   │   │       ├───FBAudienceNetwork.framework
│   │   │   │       │   │   FBAudienceNetwork
│   │   │   │       │   │
│   │   │   │       │   ├───Headers
│   │   │   │       │   │       FBAdImage.h
│   │   │   │       │   │       FBAdSettings.h
│   │   │   │       │   │       FBAdView.h
│   │   │   │       │   │       FBAudienceNetwork.h
│   │   │   │       │   │       FBInterstitialAd.h
│   │   │   │       │   │       FBNativeAd.h
│   │   │   │       │   │
│   │   │   │       │   └───Versions
│   │   │   │       │       ├───A
│   │   │   │       │       │   │   FBAudienceNetwork
│   │   │   │       │       │   │
│   │   │   │       │       │   ├───DeprecatedHeaders
│   │   │   │       │       │   │       FBAdImage.h
│   │   │   │       │       │   │       FBAdSettings.h
│   │   │   │       │       │   │       FBAdView.h
│   │   │   │       │       │   │       FBAudienceNetwork.h
│   │   │   │       │       │   │       FBInterstitialAd.h
│   │   │   │       │       │   │       FBNativeAd.h
│   │   │   │       │       │   │
│   │   │   │       │       │   └───Headers
│   │   │   │       │       │           FBAdImage.h
│   │   │   │       │       │           FBAdSettings.h
│   │   │   │       │       │           FBAdView.h
│   │   │   │       │       │           FBAudienceNetwork.h
│   │   │   │       │       │           FBInterstitialAd.h
│   │   │   │       │       │           FBNativeAd.h
│   │   │   │       │       │
│   │   │   │       │       └───Current
│   │   │   │       │           │   FBAudienceNetwork
│   │   │   │       │           │
│   │   │   │       │           ├───DeprecatedHeaders
│   │   │   │       │           │       FBAdImage.h
│   │   │   │       │           │       FBAdSettings.h
│   │   │   │       │           │       FBAdView.h
│   │   │   │       │           │       FBAudienceNetwork.h
│   │   │   │       │           │       FBInterstitialAd.h
│   │   │   │       │           │       FBNativeAd.h
│   │   │   │       │           │
│   │   │   │       │           └───Headers
│   │   │   │       │                   FBAdImage.h
│   │   │   │       │                   FBAdSettings.h
│   │   │   │       │                   FBAdView.h
│   │   │   │       │                   FBAudienceNetwork.h
│   │   │   │       │                   FBInterstitialAd.h
│   │   │   │       │                   FBNativeAd.h
│   │   │   │       │
│   │   │   │       ├───PluginFacebookAds
│   │   │   │       │       AdsFacebook.h
│   │   │   │       │       AdsFacebook.m
│   │   │   │       │       PluginFacebookAds-Prefix.pch
│   │   │   │       │
│   │   │   │       └───PluginFacebookAds.xcodeproj
│   │   │   │               project.pbxproj
│   │   │   │
│   │   │   ├───flurry
│   │   │   │   ├───proj.android
│   │   │   │   │   │   .classpath
│   │   │   │   │   │   .project
│   │   │   │   │   │   AndroidManifest.xml
│   │   │   │   │   │   build.xml
│   │   │   │   │   │   ForManifest.xml
│   │   │   │   │   │   project.properties
│   │   │   │   │   │
│   │   │   │   │   ├───sdk
│   │   │   │   │   │       FlurryAgent.jar
│   │   │   │   │   │
│   │   │   │   │   └───src
│   │   │   │   │       └───org
│   │   │   │   │           └───cocos2dx
│   │   │   │   │               └───plugin
│   │   │   │   │                       AdsFlurry.java
│   │   │   │   │                       AnalyticsFlurry.java
│   │   │   │   │
│   │   │   │   └───proj.ios
│   │   │   │       │   AdsFlurry.h
│   │   │   │       │   AdsFlurry.m
│   │   │   │       │   AnalyticsFlurry.h
│   │   │   │       │   AnalyticsFlurry.m
│   │   │   │       │   Flurry.h
│   │   │   │       │   libFlurry.a
│   │   │   │       │   PluginFlurry-Prefix.pch
│   │   │   │       │
│   │   │   │       ├───FlurryAds
│   │   │   │       │       FlurryAdDelegate.h
│   │   │   │       │       FlurryAds.h
│   │   │   │       │       libFlurryAds.a
│   │   │   │       │
│   │   │   │       └───PluginFlurry.xcodeproj
│   │   │   │               project.pbxproj
│   │   │   │
│   │   │   ├───googleplay
│   │   │   │   │   Readme.md
│   │   │   │   │
│   │   │   │   └───proj.android
│   │   │   │       │   .classpath
│   │   │   │       │   .project
│   │   │   │       │   AndroidManifest.xml
│   │   │   │       │   build.xml
│   │   │   │       │   ForManifest.xml
│   │   │   │       │   Notes.txt
│   │   │   │       │   proguard-project.txt
│   │   │   │       │   project.properties
│   │   │   │       │
│   │   │   │       └───src
│   │   │   │           ├───com
│   │   │   │           │   └───android
│   │   │   │           │       └───vending
│   │   │   │           │           └───billing
│   │   │   │           │                   IInAppBillingService.aidl
│   │   │   │           │
│   │   │   │           └───org
│   │   │   │               └───cocos2dx
│   │   │   │                   └───plugin
│   │   │   │                       │   IAPGooglePlay.java
│   │   │   │                       │
│   │   │   │                       └───util
│   │   │   │                               Base64.java
│   │   │   │                               Base64DecoderException.java
│   │   │   │                               IabException.java
│   │   │   │                               IabHelper.java
│   │   │   │                               IabResult.java
│   │   │   │                               Inventory.java
│   │   │   │                               Purchase.java
│   │   │   │                               Security.java
│   │   │   │                               SkuDetails.java
│   │   │   │
│   │   │   ├───iosiap
│   │   │   │   └───proj.ios
│   │   │   │       ├───IOSIAP
│   │   │   │       │       IOSIAP.h
│   │   │   │       │       IOSIAP.m
│   │   │   │       │       PluginIAP-Prefix.pch
│   │   │   │       │
│   │   │   │       └───PluginIAP.xcodeproj
│   │   │   │               project.pbxproj
│   │   │   │
│   │   │   ├───nd91
│   │   │   │   └───proj.android
│   │   │   │       │   .classpath
│   │   │   │       │   .project
│   │   │   │       │   AndroidManifest.xml
│   │   │   │       │   build.xml
│   │   │   │       │   ForManifest.xml
│   │   │   │       │   project.properties
│   │   │   │       │
│   │   │   │       ├───DependProject
│   │   │   │       │   │   .classpath
│   │   │   │       │   │   .project
│   │   │   │       │   │   AndroidManifest.xml
│   │   │   │       │   │   project.properties
│   │   │   │       │   │
│   │   │   │       │   └───res
│   │   │   │       │       ├───anim
│   │   │   │       │       │       nd_flipin.xml
│   │   │   │       │       │       nd_flipin_reverse.xml
│   │   │   │       │       │       nd_flipout.xml
│   │   │   │       │       │       nd_flipout_reverse.xml
│   │   │   │       │       │
│   │   │   │       │       ├───drawable
│   │   │   │       │       │       nd3_3rd_platform_icon.png
│   │   │   │       │       │       nd3_3rd_platform_icon_more.png
│   │   │   │       │       │       nd3_91.png
│   │   │   │       │       │       nd3_achieve.png
│   │   │   │       │       │       nd3_achievement_lock.png
│   │   │   │       │       │       nd3_activity_action_above_bg.9.png
│   │   │   │       │       │       nd3_add.png
│   │   │   │       │       │       nd3_agreement_logo.png
│   │   │   │       │       │       nd3_app_icon_default.png
│   │   │   │       │       │       nd3_background.png
│   │   │   │       │       │       nd3_background_xml.xml
│   │   │   │       │       │       nd3_banner.9.png
│   │   │   │       │       │       nd3_banner_bg.9.png
│   │   │   │       │       │       nd3_banner_logo.png
│   │   │   │       │       │       nd3_bbs_icon.png
│   │   │   │       │       │       nd3_bg.png
│   │   │   │       │       │       nd3_bizarre_image.png
│   │   │   │       │       │       nd3_bk1.9.png
│   │   │   │       │       │       nd3_bm.9.png
│   │   │   │       │       │       nd3_bnt_01.9.png
│   │   │   │       │       │       nd3_bnt_zhuxiao.png
│   │   │   │       │       │       nd3_bottom_bar_bg.9.png
│   │   │   │       │       │       nd3_button.xml
│   │   │   │       │       │       nd3_button1.png
│   │   │   │       │       │       nd3_button2.png
│   │   │   │       │       │       nd3_button_02.xml
│   │   │   │       │       │       nd3_button_130_01.png
│   │   │   │       │       │       nd3_button_130_03.png
│   │   │   │       │       │       nd3_button_278.png
│   │   │   │       │       │       nd3_button_action.xml
│   │   │   │       │       │       nd3_button_bg_02.png
│   │   │   │       │       │       nd3_button_bg_02_press.png
│   │   │   │       │       │       nd3_button_bg_dis.png
│   │   │   │       │       │       nd3_button_bg_dis02.png
│   │   │   │       │       │       nd3_button_logout.xml
│   │   │   │       │       │       nd3_button_long.9.png
│   │   │   │       │       │       nd3_button_long_press.9.png
│   │   │   │       │       │       nd3_button_old.xml
│   │   │   │       │       │       nd3_button_radio.png
│   │   │   │       │       │       nd3_button_x.xml
│   │   │   │       │       │       nd3_button_x1.png
│   │   │   │       │       │       nd3_checkbox_button.xml
│   │   │   │       │       │       nd3_check_yes.png
│   │   │   │       │       │       nd3_close.png
│   │   │   │       │       │       nd3_default_portrait.png
│   │   │   │       │       │       nd3_default_portrait_big.png
│   │   │   │       │       │       nd3_friend_del_button.xml
│   │   │   │       │       │       nd3_friend_section_bg.9.png
│   │   │   │       │       │       nd3_game_detail.png
│   │   │   │       │       │       nd3_game_error_bg.png
│   │   │   │       │       │       nd3_game_face.png
│   │   │   │       │       │       nd3_game_head.png
│   │   │   │       │       │       nd3_headbar.png
│   │   │   │       │       │       nd3_head_bg.png
│   │   │   │       │       │       nd3_horizontal_line.9.png
│   │   │   │       │       │       nd3_icon11.png
│   │   │   │       │       │       nd3_icon12.png
│   │   │   │       │       │       nd3_icon_01.png
│   │   │   │       │       │       nd3_icon_05.png
│   │   │   │       │       │       nd3_icon_06.png
│   │   │   │       │       │       nd3_icon_07.png
│   │   │   │       │       │       nd3_icon_08.png
│   │   │   │       │       │       nd3_icon_21.png
│   │   │   │       │       │       nd3_icon_22.png
│   │   │   │       │       │       nd3_icon_error.png
│   │   │   │       │       │       nd3_icon_more01.png
│   │   │   │       │       │       nd3_icon_more02.png
│   │   │   │       │       │       nd3_icon_more03.png
│   │   │   │       │       │       nd3_icon_more04.png
│   │   │   │       │       │       nd3_icon_more05.png
│   │   │   │       │       │       nd3_icon_more06.png
│   │   │   │       │       │       nd3_icon_point.png
│   │   │   │       │       │       nd3_icon_selected.png
│   │   │   │       │       │       nd3_image81.png
│   │   │   │       │       │       nd3_image82.png
│   │   │   │       │       │       nd3_image_48_bg.xml
│   │   │   │       │       │       nd3_inputbox_bg1.9.png
│   │   │   │       │       │       nd3_input_1.9.png
│   │   │   │       │       │       nd3_input_2.9.png
│   │   │   │       │       │       nd3_input_bg.png
│   │   │   │       │       │       nd3_input_gray.xml
│   │   │   │       │       │       nd3_invite_image.png
│   │   │   │       │       │       nd3_leaderboard_default.png
│   │   │   │       │       │       nd3_line.9.png
│   │   │   │       │       │       nd3_list_bg.9.png
│   │   │   │       │       │       nd3_list_separator.png
│   │   │   │       │       │       nd3_mainfriend_1.png
│   │   │   │       │       │       nd3_mainfriend_2.png
│   │   │   │       │       │       nd3_maingame_1.png
│   │   │   │       │       │       nd3_maingame_2.png
│   │   │   │       │       │       nd3_mainmessage_1.png
│   │   │   │       │       │       nd3_mainmessage_2.png
│   │   │   │       │       │       nd3_mainmore_1.png
│   │   │   │       │       │       nd3_mainmore_2.png
│   │   │   │       │       │       nd3_mainpage_1.png
│   │   │   │       │       │       nd3_mainpage_2.png
│   │   │   │       │       │       nd3_message_item_1_bg.xml
│   │   │   │       │       │       nd3_message_item_2_bg.xml
│   │   │   │       │       │       nd3_mood_bg.9.png
│   │   │   │       │       │       nd3_msge_friend.9.png
│   │   │   │       │       │       nd3_msge_owen.9.png
│   │   │   │       │       │       nd3_new_message.9.png
│   │   │   │       │       │       nd3_new_message_flag.png
│   │   │   │       │       │       nd3_pay_checkbox_button.xml
│   │   │   │       │       │       nd3_platform_logo.png
│   │   │   │       │       │       nd3_portrait_edit_bg.png
│   │   │   │       │       │       nd3_progress_large.xml
│   │   │   │       │       │       nd3_rank_1.png
│   │   │   │       │       │       nd3_rank_2.png
│   │   │   │       │       │       nd3_rank_3.png
│   │   │   │       │       │       nd3_rank_choice_left_1.9.png
│   │   │   │       │       │       nd3_rank_choice_left_2.9.png
│   │   │   │       │       │       nd3_rank_choice_left_btn_bg.xml
│   │   │   │       │       │       nd3_rank_choice_middle_1.9.png
│   │   │   │       │       │       nd3_rank_choice_middle_2.9.png
│   │   │   │       │       │       nd3_rank_choice_middle_btn_bg.xml
│   │   │   │       │       │       nd3_rank_choice_right_1.9.png
│   │   │   │       │       │       nd3_rank_choice_right_2.9.png
│   │   │   │       │       │       nd3_rank_choice_right_btn_bg.xml
│   │   │   │       │       │       nd3_rank_image.png
│   │   │   │       │       │       nd3_redbtn.9.png
│   │   │   │       │       │       nd3_redbtn_down.9.png
│   │   │   │       │       │       nd3_regist_checked.xml
│   │   │   │       │       │       nd3_round_bg.xml
│   │   │   │       │       │       nd3_search_edit_bg.9.png
│   │   │   │       │       │       nd3_search_edit_left.9.png
│   │   │   │       │       │       nd3_search_layout_bg.9.png
│   │   │   │       │       │       nd3_showplayer.png
│   │   │   │       │       │       nd3_square_checkbox_button.xml
│   │   │   │       │       │       nd3_switch_image.png
│   │   │   │       │       │       nd3_switch_image_white.png
│   │   │   │       │       │       nd3_title_bar_action_btn.9.png
│   │   │   │       │       │       nd3_title_bar_action_btn_pressed.9.png
│   │   │   │       │       │       nd3_title_bar_action_btn_xml.xml
│   │   │   │       │       │       nd3_title_bar_bg.9.png
│   │   │   │       │       │       nd3_title_bar_return_btn.9.png
│   │   │   │       │       │       nd3_title_bar_return_btn_pressed.9.png
│   │   │   │       │       │       nd3_title_bar_return_btn_xml.xml
│   │   │   │       │       │       nd3_user_item_bg.xml
│   │   │   │       │       │       nd3_vertical_line.png
│   │   │   │       │       │       nd3_white_bg.9.png
│   │   │   │       │       │       nd_ad.png
│   │   │   │       │       │       nd_blue.xml
│   │   │   │       │       │       nd_blue1.9.png
│   │   │   │       │       │       nd_blue2.9.png
│   │   │   │       │       │       nd_book.png
│   │   │   │       │       │       nd_btn_add.png
│   │   │   │       │       │       nd_btn_add_press.png
│   │   │   │       │       │       nd_btn_buy.9.png
│   │   │   │       │       │       nd_btn_buy_press.9.png
│   │   │   │       │       │       nd_btn_reduce.png
│   │   │   │       │       │       nd_btn_reduce_press.png
│   │   │   │       │       │       nd_button_action_add.xml
│   │   │   │       │       │       nd_button_action_buy.xml
│   │   │   │       │       │       nd_button_action_reduce.xml
│   │   │   │       │       │       nd_change_account.png
│   │   │   │       │       │       nd_c_blur.xml
│   │   │   │       │       │       nd_c_blur1.9.png
│   │   │   │       │       │       nd_c_blur2.9.png
│   │   │   │       │       │       nd_direct_login.9.png
│   │   │   │       │       │       nd_direct_logo.png
│   │   │   │       │       │       nd_download.xml
│   │   │   │       │       │       nd_gamecoin.png
│   │   │   │       │       │       nd_gcsdk_bezel_border.9.png
│   │   │   │       │       │       nd_gcsdk_bezel_mask.9.png
│   │   │   │       │       │       nd_goods_count_input_bg.9.png
│   │   │   │       │       │       nd_goods_default.png
│   │   │   │       │       │       nd_goods_detail_default.png
│   │   │   │       │       │       nd_goods_limit_stock.png
│   │   │   │       │       │       nd_goods_limit_time.png
│   │   │   │       │       │       nd_goods_no_stock.png
│   │   │   │       │       │       nd_goods_price_down.png
│   │   │   │       │       │       nd_green.xml
│   │   │   │       │       │       nd_green1.9.png
│   │   │   │       │       │       nd_green2.9.png
│   │   │   │       │       │       nd_input.9.png
│   │   │   │       │       │       nd_leaderboard_left_1.9.png
│   │   │   │       │       │       nd_leaderboard_left_2.9.png
│   │   │   │       │       │       nd_leaderboard_left_btn_bg.xml
│   │   │   │       │       │       nd_leaderboard_right_1.9.png
│   │   │   │       │       │       nd_leaderboard_right_2.9.png
│   │   │   │       │       │       nd_leaderboard_right_btn_bg.xml
│   │   │   │       │       │       nd_list_btn_delete_normal.9.png
│   │   │   │       │       │       nd_list_btn_delete_pressed.9.png
│   │   │   │       │       │       nd_list_btn_delete_selector.xml
│   │   │   │       │       │       nd_login_btn_land_selector.xml
│   │   │   │       │       │       nd_login_btn_normal_land.9.png
│   │   │   │       │       │       nd_login_btn_normal_portrait.9.png
│   │   │   │       │       │       nd_login_btn_portrait_selector.xml
│   │   │   │       │       │       nd_login_btn_pressed_land.9.png
│   │   │   │       │       │       nd_login_btn_pressed_portrait.9.png
│   │   │   │       │       │       nd_logo48.png
│   │   │   │       │       │       nd_ordinary.png
│   │   │   │       │       │       nd_register_btn_normal_portrait.9.png
│   │   │   │       │       │       nd_register_btn_portrait_selector.xml
│   │   │   │       │       │       nd_register_btn_pressed_portrait.9.png
│   │   │   │       │       │       nd_satisfied.png
│   │   │   │       │       │       nd_service.png
│   │   │   │       │       │       nd_slider_handle_h.xml
│   │   │   │       │       │       nd_slider_handle_h_expand.xml
│   │   │   │       │       │       nd_slider_handle_v.xml
│   │   │   │       │       │       nd_slider_handle_v_expand.xml
│   │   │   │       │       │       nd_theme.png
│   │   │   │       │       │       nd_true.png
│   │   │   │       │       │       nd_unsatisfied.png
│   │   │   │       │       │       nd_warn.png
│   │   │   │       │       │       nd_white_btn.xml
│   │   │   │       │       │       nd_white_btn_1.9.png
│   │   │   │       │       │       nd_white_btn_2.9.png
│   │   │   │       │       │       nd_winning.png
│   │   │   │       │       │       nd_xline.png
│   │   │   │       │       │
│   │   │   │       │       ├───drawable-hdpi
│   │   │   │       │       │       nd_download_1.9.png
│   │   │   │       │       │       nd_download_2.9.png
│   │   │   │       │       │       nd_flip_bg.png
│   │   │   │       │       │       nd_slider_content_h.9.png
│   │   │   │       │       │       nd_slider_content_v.9.png
│   │   │   │       │       │       nd_slider_handle_h_1.9.png
│   │   │   │       │       │       nd_slider_handle_h_1_expand.9.png
│   │   │   │       │       │       nd_slider_handle_h_2.9.png
│   │   │   │       │       │       nd_slider_handle_h_2_expand.9.png
│   │   │   │       │       │       nd_slider_handle_v_1.9.png
│   │   │   │       │       │       nd_slider_handle_v_1_expand.9.png
│   │   │   │       │       │       nd_slider_handle_v_2.9.png
│   │   │   │       │       │       nd_slider_handle_v_2_expand.9.png
│   │   │   │       │       │       nd_slider_next_h.png
│   │   │   │       │       │       nd_slider_next_v.png
│   │   │   │       │       │       nd_slider_pre_h.png
│   │   │   │       │       │       nd_slider_pre_v.png
│   │   │   │       │       │
│   │   │   │       │       ├───drawable-xhdpi
│   │   │   │       │       │       nd_gcsdk_bg_tips.9.png
│   │   │   │       │       │       nd_gcsdk_box_bg.png
│   │   │   │       │       │       nd_gcsdk_box_btn_bg.png
│   │   │   │       │       │       nd_gcsdk_box_close.png
│   │   │   │       │       │       nd_gcsdk_box_label_bg.png
│   │   │   │       │       │       nd_gcsdk_box_logo.png
│   │   │   │       │       │       nd_gcsdk_box_title_line.png
│   │   │   │       │       │       nd_gcsdk_box_tit_bg.png
│   │   │   │       │       │       nd_gcsdk_exit_txt_bg.9.png
│   │   │   │       │       │       nd_gcsdk_gamecenter_default.png
│   │   │   │       │       │       nd_gcsdk_gamezone_default.png
│   │   │   │       │       │       nd_gcsdk_gc_logo_default.png
│   │   │   │       │       │       nd_gcsdk_image_default.jpg
│   │   │   │       │       │       nd_gcsdk_label_bg.9.png
│   │   │   │       │       │       nd_gcsdk_loading_bg.jpg
│   │   │   │       │       │       nd_gcsdk_loading_logo.png
│   │   │   │       │       │       nd_gcsdk_loading_pot_1.png
│   │   │   │       │       │       nd_gcsdk_loading_pot_2.png
│   │   │   │       │       │
│   │   │   │       │       ├───layout
│   │   │   │       │       │       nd3_account_bind_bind.xml
│   │   │   │       │       │       nd3_account_bind_register.xml
│   │   │   │       │       │       nd3_account_email_item.xml
│   │   │   │       │       │       nd3_account_login.xml
│   │   │   │       │       │       nd3_account_login_item.xml
│   │   │   │       │       │       nd3_account_login_land.xml
│   │   │   │       │       │       nd3_account_login_other_item.xml
│   │   │   │       │       │       nd3_account_login_portrait.xml
│   │   │   │       │       │       nd3_account_oauth_bind.xml
│   │   │   │       │       │       nd3_account_official.xml
│   │   │   │       │       │       nd3_account_official_landscape.xml
│   │   │   │       │       │       nd3_account_official_portrait.xml
│   │   │   │       │       │       nd3_account_other_login.xml
│   │   │   │       │       │       nd3_account_register.xml
│   │   │   │       │       │       nd3_account_register_agreement.xml
│   │   │   │       │       │       nd3_account_register_phone.xml
│   │   │   │       │       │       nd3_account_register_quick.xml
│   │   │   │       │       │       nd3_account_secret_find.xml
│   │   │   │       │       │       nd3_account_secret_set.xml
│   │   │   │       │       │       nd3_account_sina.xml
│   │   │   │       │       │       nd3_achieve_detail.xml
│   │   │   │       │       │       nd3_activity_action_template.xml
│   │   │   │       │       │       nd3_activity_content_reg_template_1.xml
│   │   │   │       │       │       nd3_activity_content_reg_template_2.xml
│   │   │   │       │       │       nd3_activity_content_reg_template_2_ext.xml
│   │   │   │       │       │       nd3_activity_content_reg_template_3.xml
│   │   │   │       │       │       nd3_activity_content_reg_template_4.xml
│   │   │   │       │       │       nd3_activity_detail.xml
│   │   │   │       │       │       nd3_activity_detail_plus_image.xml
│   │   │   │       │       │       nd3_activity_detail_plus_list.xml
│   │   │   │       │       │       nd3_activity_detail_plus_list_ext.xml
│   │   │   │       │       │       nd3_activity_head_reg.xml
│   │   │   │       │       │       nd3_activity_no_action_template.xml
│   │   │   │       │       │       nd3_app_feedback.xml
│   │   │   │       │       │       nd3_app_item.xml
│   │   │   │       │       │       nd3_app_property.xml
│   │   │   │       │       │       nd3_banner_layout.xml
│   │   │   │       │       │       nd3_blank_listview.xml
│   │   │   │       │       │       nd3_bottom_bar.xml
│   │   │   │       │       │       nd3_category_item.xml
│   │   │   │       │       │       nd3_category_plus_image_item.xml
│   │   │   │       │       │       nd3_control_center.xml
│   │   │   │       │       │       nd3_dispatch_search_friend.xml
│   │   │   │       │       │       nd3_empty_listview.xml
│   │   │   │       │       │       nd3_frame.xml
│   │   │   │       │       │       nd3_friend_home.xml
│   │   │   │       │       │       nd3_friend_remark_setting.xml
│   │   │   │       │       │       nd3_friend_section.xml
│   │   │   │       │       │       nd3_friend_section_list_item.xml
│   │   │   │       │       │       nd3_friend_section_panel.xml
│   │   │   │       │       │       nd3_game_content.xml
│   │   │   │       │       │       nd3_game_main.xml
│   │   │   │       │       │       nd3_home.xml
│   │   │   │       │       │       nd3_home_land.xml
│   │   │   │       │       │       nd3_home_personal.xml
│   │   │   │       │       │       nd3_home_portrait.xml
│   │   │   │       │       │       nd3_invite_friend.xml
│   │   │   │       │       │       nd3_invite_friend_choice.xml
│   │   │   │       │       │       nd3_invite_friend_item.xml
│   │   │   │       │       │       nd3_leaderboard_category.xml
│   │   │   │       │       │       nd3_leaderboard_list_item.xml
│   │   │   │       │       │       nd3_listview_footer.xml
│   │   │   │       │       │       nd3_listview_footer_ext.xml
│   │   │   │       │       │       nd3_listview_template.xml
│   │   │   │       │       │       nd3_listview_template_no_divider.xml
│   │   │   │       │       │       nd3_mesg_main.xml
│   │   │   │       │       │       nd3_message_friendmsge_list.xml
│   │   │   │       │       │       nd3_message_main.xml
│   │   │   │       │       │       nd3_message_receive_item.xml
│   │   │   │       │       │       nd3_message_record_item.xml
│   │   │   │       │       │       nd3_message_send.xml
│   │   │   │       │       │       nd3_message_send_item.xml
│   │   │   │       │       │       nd3_more_about.xml
│   │   │   │       │       │       nd3_more_account.xml
│   │   │   │       │       │       nd3_more_bean_recharge.xml
│   │   │   │       │       │       nd3_more_consumes.xml
│   │   │   │       │       │       nd3_more_consume_detail.xml
│   │   │   │       │       │       nd3_more_info.xml
│   │   │   │       │       │       nd3_more_info_edit_head_dialog.xml
│   │   │   │       │       │       nd3_more_more.xml
│   │   │   │       │       │       nd3_more_no_password.xml
│   │   │   │       │       │       nd3_more_password.xml
│   │   │   │       │       │       nd3_more_permission.xml
│   │   │   │       │       │       nd3_more_recharges.xml
│   │   │   │       │       │       nd3_more_recharge_detail.xml
│   │   │   │       │       │       nd3_more_records.xml
│   │   │   │       │       │       nd3_more_records_item.xml
│   │   │   │       │       │       nd3_myfriend.xml
│   │   │   │       │       │       nd3_network_error.xml
│   │   │   │       │       │       nd3_normal_search.xml
│   │   │   │       │       │       nd3_pay_friend_item.xml
│   │   │   │       │       │       nd3_pay_pass.xml
│   │   │   │       │       │       nd3_pay_password_check.xml
│   │   │   │       │       │       nd3_pay_products_item.xml
│   │   │   │       │       │       nd3_pay_select_friend.xml
│   │   │   │       │       │       nd3_pay_template.xml
│   │   │   │       │       │       nd3_personinfo.xml
│   │   │   │       │       │       nd3_person_info_detail.xml
│   │   │   │       │       │       nd3_progressbar.xml
│   │   │   │       │       │       nd3_recharge_record.xml
│   │   │   │       │       │       nd3_searchfriend_condition.xml
│   │   │   │       │       │       nd3_share_bind_account_item.xml
│   │   │   │       │       │       nd3_share_sina.xml
│   │   │   │       │       │       nd3_share_unbind_account_item.xml
│   │   │   │       │       │       nd3_stranger_home.xml
│   │   │   │       │       │       nd3_sysmessage_detail_action.xml
│   │   │   │       │       │       nd3_sysmessage_detail_app.xml
│   │   │   │       │       │       nd3_sysmessage_detail_no_action.xml
│   │   │   │       │       │       nd3_sysmessage_head_reg.xml
│   │   │   │       │       │       nd3_thirdplatform_item.xml
│   │   │   │       │       │       nd3_title_bar.xml
│   │   │   │       │       │       nd3_user_fangle.xml
│   │   │   │       │       │       nd3_user_fangle_ext.xml
│   │   │   │       │       │       nd3_user_item.xml
│   │   │   │       │       │       nd3_user_item_divider.xml
│   │   │   │       │       │       nd3_user_message.xml
│   │   │   │       │       │       nd3_user_message_switcher.xml
│   │   │   │       │       │       nd3_version_update.xml
│   │   │   │       │       │       nd3_write_message.xml
│   │   │   │       │       │       nd_account_list_item.xml
│   │   │   │       │       │       nd_account_manage.xml
│   │   │   │       │       │       nd_bind_phone_lottery.xml
│   │   │   │       │       │       nd_bind_phone_number.xml
│   │   │   │       │       │       nd_bind_phone_number_result.xml
│   │   │   │       │       │       nd_bind_phone_number_tip.xml
│   │   │   │       │       │       nd_bind_phone_number_unactivity_tip.xml
│   │   │   │       │       │       nd_check_version.xml
│   │   │   │       │       │       nd_feedback_faq.xml
│   │   │   │       │       │       nd_feedback_faq_list.xml
│   │   │   │       │       │       nd_feedback_fb.xml
│   │   │   │       │       │       nd_feedback_menu.xml
│   │   │   │       │       │       nd_feedback_menu_item.xml
│   │   │   │       │       │       nd_feedback_my_fb_item.xml
│   │   │   │       │       │       nd_feedback_my_fb_list.xml
│   │   │   │       │       │       nd_feedback_pj_landscape.xml
│   │   │   │       │       │       nd_feedback_pj_portrait.xml
│   │   │   │       │       │       nd_feedback_reply.xml
│   │   │   │       │       │       nd_feedback_reply_bottom.xml
│   │   │   │       │       │       nd_feedback_reply_item_left.xml
│   │   │   │       │       │       nd_feedback_reply_item_right.xml
│   │   │   │       │       │       nd_find_password.xml
│   │   │   │       │       │       nd_gcsdk_custom_toast.xml
│   │   │   │       │       │       nd_gcsdk_exitpage.xml
│   │   │   │       │       │       nd_gcsdk_pausepage.xml
│   │   │   │       │       │       nd_gcsdk_project_view_type_1.xml
│   │   │   │       │       │       nd_gcsdk_project_view_type_2.xml
│   │   │   │       │       │       nd_gcsdk_project_view_type_3.xml
│   │   │   │       │       │       nd_goods_detail.xml
│   │   │   │       │       │       nd_goods_list.xml
│   │   │   │       │       │       nd_goods_list_item.xml
│   │   │   │       │       │       nd_leaderboard.xml
│   │   │   │       │       │       nd_leaderboard_list_header.xml
│   │   │   │       │       │       nd_leaderboard_switcher_landscape_1.xml
│   │   │   │       │       │       nd_leaderboard_switcher_portrait_1.xml
│   │   │   │       │       │       nd_login_director.xml
│   │   │   │       │       │       nd_set_password.xml
│   │   │   │       │       │       nd_softpromotion_flipitem.xml
│   │   │   │       │       │       nd_softpromotion_listitem.xml
│   │   │   │       │       │       nd_softpromotion_slider_h.xml
│   │   │   │       │       │       nd_softpromotion_slider_item.xml
│   │   │   │       │       │       nd_softpromotion_slider_v.xml
│   │   │   │       │       │       nd_softwarepromotion.xml
│   │   │   │       │       │       nd_unbind_phone_number.xml
│   │   │   │       │       │
│   │   │   │       │       ├───raw
│   │   │   │       │       │       nd_res.zip
│   │   │   │       │       │
│   │   │   │       │       └───values
│   │   │   │       │               nd3_misc.xml
│   │   │   │       │               nd3_sdk_error_strings.xml
│   │   │   │       │               nd3_strings.xml
│   │   │   │       │               nd_gcsdk_colors.xml
│   │   │   │       │               nd_gcsdk_misc.xml
│   │   │   │       │               nd_gcsdk_strings.xml
│   │   │   │       │               nd_gcsdk_styles.xml
│   │   │   │       │
│   │   │   │       ├───sdk
│   │   │   │       │       NdComPlatform.jar
│   │   │   │       │
│   │   │   │       └───src
│   │   │   │           └───org
│   │   │   │               └───cocos2dx
│   │   │   │                   └───plugin
│   │   │   │                           IAPNd91.java
│   │   │   │                           IAPOnlineNd91.java
│   │   │   │                           Nd91Wrapper.java
│   │   │   │                           SocialNd91.java
│   │   │   │                           UserNd91.java
│   │   │   │
│   │   │   ├───qh360
│   │   │   │   └───proj.android
│   │   │   │       │   .classpath
│   │   │   │       │   .project
│   │   │   │       │   AndroidManifest.xml
│   │   │   │       │   build.xml
│   │   │   │       │   ForManifest.xml
│   │   │   │       │   project.properties
│   │   │   │       │
│   │   │   │       ├───CLibs
│   │   │   │       │   ├───armeabi
│   │   │   │       │   │       libpaypalm_app_plugin_jar_360game.so
│   │   │   │       │   │
│   │   │   │       │   └───mips
│   │   │   │       │           libpaypalm_app_plugin_jar_360game.so
│   │   │   │       │
│   │   │   │       ├───ForAssets
│   │   │   │       │   │   alipay_plugin.apk
│   │   │   │       │   │   bin_app_plugin.bin
│   │   │   │       │   │   pro.jar
│   │   │   │       │   │   upomp_bypay_config.xml
│   │   │   │       │   │
│   │   │   │       │   └───res
│   │   │   │       │       │   bind_phone_button_normal.9.png
│   │   │   │       │       │   bind_phone_button_pressed.9.png
│   │   │   │       │       │   bind_phone_other_indicator.png
│   │   │   │       │       │   bind_phone_popup_message_arrow.png
│   │   │   │       │       │   bind_phone_title.png
│   │   │   │       │       │   box_off.png
│   │   │   │       │       │   box_on.png
│   │   │   │       │       │   button_gray_disable.9.png
│   │   │   │       │       │   button_gray_normal.9.png
│   │   │   │       │       │   button_gray_press.9.png
│   │   │   │       │       │   checkphone_resetpwd_title.png
│   │   │   │       │       │   check_phone_title.png
│   │   │   │       │       │   close_btn_normal.png
│   │   │   │       │       │   close_btn_press.png
│   │   │   │       │       │   del.png
│   │   │   │       │       │   dialog_bg.9.png
│   │   │   │       │       │   dot.png
│   │   │   │       │       │   dropdown_btn_normal.png
│   │   │   │       │       │   dropdown_btn_normal_.png
│   │   │   │       │       │   dropdown_btn_press.png
│   │   │   │       │       │   dropdown_btn_press_.png
│   │   │   │       │       │   drop_down.9.png
│   │   │   │       │       │   dr_btn_normal.9.png
│   │   │   │       │       │   dr_btn_press.9.png
│   │   │   │       │       │   find_pwd_title.png
│   │   │   │       │       │   guardianship_btn_normal.9.png
│   │   │   │       │       │   guardianship_btn_press.9.png
│   │   │   │       │       │   input_box_.9.png
│   │   │   │       │       │   known_btn_normal.9.png
│   │   │   │       │       │   known_btn_press.9.png
│   │   │   │       │       │   line.9.png
│   │   │   │       │       │   load_success.png
│   │   │   │       │       │   login_bg.9.png
│   │   │   │       │       │   login_logo.png
│   │   │   │       │       │   login_onekey_bg_b.9.png
│   │   │   │       │       │   login_onekey_bg_t.9.png
│   │   │   │       │       │   login_onekey_button.9.png
│   │   │   │       │       │   login_onekey_cellphone.png
│   │   │   │       │       │   login_onekey_icon_right.png
│   │   │   │       │       │   login_onekey_separator.9.png
│   │   │   │       │       │   login_onekey_title.png
│   │   │   │       │       │   no_simcard_title.png
│   │   │   │       │       │   phone_num_get_failed_title.png
│   │   │   │       │       │   phone_used_dlg_title.png
│   │   │   │       │       │   profile_head.png
│   │   │   │       │       │   profile_head_pic1.png
│   │   │   │       │       │   profile_head_pic2.png
│   │   │   │       │       │   profile_head_pic3.png
│   │   │   │       │       │   profile_head_pic4.png
│   │   │   │       │       │   profile_head_pic_default.png
│   │   │   │       │       │   profile_left_button_icon.png
│   │   │   │       │       │   profile_left_button_normal.9.png
│   │   │   │       │       │   profile_left_button_press.9.png
│   │   │   │       │       │   profile_pics.9.png
│   │   │   │       │       │   profile_right_button_icon.png
│   │   │   │       │       │   profile_right_button_normal.9.png
│   │   │   │       │       │   profile_right_button_press.9.png
│   │   │   │       │       │   profile_title_bg.png
│   │   │   │       │       │   qihoo_loadingmotion.png
│   │   │   │       │       │   qihoo_logo.png
│   │   │   │       │       │   qihoo_pay_dialog_bg.9.png
│   │   │   │       │       │   qihoo_pup_bg.9.png
│   │   │   │       │       │   register_logo.png
│   │   │   │       │       │   reg_360account_title.png
│   │   │   │       │       │   reg_logo.png
│   │   │   │       │       │   reg_success_title.png
│   │   │   │       │       │   reg_tab_bg_off.9.png
│   │   │   │       │       │   reg_tab_bg_on_left.9.png
│   │   │   │       │       │   reg_tab_bg_on_right.9.png
│   │   │   │       │       │   reg_tip.png
│   │   │   │       │       │   reg_title_back.png
│   │   │   │       │       │   reg_title_bg.9.png
│   │   │   │       │       │   reg_title_btn_back_normal.9.png
│   │   │   │       │       │   reg_title_btn_back_normal.png
│   │   │   │       │       │   reg_title_btn_back_press.9.png
│   │   │   │       │       │   reg_title_btn_back_press.png
│   │   │   │       │       │   reset_pwd_title.png
│   │   │   │       │       │   select_o.png
│   │   │   │       │       │   switch_btn_bg.9.png
│   │   │   │       │       │   switch_btn_left.png
│   │   │   │       │       │   switch_btn_normal.9.png
│   │   │   │       │       │   switch_btn_press.9.png
│   │   │   │       │       │   tip_bg.9.png
│   │   │   │       │       │   title_bg.9.png
│   │   │   │       │       │   toast_bg.9.png
│   │   │   │       │       │   wait_bg.9.png
│   │   │   │       │       │   zc_btn_normal.9.png
│   │   │   │       │       │   zc_btn_press.9.png
│   │   │   │       │       │
│   │   │   │       │       ├───icon
│   │   │   │       │       │       account_setting_name_bg.9.png
│   │   │   │       │       │       arrow_down.png
│   │   │   │       │       │       arrow_up.png
│   │   │   │       │       │       bank_icon_abc.png
│   │   │   │       │       │       bank_icon_bob.png
│   │   │   │       │       │       bank_icon_boc.png
│   │   │   │       │       │       bank_icon_bos.png
│   │   │   │       │       │       bank_icon_ccb.png
│   │   │   │       │       │       bank_icon_ceb.png
│   │   │   │       │       │       bank_icon_cib.png
│   │   │   │       │       │       bank_icon_cmb.png
│   │   │   │       │       │       bank_icon_cmbc.png
│   │   │   │       │       │       bank_icon_default.png
│   │   │   │       │       │       bank_icon_ecitic.png
│   │   │   │       │       │       bank_icon_gdb.png
│   │   │   │       │       │       bank_icon_gzcb.png
│   │   │   │       │       │       bank_icon_hxb.png
│   │   │   │       │       │       bank_icon_icbc.png
│   │   │   │       │       │       bank_icon_pingan.png
│   │   │   │       │       │       bank_icon_psbc.png
│   │   │   │       │       │       bank_icon_sdb.png
│   │   │   │       │       │       bank_icon_spdb.png
│   │   │   │       │       │       bank_name_bg.9.png
│   │   │   │       │       │       bg_pao_my.9.png
│   │   │   │       │       │       bg_pao_my_h.9.png
│   │   │   │       │       │       bg_pao_you.9.png
│   │   │   │       │       │       bg_pao_you_h.9.png
│   │   │   │       │       │       bind_phone.png
│   │   │   │       │       │       box_off.png
│   │   │   │       │       │       box_on.png
│   │   │   │       │       │       btn_back_normal.9.png
│   │   │   │       │       │       btn_back_pressed.9.png
│   │   │   │       │       │       btn_post_try_normal.9.png
│   │   │   │       │       │       btn_post_try_pressed.9.png
│   │   │   │       │       │       btn_post_view_normal.9.png
│   │   │   │       │       │       btn_post_view_pressed.9.png
│   │   │   │       │       │       bubble_bg_h.9.png
│   │   │   │       │       │       bubble_bg_s.9.png
│   │   │   │       │       │       can_not_open_page_3g_close.png
│   │   │   │       │       │       can_not_open_page_3g_open.png
│   │   │   │       │       │       can_not_open_page_anzai.png
│   │   │   │       │       │       can_not_open_page_line.png
│   │   │   │       │       │       can_not_open_page_refresh.png
│   │   │   │       │       │       can_not_open_page_wifi_close.png
│   │   │   │       │       │       can_not_open_page_wifi_open.png
│   │   │   │       │       │       close_btn_normal.png
│   │   │   │       │       │       close_btn_press.png
│   │   │   │       │       │       credit_date.png
│   │   │   │       │       │       credit_verify.png
│   │   │   │       │       │       del.png
│   │   │   │       │       │       dialog_bg.9.png
│   │   │   │       │       │       dropdown_normal.9.png
│   │   │   │       │       │       dropdown_pressed.9.png
│   │   │   │       │       │       drop_down.9.png
│   │   │   │       │       │       dr_btn_disable.9.png
│   │   │   │       │       │       dr_btn_normal.9.png
│   │   │   │       │       │       dr_btn_press.9.png
│   │   │   │       │       │       faq_list_item_bg_normal.9.png
│   │   │   │       │       │       faq_list_item_bg_select.9.png
│   │   │   │       │       │       go_bbs_btn_normal.9.png
│   │   │   │       │       │       go_bbs_btn_press.9.png
│   │   │   │       │       │       header_icon.png
│   │   │   │       │       │       icon.png
│   │   │   │       │       │       icon_info.png
│   │   │   │       │       │       input_bottom_bg.9.png
│   │   │   │       │       │       input_box_.9.png
│   │   │   │       │       │       input_img_normal.png
│   │   │   │       │       │       input_img_pressed.png
│   │   │   │       │       │       jian.png
│   │   │   │       │       │       known_btn_normal.9.png
│   │   │   │       │       │       known_btn_press.9.png
│   │   │   │       │       │       left_s_bg.9.png
│   │   │   │       │       │       line.9.png
│   │   │   │       │       │       list_bg_H.9.png
│   │   │   │       │       │       list_bg_normal.9.png
│   │   │   │       │       │       money_line.9.png
│   │   │   │       │       │       paybtn_default.9.png
│   │   │   │       │       │       paybtn_disable.9.png
│   │   │   │       │       │       paybtn_pressed.9.png
│   │   │   │       │       │       pay_credit_selected_tag.png
│   │   │   │       │       │       pay_credit_unselected_tag.png
│   │   │   │       │       │       pay_float_bg.9.png
│   │   │   │       │       │       pay_float_card_bg.9.png
│   │   │   │       │       │       pay_float_close_d.png
│   │   │   │       │       │       pay_float_close_p.png
│   │   │   │       │       │       pay_float_failure.png
│   │   │   │       │       │       pay_float_input_clean.png
│   │   │   │       │       │       pay_float_input_clean_pressed.png
│   │   │   │       │       │       pay_float_ok.png
│   │   │   │       │       │       pay_float_other_pay_d.9.png
│   │   │   │       │       │       pay_float_other_pay_p.9.png
│   │   │   │       │       │       pay_float_tiket_left.png
│   │   │   │       │       │       pay_float_tiket_middle.png
│   │   │   │       │       │       pay_float_tiket_right.png
│   │   │   │       │       │       pay_float_translating.png
│   │   │   │       │       │       pay_quick_icon.png
│   │   │   │       │       │       pay_record_tab_selected.9.png
│   │   │   │       │       │       pay_user_guide_bg.9.png
│   │   │   │       │       │       pay_user_guide_btn.9.png
│   │   │   │       │       │       pay_user_guide_guard.png
│   │   │   │       │       │       pay_user_guide_money.png
│   │   │   │       │       │       pay_user_guide_page.png
│   │   │   │       │       │       pay_user_guide_page_now.png
│   │   │   │       │       │       popup_menu_bg.9.png
│   │   │   │       │       │       popup_menu_icon.png
│   │   │   │       │       │       post_alert_fail.9.png
│   │   │   │       │       │       post_alert_ok.9.png
│   │   │   │       │       │       post_fail_icon.png
│   │   │   │       │       │       post_image_opt_add.png
│   │   │   │       │       │       post_image_opt_bg.9.png
│   │   │   │       │       │       post_image_opt_del.png
│   │   │   │       │       │       post_img_bg.9.png
│   │   │   │       │       │       post_input_bg.9.png
│   │   │   │       │       │       post_no_img_normal.png
│   │   │   │       │       │       post_ok_icon.png
│   │   │   │       │       │       qib_balance_dot.png
│   │   │   │       │       │       qib_refresh_btn_disabled.9.png
│   │   │   │       │       │       qib_refresh_btn_normal.9.png
│   │   │   │       │       │       qib_refresh_btn_pressed.9.png
│   │   │   │       │       │       qib_refresh_land_btn_disabled.9.png
│   │   │   │       │       │       qib_refresh_land_btn_normal.9.png
│   │   │   │       │       │       qib_refresh_land_btn_pressed.9.png
│   │   │   │       │       │       qihoo_btn_red_disabled.9.png
│   │   │   │       │       │       qihoo_btn_red_normal.9.png
│   │   │   │       │       │       qihoo_btn_red_pressed.9.png
│   │   │   │       │       │       qihoo_button_normal.9.png
│   │   │   │       │       │       qihoo_button_orange_disabled.9.png
│   │   │   │       │       │       qihoo_button_pressed.9.png
│   │   │   │       │       │       qihoo_credit_binder_selected.9.png
│   │   │   │       │       │       qihoo_credit_bingder_unselected.9.png
│   │   │   │       │       │       qihoo_gray_button_normal.9.png
│   │   │   │       │       │       qihoo_gray_button_press.9.png
│   │   │   │       │       │       qihoo_inficon.png
│   │   │   │       │       │       qihoo_info.png
│   │   │   │       │       │       qihoo_listitem_bg.9.png
│   │   │   │       │       │       qihoo_listitem_bg_pressed_v.9.png
│   │   │   │       │       │       qihoo_listitem_bg_v.9.png
│   │   │   │       │       │       qihoo_loadingmotion.png
│   │   │   │       │       │       qihoo_pay_dialog_bg.9.png
│   │   │   │       │       │       qihoo_pay_success_bindphone_arrow.png
│   │   │   │       │       │       qihoo_pay_success_bindphone_bg.9.png
│   │   │   │       │       │       qihoo_pay_success_bindphone_icon.png
│   │   │   │       │       │       qihoo_pay_sucess.png
│   │   │   │       │       │       qihoo_popup_bg.9.png
│   │   │   │       │       │       qihoo_popup_title.9.png
│   │   │   │       │       │       qihoo_pup_bg.9.png
│   │   │   │       │       │       qihoo_textbox.9.png
│   │   │   │       │       │       qihoo_xianpei.png
│   │   │   │       │       │       qihoo_zhifu_bg.9.png
│   │   │   │       │       │       quit_alert_close_btn.png
│   │   │   │       │       │       quit_game_btn_normal.9.png
│   │   │   │       │       │       quit_game_btn_press.9.png
│   │   │   │       │       │       reg_logo.png
│   │   │   │       │       │       reg_title_back.png
│   │   │   │       │       │       reg_title_bg.9.png
│   │   │   │       │       │       reg_title_btn_back_normal.9.png
│   │   │   │       │       │       reg_title_btn_back_press.9.png
│   │   │   │       │       │       right_selected_bg.9.png
│   │   │   │       │       │       right_s_bg.9.png
│   │   │   │       │       │       right_s_line.9.png
│   │   │   │       │       │       select_money_bg.9.png
│   │   │   │       │       │       select_money_title.9.png
│   │   │   │       │       │       seperator_h.png
│   │   │   │       │       │       seperator_v.png
│   │   │   │       │       │       settings_bbs_normal.png
│   │   │   │       │       │       settings_bbs_pressed.png
│   │   │   │       │       │       settings_bg_left.9.png
│   │   │   │       │       │       settings_bg_right.9.png
│   │   │   │       │       │       settings_bind_phone_normal.png
│   │   │   │       │       │       settings_bind_phone_pressed.png
│   │   │   │       │       │       settings_close_normal.png
│   │   │   │       │       │       settings_close_pressed.png
│   │   │   │       │       │       settings_hide_normal.png
│   │   │   │       │       │       settings_hide_pressed.png
│   │   │   │       │       │       settings_icon_normal.png
│   │   │   │       │       │       settings_icon_pressed.png
│   │   │   │       │       │       settings_service_normal.png
│   │   │   │       │       │       settings_service_pressed.png
│   │   │   │       │       │       single_choice_checked.png
│   │   │   │       │       │       single_choice_unchecked.png
│   │   │   │       │       │       suggest_name_list_bg.9.png
│   │   │   │       │       │       tab_bg_v.9.png
│   │   │   │       │       │       tab_left_normal.9.png
│   │   │   │       │       │       tab_left_pressed.9.png
│   │   │   │       │       │       tab_right_normal.9.png
│   │   │   │       │       │       tab_right_pressed.9.png
│   │   │   │       │       │       tab_zhong_normal.9.png
│   │   │   │       │       │       tab_zhong_pressed.9.png
│   │   │   │       │       │       tip_bg.9.png
│   │   │   │       │       │       title.9.png
│   │   │   │       │       │       title_bg.9.png
│   │   │   │       │       │       toast_bg.9.png
│   │   │   │       │       │       t_new.9.png
│   │   │   │       │       │       vertical_title_bg.9.png
│   │   │   │       │       │
│   │   │   │       │       ├───icon-mdpi
│   │   │   │       │       │       box_off.png
│   │   │   │       │       │       box_on.png
│   │   │   │       │       │       dr_btn_normal.9.png
│   │   │   │       │       │       dr_btn_press.9.png
│   │   │   │       │       │       input_box_.9.png
│   │   │   │       │       │       known_btn_normal.9.png
│   │   │   │       │       │       known_btn_press.9.png
│   │   │   │       │       │       post_input_bg.9.png
│   │   │   │       │       │       qihoo_inficon.png
│   │   │   │       │       │
│   │   │   │       │       └───Mdpi
│   │   │   │       │               box_off.png
│   │   │   │       │               box_on.png
│   │   │   │       │               dropdown_btn_normal.png
│   │   │   │       │               dropdown_btn_normal_.png
│   │   │   │       │               dropdown_btn_press.png
│   │   │   │       │               dropdown_btn_press_.png
│   │   │   │       │               dr_btn_normal.9.png
│   │   │   │       │               dr_btn_press.9.png
│   │   │   │       │               guardianship_btn_normal.9.png
│   │   │   │       │               guardianship_btn_press.9.png
│   │   │   │       │               input_box_.9.png
│   │   │   │       │               known_btn_normal.9.png
│   │   │   │       │               known_btn_press.9.png
│   │   │   │       │               zc_btn_normal.9.png
│   │   │   │       │               zc_btn_press.9.png
│   │   │   │       │
│   │   │   │       ├───ForRes
│   │   │   │       │   ├───anim
│   │   │   │       │   │       zsht_loading.xml
│   │   │   │       │   │
│   │   │   │       │   ├───drawable
│   │   │   │       │   │       upomp_bypay_btn1.xml
│   │   │   │       │   │       upomp_bypay_btn2.xml
│   │   │   │       │   │       upomp_bypay_btn3.xml
│   │   │   │       │   │       upomp_bypay_btn4.xml
│   │   │   │       │   │       upomp_bypay_btn5.xml
│   │   │   │       │   │       upomp_bypay_btn6.xml
│   │   │   │       │   │       upomp_bypay_btn_card.xml
│   │   │   │       │   │       upomp_bypay_btn_enter1.xml
│   │   │   │       │   │       upomp_bypay_btn_enter2.xml
│   │   │   │       │   │       upomp_bypay_btn_esc1.xml
│   │   │   │       │   │       upomp_bypay_btn_esc2.xml
│   │   │   │       │   │       upomp_bypay_btn_letter.xml
│   │   │   │       │   │       upomp_bypay_btn_member1.xml
│   │   │   │       │   │       upomp_bypay_btn_member2.xml
│   │   │   │       │   │       upomp_bypay_btn_month.xml
│   │   │   │       │   │       upomp_bypay_btn_newweb.xml
│   │   │   │       │   │       upomp_bypay_btn_number.xml
│   │   │   │       │   │       upomp_bypay_btn_set.xml
│   │   │   │       │   │       upomp_bypay_btn_symbol.xml
│   │   │   │       │   │       upomp_bypay_btn_title_esc.xml
│   │   │   │       │   │       upomp_bypay_btn_year.xml
│   │   │   │       │   │       upomp_bypay_checkbox.xml
│   │   │   │       │   │       upomp_bypay_input_btn2.xml
│   │   │   │       │   │       upomp_bypay_input_btn4.xml
│   │   │   │       │   │       upomp_bypay_keyboard_btn_clear.xml
│   │   │   │       │   │       upomp_bypay_keyboard_btn_enter.xml
│   │   │   │       │   │       upomp_bypay_keyboard_btn_l_clear.xml
│   │   │   │       │   │       upomp_bypay_open_btn_enter.xml
│   │   │   │       │   │       upomp_bypay_progress.xml
│   │   │   │       │   │       upomp_bypay_progress_init.xml
│   │   │   │       │   │       zsht_authcode_style.xml
│   │   │   │       │   │       zsht_back.9.png
│   │   │   │       │   │       zsht_back_pressed.9.png
│   │   │   │       │   │       zsht_back_style.xml
│   │   │   │       │   │       zsht_button.9.png
│   │   │   │       │   │       zsht_button_pressed.9.png
│   │   │   │       │   │       zsht_button_style.xml
│   │   │   │       │   │       zsht_get_authcode_button.9.png
│   │   │   │       │   │       zsht_get_authcode_button_enable.9.png
│   │   │   │       │   │       zsht_get_authcode_button_pressed.9.png
│   │   │   │       │   │       zsht_input.9.png
│   │   │   │       │   │       zsht_input_focused.9.png
│   │   │   │       │   │       zsht_input_style.xml
│   │   │   │       │   │       zsht_keyboard_background.9.png
│   │   │   │       │   │       zsht_keyboard_button.9.png
│   │   │   │       │   │       zsht_keyboard_title.9.png
│   │   │   │       │   │       zsht_line.9.png
│   │   │   │       │   │       zsht_loading_01.png
│   │   │   │       │   │       zsht_loading_02.png
│   │   │   │       │   │       zsht_loading_03.png
│   │   │   │       │   │       zsht_loading_04.png
│   │   │   │       │   │       zsht_loading_05.png
│   │   │   │       │   │       zsht_loading_06.png
│   │   │   │       │   │       zsht_loading_07.png
│   │   │   │       │   │       zsht_loading_logo.png
│   │   │   │       │   │       zsht_order_message.9.png
│   │   │   │       │   │       zsht_pp_logo.png
│   │   │   │       │   │       zsht_success.png
│   │   │   │       │   │       zsht_title.9.png
│   │   │   │       │   │       zsht_title_image.png
│   │   │   │       │   │
│   │   │   │       │   ├───drawable-hdpi
│   │   │   │       │   │       upomp_bypay_bank_list_icon1.png
│   │   │   │       │   │       upomp_bypay_bank_list_icon2.png
│   │   │   │       │   │       upomp_bypay_bank_list_icon3.png
│   │   │   │       │   │       upomp_bypay_bank_list_title1.png
│   │   │   │       │   │       upomp_bypay_bank_list_title2.png
│   │   │   │       │   │       upomp_bypay_bg.png
│   │   │   │       │   │       upomp_bypay_bottom.png
│   │   │   │       │   │       upomp_bypay_bottom_about.png
│   │   │   │       │   │       upomp_bypay_bottom_line.png
│   │   │   │       │   │       upomp_bypay_btn_change.png
│   │   │   │       │   │       upomp_bypay_btn_change_click.png
│   │   │   │       │   │       upomp_bypay_btn_enter2_bg.png
│   │   │   │       │   │       upomp_bypay_btn_enter2_bg_click.png
│   │   │   │       │   │       upomp_bypay_btn_enter_bg.png
│   │   │   │       │   │       upomp_bypay_btn_enter_bg_click.png
│   │   │   │       │   │       upomp_bypay_btn_esc2_bg.png
│   │   │   │       │   │       upomp_bypay_btn_esc2_bg_click.png
│   │   │   │       │   │       upomp_bypay_btn_esc_bg.png
│   │   │   │       │   │       upomp_bypay_btn_esc_bg_click.png
│   │   │   │       │   │       upomp_bypay_card_btn1.png
│   │   │   │       │   │       upomp_bypay_card_btn2.png
│   │   │   │       │   │       upomp_bypay_card_btn3.png
│   │   │   │       │   │       upomp_bypay_card_icon1.png
│   │   │   │       │   │       upomp_bypay_card_on_bg.png
│   │   │   │       │   │       upomp_bypay_card_on_icon.png
│   │   │   │       │   │       upomp_bypay_card_select.png
│   │   │   │       │   │       upomp_bypay_card_select1.png
│   │   │   │       │   │       upomp_bypay_card_select2.png
│   │   │   │       │   │       upomp_bypay_card_select_click.png
│   │   │   │       │   │       upomp_bypay_cvn2.png
│   │   │   │       │   │       upomp_bypay_icon.png
│   │   │   │       │   │       upomp_bypay_icon_card.png
│   │   │   │       │   │       upomp_bypay_icon_jiantou.png
│   │   │   │       │   │       upomp_bypay_icon_pw.png
│   │   │   │       │   │       upomp_bypay_index_bot_bg.png
│   │   │   │       │   │       upomp_bypay_info_bg.png
│   │   │   │       │   │       upomp_bypay_info_bot1.png
│   │   │   │       │   │       upomp_bypay_info_bot2.png
│   │   │   │       │   │       upomp_bypay_info_bot3.png
│   │   │   │       │   │       upomp_bypay_info_bot4.png
│   │   │   │       │   │       upomp_bypay_info_btn1.png
│   │   │   │       │   │       upomp_bypay_info_btn1_click.png
│   │   │   │       │   │       upomp_bypay_info_btn2.png
│   │   │   │       │   │       upomp_bypay_info_btn2_click.png
│   │   │   │       │   │       upomp_bypay_info_btn3.png
│   │   │   │       │   │       upomp_bypay_info_btn3_click.png
│   │   │   │       │   │       upomp_bypay_info_btn4.png
│   │   │   │       │   │       upomp_bypay_info_btn4_click.png
│   │   │   │       │   │       upomp_bypay_info_btn5.png
│   │   │   │       │   │       upomp_bypay_info_btn5_click.png
│   │   │   │       │   │       upomp_bypay_info_btn6.png
│   │   │   │       │   │       upomp_bypay_info_btn6_click.png
│   │   │   │       │   │       upomp_bypay_info_icon1.png
│   │   │   │       │   │       upomp_bypay_info_icon2.png
│   │   │   │       │   │       upomp_bypay_info_icon3.png
│   │   │   │       │   │       upomp_bypay_info_icon4.png
│   │   │   │       │   │       upomp_bypay_info_icon5.png
│   │   │   │       │   │       upomp_bypay_info_icon6.png
│   │   │   │       │   │       upomp_bypay_info_icon7.png
│   │   │   │       │   │       upomp_bypay_info_left.png
│   │   │   │       │   │       upomp_bypay_info_right.png
│   │   │   │       │   │       upomp_bypay_info_select_1.png
│   │   │   │       │   │       upomp_bypay_info_select_2.png
│   │   │   │       │   │       upomp_bypay_info_top1.png
│   │   │   │       │   │       upomp_bypay_info_top2.png
│   │   │   │       │   │       upomp_bypay_info_top3.png
│   │   │   │       │   │       upomp_bypay_input_2.png
│   │   │   │       │   │       upomp_bypay_input_bg.png
│   │   │   │       │   │       upomp_bypay_input_bg_on.png
│   │   │   │       │   │       upomp_bypay_input_btn_2.png
│   │   │   │       │   │       upomp_bypay_input_btn_2_click.png
│   │   │   │       │   │       upomp_bypay_input_btn_4.png
│   │   │   │       │   │       upomp_bypay_input_btn_4_click.png
│   │   │   │       │   │       upomp_bypay_input_btn_hq.png
│   │   │   │       │   │       upomp_bypay_input_btn_hq_click.png
│   │   │   │       │   │       upomp_bypay_input_icon.png
│   │   │   │       │   │       upomp_bypay_keyboard_bg.png
│   │   │   │       │   │       upomp_bypay_keyboard_btn1_default.png
│   │   │   │       │   │       upomp_bypay_keyboard_btn1_on.png
│   │   │   │       │   │       upomp_bypay_keyboard_btn_clear_default.png
│   │   │   │       │   │       upomp_bypay_keyboard_btn_clear_on.png
│   │   │   │       │   │       upomp_bypay_keyboard_btn_enter_default.png
│   │   │   │       │   │       upomp_bypay_keyboard_btn_enter_on.png
│   │   │   │       │   │       upomp_bypay_keyboard_fh_bg.png
│   │   │   │       │   │       upomp_bypay_keyboard_fh_bg_on.png
│   │   │   │       │   │       upomp_bypay_keyboard_input_bg.png
│   │   │   │       │   │       upomp_bypay_keyboard_letter_a1.png
│   │   │   │       │   │       upomp_bypay_keyboard_letter_a2.png
│   │   │   │       │   │       upomp_bypay_keyboard_letter_bg.png
│   │   │   │       │   │       upomp_bypay_keyboard_letter_bg_on.png
│   │   │   │       │   │       upomp_bypay_keyboard_letter_clear_bg.png
│   │   │   │       │   │       upomp_bypay_keyboard_letter_clear_bg_on.png
│   │   │   │       │   │       upomp_bypay_keyboard_nav_bg.png
│   │   │   │       │   │       upomp_bypay_keyboard_number_bg.png
│   │   │   │       │   │       upomp_bypay_keyboard_number_bg_on.png
│   │   │   │       │   │       upomp_bypay_keyboard_pw_bg.png
│   │   │   │       │   │       upomp_bypay_loading_bg.png
│   │   │   │       │   │       upomp_bypay_loading_bg2.png
│   │   │   │       │   │       upomp_bypay_loading_logo.png
│   │   │   │       │   │       upomp_bypay_loading_tag.png
│   │   │   │       │   │       upomp_bypay_login_open_bg.png
│   │   │   │       │   │       upomp_bypay_main_line.png
│   │   │   │       │   │       upomp_bypay_member_btn1.png
│   │   │   │       │   │       upomp_bypay_member_btn1_click.png
│   │   │   │       │   │       upomp_bypay_member_btn2.png
│   │   │   │       │   │       upomp_bypay_member_btn2_click.png
│   │   │   │       │   │       upomp_bypay_open_bg.png
│   │   │   │       │   │       upomp_bypay_open_bg2.png
│   │   │   │       │   │       upomp_bypay_open_btn.png
│   │   │   │       │   │       upomp_bypay_open_btn_click.png
│   │   │   │       │   │       upomp_bypay_open_icon.png
│   │   │   │       │   │       upomp_bypay_psw_bg.png
│   │   │   │       │   │       upomp_bypay_select_card_add.png
│   │   │   │       │   │       upomp_bypay_select_card_bg.png
│   │   │   │       │   │       upomp_bypay_select_month.png
│   │   │   │       │   │       upomp_bypay_select_month_on.png
│   │   │   │       │   │       upomp_bypay_select_year.png
│   │   │   │       │   │       upomp_bypay_select_year_on.png
│   │   │   │       │   │       upomp_bypay_spinner.png
│   │   │   │       │   │       upomp_bypay_tips_bg.png
│   │   │   │       │   │       upomp_bypay_title_bg.png
│   │   │   │       │   │       upomp_bypay_title_btn.png
│   │   │   │       │   │       upomp_bypay_title_btn_click.png
│   │   │   │       │   │       upomp_bypay_toast_bg.png
│   │   │   │       │   │       upomp_bypay_view_xy.png
│   │   │   │       │   │
│   │   │   │       │   ├───layout
│   │   │   │       │   │       upomp_bypay_about.xml
│   │   │   │       │   │       upomp_bypay_about_btn.xml
│   │   │   │       │   │       upomp_bypay_activity_dialog.xml
│   │   │   │       │   │       upomp_bypay_auth_bind_card.xml
│   │   │   │       │   │       upomp_bypay_bindcard_credit.xml
│   │   │   │       │   │       upomp_bypay_bindcard_debit.xml
│   │   │   │       │   │       upomp_bypay_bindcard_pan.xml
│   │   │   │       │   │       upomp_bypay_bindcard_result.xml
│   │   │   │       │   │       upomp_bypay_cardlist_content.xml
│   │   │   │       │   │       upomp_bypay_get_pass.xml
│   │   │   │       │   │       upomp_bypay_image_cvn2.xml
│   │   │   │       │   │       upomp_bypay_keyboard_dialog.xml
│   │   │   │       │   │       upomp_bypay_keyboard_letter.xml
│   │   │   │       │   │       upomp_bypay_keyboard_num.xml
│   │   │   │       │   │       upomp_bypay_keyboard_symbol.xml
│   │   │   │       │   │       upomp_bypay_onuser_cardmanage.xml
│   │   │   │       │   │       upomp_bypay_onuser_change_psw.xml
│   │   │   │       │   │       upomp_bypay_onuser_change_tel.xml
│   │   │   │       │   │       upomp_bypay_onuser_tel.xml
│   │   │   │       │   │       upomp_bypay_onuser_usermanage.xml
│   │   │   │       │   │       upomp_bypay_pay_main.xml
│   │   │   │       │   │       upomp_bypay_pay_result.xml
│   │   │   │       │   │       upomp_bypay_pay_result_lose.xml
│   │   │   │       │   │       upomp_bypay_register.xml
│   │   │   │       │   │       upomp_bypay_register2.xml
│   │   │   │       │   │       upomp_bypay_register_result.xml
│   │   │   │       │   │       upomp_bypay_splash.xml
│   │   │   │       │   │       upomp_bypay_support_card.xml
│   │   │   │       │   │       upomp_bypay_support_card_list.xml
│   │   │   │       │   │       upomp_bypay_userprotocal.xml
│   │   │   │       │   │       upomp_bypay_user_credit.xml
│   │   │   │       │   │       upomp_bypay_user_debit.xml
│   │   │   │       │   │       zsht_bankcard_agreement.xml
│   │   │   │       │   │       zsht_bankcard_pay.xml
│   │   │   │       │   │       zsht_griditems.xml
│   │   │   │       │   │       zsht_loading_process_dialog_anim.xml
│   │   │   │       │   │       zsht_success_page.xml
│   │   │   │       │   │       zsht_user_message.xml
│   │   │   │       │   │
│   │   │   │       │   ├───raw
│   │   │   │       │   │       upomp_bypay_click.ogg
│   │   │   │       │   │
│   │   │   │       │   └───values
│   │   │   │       │           upomp_strings.xml
│   │   │   │       │           upomp_styles.xml
│   │   │   │       │           zsht_strings.xml
│   │   │   │       │           zsht_styles.xml
│   │   │   │       │
│   │   │   │       ├───sdk
│   │   │   │       │       360SDK.jar
│   │   │   │       │       annotations.jar
│   │   │   │       │       upomp_bypay_lib.jar
│   │   │   │       │       zsht_app_360game.jar
│   │   │   │       │
│   │   │   │       └───src
│   │   │   │           └───org
│   │   │   │               └───cocos2dx
│   │   │   │                   └───plugin
│   │   │   │                           IAPOnlineQH360.java
│   │   │   │                           QH360Wrapper.java
│   │   │   │                           UserQH360.java
│   │   │   │
│   │   │   ├───twitter
│   │   │   │   ├───proj.android
│   │   │   │   │   │   .classpath
│   │   │   │   │   │   .project
│   │   │   │   │   │   AndroidManifest.xml
│   │   │   │   │   │   build.xml
│   │   │   │   │   │   ForManifest.xml
│   │   │   │   │   │   project.properties
│   │   │   │   │   │
│   │   │   │   │   ├───sdk
│   │   │   │   │   │       signpost-commonshttp4-1.2.1.1.jar
│   │   │   │   │   │       signpost-core-1.2.1.1.jar
│   │   │   │   │   │       signpost-jetty6-1.2.1.1.jar
│   │   │   │   │   │       twitter4j-core-android-3.0.1.jar
│   │   │   │   │   │
│   │   │   │   │   └───src
│   │   │   │   │       └───org
│   │   │   │   │           └───cocos2dx
│   │   │   │   │               └───plugin
│   │   │   │   │                       Consts.java
│   │   │   │   │                       ShareTwitter.java
│   │   │   │   │                       TwitterApp.java
│   │   │   │   │                       TwitterDialog.java
│   │   │   │   │                       TwitterSession.java
│   │   │   │   │
│   │   │   │   └───proj.ios
│   │   │   │       │   PluginTwitter-Prefix.pch
│   │   │   │       │   ShareTwitter.h
│   │   │   │       │   ShareTwitter.m
│   │   │   │       │
│   │   │   │       ├───FHSTwitterEngine
│   │   │   │       │   │   FHSTwitterEngine.h
│   │   │   │       │   │   FHSTwitterEngine.m
│   │   │   │       │   │
│   │   │   │       │   └───OAuthConsumer
│   │   │   │       │       │   OAConsumer.h
│   │   │   │       │       │   OAConsumer.m
│   │   │   │       │       │   OAHMAC_SHA1SignatureProvider.h
│   │   │   │       │       │   OAHMAC_SHA1SignatureProvider.m
│   │   │   │       │       │   OAMutableURLRequest.h
│   │   │   │       │       │   OAMutableURLRequest.m
│   │   │   │       │       │   OARequestParameter.h
│   │   │   │       │       │   OARequestParameter.m
│   │   │   │       │       │   OAServiceTicket.h
│   │   │   │       │       │   OAServiceTicket.m
│   │   │   │       │       │   OAToken.h
│   │   │   │       │       │   OAToken.m
│   │   │   │       │       │   OAuthConsumer.h
│   │   │   │       │       │
│   │   │   │       │       ├───Categories
│   │   │   │       │       │       NSString+URLEncoding.h
│   │   │   │       │       │       NSString+URLEncoding.m
│   │   │   │       │       │
│   │   │   │       │       └───Crytpo
│   │   │   │       │               Base64TranscoderFHS.c
│   │   │   │       │               Base64TranscoderFHS.h
│   │   │   │       │
│   │   │   │       └───PluginTwitter.xcodeproj
│   │   │   │               project.pbxproj
│   │   │   │
│   │   │   ├───uc
│   │   │   │   └───proj.android
│   │   │   │       │   .classpath
│   │   │   │       │   .project
│   │   │   │       │   AndroidManifest.xml
│   │   │   │       │   build.xml
│   │   │   │       │   ForManifest.xml
│   │   │   │       │   project.properties
│   │   │   │       │
│   │   │   │       ├───sdk
│   │   │   │       │       alipay_plugin.jar
│   │   │   │       │       UCGameSDK.jar
│   │   │   │       │
│   │   │   │       └───src
│   │   │   │           └───org
│   │   │   │               └───cocos2dx
│   │   │   │                   └───plugin
│   │   │   │                           IAPOnlineUC.java
│   │   │   │                           UCWrapper.java
│   │   │   │                           UserUC.java
│   │   │   │
│   │   │   ├───umeng
│   │   │   │   ├───proj.android
│   │   │   │   │   │   .classpath
│   │   │   │   │   │   .project
│   │   │   │   │   │   AndroidManifest.xml
│   │   │   │   │   │   build.xml
│   │   │   │   │   │   ForManifest.xml
│   │   │   │   │   │   project.properties
│   │   │   │   │   │
│   │   │   │   │   ├───sdk
│   │   │   │   │   │       umeng_sdk.jar
│   │   │   │   │   │
│   │   │   │   │   └───src
│   │   │   │   │       └───org
│   │   │   │   │           └───cocos2dx
│   │   │   │   │               └───plugin
│   │   │   │   │                       AnalyticsUmeng.java
│   │   │   │   │
│   │   │   │   └───proj.ios
│   │   │   │       │   AnalyticsUmeng.h
│   │   │   │       │   AnalyticsUmeng.m
│   │   │   │       │   libMobClickLibrary.a
│   │   │   │       │   MobClick.h
│   │   │   │       │   PluginUmeng-Prefix.pch
│   │   │   │       │
│   │   │   │       └───PluginUmeng.xcodeproj
│   │   │   │               project.pbxproj
│   │   │   │
│   │   │   └───weibo
│   │   │       ├───proj.android
│   │   │       │   │   .classpath
│   │   │       │   │   .project
│   │   │       │   │   AndroidManifest.xml
│   │   │       │   │   build.xml
│   │   │       │   │   ForManifest.xml
│   │   │       │   │   project.properties
│   │   │       │   │
│   │   │       │   ├───sdk
│   │   │       │   │       weibosdk.jar
│   │   │       │   │
│   │   │       │   └───src
│   │   │       │       └───org
│   │   │       │           └───cocos2dx
│   │   │       │               └───plugin
│   │   │       │                       AccessTokenKeeper.java
│   │   │       │                       ShareWeibo.java
│   │   │       │
│   │   │       └───proj.ios
│   │   │           │   PluginWeibo-Prefix.pch
│   │   │           │   ShareWeibo.h
│   │   │           │   ShareWeibo.m
│   │   │           │
│   │   │           ├───JSONKit
│   │   │           │       JSONKit.h
│   │   │           │       JSONKit.m
│   │   │           │
│   │   │           ├───PluginWeibo.xcodeproj
│   │   │           │       project.pbxproj
│   │   │           │
│   │   │           └───SinaWeibo
│   │   │               │   SinaWeibo.h
│   │   │               │   SinaWeibo.m
│   │   │               │   SinaWeiboAuthorizeView.h
│   │   │               │   SinaWeiboAuthorizeView.m
│   │   │               │   SinaWeiboConstants.h
│   │   │               │   SinaWeiboRequest.h
│   │   │               │   SinaWeiboRequest.m
│   │   │               │
│   │   │               └───SinaWeibo.bundle
│   │   │                   └───images
│   │   │                           close.png
│   │   │                           close@2x.png
│   │   │
│   │   ├───protocols
│   │   │   │   PluginManager.cpp
│   │   │   │   PluginParam.cpp
│   │   │   │
│   │   │   ├───include
│   │   │   │       AgentManager.h
│   │   │   │       FacebookAgent.h
│   │   │   │       iOSIAPAgent.h
│   │   │   │       PluginFactory.h
│   │   │   │       PluginManager.h
│   │   │   │       PluginParam.h
│   │   │   │       PluginProtocol.h
│   │   │   │       ProtocolAds.h
│   │   │   │       ProtocolAnalytics.h
│   │   │   │       ProtocolIAP.h
│   │   │   │       ProtocolShare.h
│   │   │   │       ProtocolSocial.h
│   │   │   │       ProtocolUser.h
│   │   │   │
│   │   │   ├───platform
│   │   │   │   ├───android
│   │   │   │   │       AgentManager.cpp
│   │   │   │   │       FacebookAgent.cpp
│   │   │   │   │       PluginFactory.cpp
│   │   │   │   │       PluginJavaData.h
│   │   │   │   │       PluginJniHelper.cpp
│   │   │   │   │       PluginJniHelper.h
│   │   │   │   │       PluginJniMacros.h
│   │   │   │   │       PluginProtocol.cpp
│   │   │   │   │       PluginUtils.cpp
│   │   │   │   │       PluginUtils.h
│   │   │   │   │       ProtocolAds.cpp
│   │   │   │   │       ProtocolAnalytics.cpp
│   │   │   │   │       ProtocolIAP.cpp
│   │   │   │   │       ProtocolShare.cpp
│   │   │   │   │       ProtocolSocial.cpp
│   │   │   │   │       ProtocolUser.cpp
│   │   │   │   │
│   │   │   │   └───ios
│   │   │   │           AdsWrapper.h
│   │   │   │           AdsWrapper.mm
│   │   │   │           AgentManager.mm
│   │   │   │           FacebookAgent.mm
│   │   │   │           IAPWrapper.h
│   │   │   │           IAPWrapper.mm
│   │   │   │           InterfaceAds.h
│   │   │   │           InterfaceAnalytics.h
│   │   │   │           InterfaceIAP.h
│   │   │   │           InterfaceShare.h
│   │   │   │           InterfaceSocial.h
│   │   │   │           InterfaceUser.h
│   │   │   │           iOSIAPAgent.mm
│   │   │   │           ParseUtils.h
│   │   │   │           ParseUtils.m
│   │   │   │           PluginFactory.mm
│   │   │   │           PluginOCMacros.h
│   │   │   │           PluginProtocol.mm
│   │   │   │           PluginUtilsIOS.h
│   │   │   │           PluginUtilsIOS.mm
│   │   │   │           ProtocolAds.mm
│   │   │   │           ProtocolAnalytics.mm
│   │   │   │           ProtocolIAP.mm
│   │   │   │           ProtocolShare.mm
│   │   │   │           ProtocolSocial.mm
│   │   │   │           ProtocolUser.mm
│   │   │   │           ShareWrapper.h
│   │   │   │           ShareWrapper.mm
│   │   │   │           SocialWrapper.h
│   │   │   │           SocialWrapper.mm
│   │   │   │           UserWrapper.h
│   │   │   │           UserWrapper.mm
│   │   │   │
│   │   │   ├───proj.android
│   │   │   │   │   .classpath
│   │   │   │   │   .project
│   │   │   │   │   AndroidManifest.xml
│   │   │   │   │   build.xml
│   │   │   │   │   build_native.sh
│   │   │   │   │   project.properties
│   │   │   │   │
│   │   │   │   ├───jni
│   │   │   │   │       Android.mk
│   │   │   │   │       Application.mk
│   │   │   │   │
│   │   │   │   └───src
│   │   │   │       └───org
│   │   │   │           └───cocos2dx
│   │   │   │               └───plugin
│   │   │   │                       AdsWrapper.java
│   │   │   │                       IAPWrapper.java
│   │   │   │                       InterfaceAds.java
│   │   │   │                       InterfaceAnalytics.java
│   │   │   │                       InterfaceIAP.java
│   │   │   │                       InterfaceShare.java
│   │   │   │                       InterfaceSocial.java
│   │   │   │                       InterfaceUser.java
│   │   │   │                       PluginListener.java
│   │   │   │                       PluginWrapper.java
│   │   │   │                       ShareWrapper.java
│   │   │   │                       SocialWrapper.java
│   │   │   │                       UserWrapper.java
│   │   │   │
│   │   │   └───proj.ios
│   │   │       │   PluginProtocol-Prefix.pch
│   │   │       │
│   │   │       └───PluginProtocol.xcodeproj
│   │   │               project.pbxproj
│   │   │
│   │   └───tools
│   │       │   android-build.py
│   │       │   config.sh
│   │       │   gameDevGuide.sh
│   │       │   publish.sh
│   │       │
│   │       ├───android
│   │       │       build_common.xml
│   │       │
│   │       ├───pluginx-bindings-generator
│   │       │   │   conversions.yaml
│   │       │   │   genbindings-all.sh
│   │       │   │   genbindings-lua.py
│   │       │   │   genbindings.sh
│   │       │   │   modify_include.sed
│   │       │   │
│   │       │   ├───tojs
│   │       │   │       cocos2dx_pluginx.ini
│   │       │   │
│   │       │   └───tolua
│   │       │           cocos2dx_pluginx.ini
│   │       │
│   │       ├───toolsForGame
│   │       │       addPluginForGame.sh
│   │       │       main.py
│   │       │       modifyAppMK.sh
│   │       │       modifyClassPath.py
│   │       │       modifyManifest.py
│   │       │       modifyMK.sh
│   │       │       modifyProject.py
│   │       │       modifyRes.sh
│   │       │       steps.py
│   │       │
│   │       └───toolsForPublish
│   │               checkEnvironment.sh
│   │               genPrebuildMK.sh
│   │               publishPlugin.sh
│   │
│   └───tools
│       │   missing-tools.txt
│       │
│       ├───coding-style
│       │       include-linter.py
│       │       tailing-spaces.py
│       │
│       ├───fbx-conv
│       │   │   README.md
│       │   │
│       │   └───mac
│       │           fbx-conv
│       │           libfbxsdk.dylib
│       │
│       ├───particle
│       │       convert_YCoordFlipped.py
│       │
│       ├───performance-analyze
│       │       convertor.py
│       │       README.md
│       │
│       └───simulator
│           │   .cocos-project.json
│           │   .project
│           │   config.json
│           │
│           ├───frameworks
│           │   └───runtime-src
│           │       ├───Classes
│           │       │       AppDelegate.cpp
│           │       │       AppDelegate.h
│           │       │
│           │       ├───proj.android
│           │       │   │   .classpath
│           │       │   │   .project
│           │       │   │   AndroidManifest.xml
│           │       │   │   ant.properties
│           │       │   │   build-cfg.json
│           │       │   │   build.xml
│           │       │   │   proguard-project.txt
│           │       │   │   project.properties
│           │       │   │
│           │       │   ├───.settings
│           │       │   │       org.eclipse.jdt.core.prefs
│           │       │   │
│           │       │   ├───jni
│           │       │   │   │   Android.mk
│           │       │   │   │   Application.mk
│           │       │   │   │
│           │       │   │   └───hellolua
│           │       │   │           main.cpp
│           │       │   │
│           │       │   ├───res
│           │       │   │   ├───drawable-hdpi
│           │       │   │   │       icon.png
│           │       │   │   │
│           │       │   │   ├───drawable-ldpi
│           │       │   │   │       icon.png
│           │       │   │   │
│           │       │   │   ├───drawable-mdpi
│           │       │   │   │       icon.png
│           │       │   │   │
│           │       │   │   └───values
│           │       │   │           strings.xml
│           │       │   │
│           │       │   └───src
│           │       │       └───org
│           │       │           └───cocos2dx
│           │       │               └───lua
│           │       │                       AppActivity.java
│           │       │
│           │       ├───proj.ios_mac
│           │       │   ├───ios
│           │       │   │       AppController.h
│           │       │   │       AppController.mm
│           │       │   │       build-cfg.json
│           │       │   │       Default-568h@2x.png
│           │       │   │       Default-667h@2x.png
│           │       │   │       Default-736h@3x.png
│           │       │   │       Default.png
│           │       │   │       Default@2x.png
│           │       │   │       Icon-100.png
│           │       │   │       Icon-114.png
│           │       │   │       Icon-120.png
│           │       │   │       Icon-144.png
│           │       │   │       Icon-152.png
│           │       │   │       Icon-29.png
│           │       │   │       Icon-40.png
│           │       │   │       Icon-50.png
│           │       │   │       Icon-57.png
│           │       │   │       Icon-58.png
│           │       │   │       Icon-72.png
│           │       │   │       Icon-76.png
│           │       │   │       Icon-80.png
│           │       │   │       Info.plist
│           │       │   │       main.m
│           │       │   │       Prefix.pch
│           │       │   │       RootViewController.h
│           │       │   │       RootViewController.mm
│           │       │   │
│           │       │   ├───mac
│           │       │   │   │   build-cfg.json
│           │       │   │   │   ConsoleWindowController.h
│           │       │   │   │   ConsoleWindowController.m
│           │       │   │   │   Icon.icns
│           │       │   │   │   Info.plist
│           │       │   │   │   main.m
│           │       │   │   │   Prefix.pch
│           │       │   │   │   SimulatorApp.h
│           │       │   │   │   SimulatorApp.mm
│           │       │   │   │
│           │       │   │   ├───Base.lproj
│           │       │   │   │       ConsoleWindow.xib
│           │       │   │   │       MainMenu.xib
│           │       │   │   │
│           │       │   │   ├───en.lproj
│           │       │   │   │       MainMenu.xib
│           │       │   │   │
│           │       │   │   └───zh-Hans.lproj
│           │       │   │           ConsoleWindow.strings
│           │       │   │           MainMenu.xib
│           │       │   │
│           │       │   └───simulator.xcodeproj
│           │       │           project.pbxproj
│           │       │
│           │       └───proj.win32
│           │           │   build-cfg.json
│           │           │   game.rc
│           │           │   main.cpp
│           │           │   main.h
│           │           │   resource.h
│           │           │   simulator.sln
│           │           │   simulator.vcxproj
│           │           │   simulator.vcxproj.filters
│           │           │   simulator.vcxproj.user
│           │           │   SimulatorWin.cpp
│           │           │   SimulatorWin.h
│           │           │   stdafx.cpp
│           │           │   stdafx.h
│           │           │   targetver.h
│           │           │
│           │           └───res
│           │                   game.ico
│           │
│           └───libsimulator
│               ├───lib
│               │   │   AppEvent.cpp
│               │   │   AppEvent.h
│               │   │   AppLang.cpp
│               │   │   AppLang.h
│               │   │   cocos2dx_extra.h
│               │   │   DeviceEx.h
│               │   │   PlayerEditBoxServiceProtocol.h
│               │   │   PlayerFileDialogServiceProtocol.h
│               │   │   PlayerMacros.h
│               │   │   PlayerMenuServiceProtocol.cpp
│               │   │   PlayerMenuServiceProtocol.h
│               │   │   PlayerMessageBoxServiceProtocol.h
│               │   │   PlayerProtocol.cpp
│               │   │   PlayerProtocol.h
│               │   │   PlayerServiceProtocol.cpp
│               │   │   PlayerServiceProtocol.h
│               │   │   PlayerSettings.cpp
│               │   │   PlayerSettings.h
│               │   │   PlayerTaskServiceProtocol.cpp
│               │   │   PlayerTaskServiceProtocol.h
│               │   │   PlayerUtils.cpp
│               │   │   PlayerUtils.h
│               │   │   SimulatorExport.h
│               │   │
│               │   ├───network
│               │   │       CCHTTPRequest.cpp
│               │   │       CCHTTPRequest.h
│               │   │       CCHTTPRequestDelegate.h
│               │   │
│               │   ├───platform
│               │   │   ├───mac
│               │   │   │   │   DeviceEx-mac.mm
│               │   │   │   │   PlayerEditBoxServiceMac.h
│               │   │   │   │   PlayerEditBoxServiceMac.mm
│               │   │   │   │   PlayerFileDialogServiceMac.h
│               │   │   │   │   PlayerFileDialogServiceMac.mm
│               │   │   │   │   PlayerMac.h
│               │   │   │   │   PlayerMac.mm
│               │   │   │   │   PlayerMenuServiceMac.h
│               │   │   │   │   PlayerMenuServiceMac.mm
│               │   │   │   │   PlayerMessageBoxServiceMac.h
│               │   │   │   │   PlayerMessageBoxServiceMac.mm
│               │   │   │   │   PlayerTaskServiceMac.h
│               │   │   │   │   PlayerTaskServiceMac.mm
│               │   │   │   │   Runtime_ios-mac.mm
│               │   │   │   │
│               │   │   │   └───openudid
│               │   │   │           OpenUDIDMac.h
│               │   │   │           OpenUDIDMac.m
│               │   │   │
│               │   │   └───win32
│               │   │           DeviceEx-win32.cpp
│               │   │           PlayerEditBoxServiceWin.cpp
│               │   │           PlayerEditBoxServiceWin.h
│               │   │           PlayerFileDialogServiceWin.cpp
│               │   │           PlayerFileDialogServiceWin.h
│               │   │           PlayerMenuServiceWin.cpp
│               │   │           PlayerMenuServiceWin.h
│               │   │           PlayerMessageBoxServiceWin.cpp
│               │   │           PlayerMessageBoxServiceWin.h
│               │   │           PlayerTaskServiceWin.cpp
│               │   │           PlayerTaskServiceWin.h
│               │   │           PlayerWin.cpp
│               │   │           PlayerWin.h
│               │   │           SimulatorWin.cpp
│               │   │
│               │   ├───ProjectConfig
│               │   │       ProjectConfig.cpp
│               │   │       ProjectConfig.h
│               │   │       SimulatorConfig.cpp
│               │   │       SimulatorConfig.h
│               │   │
│               │   ├───protobuf-lite
│               │   │   │   config.h
│               │   │   │
│               │   │   └───google
│               │   │       └───protobuf
│               │   │           │   extension_set.cc
│               │   │           │   extension_set.h
│               │   │           │   generated_message_util.cc
│               │   │           │   generated_message_util.h
│               │   │           │   message_lite.cc
│               │   │           │   message_lite.h
│               │   │           │   repeated_field.cc
│               │   │           │   repeated_field.h
│               │   │           │   wire_format_lite.cc
│               │   │           │   wire_format_lite.h
│               │   │           │   wire_format_lite_inl.h
│               │   │           │
│               │   │           ├───io
│               │   │           │       coded_stream.cc
│               │   │           │       coded_stream.h
│               │   │           │       coded_stream_inl.h
│               │   │           │       zero_copy_stream.cc
│               │   │           │       zero_copy_stream.h
│               │   │           │       zero_copy_stream_impl.h
│               │   │           │       zero_copy_stream_impl_lite.cc
│               │   │           │       zero_copy_stream_impl_lite.h
│               │   │           │
│               │   │           └───stubs
│               │   │                   atomicops.h
│               │   │                   atomicops_internals_arm_gcc.h
│               │   │                   atomicops_internals_atomicword_compat.h
│               │   │                   atomicops_internals_generic_gcc.h
│               │   │                   atomicops_internals_macosx.h
│               │   │                   atomicops_internals_x86_gcc.cc
│               │   │                   atomicops_internals_x86_gcc.h
│               │   │                   atomicops_internals_x86_msvc.cc
│               │   │                   atomicops_internals_x86_msvc.h
│               │   │                   common.cc
│               │   │                   common.h
│               │   │                   hash.h
│               │   │                   map-util.h
│               │   │                   once.cc
│               │   │                   once.h
│               │   │                   platform_macros.h
│               │   │                   stl_util.h
│               │   │                   stringprintf.cc
│               │   │                   stringprintf.h
│               │   │                   template_util.h
│               │   │                   type_traits.h
│               │   │
│               │   └───runtime
│               │           ConfigParser.cpp
│               │           ConfigParser.h
│               │           ConnectWaitLayer.cpp
│               │           ConnectWaitLayer.h
│               │           ConsoleCommand.cpp
│               │           ConsoleCommand.h
│               │           FileServer.cpp
│               │           FileServer.h
│               │           Landscape_png.cpp
│               │           PlayDisable_png.cpp
│               │           PlayEnable_png.cpp
│               │           Portrait_png.cpp
│               │           Protos.pb.cc
│               │           Protos.pb.h
│               │           ResData.h
│               │           Runtime.cpp
│               │           Runtime.h
│               │           RuntimeCCSImpl.cpp
│               │           RuntimeCCSImpl.h
│               │           RuntimeProtocol.cpp
│               │           RuntimeProtocol.h
│               │           Shine_png.cpp
│               │           VisibleRect.cpp
│               │           VisibleRect.h
│               │           Widget_mac.h
│               │           Widget_mac.mm
│               │
│               ├───proj.android
│               │   │   Android.mk
│               │   │
│               │   └───hellolua
│               │           Runtime_android.cpp
│               │
│               ├───proj.ios_mac
│               │   ├───ios
│               │   │       Prefix.pch
│               │   │
│               │   ├───libsimulator.xcodeproj
│               │   │       project.pbxproj
│               │   │
│               │   └───mac
│               │           Prefix.pch
│               │
│               └───proj.win32
│                       libsimulator.vcxproj
│                       libsimulator.vcxproj.filters
│                       Runtime_win32.cpp
│                       stdafx.cpp
│                       stdafx.h
│                       targetver.h
│
├───proj.android
│   │   .classpath
│   │   .cproject
│   │   .project
│   │   AndroidManifest.xml
│   │   ant.properties
│   │   build-cfg.json
│   │   build.xml
│   │   proguard-project.txt
│   │   project.properties
│   │
│   ├───.externalToolBuilders
│   │       org.eclipse.cdt.managedbuilder.core.genmakebuilder.launch
│   │
│   ├───.settings
│   │       org.eclipse.cdt.codan.core.prefs
│   │       org.eclipse.cdt.core.prefs
│   │       org.eclipse.ltk.core.refactoring.prefs
│   │
│   ├───jni
│   │   │   Android.mk
│   │   │   Application.mk
│   │   │
│   │   └───hellocpp
│   │           main.cpp
│   │
│   ├───res
│   │   ├───drawable-hdpi
│   │   │       icon.png
│   │   │
│   │   ├───drawable-ldpi
│   │   │       icon.png
│   │   │
│   │   ├───drawable-mdpi
│   │   │       icon.png
│   │   │
│   │   └───values
│   │           strings.xml
│   │
│   └───src
│       └───org
│           └───cocos2dx
│               └───cpp
│                       AppActivity.java
│
├───proj.android-studio
│   │   .gitignore
│   │   build-cfg.json
│   │   build.gradle
│   │   gradle.properties
│   │   gradlew
│   │   gradlew.bat
│   │   settings.gradle
│   │
│   ├───app
│   │   │   .gitignore
│   │   │   AndroidManifest.xml
│   │   │   build.gradle
│   │   │   proguard-rules.pro
│   │   │   project.properties
│   │   │
│   │   ├───jni
│   │   │   │   Android.mk
│   │   │   │   Application.mk
│   │   │   │
│   │   │   └───hellocpp
│   │   │           main.cpp
│   │   │
│   │   ├───res
│   │   │   ├───mipmap-hdpi
│   │   │   │       ic_launcher.png
│   │   │   │
│   │   │   ├───mipmap-mdpi
│   │   │   │       ic_launcher.png
│   │   │   │
│   │   │   ├───mipmap-xhdpi
│   │   │   │       ic_launcher.png
│   │   │   │
│   │   │   ├───mipmap-xxhdpi
│   │   │   │       ic_launcher.png
│   │   │   │
│   │   │   └───values
│   │   │           strings.xml
│   │   │
│   │   └───src
│   │       └───org
│   │           └───cocos2dx
│   │               └───cpp
│   │                       AppActivity.java
│   │
│   └───gradle
│       └───wrapper
│               gradle-wrapper.jar
│               gradle-wrapper.properties
│
├───proj.ios_mac
│   ├───CocosBasic.xcodeproj
│   │       project.pbxproj
│   │
│   ├───ios
│   │       AppController.h
│   │       AppController.mm
│   │       Default-568h@2x.png
│   │       Default-667h@2x.png
│   │       Default-736h@3x.png
│   │       Default-Landscape~ipad.png
│   │       Default.png
│   │       Default@2x.png
│   │       Icon-100.png
│   │       Icon-114.png
│   │       Icon-120.png
│   │       Icon-144.png
│   │       Icon-152.png
│   │       Icon-180.png
│   │       Icon-29.png
│   │       Icon-40.png
│   │       Icon-50.png
│   │       Icon-57.png
│   │       Icon-58.png
│   │       Icon-72.png
│   │       Icon-76.png
│   │       Icon-80.png
│   │       Icon-87.png
│   │       Info.plist
│   │       main.m
│   │       Prefix.pch
│   │       RootViewController.h
│   │       RootViewController.mm
│   │
│   └───mac
│           Icon.icns
│           Info.plist
│           main.cpp
│           Prefix.pch
│
├───proj.linux
│       main.cpp
│
├───proj.tizen
│   │   .cproject
│   │   .exportMap
│   │   .gitignore
│   │   .project
│   │   .tproject
│   │   copy_resource.sh
│   │   tizen-manifest.xml
│   │
│   ├───res
│   │       .gitkeep
│   │
│   ├───shared
│   │   └───res
│   │           CocosBasic.png
│   │
│   └───src
│           main.cpp
│
├───proj.win10
│   │   CocosBasic.sln
│   │
│   └───App
│       │   App.xaml
│       │   App.xaml.cpp
│       │   App.xaml.h
│       │   CocosBasic.vcxproj
│       │   CocosBasic.vcxproj.filters
│       │   CocosBasic_TemporaryKey.pfx
│       │   Package.appxmanifest
│       │   pch.cpp
│       │   pch.h
│       │   resources.props
│       │
│       ├───Assets
│       │       LockScreenLogo.scale-200.png
│       │       SplashScreen.scale-200.png
│       │       Square150x150Logo.scale-200.png
│       │       Square44x44Logo.scale-200.png
│       │       Square44x44Logo.targetsize-24_altform-unplated.png
│       │       StoreLogo.png
│       │       Wide310x150Logo.scale-200.png
│       │
│       └───Cocos2dEngine
│               Cocos2dRenderer.cpp
│               Cocos2dRenderer.h
│               OpenGLES.cpp
│               OpenGLES.h
│               OpenGLESPage.xaml
│               OpenGLESPage.xaml.cpp
│               OpenGLESPage.xaml.h
│
├───proj.win32
│   │   build-cfg.json
│   │   CocosBasic.sln
│   │   CocosBasic.vcxproj
│   │   CocosBasic.vcxproj.filters
│   │   CocosBasic.vcxproj.user
│   │   game.rc
│   │   main.cpp
│   │   main.h
│   │   resource.h
│   │
│   └───res
│           game.ico
│
├───proj.win8.1-universal
│   │   CocosBasic.sln
│   │
│   ├───App.Shared
│   │       App.xaml
│   │       App.xaml.cpp
│   │       App.xaml.h
│   │       Cocos2dRenderer.cpp
│   │       Cocos2dRenderer.h
│   │       CocosBasic.Shared.vcxitems
│   │       CocosBasic.Shared.vcxitems.filters
│   │       OpenGLES.cpp
│   │       OpenGLES.h
│   │       OpenGLESPage.xaml
│   │       OpenGLESPage.xaml.cpp
│   │       OpenGLESPage.xaml.h
│   │       pch.cpp
│   │       pch.h
│   │
│   ├───App.Windows
│   │   │   CocosBasic.Windows.vcxproj
│   │   │   CocosBasic.Windows.vcxproj.filters
│   │   │   CocosBasic.Windows_TemporaryKey.pfx
│   │   │   Package.appxmanifest
│   │   │
│   │   └───Assets
│   │           Logo.scale-100.png
│   │           SmallLogo.scale-100.png
│   │           SplashScreen.scale-100.png
│   │           StoreLogo.scale-100.png
│   │
│   └───App.WindowsPhone
│       │   CocosBasic.WindowsPhone.vcxproj
│       │   CocosBasic.WindowsPhone.vcxproj.filters
│       │   Package.appxmanifest
│       │
│       └───Assets
│               Logo.scale-240.png
│               SmallLogo.scale-240.png
│               SplashScreen.scale-240.png
│               Square71x71Logo.scale-240.png
│               StoreLogo.scale-240.png
│               WideLogo.scale-240.png
│
├───Resources
│   │   CloseNormal.png
│   │   CloseSelected.png
│   │   HelloWorld.png
│   │
│   ├───fonts
│   │       arial.ttf
│   │       Marker Felt.ttf
│   │
│   └───res
│           .gitkeep
│
└───_misc
        Project Structure and Contents.PNG
```
