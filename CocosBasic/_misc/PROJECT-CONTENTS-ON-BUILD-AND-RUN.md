### Project Contents on Build and Run

```
C:\Users\droid\onGit\cocos2d-x-templates\CocosBasic>tree /f
Folder PATH listing for volume OS
Volume serial number is 00000012 266E:E77F
C:.
│   $
│   .cocos-project.json
│   CMakeLists.txt
│   README.md
│   sam.txt
│
├───bin
│   └───debug
│       └───android
│               CocosBasic-debug.apk
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
│   │   │   │   │   │   .d
│   │   │   │   │   │   .project
│   │   │   │   │   │   AndroidManifest.xml
│   │   │   │   │   │   ant.properties
│   │   │   │   │   │   build.xml
│   │   │   │   │   │   lint.xml
│   │   │   │   │   │   local.properties
│   │   │   │   │   │   proguard-project.txt
│   │   │   │   │   │   project.properties
│   │   │   │   │   │
│   │   │   │   │   ├───.settings
│   │   │   │   │   │       org.eclipse.jdt.core.prefs
│   │   │   │   │   │
│   │   │   │   │   ├───bin
│   │   │   │   │   │   │   AndroidManifest.xml
│   │   │   │   │   │   │   AndroidManifest.xml.d
│   │   │   │   │   │   │   build.prop
│   │   │   │   │   │   │   classes.jar
│   │   │   │   │   │   │   jarlist.cache
│   │   │   │   │   │   │   proguard.txt
│   │   │   │   │   │   │
│   │   │   │   │   │   ├───aidl
│   │   │   │   │   │   │   └───com
│   │   │   │   │   │   │       └───enhance
│   │   │   │   │   │   │           └───gameservice
│   │   │   │   │   │   │                   IGameTuningService.aidl
│   │   │   │   │   │   │
│   │   │   │   │   │   ├───classes
│   │   │   │   │   │   │   ├───com
│   │   │   │   │   │   │   │   └───enhance
│   │   │   │   │   │   │   │       └───gameservice
│   │   │   │   │   │   │   │               IGameTuningService$Stub$Proxy.class
│   │   │   │   │   │   │   │               IGameTuningService$Stub.class
│   │   │   │   │   │   │   │               IGameTuningService.class
│   │   │   │   │   │   │   │
│   │   │   │   │   │   │   └───org
│   │   │   │   │   │   │       └───cocos2dx
│   │   │   │   │   │   │           └───lib
│   │   │   │   │   │   │                   BuildConfig.class
│   │   │   │   │   │   │                   Cocos2dxAccelerometer.class
│   │   │   │   │   │   │                   Cocos2dxActivity$1.class
│   │   │   │   │   │   │                   Cocos2dxActivity$Cocos2dxEGLConfigChooser$ConfigValue.class
│   │   │   │   │   │   │                   Cocos2dxActivity$Cocos2dxEGLConfigChooser.class
│   │   │   │   │   │   │                   Cocos2dxActivity.class
│   │   │   │   │   │   │                   Cocos2dxBitmap.class
│   │   │   │   │   │   │                   Cocos2dxDownloader$1.class
│   │   │   │   │   │   │                   Cocos2dxDownloader$2.class
│   │   │   │   │   │   │                   Cocos2dxDownloader$3$1.class
│   │   │   │   │   │   │                   Cocos2dxDownloader$3.class
│   │   │   │   │   │   │                   Cocos2dxDownloader$4.class
│   │   │   │   │   │   │                   Cocos2dxDownloader.class
│   │   │   │   │   │   │                   Cocos2dxEditBox.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$1$1$1.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$1$1.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$1$2$1.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$1$2$2.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$1$2.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$1$3.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$1$4.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$1.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$10.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$11.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$12.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$13.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$14.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$15.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$2.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$3.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$4.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$5.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$6.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$7.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$8.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper$9.class
│   │   │   │   │   │   │                   Cocos2dxEditBoxHelper.class
│   │   │   │   │   │   │                   Cocos2dxGLSurfaceView$1.class
│   │   │   │   │   │   │                   Cocos2dxGLSurfaceView$10.class
│   │   │   │   │   │   │                   Cocos2dxGLSurfaceView$11.class
│   │   │   │   │   │   │                   Cocos2dxGLSurfaceView$12.class
│   │   │   │   │   │   │                   Cocos2dxGLSurfaceView$13.class
│   │   │   │   │   │   │                   Cocos2dxGLSurfaceView$14.class
│   │   │   │   │   │   │                   Cocos2dxGLSurfaceView$2.class
│   │   │   │   │   │   │                   Cocos2dxGLSurfaceView$3.class
│   │   │   │   │   │   │                   Cocos2dxGLSurfaceView$4.class
│   │   │   │   │   │   │                   Cocos2dxGLSurfaceView$5.class
│   │   │   │   │   │   │                   Cocos2dxGLSurfaceView$6.class
│   │   │   │   │   │   │                   Cocos2dxGLSurfaceView$7.class
│   │   │   │   │   │   │                   Cocos2dxGLSurfaceView$8.class
│   │   │   │   │   │   │                   Cocos2dxGLSurfaceView$9.class
│   │   │   │   │   │   │                   Cocos2dxGLSurfaceView.class
│   │   │   │   │   │   │                   Cocos2dxHandler$1.class
│   │   │   │   │   │   │                   Cocos2dxHandler$DialogMessage.class
│   │   │   │   │   │   │                   Cocos2dxHandler.class
│   │   │   │   │   │   │                   Cocos2dxHelper$1.class
│   │   │   │   │   │   │                   Cocos2dxHelper$2.class
│   │   │   │   │   │   │                   Cocos2dxHelper$Cocos2dxHelperListener.class
│   │   │   │   │   │   │                   Cocos2dxHelper.class
│   │   │   │   │   │   │                   Cocos2dxHttpURLConnection.class
│   │   │   │   │   │   │                   Cocos2dxJavascriptJavaBridge.class
│   │   │   │   │   │   │                   Cocos2dxLocalStorage$DBOpenHelper.class
│   │   │   │   │   │   │                   Cocos2dxLocalStorage.class
│   │   │   │   │   │   │                   Cocos2dxLuaJavaBridge.class
│   │   │   │   │   │   │                   Cocos2dxMusic.class
│   │   │   │   │   │   │                   Cocos2dxReflectionHelper.class
│   │   │   │   │   │   │                   Cocos2dxRenderer.class
│   │   │   │   │   │   │                   Cocos2dxSound$OnLoadCompletedListener.class
│   │   │   │   │   │   │                   Cocos2dxSound$SoundInfoForLoadedCompleted.class
│   │   │   │   │   │   │                   Cocos2dxSound.class
│   │   │   │   │   │   │                   Cocos2dxTextInputWrapper.class
│   │   │   │   │   │   │                   Cocos2dxTypefaces.class
│   │   │   │   │   │   │                   Cocos2dxVideoHelper$1.class
│   │   │   │   │   │   │                   Cocos2dxVideoHelper$VideoEventRunnable.class
│   │   │   │   │   │   │                   Cocos2dxVideoHelper$VideoHandler.class
│   │   │   │   │   │   │                   Cocos2dxVideoHelper.class
│   │   │   │   │   │   │                   Cocos2dxVideoView$1.class
│   │   │   │   │   │   │                   Cocos2dxVideoView$2.class
│   │   │   │   │   │   │                   Cocos2dxVideoView$3.class
│   │   │   │   │   │   │                   Cocos2dxVideoView$4$1.class
│   │   │   │   │   │   │                   Cocos2dxVideoView$4.class
│   │   │   │   │   │   │                   Cocos2dxVideoView$5.class
│   │   │   │   │   │   │                   Cocos2dxVideoView$6.class
│   │   │   │   │   │   │                   Cocos2dxVideoView$OnVideoEventListener.class
│   │   │   │   │   │   │                   Cocos2dxVideoView.class
│   │   │   │   │   │   │                   Cocos2dxWebView$Cocos2dxWebViewClient$1.class
│   │   │   │   │   │   │                   Cocos2dxWebView$Cocos2dxWebViewClient$2.class
│   │   │   │   │   │   │                   Cocos2dxWebView$Cocos2dxWebViewClient$3.class
│   │   │   │   │   │   │                   Cocos2dxWebView$Cocos2dxWebViewClient.class
│   │   │   │   │   │   │                   Cocos2dxWebView.class
│   │   │   │   │   │   │                   Cocos2dxWebViewHelper$1.class
│   │   │   │   │   │   │                   Cocos2dxWebViewHelper$10.class
│   │   │   │   │   │   │                   Cocos2dxWebViewHelper$11.class
│   │   │   │   │   │   │                   Cocos2dxWebViewHelper$12.class
│   │   │   │   │   │   │                   Cocos2dxWebViewHelper$13.class
│   │   │   │   │   │   │                   Cocos2dxWebViewHelper$14.class
│   │   │   │   │   │   │                   Cocos2dxWebViewHelper$15.class
│   │   │   │   │   │   │                   Cocos2dxWebViewHelper$16.class
│   │   │   │   │   │   │                   Cocos2dxWebViewHelper$17.class
│   │   │   │   │   │   │                   Cocos2dxWebViewHelper$2.class
│   │   │   │   │   │   │                   Cocos2dxWebViewHelper$3.class
│   │   │   │   │   │   │                   Cocos2dxWebViewHelper$4.class
│   │   │   │   │   │   │                   Cocos2dxWebViewHelper$5.class
│   │   │   │   │   │   │                   Cocos2dxWebViewHelper$6.class
│   │   │   │   │   │   │                   Cocos2dxWebViewHelper$7.class
│   │   │   │   │   │   │                   Cocos2dxWebViewHelper$8.class
│   │   │   │   │   │   │                   Cocos2dxWebViewHelper$9.class
│   │   │   │   │   │   │                   Cocos2dxWebViewHelper.class
│   │   │   │   │   │   │                   DataTaskHandler.class
│   │   │   │   │   │   │                   DownloadTask.class
│   │   │   │   │   │   │                   FileTaskHandler.class
│   │   │   │   │   │   │                   GameControllerAdapter$1.class
│   │   │   │   │   │   │                   GameControllerAdapter$2.class
│   │   │   │   │   │   │                   GameControllerAdapter$3.class
│   │   │   │   │   │   │                   GameControllerAdapter$4.class
│   │   │   │   │   │   │                   GameControllerAdapter.class
│   │   │   │   │   │   │                   GameControllerDelegate$ControllerEventListener.class
│   │   │   │   │   │   │                   GameControllerDelegate.class
│   │   │   │   │   │   │                   GameControllerUtils.class
│   │   │   │   │   │   │                   ResizeLayout$1.class
│   │   │   │   │   │   │                   ResizeLayout.class
│   │   │   │   │   │   │                   ShouldStartLoadingWorker.class
│   │   │   │   │   │   │
│   │   │   │   │   │   ├───dexedLibs
│   │   │   │   │   │   └───res
│   │   │   │   │   ├───gen
│   │   │   │   │   │   │   R.java.d
│   │   │   │   │   │   │
│   │   │   │   │   │   ├───com
│   │   │   │   │   │   │   └───enhance
│   │   │   │   │   │   │       └───gameservice
│   │   │   │   │   │   │               IGameTuningService.java
│   │   │   │   │   │   │
│   │   │   │   │   │   └───org
│   │   │   │   │   │       └───cocos2dx
│   │   │   │   │   │           └───lib
│   │   │   │   │   │                   BuildConfig.java
│   │   │   │   │   │
│   │   │   │   │   ├───libs
│   │   │   │   │   │       android-async-http-1.4.9.jar
│   │   │   │   │   │       com.android.vending.expansion.zipfile.jar
│   │   │   │   │   │       httpclient-4.4.1.1.jar
│   │   │   │   │   │
│   │   │   │   │   ├───res
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
│   │   local.properties
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
│   ├───assets
│   │   │   CloseNormal.png
│   │   │   CloseSelected.png
│   │   │   HelloWorld.png
│   │   │
│   │   ├───fonts
│   │   │       arial.ttf
│   │   │       Marker Felt.ttf
│   │   │
│   │   └───res
│   │           .gitkeep
│   │
│   ├───bin
│   │   │   AndroidManifest.xml
│   │   │   AndroidManifest.xml.d
│   │   │   build.prop
│   │   │   classes.dex
│   │   │   classes.dex.d
│   │   │   CocosBasic-debug-unaligned.apk
│   │   │   CocosBasic-debug-unaligned.apk.d
│   │   │   CocosBasic-debug.apk
│   │   │   CocosBasic.ap_
│   │   │   CocosBasic.ap_.d
│   │   │   jarlist.cache
│   │   │   proguard.txt
│   │   │   R.txt
│   │   │
│   │   ├───classes
│   │   │   ├───com
│   │   │   │   └───trdroid
│   │   │   │       └───basicgame
│   │   │   │               BuildConfig.class
│   │   │   │               R$attr.class
│   │   │   │               R$drawable.class
│   │   │   │               R$string.class
│   │   │   │               R.class
│   │   │   │
│   │   │   └───org
│   │   │       └───cocos2dx
│   │   │           └───cpp
│   │   │                   AppActivity.class
│   │   │
│   │   ├───dexedLibs
│   │   │       android-async-http-1.4.9-cb288ed6be9795ff5c08b644ee8a105d.jar
│   │   │       classes-742bd190eaa641697213f114deac58d8.jar
│   │   │       com.android.vending.expansion.zipfile-ce09a94997edcee72b94a2ae60adfb01.jar
│   │   │       httpclient-4.4.1.1-e8fb98f14eb95fa71397f35b28b82c4b.jar
│   │   │
│   │   └───res
│   │       ├───drawable-hdpi
│   │       │       icon.png
│   │       │
│   │       ├───drawable-ldpi
│   │       │       icon.png
│   │       │
│   │       └───drawable-mdpi
│   │               icon.png
│   │
│   ├───gen
│   │   │   R.java.d
│   │   │
│   │   └───com
│   │       └───trdroid
│   │           └───basicgame
│   │                   BuildConfig.java
│   │                   R.java
│   │
│   ├───jni
│   │   │   Android.mk
│   │   │   Application.mk
│   │   │
│   │   └───hellocpp
│   │           main.cpp
│   │
│   ├───libs
│   │   └───armeabi
│   │           gdb.setup
│   │           gdbserver
│   │           libMyGame.so
│   │
│   ├───obj
│   │   └───local
│   │       └───armeabi
│   │           │   flatbuffers.a
│   │           │   libaudioengine.a
│   │           │   libbox2d.a
│   │           │   libbullet.a
│   │           │   libcocos2d.a
│   │           │   libcocos2dandroid.a
│   │           │   libcocos2dxinternal.a
│   │           │   libcocos3d.a
│   │           │   libcocosbuilder.a
│   │           │   libcocosdenshion.a
│   │           │   libcocostudio.a
│   │           │   libcpufeatures.a
│   │           │   libextension.a
│   │           │   libMyGame.so
│   │           │   libnetwork.a
│   │           │   librecast.a
│   │           │   libspine.a
│   │           │   libui.a
│   │           │
│   │           └───objs-debug
│   │               ├───audioengine_static
│   │               │   │   AssetFd.o
│   │               │   │   AssetFd.o.d
│   │               │   │   AudioDecoder.o
│   │               │   │   AudioDecoder.o.d
│   │               │   │   AudioEngine-inl.o
│   │               │   │   AudioEngine-inl.o.d
│   │               │   │   AudioMixer.o
│   │               │   │   AudioMixer.o.d
│   │               │   │   AudioMixerController.o
│   │               │   │   AudioMixerController.o.d
│   │               │   │   AudioPlayerProvider.o
│   │               │   │   AudioPlayerProvider.o.d
│   │               │   │   AudioResampler.o
│   │               │   │   AudioResampler.o.d
│   │               │   │   AudioResamplerCubic.o
│   │               │   │   AudioResamplerCubic.o.d
│   │               │   │   CCThreadPool.o
│   │               │   │   CCThreadPool.o.d
│   │               │   │   PcmAudioPlayer.o
│   │               │   │   PcmAudioPlayer.o.d
│   │               │   │   PcmAudioService.o
│   │               │   │   PcmAudioService.o.d
│   │               │   │   PcmBufferProvider.o
│   │               │   │   PcmBufferProvider.o.d
│   │               │   │   PcmData.o
│   │               │   │   PcmData.o.d
│   │               │   │   Track.o
│   │               │   │   Track.o.d
│   │               │   │   UrlAudioPlayer.o
│   │               │   │   UrlAudioPlayer.o.d
│   │               │   │
│   │               │   ├───audio_utils
│   │               │   │       format.o
│   │               │   │       format.o.d
│   │               │   │       minifloat.o
│   │               │   │       minifloat.o.d
│   │               │   │       primitives.o
│   │               │   │       primitives.o.d
│   │               │   │
│   │               │   ├───utils
│   │               │   │       Utils.o
│   │               │   │       Utils.o.d
│   │               │   │
│   │               │   └───__
│   │               │           AudioEngine.o
│   │               │           AudioEngine.o.d
│   │               │
│   │               ├───box2d_static
│   │               │   ├───Collision
│   │               │   │   │   b2BroadPhase.o
│   │               │   │   │   b2BroadPhase.o.d
│   │               │   │   │   b2CollideCircle.o
│   │               │   │   │   b2CollideCircle.o.d
│   │               │   │   │   b2CollideEdge.o
│   │               │   │   │   b2CollideEdge.o.d
│   │               │   │   │   b2CollidePolygon.o
│   │               │   │   │   b2CollidePolygon.o.d
│   │               │   │   │   b2Collision.o
│   │               │   │   │   b2Collision.o.d
│   │               │   │   │   b2Distance.o
│   │               │   │   │   b2Distance.o.d
│   │               │   │   │   b2DynamicTree.o
│   │               │   │   │   b2DynamicTree.o.d
│   │               │   │   │   b2TimeOfImpact.o
│   │               │   │   │   b2TimeOfImpact.o.d
│   │               │   │   │
│   │               │   │   └───Shapes
│   │               │   │           b2ChainShape.o
│   │               │   │           b2ChainShape.o.d
│   │               │   │           b2CircleShape.o
│   │               │   │           b2CircleShape.o.d
│   │               │   │           b2EdgeShape.o
│   │               │   │           b2EdgeShape.o.d
│   │               │   │           b2PolygonShape.o
│   │               │   │           b2PolygonShape.o.d
│   │               │   │
│   │               │   ├───Common
│   │               │   │       b2BlockAllocator.o
│   │               │   │       b2BlockAllocator.o.d
│   │               │   │       b2Draw.o
│   │               │   │       b2Draw.o.d
│   │               │   │       b2Math.o
│   │               │   │       b2Math.o.d
│   │               │   │       b2Settings.o
│   │               │   │       b2Settings.o.d
│   │               │   │       b2StackAllocator.o
│   │               │   │       b2StackAllocator.o.d
│   │               │   │       b2Timer.o
│   │               │   │       b2Timer.o.d
│   │               │   │
│   │               │   ├───Dynamics
│   │               │   │   │   b2Body.o
│   │               │   │   │   b2Body.o.d
│   │               │   │   │   b2ContactManager.o
│   │               │   │   │   b2ContactManager.o.d
│   │               │   │   │   b2Fixture.o
│   │               │   │   │   b2Fixture.o.d
│   │               │   │   │   b2Island.o
│   │               │   │   │   b2Island.o.d
│   │               │   │   │   b2World.o
│   │               │   │   │   b2World.o.d
│   │               │   │   │   b2WorldCallbacks.o
│   │               │   │   │   b2WorldCallbacks.o.d
│   │               │   │   │
│   │               │   │   ├───Contacts
│   │               │   │   │       b2ChainAndCircleContact.o
│   │               │   │   │       b2ChainAndCircleContact.o.d
│   │               │   │   │       b2ChainAndPolygonContact.o
│   │               │   │   │       b2ChainAndPolygonContact.o.d
│   │               │   │   │       b2CircleContact.o
│   │               │   │   │       b2CircleContact.o.d
│   │               │   │   │       b2Contact.o
│   │               │   │   │       b2Contact.o.d
│   │               │   │   │       b2ContactSolver.o
│   │               │   │   │       b2ContactSolver.o.d
│   │               │   │   │       b2EdgeAndCircleContact.o
│   │               │   │   │       b2EdgeAndCircleContact.o.d
│   │               │   │   │       b2EdgeAndPolygonContact.o
│   │               │   │   │       b2EdgeAndPolygonContact.o.d
│   │               │   │   │       b2PolygonAndCircleContact.o
│   │               │   │   │       b2PolygonAndCircleContact.o.d
│   │               │   │   │       b2PolygonContact.o
│   │               │   │   │       b2PolygonContact.o.d
│   │               │   │   │
│   │               │   │   └───Joints
│   │               │   │           b2DistanceJoint.o
│   │               │   │           b2DistanceJoint.o.d
│   │               │   │           b2FrictionJoint.o
│   │               │   │           b2FrictionJoint.o.d
│   │               │   │           b2GearJoint.o
│   │               │   │           b2GearJoint.o.d
│   │               │   │           b2Joint.o
│   │               │   │           b2Joint.o.d
│   │               │   │           b2MotorJoint.o
│   │               │   │           b2MotorJoint.o.d
│   │               │   │           b2MouseJoint.o
│   │               │   │           b2MouseJoint.o.d
│   │               │   │           b2PrismaticJoint.o
│   │               │   │           b2PrismaticJoint.o.d
│   │               │   │           b2PulleyJoint.o
│   │               │   │           b2PulleyJoint.o.d
│   │               │   │           b2RevoluteJoint.o
│   │               │   │           b2RevoluteJoint.o.d
│   │               │   │           b2RopeJoint.o
│   │               │   │           b2RopeJoint.o.d
│   │               │   │           b2WeldJoint.o
│   │               │   │           b2WeldJoint.o.d
│   │               │   │           b2WheelJoint.o
│   │               │   │           b2WheelJoint.o.d
│   │               │   │
│   │               │   └───Rope
│   │               │           b2Rope.o
│   │               │           b2Rope.o.d
│   │               │
│   │               ├───bullet_static
│   │               │   ├───BulletCollision
│   │               │   │   ├───BroadphaseCollision
│   │               │   │   │       btAxisSweep3.o
│   │               │   │   │       btAxisSweep3.o.d
│   │               │   │   │       btBroadphaseProxy.o
│   │               │   │   │       btBroadphaseProxy.o.d
│   │               │   │   │       btCollisionAlgorithm.o
│   │               │   │   │       btCollisionAlgorithm.o.d
│   │               │   │   │       btDbvt.o
│   │               │   │   │       btDbvt.o.d
│   │               │   │   │       btDbvtBroadphase.o
│   │               │   │   │       btDbvtBroadphase.o.d
│   │               │   │   │       btDispatcher.o
│   │               │   │   │       btDispatcher.o.d
│   │               │   │   │       btMultiSapBroadphase.o
│   │               │   │   │       btMultiSapBroadphase.o.d
│   │               │   │   │       btOverlappingPairCache.o
│   │               │   │   │       btOverlappingPairCache.o.d
│   │               │   │   │       btQuantizedBvh.o
│   │               │   │   │       btQuantizedBvh.o.d
│   │               │   │   │       btSimpleBroadphase.o
│   │               │   │   │       btSimpleBroadphase.o.d
│   │               │   │   │
│   │               │   │   ├───CollisionDispatch
│   │               │   │   │       btActivatingCollisionAlgorithm.o
│   │               │   │   │       btActivatingCollisionAlgorithm.o.d
│   │               │   │   │       btBox2dBox2dCollisionAlgorithm.o
│   │               │   │   │       btBox2dBox2dCollisionAlgorithm.o.d
│   │               │   │   │       btBoxBoxCollisionAlgorithm.o
│   │               │   │   │       btBoxBoxCollisionAlgorithm.o.d
│   │               │   │   │       btBoxBoxDetector.o
│   │               │   │   │       btBoxBoxDetector.o.d
│   │               │   │   │       btCollisionDispatcher.o
│   │               │   │   │       btCollisionDispatcher.o.d
│   │               │   │   │       btCollisionObject.o
│   │               │   │   │       btCollisionObject.o.d
│   │               │   │   │       btCollisionWorld.o
│   │               │   │   │       btCollisionWorld.o.d
│   │               │   │   │       btCompoundCollisionAlgorithm.o
│   │               │   │   │       btCompoundCollisionAlgorithm.o.d
│   │               │   │   │       btCompoundCompoundCollisionAlgorithm.o
│   │               │   │   │       btCompoundCompoundCollisionAlgorithm.o.d
│   │               │   │   │       btConvex2dConvex2dAlgorithm.o
│   │               │   │   │       btConvex2dConvex2dAlgorithm.o.d
│   │               │   │   │       btConvexConcaveCollisionAlgorithm.o
│   │               │   │   │       btConvexConcaveCollisionAlgorithm.o.d
│   │               │   │   │       btConvexConvexAlgorithm.o
│   │               │   │   │       btConvexConvexAlgorithm.o.d
│   │               │   │   │       btConvexPlaneCollisionAlgorithm.o
│   │               │   │   │       btConvexPlaneCollisionAlgorithm.o.d
│   │               │   │   │       btDefaultCollisionConfiguration.o
│   │               │   │   │       btDefaultCollisionConfiguration.o.d
│   │               │   │   │       btEmptyCollisionAlgorithm.o
│   │               │   │   │       btEmptyCollisionAlgorithm.o.d
│   │               │   │   │       btGhostObject.o
│   │               │   │   │       btGhostObject.o.d
│   │               │   │   │       btHashedSimplePairCache.o
│   │               │   │   │       btHashedSimplePairCache.o.d
│   │               │   │   │       btInternalEdgeUtility.o
│   │               │   │   │       btInternalEdgeUtility.o.d
│   │               │   │   │       btManifoldResult.o
│   │               │   │   │       btManifoldResult.o.d
│   │               │   │   │       btSimulationIslandManager.o
│   │               │   │   │       btSimulationIslandManager.o.d
│   │               │   │   │       btSphereBoxCollisionAlgorithm.o
│   │               │   │   │       btSphereBoxCollisionAlgorithm.o.d
│   │               │   │   │       btSphereSphereCollisionAlgorithm.o
│   │               │   │   │       btSphereSphereCollisionAlgorithm.o.d
│   │               │   │   │       btSphereTriangleCollisionAlgorithm.o
│   │               │   │   │       btSphereTriangleCollisionAlgorithm.o.d
│   │               │   │   │       btUnionFind.o
│   │               │   │   │       btUnionFind.o.d
│   │               │   │   │       SphereTriangleDetector.o
│   │               │   │   │       SphereTriangleDetector.o.d
│   │               │   │   │
│   │               │   │   ├───CollisionShapes
│   │               │   │   │       btBox2dShape.o
│   │               │   │   │       btBox2dShape.o.d
│   │               │   │   │       btBoxShape.o
│   │               │   │   │       btBoxShape.o.d
│   │               │   │   │       btBvhTriangleMeshShape.o
│   │               │   │   │       btBvhTriangleMeshShape.o.d
│   │               │   │   │       btCapsuleShape.o
│   │               │   │   │       btCapsuleShape.o.d
│   │               │   │   │       btCollisionShape.o
│   │               │   │   │       btCollisionShape.o.d
│   │               │   │   │       btCompoundShape.o
│   │               │   │   │       btCompoundShape.o.d
│   │               │   │   │       btConcaveShape.o
│   │               │   │   │       btConcaveShape.o.d
│   │               │   │   │       btConeShape.o
│   │               │   │   │       btConeShape.o.d
│   │               │   │   │       btConvex2dShape.o
│   │               │   │   │       btConvex2dShape.o.d
│   │               │   │   │       btConvexHullShape.o
│   │               │   │   │       btConvexHullShape.o.d
│   │               │   │   │       btConvexInternalShape.o
│   │               │   │   │       btConvexInternalShape.o.d
│   │               │   │   │       btConvexPointCloudShape.o
│   │               │   │   │       btConvexPointCloudShape.o.d
│   │               │   │   │       btConvexPolyhedron.o
│   │               │   │   │       btConvexPolyhedron.o.d
│   │               │   │   │       btConvexShape.o
│   │               │   │   │       btConvexShape.o.d
│   │               │   │   │       btConvexTriangleMeshShape.o
│   │               │   │   │       btConvexTriangleMeshShape.o.d
│   │               │   │   │       btCylinderShape.o
│   │               │   │   │       btCylinderShape.o.d
│   │               │   │   │       btEmptyShape.o
│   │               │   │   │       btEmptyShape.o.d
│   │               │   │   │       btHeightfieldTerrainShape.o
│   │               │   │   │       btHeightfieldTerrainShape.o.d
│   │               │   │   │       btMinkowskiSumShape.o
│   │               │   │   │       btMinkowskiSumShape.o.d
│   │               │   │   │       btMultimaterialTriangleMeshShape.o
│   │               │   │   │       btMultimaterialTriangleMeshShape.o.d
│   │               │   │   │       btMultiSphereShape.o
│   │               │   │   │       btMultiSphereShape.o.d
│   │               │   │   │       btOptimizedBvh.o
│   │               │   │   │       btOptimizedBvh.o.d
│   │               │   │   │       btPolyhedralConvexShape.o
│   │               │   │   │       btPolyhedralConvexShape.o.d
│   │               │   │   │       btScaledBvhTriangleMeshShape.o
│   │               │   │   │       btScaledBvhTriangleMeshShape.o.d
│   │               │   │   │       btShapeHull.o
│   │               │   │   │       btShapeHull.o.d
│   │               │   │   │       btSphereShape.o
│   │               │   │   │       btSphereShape.o.d
│   │               │   │   │       btStaticPlaneShape.o
│   │               │   │   │       btStaticPlaneShape.o.d
│   │               │   │   │       btStridingMeshInterface.o
│   │               │   │   │       btStridingMeshInterface.o.d
│   │               │   │   │       btTetrahedronShape.o
│   │               │   │   │       btTetrahedronShape.o.d
│   │               │   │   │       btTriangleBuffer.o
│   │               │   │   │       btTriangleBuffer.o.d
│   │               │   │   │       btTriangleCallback.o
│   │               │   │   │       btTriangleCallback.o.d
│   │               │   │   │       btTriangleIndexVertexArray.o
│   │               │   │   │       btTriangleIndexVertexArray.o.d
│   │               │   │   │       btTriangleIndexVertexMaterialArray.o
│   │               │   │   │       btTriangleIndexVertexMaterialArray.o.d
│   │               │   │   │       btTriangleMesh.o
│   │               │   │   │       btTriangleMesh.o.d
│   │               │   │   │       btTriangleMeshShape.o
│   │               │   │   │       btTriangleMeshShape.o.d
│   │               │   │   │       btUniformScalingShape.o
│   │               │   │   │       btUniformScalingShape.o.d
│   │               │   │   │
│   │               │   │   ├───Gimpact
│   │               │   │   │       btContactProcessing.o
│   │               │   │   │       btContactProcessing.o.d
│   │               │   │   │       btGenericPoolAllocator.o
│   │               │   │   │       btGenericPoolAllocator.o.d
│   │               │   │   │       btGImpactBvh.o
│   │               │   │   │       btGImpactBvh.o.d
│   │               │   │   │       btGImpactCollisionAlgorithm.o
│   │               │   │   │       btGImpactCollisionAlgorithm.o.d
│   │               │   │   │       btGImpactQuantizedBvh.o
│   │               │   │   │       btGImpactQuantizedBvh.o.d
│   │               │   │   │       btGImpactShape.o
│   │               │   │   │       btGImpactShape.o.d
│   │               │   │   │       btTriangleShapeEx.o
│   │               │   │   │       btTriangleShapeEx.o.d
│   │               │   │   │       gim_box_set.o
│   │               │   │   │       gim_box_set.o.d
│   │               │   │   │       gim_contact.o
│   │               │   │   │       gim_contact.o.d
│   │               │   │   │       gim_memory.o
│   │               │   │   │       gim_memory.o.d
│   │               │   │   │       gim_tri_collision.o
│   │               │   │   │       gim_tri_collision.o.d
│   │               │   │   │
│   │               │   │   └───NarrowPhaseCollision
│   │               │   │           btContinuousConvexCollision.o
│   │               │   │           btContinuousConvexCollision.o.d
│   │               │   │           btConvexCast.o
│   │               │   │           btConvexCast.o.d
│   │               │   │           btGjkConvexCast.o
│   │               │   │           btGjkConvexCast.o.d
│   │               │   │           btGjkEpa2.o
│   │               │   │           btGjkEpa2.o.d
│   │               │   │           btGjkEpaPenetrationDepthSolver.o
│   │               │   │           btGjkEpaPenetrationDepthSolver.o.d
│   │               │   │           btGjkPairDetector.o
│   │               │   │           btGjkPairDetector.o.d
│   │               │   │           btMinkowskiPenetrationDepthSolver.o
│   │               │   │           btMinkowskiPenetrationDepthSolver.o.d
│   │               │   │           btPersistentManifold.o
│   │               │   │           btPersistentManifold.o.d
│   │               │   │           btPolyhedralContactClipping.o
│   │               │   │           btPolyhedralContactClipping.o.d
│   │               │   │           btRaycastCallback.o
│   │               │   │           btRaycastCallback.o.d
│   │               │   │           btSubSimplexConvexCast.o
│   │               │   │           btSubSimplexConvexCast.o.d
│   │               │   │           btVoronoiSimplexSolver.o
│   │               │   │           btVoronoiSimplexSolver.o.d
│   │               │   │
│   │               │   ├───BulletDynamics
│   │               │   │   ├───Character
│   │               │   │   │       btKinematicCharacterController.o
│   │               │   │   │       btKinematicCharacterController.o.d
│   │               │   │   │
│   │               │   │   ├───ConstraintSolver
│   │               │   │   │       btConeTwistConstraint.o
│   │               │   │   │       btConeTwistConstraint.o.d
│   │               │   │   │       btContactConstraint.o
│   │               │   │   │       btContactConstraint.o.d
│   │               │   │   │       btFixedConstraint.o
│   │               │   │   │       btFixedConstraint.o.d
│   │               │   │   │       btGearConstraint.o
│   │               │   │   │       btGearConstraint.o.d
│   │               │   │   │       btGeneric6DofConstraint.o
│   │               │   │   │       btGeneric6DofConstraint.o.d
│   │               │   │   │       btGeneric6DofSpringConstraint.o
│   │               │   │   │       btGeneric6DofSpringConstraint.o.d
│   │               │   │   │       btHinge2Constraint.o
│   │               │   │   │       btHinge2Constraint.o.d
│   │               │   │   │       btHingeConstraint.o
│   │               │   │   │       btHingeConstraint.o.d
│   │               │   │   │       btPoint2PointConstraint.o
│   │               │   │   │       btPoint2PointConstraint.o.d
│   │               │   │   │       btSequentialImpulseConstraintSolver.o
│   │               │   │   │       btSequentialImpulseConstraintSolver.o.d
│   │               │   │   │       btSliderConstraint.o
│   │               │   │   │       btSliderConstraint.o.d
│   │               │   │   │       btSolve2LinearConstraint.o
│   │               │   │   │       btSolve2LinearConstraint.o.d
│   │               │   │   │       btTypedConstraint.o
│   │               │   │   │       btTypedConstraint.o.d
│   │               │   │   │       btUniversalConstraint.o
│   │               │   │   │       btUniversalConstraint.o.d
│   │               │   │   │
│   │               │   │   ├───Dynamics
│   │               │   │   │       btDiscreteDynamicsWorld.o
│   │               │   │   │       btDiscreteDynamicsWorld.o.d
│   │               │   │   │       btRigidBody.o
│   │               │   │   │       btRigidBody.o.d
│   │               │   │   │       btSimpleDynamicsWorld.o
│   │               │   │   │       btSimpleDynamicsWorld.o.d
│   │               │   │   │
│   │               │   │   ├───Featherstone
│   │               │   │   │       btMultiBody.o
│   │               │   │   │       btMultiBody.o.d
│   │               │   │   │       btMultiBodyConstraint.o
│   │               │   │   │       btMultiBodyConstraint.o.d
│   │               │   │   │       btMultiBodyConstraintSolver.o
│   │               │   │   │       btMultiBodyConstraintSolver.o.d
│   │               │   │   │       btMultiBodyDynamicsWorld.o
│   │               │   │   │       btMultiBodyDynamicsWorld.o.d
│   │               │   │   │       btMultiBodyJointLimitConstraint.o
│   │               │   │   │       btMultiBodyJointLimitConstraint.o.d
│   │               │   │   │       btMultiBodyJointMotor.o
│   │               │   │   │       btMultiBodyJointMotor.o.d
│   │               │   │   │       btMultiBodyPoint2Point.o
│   │               │   │   │       btMultiBodyPoint2Point.o.d
│   │               │   │   │
│   │               │   │   ├───MLCPSolvers
│   │               │   │   │       btDantzigLCP.o
│   │               │   │   │       btDantzigLCP.o.d
│   │               │   │   │       btMLCPSolver.o
│   │               │   │   │       btMLCPSolver.o.d
│   │               │   │   │
│   │               │   │   └───Vehicle
│   │               │   │           btRaycastVehicle.o
│   │               │   │           btRaycastVehicle.o.d
│   │               │   │           btWheelInfo.o
│   │               │   │           btWheelInfo.o.d
│   │               │   │
│   │               │   ├───BulletMultiThreaded
│   │               │   │   │   btGpu3DGridBroadphase.o
│   │               │   │   │   btGpu3DGridBroadphase.o.d
│   │               │   │   │   btParallelConstraintSolver.o
│   │               │   │   │   btParallelConstraintSolver.o.d
│   │               │   │   │   btThreadSupportInterface.o
│   │               │   │   │   btThreadSupportInterface.o.d
│   │               │   │   │   PosixThreadSupport.o
│   │               │   │   │   PosixThreadSupport.o.d
│   │               │   │   │   SequentialThreadSupport.o
│   │               │   │   │   SequentialThreadSupport.o.d
│   │               │   │   │   SpuCollisionObjectWrapper.o
│   │               │   │   │   SpuCollisionObjectWrapper.o.d
│   │               │   │   │   SpuCollisionTaskProcess.o
│   │               │   │   │   SpuCollisionTaskProcess.o.d
│   │               │   │   │   SpuContactManifoldCollisionAlgorithm.o
│   │               │   │   │   SpuContactManifoldCollisionAlgorithm.o.d
│   │               │   │   │   SpuFakeDma.o
│   │               │   │   │   SpuFakeDma.o.d
│   │               │   │   │   SpuGatheringCollisionDispatcher.o
│   │               │   │   │   SpuGatheringCollisionDispatcher.o.d
│   │               │   │   │   SpuLibspe2Support.o
│   │               │   │   │   SpuLibspe2Support.o.d
│   │               │   │   │   SpuSampleTaskProcess.o
│   │               │   │   │   SpuSampleTaskProcess.o.d
│   │               │   │   │
│   │               │   │   ├───SpuNarrowPhaseCollisionTask
│   │               │   │   │       boxBoxDistance.o
│   │               │   │   │       boxBoxDistance.o.d
│   │               │   │   │       SpuCollisionShapes.o
│   │               │   │   │       SpuCollisionShapes.o.d
│   │               │   │   │       SpuContactResult.o
│   │               │   │   │       SpuContactResult.o.d
│   │               │   │   │       SpuGatheringCollisionTask.o
│   │               │   │   │       SpuGatheringCollisionTask.o.d
│   │               │   │   │       SpuMinkowskiPenetrationDepthSolver.o
│   │               │   │   │       SpuMinkowskiPenetrationDepthSolver.o.d
│   │               │   │   │
│   │               │   │   └───SpuSampleTask
│   │               │   │           SpuSampleTask.o
│   │               │   │           SpuSampleTask.o.d
│   │               │   │
│   │               │   ├───LinearMath
│   │               │   │       btAlignedAllocator.o
│   │               │   │       btAlignedAllocator.o.d
│   │               │   │       btConvexHull.o
│   │               │   │       btConvexHull.o.d
│   │               │   │       btConvexHullComputer.o
│   │               │   │       btConvexHullComputer.o.d
│   │               │   │       btGeometryUtil.o
│   │               │   │       btGeometryUtil.o.d
│   │               │   │       btPolarDecomposition.o
│   │               │   │       btPolarDecomposition.o.d
│   │               │   │       btQuickprof.o
│   │               │   │       btQuickprof.o.d
│   │               │   │       btSerializer.o
│   │               │   │       btSerializer.o.d
│   │               │   │       btVector3.o
│   │               │   │       btVector3.o.d
│   │               │   │
│   │               │   └───MiniCL
│   │               │       │   MiniCL.o
│   │               │       │   MiniCL.o.d
│   │               │       │   MiniCLTaskScheduler.o
│   │               │       │   MiniCLTaskScheduler.o.d
│   │               │       │
│   │               │       └───MiniCLTask
│   │               │               MiniCLTask.o
│   │               │               MiniCLTask.o.d
│   │               │
│   │               ├───cocos2dxandroid_static
│   │               │   │   CCApplication-android.o
│   │               │   │   CCApplication-android.o.d
│   │               │   │   CCCommon-android.o
│   │               │   │   CCCommon-android.o.d
│   │               │   │   CCDevice-android.o
│   │               │   │   CCDevice-android.o.d
│   │               │   │   CCEnhanceAPI-android.o
│   │               │   │   CCEnhanceAPI-android.o.d
│   │               │   │   CCFileUtils-android.o
│   │               │   │   CCFileUtils-android.o.d
│   │               │   │   CCGLViewImpl-android.o
│   │               │   │   CCGLViewImpl-android.o.d
│   │               │   │   javaactivity-android.o
│   │               │   │   javaactivity-android.o.d
│   │               │   │
│   │               │   └───jni
│   │               │           Java_org_cocos2dx_lib_Cocos2dxAccelerometer.o
│   │               │           Java_org_cocos2dx_lib_Cocos2dxAccelerometer.o.d
│   │               │           Java_org_cocos2dx_lib_Cocos2dxBitmap.o
│   │               │           Java_org_cocos2dx_lib_Cocos2dxBitmap.o.d
│   │               │           Java_org_cocos2dx_lib_Cocos2dxHelper.o
│   │               │           Java_org_cocos2dx_lib_Cocos2dxHelper.o.d
│   │               │           Java_org_cocos2dx_lib_Cocos2dxRenderer.o
│   │               │           Java_org_cocos2dx_lib_Cocos2dxRenderer.o.d
│   │               │           JniHelper.o
│   │               │           JniHelper.o.d
│   │               │           TouchesJni.o
│   │               │           TouchesJni.o.d
│   │               │
│   │               ├───cocos2dx_internal_static
│   │               │   │   cocos2d.o
│   │               │   │   cocos2d.o.d
│   │               │   │
│   │               │   ├───2d
│   │               │   │       CCAction.o
│   │               │   │       CCAction.o.d
│   │               │   │       CCActionCamera.o
│   │               │   │       CCActionCamera.o.d
│   │               │   │       CCActionCatmullRom.o
│   │               │   │       CCActionCatmullRom.o.d
│   │               │   │       CCActionEase.o
│   │               │   │       CCActionEase.o.d
│   │               │   │       CCActionGrid.o
│   │               │   │       CCActionGrid.o.d
│   │               │   │       CCActionGrid3D.o
│   │               │   │       CCActionGrid3D.o.d
│   │               │   │       CCActionInstant.o
│   │               │   │       CCActionInstant.o.d
│   │               │   │       CCActionInterval.o
│   │               │   │       CCActionInterval.o.d
│   │               │   │       CCActionManager.o
│   │               │   │       CCActionManager.o.d
│   │               │   │       CCActionPageTurn3D.o
│   │               │   │       CCActionPageTurn3D.o.d
│   │               │   │       CCActionProgressTimer.o
│   │               │   │       CCActionProgressTimer.o.d
│   │               │   │       CCActionTiledGrid.o
│   │               │   │       CCActionTiledGrid.o.d
│   │               │   │       CCActionTween.o
│   │               │   │       CCActionTween.o.d
│   │               │   │       CCAnimation.o
│   │               │   │       CCAnimation.o.d
│   │               │   │       CCAnimationCache.o
│   │               │   │       CCAnimationCache.o.d
│   │               │   │       CCAtlasNode.o
│   │               │   │       CCAtlasNode.o.d
│   │               │   │       CCAutoPolygon.o
│   │               │   │       CCAutoPolygon.o.d
│   │               │   │       CCCamera.o
│   │               │   │       CCCamera.o.d
│   │               │   │       CCCameraBackgroundBrush.o
│   │               │   │       CCCameraBackgroundBrush.o.d
│   │               │   │       CCClippingNode.o
│   │               │   │       CCClippingNode.o.d
│   │               │   │       CCClippingRectangleNode.o
│   │               │   │       CCClippingRectangleNode.o.d
│   │               │   │       CCComponent.o
│   │               │   │       CCComponent.o.d
│   │               │   │       CCComponentContainer.o
│   │               │   │       CCComponentContainer.o.d
│   │               │   │       CCDrawingPrimitives.o
│   │               │   │       CCDrawingPrimitives.o.d
│   │               │   │       CCDrawNode.o
│   │               │   │       CCDrawNode.o.d
│   │               │   │       CCFastTMXLayer.o
│   │               │   │       CCFastTMXLayer.o.d
│   │               │   │       CCFastTMXTiledMap.o
│   │               │   │       CCFastTMXTiledMap.o.d
│   │               │   │       CCFont.o
│   │               │   │       CCFont.o.d
│   │               │   │       CCFontAtlas.o
│   │               │   │       CCFontAtlas.o.d
│   │               │   │       CCFontAtlasCache.o
│   │               │   │       CCFontAtlasCache.o.d
│   │               │   │       CCFontCharMap.o
│   │               │   │       CCFontCharMap.o.d
│   │               │   │       CCFontFNT.o
│   │               │   │       CCFontFNT.o.d
│   │               │   │       CCFontFreeType.o
│   │               │   │       CCFontFreeType.o.d
│   │               │   │       CCGLBufferedNode.o
│   │               │   │       CCGLBufferedNode.o.d
│   │               │   │       CCGrabber.o
│   │               │   │       CCGrabber.o.d
│   │               │   │       CCGrid.o
│   │               │   │       CCGrid.o.d
│   │               │   │       CCLabel.o
│   │               │   │       CCLabel.o.d
│   │               │   │       CCLabelAtlas.o
│   │               │   │       CCLabelAtlas.o.d
│   │               │   │       CCLabelBMFont.o
│   │               │   │       CCLabelBMFont.o.d
│   │               │   │       CCLabelTextFormatter.o
│   │               │   │       CCLabelTextFormatter.o.d
│   │               │   │       CCLabelTTF.o
│   │               │   │       CCLabelTTF.o.d
│   │               │   │       CCLayer.o
│   │               │   │       CCLayer.o.d
│   │               │   │       CCLight.o
│   │               │   │       CCLight.o.d
│   │               │   │       CCMenu.o
│   │               │   │       CCMenu.o.d
│   │               │   │       CCMenuItem.o
│   │               │   │       CCMenuItem.o.d
│   │               │   │       CCMotionStreak.o
│   │               │   │       CCMotionStreak.o.d
│   │               │   │       CCNode.o
│   │               │   │       CCNode.o.d
│   │               │   │       CCNodeGrid.o
│   │               │   │       CCNodeGrid.o.d
│   │               │   │       CCParallaxNode.o
│   │               │   │       CCParallaxNode.o.d
│   │               │   │       CCParticleBatchNode.o
│   │               │   │       CCParticleBatchNode.o.d
│   │               │   │       CCParticleExamples.o
│   │               │   │       CCParticleExamples.o.d
│   │               │   │       CCParticleSystem.o
│   │               │   │       CCParticleSystem.o.d
│   │               │   │       CCParticleSystemQuad.o
│   │               │   │       CCParticleSystemQuad.o.d
│   │               │   │       CCProgressTimer.o
│   │               │   │       CCProgressTimer.o.d
│   │               │   │       CCProtectedNode.o
│   │               │   │       CCProtectedNode.o.d
│   │               │   │       CCRenderTexture.o
│   │               │   │       CCRenderTexture.o.d
│   │               │   │       CCScene.o
│   │               │   │       CCScene.o.d
│   │               │   │       CCSprite.o
│   │               │   │       CCSprite.o.d
│   │               │   │       CCSpriteBatchNode.o
│   │               │   │       CCSpriteBatchNode.o.d
│   │               │   │       CCSpriteFrame.o
│   │               │   │       CCSpriteFrame.o.d
│   │               │   │       CCSpriteFrameCache.o
│   │               │   │       CCSpriteFrameCache.o.d
│   │               │   │       CCTextFieldTTF.o
│   │               │   │       CCTextFieldTTF.o.d
│   │               │   │       CCTileMapAtlas.o
│   │               │   │       CCTileMapAtlas.o.d
│   │               │   │       CCTMXLayer.o
│   │               │   │       CCTMXLayer.o.d
│   │               │   │       CCTMXObjectGroup.o
│   │               │   │       CCTMXObjectGroup.o.d
│   │               │   │       CCTMXTiledMap.o
│   │               │   │       CCTMXTiledMap.o.d
│   │               │   │       CCTMXXMLParser.o
│   │               │   │       CCTMXXMLParser.o.d
│   │               │   │       CCTransition.o
│   │               │   │       CCTransition.o.d
│   │               │   │       CCTransitionPageTurn.o
│   │               │   │       CCTransitionPageTurn.o.d
│   │               │   │       CCTransitionProgress.o
│   │               │   │       CCTransitionProgress.o.d
│   │               │   │       CCTweenFunction.o
│   │               │   │       CCTweenFunction.o.d
│   │               │   │
│   │               │   ├───3d
│   │               │   │       CCFrustum.o
│   │               │   │       CCFrustum.o.d
│   │               │   │       CCPlane.o
│   │               │   │       CCPlane.o.d
│   │               │   │
│   │               │   ├───base
│   │               │   │   │   atitc.o
│   │               │   │   │   atitc.o.d
│   │               │   │   │   base64.o
│   │               │   │   │   base64.o.d
│   │               │   │   │   CCAsyncTaskPool.o
│   │               │   │   │   CCAsyncTaskPool.o.d
│   │               │   │   │   CCAutoreleasePool.o
│   │               │   │   │   CCAutoreleasePool.o.d
│   │               │   │   │   ccCArray.o
│   │               │   │   │   ccCArray.o.d
│   │               │   │   │   CCConfiguration.o
│   │               │   │   │   CCConfiguration.o.d
│   │               │   │   │   CCConsole.o
│   │               │   │   │   CCConsole.o.d
│   │               │   │   │   CCController-android.o
│   │               │   │   │   CCController-android.o.d
│   │               │   │   │   CCController.o
│   │               │   │   │   CCController.o.d
│   │               │   │   │   CCData.o
│   │               │   │   │   CCData.o.d
│   │               │   │   │   CCDataVisitor.o
│   │               │   │   │   CCDataVisitor.o.d
│   │               │   │   │   CCDirector.o
│   │               │   │   │   CCDirector.o.d
│   │               │   │   │   CCEvent.o
│   │               │   │   │   CCEvent.o.d
│   │               │   │   │   CCEventAcceleration.o
│   │               │   │   │   CCEventAcceleration.o.d
│   │               │   │   │   CCEventController.o
│   │               │   │   │   CCEventController.o.d
│   │               │   │   │   CCEventCustom.o
│   │               │   │   │   CCEventCustom.o.d
│   │               │   │   │   CCEventDispatcher.o
│   │               │   │   │   CCEventDispatcher.o.d
│   │               │   │   │   CCEventFocus.o
│   │               │   │   │   CCEventFocus.o.d
│   │               │   │   │   CCEventKeyboard.o
│   │               │   │   │   CCEventKeyboard.o.d
│   │               │   │   │   CCEventListener.o
│   │               │   │   │   CCEventListener.o.d
│   │               │   │   │   CCEventListenerAcceleration.o
│   │               │   │   │   CCEventListenerAcceleration.o.d
│   │               │   │   │   CCEventListenerController.o
│   │               │   │   │   CCEventListenerController.o.d
│   │               │   │   │   CCEventListenerCustom.o
│   │               │   │   │   CCEventListenerCustom.o.d
│   │               │   │   │   CCEventListenerFocus.o
│   │               │   │   │   CCEventListenerFocus.o.d
│   │               │   │   │   CCEventListenerKeyboard.o
│   │               │   │   │   CCEventListenerKeyboard.o.d
│   │               │   │   │   CCEventListenerMouse.o
│   │               │   │   │   CCEventListenerMouse.o.d
│   │               │   │   │   CCEventListenerTouch.o
│   │               │   │   │   CCEventListenerTouch.o.d
│   │               │   │   │   CCEventMouse.o
│   │               │   │   │   CCEventMouse.o.d
│   │               │   │   │   CCEventTouch.o
│   │               │   │   │   CCEventTouch.o.d
│   │               │   │   │   ccFPSImages.o
│   │               │   │   │   ccFPSImages.o.d
│   │               │   │   │   CCIMEDispatcher.o
│   │               │   │   │   CCIMEDispatcher.o.d
│   │               │   │   │   CCNinePatchImageParser.o
│   │               │   │   │   CCNinePatchImageParser.o.d
│   │               │   │   │   CCNS.o
│   │               │   │   │   CCNS.o.d
│   │               │   │   │   CCProfiling.o
│   │               │   │   │   CCProfiling.o.d
│   │               │   │   │   CCProperties.o
│   │               │   │   │   CCProperties.o.d
│   │               │   │   │   ccRandom.o
│   │               │   │   │   ccRandom.o.d
│   │               │   │   │   CCRef.o
│   │               │   │   │   CCRef.o.d
│   │               │   │   │   CCScheduler.o
│   │               │   │   │   CCScheduler.o.d
│   │               │   │   │   CCScriptSupport.o
│   │               │   │   │   CCScriptSupport.o.d
│   │               │   │   │   CCStencilStateManager.o
│   │               │   │   │   CCStencilStateManager.o.d
│   │               │   │   │   CCTouch.o
│   │               │   │   │   CCTouch.o.d
│   │               │   │   │   ccTypes.o
│   │               │   │   │   ccTypes.o.d
│   │               │   │   │   CCUserDefault-android.o
│   │               │   │   │   CCUserDefault-android.o.d
│   │               │   │   │   CCUserDefault.o
│   │               │   │   │   CCUserDefault.o.d
│   │               │   │   │   ccUTF8.o
│   │               │   │   │   ccUTF8.o.d
│   │               │   │   │   ccUtils.o
│   │               │   │   │   ccUtils.o.d
│   │               │   │   │   CCValue.o
│   │               │   │   │   CCValue.o.d
│   │               │   │   │   etc1.o
│   │               │   │   │   etc1.o.d
│   │               │   │   │   ObjectFactory.o
│   │               │   │   │   ObjectFactory.o.d
│   │               │   │   │   pvr.o
│   │               │   │   │   pvr.o.d
│   │               │   │   │   s3tc.o
│   │               │   │   │   s3tc.o.d
│   │               │   │   │   TGAlib.o
│   │               │   │   │   TGAlib.o.d
│   │               │   │   │   ZipUtils.o
│   │               │   │   │   ZipUtils.o.d
│   │               │   │   │
│   │               │   │   └───allocator
│   │               │   │           CCAllocatorDiagnostics.o
│   │               │   │           CCAllocatorDiagnostics.o.d
│   │               │   │           CCAllocatorGlobal.o
│   │               │   │           CCAllocatorGlobal.o.d
│   │               │   │           CCAllocatorGlobalNewDelete.o
│   │               │   │           CCAllocatorGlobalNewDelete.o.d
│   │               │   │
│   │               │   ├───deprecated
│   │               │   │       CCArray.o
│   │               │   │       CCArray.o.d
│   │               │   │       CCDeprecated.o
│   │               │   │       CCDeprecated.o.d
│   │               │   │       CCDictionary.o
│   │               │   │       CCDictionary.o.d
│   │               │   │       CCNotificationCenter.o
│   │               │   │       CCNotificationCenter.o.d
│   │               │   │       CCSet.o
│   │               │   │       CCSet.o.d
│   │               │   │       CCString.o
│   │               │   │       CCString.o.d
│   │               │   │
│   │               │   ├───math
│   │               │   │       CCAffineTransform.o
│   │               │   │       CCAffineTransform.o.d
│   │               │   │       CCGeometry.o
│   │               │   │       CCGeometry.o.d
│   │               │   │       CCVertex.o
│   │               │   │       CCVertex.o.d
│   │               │   │       Mat4.o
│   │               │   │       Mat4.o.d
│   │               │   │       MathUtil.o
│   │               │   │       MathUtil.o.d
│   │               │   │       Quaternion.o
│   │               │   │       Quaternion.o.d
│   │               │   │       TransformUtils.o
│   │               │   │       TransformUtils.o.d
│   │               │   │       Vec2.o
│   │               │   │       Vec2.o.d
│   │               │   │       Vec3.o
│   │               │   │       Vec3.o.d
│   │               │   │       Vec4.o
│   │               │   │       Vec4.o.d
│   │               │   │
│   │               │   ├───navmesh
│   │               │   │       CCNavMesh.o
│   │               │   │       CCNavMesh.o.d
│   │               │   │       CCNavMeshAgent.o
│   │               │   │       CCNavMeshAgent.o.d
│   │               │   │       CCNavMeshDebugDraw.o
│   │               │   │       CCNavMeshDebugDraw.o.d
│   │               │   │       CCNavMeshObstacle.o
│   │               │   │       CCNavMeshObstacle.o.d
│   │               │   │       CCNavMeshUtils.o
│   │               │   │       CCNavMeshUtils.o.d
│   │               │   │
│   │               │   ├───physics
│   │               │   │       CCPhysicsBody.o
│   │               │   │       CCPhysicsBody.o.d
│   │               │   │       CCPhysicsContact.o
│   │               │   │       CCPhysicsContact.o.d
│   │               │   │       CCPhysicsJoint.o
│   │               │   │       CCPhysicsJoint.o.d
│   │               │   │       CCPhysicsShape.o
│   │               │   │       CCPhysicsShape.o.d
│   │               │   │       CCPhysicsWorld.o
│   │               │   │       CCPhysicsWorld.o.d
│   │               │   │
│   │               │   ├───physics3d
│   │               │   │       CCPhysics3D.o
│   │               │   │       CCPhysics3D.o.d
│   │               │   │       CCPhysics3DComponent.o
│   │               │   │       CCPhysics3DComponent.o.d
│   │               │   │       CCPhysics3DConstraint.o
│   │               │   │       CCPhysics3DConstraint.o.d
│   │               │   │       CCPhysics3DDebugDrawer.o
│   │               │   │       CCPhysics3DDebugDrawer.o.d
│   │               │   │       CCPhysics3DObject.o
│   │               │   │       CCPhysics3DObject.o.d
│   │               │   │       CCPhysics3DShape.o
│   │               │   │       CCPhysics3DShape.o.d
│   │               │   │       CCPhysics3DWorld.o
│   │               │   │       CCPhysics3DWorld.o.d
│   │               │   │       CCPhysicsSprite3D.o
│   │               │   │       CCPhysicsSprite3D.o.d
│   │               │   │
│   │               │   ├───platform
│   │               │   │       CCFileUtils.o
│   │               │   │       CCFileUtils.o.d
│   │               │   │       CCGLView.o
│   │               │   │       CCGLView.o.d
│   │               │   │       CCImage.o
│   │               │   │       CCImage.o.d
│   │               │   │       CCSAXParser.o
│   │               │   │       CCSAXParser.o.d
│   │               │   │       CCThread.o
│   │               │   │       CCThread.o.d
│   │               │   │
│   │               │   ├───renderer
│   │               │   │       CCBatchCommand.o
│   │               │   │       CCBatchCommand.o.d
│   │               │   │       CCCustomCommand.o
│   │               │   │       CCCustomCommand.o.d
│   │               │   │       CCFrameBuffer.o
│   │               │   │       CCFrameBuffer.o.d
│   │               │   │       CCGLProgram.o
│   │               │   │       CCGLProgram.o.d
│   │               │   │       CCGLProgramCache.o
│   │               │   │       CCGLProgramCache.o.d
│   │               │   │       CCGLProgramState.o
│   │               │   │       CCGLProgramState.o.d
│   │               │   │       CCGLProgramStateCache.o
│   │               │   │       CCGLProgramStateCache.o.d
│   │               │   │       ccGLStateCache.o
│   │               │   │       ccGLStateCache.o.d
│   │               │   │       CCGroupCommand.o
│   │               │   │       CCGroupCommand.o.d
│   │               │   │       CCMaterial.o
│   │               │   │       CCMaterial.o.d
│   │               │   │       CCMeshCommand.o
│   │               │   │       CCMeshCommand.o.d
│   │               │   │       CCPass.o
│   │               │   │       CCPass.o.d
│   │               │   │       CCPrimitive.o
│   │               │   │       CCPrimitive.o.d
│   │               │   │       CCPrimitiveCommand.o
│   │               │   │       CCPrimitiveCommand.o.d
│   │               │   │       CCQuadCommand.o
│   │               │   │       CCQuadCommand.o.d
│   │               │   │       CCRenderCommand.o
│   │               │   │       CCRenderCommand.o.d
│   │               │   │       CCRenderer.o
│   │               │   │       CCRenderer.o.d
│   │               │   │       CCRenderState.o
│   │               │   │       CCRenderState.o.d
│   │               │   │       ccShaders.o
│   │               │   │       ccShaders.o.d
│   │               │   │       CCTechnique.o
│   │               │   │       CCTechnique.o.d
│   │               │   │       CCTexture2D.o
│   │               │   │       CCTexture2D.o.d
│   │               │   │       CCTextureAtlas.o
│   │               │   │       CCTextureAtlas.o.d
│   │               │   │       CCTextureCache.o
│   │               │   │       CCTextureCache.o.d
│   │               │   │       CCTextureCube.o
│   │               │   │       CCTextureCube.o.d
│   │               │   │       CCTrianglesCommand.o
│   │               │   │       CCTrianglesCommand.o.d
│   │               │   │       CCVertexAttribBinding.o
│   │               │   │       CCVertexAttribBinding.o.d
│   │               │   │       CCVertexIndexBuffer.o
│   │               │   │       CCVertexIndexBuffer.o.d
│   │               │   │       CCVertexIndexData.o
│   │               │   │       CCVertexIndexData.o.d
│   │               │   │
│   │               │   ├───vr
│   │               │   │       CCVRDistortion.o
│   │               │   │       CCVRDistortion.o.d
│   │               │   │       CCVRDistortionMesh.o
│   │               │   │       CCVRDistortionMesh.o.d
│   │               │   │       CCVRGenericHeadTracker.o
│   │               │   │       CCVRGenericHeadTracker.o.d
│   │               │   │       CCVRGenericRenderer.o
│   │               │   │       CCVRGenericRenderer.o.d
│   │               │   │
│   │               │   └───__
│   │               │       └───external
│   │               │           ├───clipper
│   │               │           │       clipper.o
│   │               │           │       clipper.o.d
│   │               │           │
│   │               │           ├───ConvertUTF
│   │               │           │       ConvertUTF.o
│   │               │           │       ConvertUTF.o.d
│   │               │           │       ConvertUTFWrapper.o
│   │               │           │       ConvertUTFWrapper.o.d
│   │               │           │
│   │               │           ├───edtaa3func
│   │               │           │       edtaa3func.o
│   │               │           │       edtaa3func.o.d
│   │               │           │
│   │               │           ├───poly2tri
│   │               │           │   ├───common
│   │               │           │   │       shapes.o
│   │               │           │   │       shapes.o.d
│   │               │           │   │
│   │               │           │   └───sweep
│   │               │           │           advancing_front.o
│   │               │           │           advancing_front.o.d
│   │               │           │           cdt.o
│   │               │           │           cdt.o.d
│   │               │           │           sweep.o
│   │               │           │           sweep.o.d
│   │               │           │           sweep_context.o
│   │               │           │           sweep_context.o.d
│   │               │           │
│   │               │           ├───tinyxml2
│   │               │           │       tinyxml2.o
│   │               │           │       tinyxml2.o.d
│   │               │           │
│   │               │           ├───unzip
│   │               │           │       ioapi.o
│   │               │           │       ioapi.o.d
│   │               │           │       ioapi_mem.o
│   │               │           │       ioapi_mem.o.d
│   │               │           │       unzip.o
│   │               │           │       unzip.o.d
│   │               │           │
│   │               │           └───xxhash
│   │               │                   xxhash.o
│   │               │                   xxhash.o.d
│   │               │
│   │               ├───cocos3d_static
│   │               │       CCAABB.o
│   │               │       CCAABB.o.d
│   │               │       CCAnimate3D.o
│   │               │       CCAnimate3D.o.d
│   │               │       CCAnimation3D.o
│   │               │       CCAnimation3D.o.d
│   │               │       CCAttachNode.o
│   │               │       CCAttachNode.o.d
│   │               │       CCBillBoard.o
│   │               │       CCBillBoard.o.d
│   │               │       CCBundle3D.o
│   │               │       CCBundle3D.o.d
│   │               │       CCBundleReader.o
│   │               │       CCBundleReader.o.d
│   │               │       CCMesh.o
│   │               │       CCMesh.o.d
│   │               │       CCMeshSkin.o
│   │               │       CCMeshSkin.o.d
│   │               │       CCMeshVertexIndexData.o
│   │               │       CCMeshVertexIndexData.o.d
│   │               │       CCMotionStreak3D.o
│   │               │       CCMotionStreak3D.o.d
│   │               │       CCOBB.o
│   │               │       CCOBB.o.d
│   │               │       CCObjLoader.o
│   │               │       CCObjLoader.o.d
│   │               │       CCRay.o
│   │               │       CCRay.o.d
│   │               │       CCSkeleton3D.o
│   │               │       CCSkeleton3D.o.d
│   │               │       CCSkybox.o
│   │               │       CCSkybox.o.d
│   │               │       CCSprite3D.o
│   │               │       CCSprite3D.o.d
│   │               │       CCSprite3DMaterial.o
│   │               │       CCSprite3DMaterial.o.d
│   │               │       CCTerrain.o
│   │               │       CCTerrain.o.d
│   │               │
│   │               ├───cocosbuilder_static
│   │               │       CCBAnimationManager.o
│   │               │       CCBAnimationManager.o.d
│   │               │       CCBFileLoader.o
│   │               │       CCBFileLoader.o.d
│   │               │       CCBKeyframe.o
│   │               │       CCBKeyframe.o.d
│   │               │       CCBReader.o
│   │               │       CCBReader.o.d
│   │               │       CCBSequence.o
│   │               │       CCBSequence.o.d
│   │               │       CCBSequenceProperty.o
│   │               │       CCBSequenceProperty.o.d
│   │               │       CCControlButtonLoader.o
│   │               │       CCControlButtonLoader.o.d
│   │               │       CCControlLoader.o
│   │               │       CCControlLoader.o.d
│   │               │       CCLabelBMFontLoader.o
│   │               │       CCLabelBMFontLoader.o.d
│   │               │       CCLabelTTFLoader.o
│   │               │       CCLabelTTFLoader.o.d
│   │               │       CCLayerColorLoader.o
│   │               │       CCLayerColorLoader.o.d
│   │               │       CCLayerGradientLoader.o
│   │               │       CCLayerGradientLoader.o.d
│   │               │       CCLayerLoader.o
│   │               │       CCLayerLoader.o.d
│   │               │       CCMenuItemImageLoader.o
│   │               │       CCMenuItemImageLoader.o.d
│   │               │       CCMenuItemLoader.o
│   │               │       CCMenuItemLoader.o.d
│   │               │       CCNode+CCBRelativePositioning.o
│   │               │       CCNode+CCBRelativePositioning.o.d
│   │               │       CCNodeLoader.o
│   │               │       CCNodeLoader.o.d
│   │               │       CCNodeLoaderLibrary.o
│   │               │       CCNodeLoaderLibrary.o.d
│   │               │       CCParticleSystemQuadLoader.o
│   │               │       CCParticleSystemQuadLoader.o.d
│   │               │       CCScale9SpriteLoader.o
│   │               │       CCScale9SpriteLoader.o.d
│   │               │       CCScrollViewLoader.o
│   │               │       CCScrollViewLoader.o.d
│   │               │       CCSpriteLoader.o
│   │               │       CCSpriteLoader.o.d
│   │               │
│   │               ├───cocosdenshion_static
│   │               │   │   ccdandroidUtils.o
│   │               │   │   ccdandroidUtils.o.d
│   │               │   │   cddSimpleAudioEngine.o
│   │               │   │   cddSimpleAudioEngine.o.d
│   │               │   │
│   │               │   └───jni
│   │               │           cddandroidAndroidJavaEngine.o
│   │               │           cddandroidAndroidJavaEngine.o.d
│   │               │
│   │               ├───cocostudio_static
│   │               │   │   CCActionFrame.o
│   │               │   │   CCActionFrame.o.d
│   │               │   │   CCActionFrameEasing.o
│   │               │   │   CCActionFrameEasing.o.d
│   │               │   │   CCActionManagerEx.o
│   │               │   │   CCActionManagerEx.o.d
│   │               │   │   CCActionNode.o
│   │               │   │   CCActionNode.o.d
│   │               │   │   CCActionObject.o
│   │               │   │   CCActionObject.o.d
│   │               │   │   CCArmature.o
│   │               │   │   CCArmature.o.d
│   │               │   │   CCArmatureAnimation.o
│   │               │   │   CCArmatureAnimation.o.d
│   │               │   │   CCArmatureDataManager.o
│   │               │   │   CCArmatureDataManager.o.d
│   │               │   │   CCArmatureDefine.o
│   │               │   │   CCArmatureDefine.o.d
│   │               │   │   CCBatchNode.o
│   │               │   │   CCBatchNode.o.d
│   │               │   │   CCBone.o
│   │               │   │   CCBone.o.d
│   │               │   │   CCColliderDetector.o
│   │               │   │   CCColliderDetector.o.d
│   │               │   │   CCComAttribute.o
│   │               │   │   CCComAttribute.o.d
│   │               │   │   CCComAudio.o
│   │               │   │   CCComAudio.o.d
│   │               │   │   CCComController.o
│   │               │   │   CCComController.o.d
│   │               │   │   CCComExtensionData.o
│   │               │   │   CCComExtensionData.o.d
│   │               │   │   CCComRender.o
│   │               │   │   CCComRender.o.d
│   │               │   │   CCDataReaderHelper.o
│   │               │   │   CCDataReaderHelper.o.d
│   │               │   │   CCDatas.o
│   │               │   │   CCDatas.o.d
│   │               │   │   CCDecorativeDisplay.o
│   │               │   │   CCDecorativeDisplay.o.d
│   │               │   │   CCDisplayFactory.o
│   │               │   │   CCDisplayFactory.o.d
│   │               │   │   CCDisplayManager.o
│   │               │   │   CCDisplayManager.o.d
│   │               │   │   CCInputDelegate.o
│   │               │   │   CCInputDelegate.o.d
│   │               │   │   CCProcessBase.o
│   │               │   │   CCProcessBase.o.d
│   │               │   │   CCSGUIReader.o
│   │               │   │   CCSGUIReader.o.d
│   │               │   │   CCSkin.o
│   │               │   │   CCSkin.o.d
│   │               │   │   CCSpriteFrameCacheHelper.o
│   │               │   │   CCSpriteFrameCacheHelper.o.d
│   │               │   │   CCSSceneReader.o
│   │               │   │   CCSSceneReader.o.d
│   │               │   │   CCTransformHelp.o
│   │               │   │   CCTransformHelp.o.d
│   │               │   │   CCTween.o
│   │               │   │   CCTween.o.d
│   │               │   │   CCUtilMath.o
│   │               │   │   CCUtilMath.o.d
│   │               │   │   CocoLoader.o
│   │               │   │   CocoLoader.o.d
│   │               │   │   CocoStudio.o
│   │               │   │   CocoStudio.o.d
│   │               │   │   DictionaryHelper.o
│   │               │   │   DictionaryHelper.o.d
│   │               │   │   FlatBuffersSerialize.o
│   │               │   │   FlatBuffersSerialize.o.d
│   │               │   │   LocalizationManager.o
│   │               │   │   LocalizationManager.o.d
│   │               │   │   TriggerBase.o
│   │               │   │   TriggerBase.o.d
│   │               │   │   TriggerMng.o
│   │               │   │   TriggerMng.o.d
│   │               │   │   TriggerObj.o
│   │               │   │   TriggerObj.o.d
│   │               │   │   WidgetCallBackHandlerProtocol.o
│   │               │   │   WidgetCallBackHandlerProtocol.o.d
│   │               │   │
│   │               │   ├───ActionTimeline
│   │               │   │       CCActionTimeline.o
│   │               │   │       CCActionTimeline.o.d
│   │               │   │       CCActionTimelineCache.o
│   │               │   │       CCActionTimelineCache.o.d
│   │               │   │       CCActionTimelineNode.o
│   │               │   │       CCActionTimelineNode.o.d
│   │               │   │       CCBoneNode.o
│   │               │   │       CCBoneNode.o.d
│   │               │   │       CCFrame.o
│   │               │   │       CCFrame.o.d
│   │               │   │       CCSkeletonNode.o
│   │               │   │       CCSkeletonNode.o.d
│   │               │   │       CCSkinNode.o
│   │               │   │       CCSkinNode.o.d
│   │               │   │       CCTimeLine.o
│   │               │   │       CCTimeLine.o.d
│   │               │   │       CSLoader.o
│   │               │   │       CSLoader.o.d
│   │               │   │
│   │               │   └───WidgetReader
│   │               │       │   WidgetReader.o
│   │               │       │   WidgetReader.o.d
│   │               │       │
│   │               │       ├───ArmatureNodeReader
│   │               │       │       ArmatureNodeReader.o
│   │               │       │       ArmatureNodeReader.o.d
│   │               │       │
│   │               │       ├───ButtonReader
│   │               │       │       ButtonReader.o
│   │               │       │       ButtonReader.o.d
│   │               │       │
│   │               │       ├───CheckBoxReader
│   │               │       │       CheckBoxReader.o
│   │               │       │       CheckBoxReader.o.d
│   │               │       │
│   │               │       ├───ComAudioReader
│   │               │       │       ComAudioReader.o
│   │               │       │       ComAudioReader.o.d
│   │               │       │
│   │               │       ├───GameMapReader
│   │               │       │       GameMapReader.o
│   │               │       │       GameMapReader.o.d
│   │               │       │
│   │               │       ├───GameNode3DReader
│   │               │       │       GameNode3DReader.o
│   │               │       │       GameNode3DReader.o.d
│   │               │       │
│   │               │       ├───ImageViewReader
│   │               │       │       ImageViewReader.o
│   │               │       │       ImageViewReader.o.d
│   │               │       │
│   │               │       ├───LayoutReader
│   │               │       │       LayoutReader.o
│   │               │       │       LayoutReader.o.d
│   │               │       │
│   │               │       ├───Light3DReader
│   │               │       │       Light3DReader.o
│   │               │       │       Light3DReader.o.d
│   │               │       │
│   │               │       ├───ListViewReader
│   │               │       │       ListViewReader.o
│   │               │       │       ListViewReader.o.d
│   │               │       │
│   │               │       ├───LoadingBarReader
│   │               │       │       LoadingBarReader.o
│   │               │       │       LoadingBarReader.o.d
│   │               │       │
│   │               │       ├───Node3DReader
│   │               │       │       Node3DReader.o
│   │               │       │       Node3DReader.o.d
│   │               │       │
│   │               │       ├───NodeReader
│   │               │       │       NodeReader.o
│   │               │       │       NodeReader.o.d
│   │               │       │
│   │               │       ├───PageViewReader
│   │               │       │       PageViewReader.o
│   │               │       │       PageViewReader.o.d
│   │               │       │
│   │               │       ├───Particle3DReader
│   │               │       │       Particle3DReader.o
│   │               │       │       Particle3DReader.o.d
│   │               │       │
│   │               │       ├───ParticleReader
│   │               │       │       ParticleReader.o
│   │               │       │       ParticleReader.o.d
│   │               │       │
│   │               │       ├───ProjectNodeReader
│   │               │       │       ProjectNodeReader.o
│   │               │       │       ProjectNodeReader.o.d
│   │               │       │
│   │               │       ├───ScrollViewReader
│   │               │       │       ScrollViewReader.o
│   │               │       │       ScrollViewReader.o.d
│   │               │       │
│   │               │       ├───SingleNodeReader
│   │               │       │       SingleNodeReader.o
│   │               │       │       SingleNodeReader.o.d
│   │               │       │
│   │               │       ├───SkeletonReader
│   │               │       │       BoneNodeReader.o
│   │               │       │       BoneNodeReader.o.d
│   │               │       │       SkeletonNodeReader.o
│   │               │       │       SkeletonNodeReader.o.d
│   │               │       │
│   │               │       ├───SliderReader
│   │               │       │       SliderReader.o
│   │               │       │       SliderReader.o.d
│   │               │       │
│   │               │       ├───Sprite3DReader
│   │               │       │       Sprite3DReader.o
│   │               │       │       Sprite3DReader.o.d
│   │               │       │
│   │               │       ├───SpriteReader
│   │               │       │       SpriteReader.o
│   │               │       │       SpriteReader.o.d
│   │               │       │
│   │               │       ├───TabControlReader
│   │               │       │       TabControlReader.o
│   │               │       │       TabControlReader.o.d
│   │               │       │
│   │               │       ├───TextAtlasReader
│   │               │       │       TextAtlasReader.o
│   │               │       │       TextAtlasReader.o.d
│   │               │       │
│   │               │       ├───TextBMFontReader
│   │               │       │       TextBMFontReader.o
│   │               │       │       TextBMFontReader.o.d
│   │               │       │
│   │               │       ├───TextFieldReader
│   │               │       │       TextFieldReader.o
│   │               │       │       TextFieldReader.o.d
│   │               │       │
│   │               │       ├───TextReader
│   │               │       │       TextReader.o
│   │               │       │       TextReader.o.d
│   │               │       │
│   │               │       └───UserCameraReader
│   │               │               UserCameraReader.o
│   │               │               UserCameraReader.o.d
│   │               │
│   │               ├───cocos_extension_static
│   │               │   ├───assets-manager
│   │               │   │       AssetsManager.o
│   │               │   │       AssetsManager.o.d
│   │               │   │       AssetsManagerEx.o
│   │               │   │       AssetsManagerEx.o.d
│   │               │   │       CCEventAssetsManagerEx.o
│   │               │   │       CCEventAssetsManagerEx.o.d
│   │               │   │       CCEventListenerAssetsManagerEx.o
│   │               │   │       CCEventListenerAssetsManagerEx.o.d
│   │               │   │       Manifest.o
│   │               │   │       Manifest.o.d
│   │               │   │
│   │               │   ├───GUI
│   │               │   │   ├───CCControlExtension
│   │               │   │   │       CCControl.o
│   │               │   │   │       CCControl.o.d
│   │               │   │   │       CCControlButton.o
│   │               │   │   │       CCControlButton.o.d
│   │               │   │   │       CCControlColourPicker.o
│   │               │   │   │       CCControlColourPicker.o.d
│   │               │   │   │       CCControlHuePicker.o
│   │               │   │   │       CCControlHuePicker.o.d
│   │               │   │   │       CCControlPotentiometer.o
│   │               │   │   │       CCControlPotentiometer.o.d
│   │               │   │   │       CCControlSaturationBrightnessPicker.o
│   │               │   │   │       CCControlSaturationBrightnessPicker.o.d
│   │               │   │   │       CCControlSlider.o
│   │               │   │   │       CCControlSlider.o.d
│   │               │   │   │       CCControlStepper.o
│   │               │   │   │       CCControlStepper.o.d
│   │               │   │   │       CCControlSwitch.o
│   │               │   │   │       CCControlSwitch.o.d
│   │               │   │   │       CCControlUtils.o
│   │               │   │   │       CCControlUtils.o.d
│   │               │   │   │       CCInvocation.o
│   │               │   │   │       CCInvocation.o.d
│   │               │   │   │
│   │               │   │   └───CCScrollView
│   │               │   │           CCScrollView.o
│   │               │   │           CCScrollView.o.d
│   │               │   │           CCTableView.o
│   │               │   │           CCTableView.o.d
│   │               │   │           CCTableViewCell.o
│   │               │   │           CCTableViewCell.o.d
│   │               │   │
│   │               │   ├───Particle3D
│   │               │   │   │   CCParticle3DAffector.o
│   │               │   │   │   CCParticle3DAffector.o.d
│   │               │   │   │   CCParticle3DEmitter.o
│   │               │   │   │   CCParticle3DEmitter.o.d
│   │               │   │   │   CCParticle3DRender.o
│   │               │   │   │   CCParticle3DRender.o.d
│   │               │   │   │   CCParticleSystem3D.o
│   │               │   │   │   CCParticleSystem3D.o.d
│   │               │   │   │
│   │               │   │   └───PU
│   │               │   │           CCPUAffector.o
│   │               │   │           CCPUAffector.o.d
│   │               │   │           CCPUAffectorManager.o
│   │               │   │           CCPUAffectorManager.o.d
│   │               │   │           CCPUAffectorTranslator.o
│   │               │   │           CCPUAffectorTranslator.o.d
│   │               │   │           CCPUAlignAffector.o
│   │               │   │           CCPUAlignAffector.o.d
│   │               │   │           CCPUAlignAffectorTranslator.o
│   │               │   │           CCPUAlignAffectorTranslator.o.d
│   │               │   │           CCPUBaseCollider.o
│   │               │   │           CCPUBaseCollider.o.d
│   │               │   │           CCPUBaseColliderTranslator.o
│   │               │   │           CCPUBaseColliderTranslator.o.d
│   │               │   │           CCPUBaseForceAffector.o
│   │               │   │           CCPUBaseForceAffector.o.d
│   │               │   │           CCPUBaseForceAffectorTranslator.o
│   │               │   │           CCPUBaseForceAffectorTranslator.o.d
│   │               │   │           CCPUBeamRender.o
│   │               │   │           CCPUBeamRender.o.d
│   │               │   │           CCPUBehaviour.o
│   │               │   │           CCPUBehaviour.o.d
│   │               │   │           CCPUBehaviourManager.o
│   │               │   │           CCPUBehaviourManager.o.d
│   │               │   │           CCPUBehaviourTranslator.o
│   │               │   │           CCPUBehaviourTranslator.o.d
│   │               │   │           CCPUBillboardChain.o
│   │               │   │           CCPUBillboardChain.o.d
│   │               │   │           CCPUBoxCollider.o
│   │               │   │           CCPUBoxCollider.o.d
│   │               │   │           CCPUBoxColliderTranslator.o
│   │               │   │           CCPUBoxColliderTranslator.o.d
│   │               │   │           CCPUBoxEmitter.o
│   │               │   │           CCPUBoxEmitter.o.d
│   │               │   │           CCPUBoxEmitterTranslator.o
│   │               │   │           CCPUBoxEmitterTranslator.o.d
│   │               │   │           CCPUCircleEmitter.o
│   │               │   │           CCPUCircleEmitter.o.d
│   │               │   │           CCPUCircleEmitterTranslator.o
│   │               │   │           CCPUCircleEmitterTranslator.o.d
│   │               │   │           CCPUCollisionAvoidanceAffector.o
│   │               │   │           CCPUCollisionAvoidanceAffector.o.d
│   │               │   │           CCPUCollisionAvoidanceAffectorTranslator.o
│   │               │   │           CCPUCollisionAvoidanceAffectorTranslator.o.d
│   │               │   │           CCPUColorAffector.o
│   │               │   │           CCPUColorAffector.o.d
│   │               │   │           CCPUColorAffectorTranslator.o
│   │               │   │           CCPUColorAffectorTranslator.o.d
│   │               │   │           CCPUDoAffectorEventHandler.o
│   │               │   │           CCPUDoAffectorEventHandler.o.d
│   │               │   │           CCPUDoAffectorEventHandlerTranslator.o
│   │               │   │           CCPUDoAffectorEventHandlerTranslator.o.d
│   │               │   │           CCPUDoEnableComponentEventHandler.o
│   │               │   │           CCPUDoEnableComponentEventHandler.o.d
│   │               │   │           CCPUDoEnableComponentEventHandlerTranslator.o
│   │               │   │           CCPUDoEnableComponentEventHandlerTranslator.o.d
│   │               │   │           CCPUDoExpireEventHandler.o
│   │               │   │           CCPUDoExpireEventHandler.o.d
│   │               │   │           CCPUDoExpireEventHandlerTranslator.o
│   │               │   │           CCPUDoExpireEventHandlerTranslator.o.d
│   │               │   │           CCPUDoFreezeEventHandler.o
│   │               │   │           CCPUDoFreezeEventHandler.o.d
│   │               │   │           CCPUDoFreezeEventHandlerTranslator.o
│   │               │   │           CCPUDoFreezeEventHandlerTranslator.o.d
│   │               │   │           CCPUDoPlacementParticleEventHandler.o
│   │               │   │           CCPUDoPlacementParticleEventHandler.o.d
│   │               │   │           CCPUDoPlacementParticleEventHandlerTranslator.o
│   │               │   │           CCPUDoPlacementParticleEventHandlerTranslator.o.d
│   │               │   │           CCPUDoScaleEventHandler.o
│   │               │   │           CCPUDoScaleEventHandler.o.d
│   │               │   │           CCPUDoScaleEventHandlerTranslator.o
│   │               │   │           CCPUDoScaleEventHandlerTranslator.o.d
│   │               │   │           CCPUDoStopSystemEventHandler.o
│   │               │   │           CCPUDoStopSystemEventHandler.o.d
│   │               │   │           CCPUDoStopSystemEventHandlerTranslator.o
│   │               │   │           CCPUDoStopSystemEventHandlerTranslator.o.d
│   │               │   │           CCPUDynamicAttribute.o
│   │               │   │           CCPUDynamicAttribute.o.d
│   │               │   │           CCPUDynamicAttributeTranslator.o
│   │               │   │           CCPUDynamicAttributeTranslator.o.d
│   │               │   │           CCPUEmitter.o
│   │               │   │           CCPUEmitter.o.d
│   │               │   │           CCPUEmitterManager.o
│   │               │   │           CCPUEmitterManager.o.d
│   │               │   │           CCPUEmitterTranslator.o
│   │               │   │           CCPUEmitterTranslator.o.d
│   │               │   │           CCPUEventHandler.o
│   │               │   │           CCPUEventHandler.o.d
│   │               │   │           CCPUEventHandlerManager.o
│   │               │   │           CCPUEventHandlerManager.o.d
│   │               │   │           CCPUEventHandlerTranslator.o
│   │               │   │           CCPUEventHandlerTranslator.o.d
│   │               │   │           CCPUFlockCenteringAffector.o
│   │               │   │           CCPUFlockCenteringAffector.o.d
│   │               │   │           CCPUFlockCenteringAffectorTranslator.o
│   │               │   │           CCPUFlockCenteringAffectorTranslator.o.d
│   │               │   │           CCPUForceField.o
│   │               │   │           CCPUForceField.o.d
│   │               │   │           CCPUForceFieldAffector.o
│   │               │   │           CCPUForceFieldAffector.o.d
│   │               │   │           CCPUForceFieldAffectorTranslator.o
│   │               │   │           CCPUForceFieldAffectorTranslator.o.d
│   │               │   │           CCPUGeometryRotator.o
│   │               │   │           CCPUGeometryRotator.o.d
│   │               │   │           CCPUGeometryRotatorTranslator.o
│   │               │   │           CCPUGeometryRotatorTranslator.o.d
│   │               │   │           CCPUGravityAffector.o
│   │               │   │           CCPUGravityAffector.o.d
│   │               │   │           CCPUGravityAffectorTranslator.o
│   │               │   │           CCPUGravityAffectorTranslator.o.d
│   │               │   │           CCPUInterParticleCollider.o
│   │               │   │           CCPUInterParticleCollider.o.d
│   │               │   │           CCPUInterParticleColliderTranslator.o
│   │               │   │           CCPUInterParticleColliderTranslator.o.d
│   │               │   │           CCPUJetAffector.o
│   │               │   │           CCPUJetAffector.o.d
│   │               │   │           CCPUJetAffectorTranslator.o
│   │               │   │           CCPUJetAffectorTranslator.o.d
│   │               │   │           CCPULineAffector.o
│   │               │   │           CCPULineAffector.o.d
│   │               │   │           CCPULineAffectorTranslator.o
│   │               │   │           CCPULineAffectorTranslator.o.d
│   │               │   │           CCPULinearForceAffector.o
│   │               │   │           CCPULinearForceAffector.o.d
│   │               │   │           CCPULinearForceAffectorTranslator.o
│   │               │   │           CCPULinearForceAffectorTranslator.o.d
│   │               │   │           CCPULineEmitter.o
│   │               │   │           CCPULineEmitter.o.d
│   │               │   │           CCPULineEmitterTranslator.o
│   │               │   │           CCPULineEmitterTranslator.o.d
│   │               │   │           CCPUListener.o
│   │               │   │           CCPUListener.o.d
│   │               │   │           CCPUMaterialManager.o
│   │               │   │           CCPUMaterialManager.o.d
│   │               │   │           CCPUMaterialTranslator.o
│   │               │   │           CCPUMaterialTranslator.o.d
│   │               │   │           CCPUMeshSurfaceEmitter.o
│   │               │   │           CCPUMeshSurfaceEmitter.o.d
│   │               │   │           CCPUMeshSurfaceEmitterTranslator.o
│   │               │   │           CCPUMeshSurfaceEmitterTranslator.o.d
│   │               │   │           CCPUNoise.o
│   │               │   │           CCPUNoise.o.d
│   │               │   │           CCPUObserver.o
│   │               │   │           CCPUObserver.o.d
│   │               │   │           CCPUObserverManager.o
│   │               │   │           CCPUObserverManager.o.d
│   │               │   │           CCPUObserverTranslator.o
│   │               │   │           CCPUObserverTranslator.o.d
│   │               │   │           CCPUOnClearObserver.o
│   │               │   │           CCPUOnClearObserver.o.d
│   │               │   │           CCPUOnClearObserverTranslator.o
│   │               │   │           CCPUOnClearObserverTranslator.o.d
│   │               │   │           CCPUOnCollisionObserver.o
│   │               │   │           CCPUOnCollisionObserver.o.d
│   │               │   │           CCPUOnCollisionObserverTranslator.o
│   │               │   │           CCPUOnCollisionObserverTranslator.o.d
│   │               │   │           CCPUOnCountObserver.o
│   │               │   │           CCPUOnCountObserver.o.d
│   │               │   │           CCPUOnCountObserverTranslator.o
│   │               │   │           CCPUOnCountObserverTranslator.o.d
│   │               │   │           CCPUOnEmissionObserver.o
│   │               │   │           CCPUOnEmissionObserver.o.d
│   │               │   │           CCPUOnEmissionObserverTranslator.o
│   │               │   │           CCPUOnEmissionObserverTranslator.o.d
│   │               │   │           CCPUOnEventFlagObserver.o
│   │               │   │           CCPUOnEventFlagObserver.o.d
│   │               │   │           CCPUOnEventFlagObserverTranslator.o
│   │               │   │           CCPUOnEventFlagObserverTranslator.o.d
│   │               │   │           CCPUOnExpireObserver.o
│   │               │   │           CCPUOnExpireObserver.o.d
│   │               │   │           CCPUOnExpireObserverTranslator.o
│   │               │   │           CCPUOnExpireObserverTranslator.o.d
│   │               │   │           CCPUOnPositionObserver.o
│   │               │   │           CCPUOnPositionObserver.o.d
│   │               │   │           CCPUOnPositionObserverTranslator.o
│   │               │   │           CCPUOnPositionObserverTranslator.o.d
│   │               │   │           CCPUOnQuotaObserver.o
│   │               │   │           CCPUOnQuotaObserver.o.d
│   │               │   │           CCPUOnQuotaObserverTranslator.o
│   │               │   │           CCPUOnQuotaObserverTranslator.o.d
│   │               │   │           CCPUOnRandomObserver.o
│   │               │   │           CCPUOnRandomObserver.o.d
│   │               │   │           CCPUOnRandomObserverTranslator.o
│   │               │   │           CCPUOnRandomObserverTranslator.o.d
│   │               │   │           CCPUOnTimeObserver.o
│   │               │   │           CCPUOnTimeObserver.o.d
│   │               │   │           CCPUOnTimeObserverTranslator.o
│   │               │   │           CCPUOnTimeObserverTranslator.o.d
│   │               │   │           CCPUOnVelocityObserver.o
│   │               │   │           CCPUOnVelocityObserver.o.d
│   │               │   │           CCPUOnVelocityObserverTranslator.o
│   │               │   │           CCPUOnVelocityObserverTranslator.o.d
│   │               │   │           CCPUParticleFollower.o
│   │               │   │           CCPUParticleFollower.o.d
│   │               │   │           CCPUParticleFollowerTranslator.o
│   │               │   │           CCPUParticleFollowerTranslator.o.d
│   │               │   │           CCPUParticleSystem3D.o
│   │               │   │           CCPUParticleSystem3D.o.d
│   │               │   │           CCPUParticleSystem3DTranslator.o
│   │               │   │           CCPUParticleSystem3DTranslator.o.d
│   │               │   │           CCPUPathFollower.o
│   │               │   │           CCPUPathFollower.o.d
│   │               │   │           CCPUPathFollowerTranslator.o
│   │               │   │           CCPUPathFollowerTranslator.o.d
│   │               │   │           CCPUPlane.o
│   │               │   │           CCPUPlane.o.d
│   │               │   │           CCPUPlaneCollider.o
│   │               │   │           CCPUPlaneCollider.o.d
│   │               │   │           CCPUPlaneColliderTranslator.o
│   │               │   │           CCPUPlaneColliderTranslator.o.d
│   │               │   │           CCPUPointEmitter.o
│   │               │   │           CCPUPointEmitter.o.d
│   │               │   │           CCPUPointEmitterTranslator.o
│   │               │   │           CCPUPointEmitterTranslator.o.d
│   │               │   │           CCPUPositionEmitter.o
│   │               │   │           CCPUPositionEmitter.o.d
│   │               │   │           CCPUPositionEmitterTranslator.o
│   │               │   │           CCPUPositionEmitterTranslator.o.d
│   │               │   │           CCPURandomiser.o
│   │               │   │           CCPURandomiser.o.d
│   │               │   │           CCPURandomiserTranslator.o
│   │               │   │           CCPURandomiserTranslator.o.d
│   │               │   │           CCPURender.o
│   │               │   │           CCPURender.o.d
│   │               │   │           CCPURendererTranslator.o
│   │               │   │           CCPURendererTranslator.o.d
│   │               │   │           CCPURibbonTrail.o
│   │               │   │           CCPURibbonTrail.o.d
│   │               │   │           CCPURibbonTrailRender.o
│   │               │   │           CCPURibbonTrailRender.o.d
│   │               │   │           CCPUScaleAffector.o
│   │               │   │           CCPUScaleAffector.o.d
│   │               │   │           CCPUScaleAffectorTranslator.o
│   │               │   │           CCPUScaleAffectorTranslator.o.d
│   │               │   │           CCPUScaleVelocityAffector.o
│   │               │   │           CCPUScaleVelocityAffector.o.d
│   │               │   │           CCPUScaleVelocityAffectorTranslator.o
│   │               │   │           CCPUScaleVelocityAffectorTranslator.o.d
│   │               │   │           CCPUScriptCompiler.o
│   │               │   │           CCPUScriptCompiler.o.d
│   │               │   │           CCPUScriptLexer.o
│   │               │   │           CCPUScriptLexer.o.d
│   │               │   │           CCPUScriptParser.o
│   │               │   │           CCPUScriptParser.o.d
│   │               │   │           CCPUScriptTranslator.o
│   │               │   │           CCPUScriptTranslator.o.d
│   │               │   │           CCPUSimpleSpline.o
│   │               │   │           CCPUSimpleSpline.o.d
│   │               │   │           CCPUSineForceAffector.o
│   │               │   │           CCPUSineForceAffector.o.d
│   │               │   │           CCPUSineForceAffectorTranslator.o
│   │               │   │           CCPUSineForceAffectorTranslator.o.d
│   │               │   │           CCPUSlaveBehaviour.o
│   │               │   │           CCPUSlaveBehaviour.o.d
│   │               │   │           CCPUSlaveBehaviourTranslator.o
│   │               │   │           CCPUSlaveBehaviourTranslator.o.d
│   │               │   │           CCPUSlaveEmitter.o
│   │               │   │           CCPUSlaveEmitter.o.d
│   │               │   │           CCPUSlaveEmitterTranslator.o
│   │               │   │           CCPUSlaveEmitterTranslator.o.d
│   │               │   │           CCPUSphere.o
│   │               │   │           CCPUSphere.o.d
│   │               │   │           CCPUSphereCollider.o
│   │               │   │           CCPUSphereCollider.o.d
│   │               │   │           CCPUSphereColliderTranslator.o
│   │               │   │           CCPUSphereColliderTranslator.o.d
│   │               │   │           CCPUSphereSurfaceEmitter.o
│   │               │   │           CCPUSphereSurfaceEmitter.o.d
│   │               │   │           CCPUSphereSurfaceEmitterTranslator.o
│   │               │   │           CCPUSphereSurfaceEmitterTranslator.o.d
│   │               │   │           CCPUTechniqueTranslator.o
│   │               │   │           CCPUTechniqueTranslator.o.d
│   │               │   │           CCPUTextureAnimator.o
│   │               │   │           CCPUTextureAnimator.o.d
│   │               │   │           CCPUTextureAnimatorTranslator.o
│   │               │   │           CCPUTextureAnimatorTranslator.o.d
│   │               │   │           CCPUTextureRotator.o
│   │               │   │           CCPUTextureRotator.o.d
│   │               │   │           CCPUTextureRotatorTranslator.o
│   │               │   │           CCPUTextureRotatorTranslator.o.d
│   │               │   │           CCPUTranslateManager.o
│   │               │   │           CCPUTranslateManager.o.d
│   │               │   │           CCPUUtil.o
│   │               │   │           CCPUUtil.o.d
│   │               │   │           CCPUVelocityMatchingAffector.o
│   │               │   │           CCPUVelocityMatchingAffector.o.d
│   │               │   │           CCPUVelocityMatchingAffectorTranslator.o
│   │               │   │           CCPUVelocityMatchingAffectorTranslator.o.d
│   │               │   │           CCPUVertexEmitter.o
│   │               │   │           CCPUVertexEmitter.o.d
│   │               │   │           CCPUVortexAffector.o
│   │               │   │           CCPUVortexAffector.o.d
│   │               │   │           CCPUVortexAffectorTranslator.o
│   │               │   │           CCPUVortexAffectorTranslator.o.d
│   │               │   │
│   │               │   └───physics-nodes
│   │               │           CCPhysicsDebugNode.o
│   │               │           CCPhysicsDebugNode.o.d
│   │               │           CCPhysicsSprite.o
│   │               │           CCPhysicsSprite.o.d
│   │               │
│   │               ├───cocos_flatbuffers_static
│   │               │       flatc.o
│   │               │       flatc.o.d
│   │               │       idl_gen_cpp.o
│   │               │       idl_gen_cpp.o.d
│   │               │       idl_gen_fbs.o
│   │               │       idl_gen_fbs.o.d
│   │               │       idl_gen_general.o
│   │               │       idl_gen_general.o.d
│   │               │       idl_gen_go.o
│   │               │       idl_gen_go.o.d
│   │               │       idl_gen_text.o
│   │               │       idl_gen_text.o.d
│   │               │       idl_parser.o
│   │               │       idl_parser.o.d
│   │               │
│   │               ├───cocos_network_static
│   │               │       CCDownloader-android.o
│   │               │       CCDownloader-android.o.d
│   │               │       CCDownloader.o
│   │               │       CCDownloader.o.d
│   │               │       HttpClient-android.o
│   │               │       HttpClient-android.o.d
│   │               │       SocketIO.o
│   │               │       SocketIO.o.d
│   │               │       WebSocket.o
│   │               │       WebSocket.o.d
│   │               │
│   │               ├───cocos_ui_static
│   │               │   │   CocosGUI.o
│   │               │   │   CocosGUI.o.d
│   │               │   │   UIAbstractCheckButton.o
│   │               │   │   UIAbstractCheckButton.o.d
│   │               │   │   UIButton.o
│   │               │   │   UIButton.o.d
│   │               │   │   UICheckBox.o
│   │               │   │   UICheckBox.o.d
│   │               │   │   UIDeprecated.o
│   │               │   │   UIDeprecated.o.d
│   │               │   │   UIHBox.o
│   │               │   │   UIHBox.o.d
│   │               │   │   UIHelper.o
│   │               │   │   UIHelper.o.d
│   │               │   │   UIImageView.o
│   │               │   │   UIImageView.o.d
│   │               │   │   UILayout.o
│   │               │   │   UILayout.o.d
│   │               │   │   UILayoutComponent.o
│   │               │   │   UILayoutComponent.o.d
│   │               │   │   UILayoutManager.o
│   │               │   │   UILayoutManager.o.d
│   │               │   │   UILayoutParameter.o
│   │               │   │   UILayoutParameter.o.d
│   │               │   │   UIListView.o
│   │               │   │   UIListView.o.d
│   │               │   │   UILoadingBar.o
│   │               │   │   UILoadingBar.o.d
│   │               │   │   UIPageView.o
│   │               │   │   UIPageView.o.d
│   │               │   │   UIPageViewIndicator.o
│   │               │   │   UIPageViewIndicator.o.d
│   │               │   │   UIRadioButton.o
│   │               │   │   UIRadioButton.o.d
│   │               │   │   UIRelativeBox.o
│   │               │   │   UIRelativeBox.o.d
│   │               │   │   UIRichText.o
│   │               │   │   UIRichText.o.d
│   │               │   │   UIScale9Sprite.o
│   │               │   │   UIScale9Sprite.o.d
│   │               │   │   UIScrollView.o
│   │               │   │   UIScrollView.o.d
│   │               │   │   UIScrollViewBar.o
│   │               │   │   UIScrollViewBar.o.d
│   │               │   │   UISlider.o
│   │               │   │   UISlider.o.d
│   │               │   │   UITabControl.o
│   │               │   │   UITabControl.o.d
│   │               │   │   UIText.o
│   │               │   │   UIText.o.d
│   │               │   │   UITextAtlas.o
│   │               │   │   UITextAtlas.o.d
│   │               │   │   UITextBMFont.o
│   │               │   │   UITextBMFont.o.d
│   │               │   │   UITextField.o
│   │               │   │   UITextField.o.d
│   │               │   │   UIVBox.o
│   │               │   │   UIVBox.o.d
│   │               │   │   UIVideoPlayer-android.o
│   │               │   │   UIVideoPlayer-android.o.d
│   │               │   │   UIWebView.o
│   │               │   │   UIWebView.o.d
│   │               │   │   UIWebViewImpl-android.o
│   │               │   │   UIWebViewImpl-android.o.d
│   │               │   │   UIWidget.o
│   │               │   │   UIWidget.o.d
│   │               │   │
│   │               │   └───UIEditBox
│   │               │           UIEditBox.o
│   │               │           UIEditBox.o.d
│   │               │           UIEditBoxImpl-android.o
│   │               │           UIEditBoxImpl-android.o.d
│   │               │           UIEditBoxImpl-common.o
│   │               │           UIEditBoxImpl-common.o.d
│   │               │
│   │               ├───cpufeatures
│   │               │       cpu-features.o
│   │               │       cpu-features.o.d
│   │               │
│   │               ├───MyGame_shared
│   │               │   ├───hellocpp
│   │               │   │       main.o
│   │               │   │       main.o.d
│   │               │   │
│   │               │   └───__
│   │               │       └───__
│   │               │           └───Classes
│   │               │                   AppDelegate.o
│   │               │                   AppDelegate.o.d
│   │               │                   HelloWorldScene.o
│   │               │                   HelloWorldScene.o.d
│   │               │
│   │               ├───recast_static
│   │               │   ├───DebugUtils
│   │               │   │       DebugDraw.o
│   │               │   │       DebugDraw.o.d
│   │               │   │       DetourDebugDraw.o
│   │               │   │       DetourDebugDraw.o.d
│   │               │   │
│   │               │   ├───Detour
│   │               │   │       DetourAlloc.o
│   │               │   │       DetourAlloc.o.d
│   │               │   │       DetourCommon.o
│   │               │   │       DetourCommon.o.d
│   │               │   │       DetourNavMesh.o
│   │               │   │       DetourNavMesh.o.d
│   │               │   │       DetourNavMeshBuilder.o
│   │               │   │       DetourNavMeshBuilder.o.d
│   │               │   │       DetourNavMeshQuery.o
│   │               │   │       DetourNavMeshQuery.o.d
│   │               │   │       DetourNode.o
│   │               │   │       DetourNode.o.d
│   │               │   │
│   │               │   ├───DetourCrowd
│   │               │   │       DetourCrowd.o
│   │               │   │       DetourCrowd.o.d
│   │               │   │       DetourLocalBoundary.o
│   │               │   │       DetourLocalBoundary.o.d
│   │               │   │       DetourObstacleAvoidance.o
│   │               │   │       DetourObstacleAvoidance.o.d
│   │               │   │       DetourPathCorridor.o
│   │               │   │       DetourPathCorridor.o.d
│   │               │   │       DetourPathQueue.o
│   │               │   │       DetourPathQueue.o.d
│   │               │   │       DetourProximityGrid.o
│   │               │   │       DetourProximityGrid.o.d
│   │               │   │
│   │               │   ├───DetourTileCache
│   │               │   │       DetourTileCache.o
│   │               │   │       DetourTileCache.o.d
│   │               │   │       DetourTileCacheBuilder.o
│   │               │   │       DetourTileCacheBuilder.o.d
│   │               │   │
│   │               │   └───fastlz
│   │               │           fastlz.o
│   │               │           fastlz.o.d
│   │               │
│   │               └───spine_static
│   │                       Animation.o
│   │                       Animation.o.d
│   │                       AnimationState.o
│   │                       AnimationState.o.d
│   │                       AnimationStateData.o
│   │                       AnimationStateData.o.d
│   │                       Atlas.o
│   │                       Atlas.o.d
│   │                       AtlasAttachmentLoader.o
│   │                       AtlasAttachmentLoader.o.d
│   │                       Attachment.o
│   │                       Attachment.o.d
│   │                       AttachmentLoader.o
│   │                       AttachmentLoader.o.d
│   │                       AttachmentVertices.o
│   │                       AttachmentVertices.o.d
│   │                       Bone.o
│   │                       Bone.o.d
│   │                       BoneData.o
│   │                       BoneData.o.d
│   │                       BoundingBoxAttachment.o
│   │                       BoundingBoxAttachment.o.d
│   │                       Cocos2dAttachmentLoader.o
│   │                       Cocos2dAttachmentLoader.o.d
│   │                       Event.o
│   │                       Event.o.d
│   │                       EventData.o
│   │                       EventData.o.d
│   │                       extension.o
│   │                       extension.o.d
│   │                       IkConstraint.o
│   │                       IkConstraint.o.d
│   │                       IkConstraintData.o
│   │                       IkConstraintData.o.d
│   │                       Json.o
│   │                       Json.o.d
│   │                       MeshAttachment.o
│   │                       MeshAttachment.o.d
│   │                       PathAttachment.o
│   │                       PathAttachment.o.d
│   │                       PathConstraint.o
│   │                       PathConstraint.o.d
│   │                       PathConstraintData.o
│   │                       PathConstraintData.o.d
│   │                       RegionAttachment.o
│   │                       RegionAttachment.o.d
│   │                       Skeleton.o
│   │                       Skeleton.o.d
│   │                       SkeletonAnimation.o
│   │                       SkeletonAnimation.o.d
│   │                       SkeletonBatch.o
│   │                       SkeletonBatch.o.d
│   │                       SkeletonBounds.o
│   │                       SkeletonBounds.o.d
│   │                       SkeletonData.o
│   │                       SkeletonData.o.d
│   │                       SkeletonJson.o
│   │                       SkeletonJson.o.d
│   │                       SkeletonRenderer.o
│   │                       SkeletonRenderer.o.d
│   │                       Skin.o
│   │                       Skin.o.d
│   │                       Slot.o
│   │                       Slot.o.d
│   │                       SlotData.o
│   │                       SlotData.o.d
│   │                       spine-cocos2dx.o
│   │                       spine-cocos2dx.o.d
│   │                       TransformConstraint.o
│   │                       TransformConstraint.o.d
│   │                       TransformConstraintData.o
│   │                       TransformConstraintData.o.d
│   │                       VertexAttachment.o
│   │                       VertexAttachment.o.d
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
        PROJECT-CONTENTS-ON-CREATION.md
        Screenshot-on-Android.png
```
