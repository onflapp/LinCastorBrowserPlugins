# LinCastorBrowserPlugins

Useful plugins and samples for LinCastor Browser app.

There are two types of plugins; one that handles URLs (including custom schemes) and the other that uses currently selected text.
The URL handler plugins are usually used to open browsers or apps, whereas the text selection plugins do text lookups.

This repository includes plugins you can use "out of the box" or as a starting point for creating your own plugins.

The plugins must be placed into app's "Application Scripts" folder **~/Library/Application\ Scripts/com.onflapp.LinCastor-Browser**.

## Install plugins using GIT
```
git clone https://github.com/onflapp/LinCastorBrowserPlugins.git
cp -r ./LinCastorBrowserPlugins/* ~/Library/Application\ Scripts/com.onflapp.LinCastor-Browser
```

## Download and install zipped plugins

1. [download zip archive](https://github.com/onflapp/LinCastorBrowserPlugins/archive/master.zip) and unzip it into a directory
2. open scripts folder (Go to LinCastor Browser's **Help / Scripts Folder** menu)
3. copy __contents__ of the zip archive to the scripts folder

## Create new plugin

A LinCastor Browser plugin is rather simple AppleScript, shell script or Automator file. The plugins are intended to be changed and modified by users. For more information see https://onflapp.github.io/LinCastorBrowserPlugins/.

## Troubleshooting

Most of these plugins require _Accessibility_ permissions to function correctly. To enable these permissions do the following:

- open **Security and Privacy** preferences
- make sure LinCastor Browser is enabled in the **Accessibility** section
- **Automation** should be enabled for MacOS 10.15

If you still have experience problems, try to remove the app and add it again.
