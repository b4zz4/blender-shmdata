# Spout addon V1.3 for Blender 3.1.0

Spout for Blender allows to stream [spout](http://spout.zeal.co/) streams from blender.

This works only for Windows 10 64 bit.

## Installation

Please make sure you have the most current Blender 3.0.x installed.

1. [download](https://github.com/maybites/blender.script.spout/releases) the addon from the releases, unzip it and drop the 'spout' folder inside the addons-folder

The default addons folder is located here:

- blender_3.0.x
  └ blender.exe
  └ 3.x
    └ scripts
      └ addons
      └ modules  

2. [download](https://pypi.org/project/SpoutGL/#files) the Python SpoutGL-library (whl - file). Make sure you select the correct python version for your blender version -> [release notes](https://wiki.blender.org/wiki/Reference/Release_Notes) -> Python API.

3. Use 7-zip to unzip the library and drag the folder named 'SpoutGL' to the modules-folder inside your script folder.

inside blender:

4. restart blender.

5. Menu > Edit > Preferences > Add-addons

6. search for spout

8. Enable it, save preferences and close preferences.

## Usage

Currently it is only possible to send Spout streams, but not to receive them.

For streaming you need a Camera object.

The plugin adds a Panel to the Camera properties called 'Streaming Texture'. The following properties are available:

* The streaming name is fixed to the camera name.
* capture/streaming resolution.
* show preview
* use eevee color management (recomended)
* chose a workspace with the desired render / shading preferences
* chose a scene and layer setup to render 

IMPORTANT:
If you desire to choose a scene and layer setup other than default, and this scene and layer has not yet been rendered by blender since you opened the blender file - blender will crash when you start streaming. Not sure if this constitutes as bug, maybe just a limitation of blender..

You should be able to create as many Cameras with streams as you wish.

## Syphon

No, this addon is unable to stream [syphon](http://syphon.v002.info/) on OSX. It is possible to do the same thing with syphon, though my tests showed dismal performances...

## Credits

Blender Plugin by Martin Froehlich.

### Special Thanks:
Obviously Lyn Jarvis for developing Spout in the first place. And without [SpoutGL for Python](https://github.com/jlai/Python-SpoutGL) developed by Jason and the valuable [hint](https://docs.blender.org/api/master/gpu.html#rendering-the-3d-view-into-a-texture) from Jonas Dichelle I would still dab in darkness...
