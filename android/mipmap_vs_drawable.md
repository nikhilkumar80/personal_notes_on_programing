# What is the difference b/w mipmap & drawable?
Mipmap folders are used for placing app/launcher icons only. Because launcher icons are used at different resolutions from thhe devices current density.
The reason they use different density  is that some launcher actually display the icons larger than they were intended.

When a resource from drawable is requested, it is chhoosen from the folder that matches the device density. The launcher may choose an icon from a different folder.
For example, Nexus-5 uses drawable from XXHDPI,  Nexus-5  launcher uses icon from XXXHDPI.

## Why can't this be achieved using drawables?
Some developeres build separate APK's for every density to keep thhe apk size down. When building separate APK's for different density, drawable folders for other densities get stripped.
