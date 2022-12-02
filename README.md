# LinCastor Browser

[LinCastor Browser](https://onflapp.github.io/blog/pages/LinCastorBrowser.html?utm_source=git) is an app that lets you choose a browser you want to open a link with. It works by becoming your default browser. When you click on a link it opens up with a menu and let you choose what action you want to take. Action can be an application or plugin script.

# Download and install zipped plugins

1. [download zip archive](https://github.com/onflapp/LinCastorBrowserPlugins/archive/master.zip) and unzip it into a directory
2. open scripts folder (Go to LinCastor Browser's **Help / Scripts Folder** menu)
3. copy __contents__ of the zip archive to the scripts folder

## Install plugins directly from GIT

```
cd ~/Library/Application\ Scripts/com.onflapp.LinCastor-Browser
git clone https://github.com/onflapp/LinCastorBrowserPlugins.git .
```

## Create new plugin

There are two types of plugins; one that handles URLs (including custom schemes) and the other that uses currently selected text.
The URL handler plugins are usually used to open browsers or apps, whereas the text selection plugins do text lookups.

This repository includes plugins you can use "out of the box" or as a starting point for creating your own plugins.

The plugins must be placed into app's "Application Scripts" folder **~/Library/Application\ Scripts/com.onflapp.LinCastor-Browser**.

A LinCastor Browser plugin is rather simple AppleScript, shell script or Automator file. The plugins are intended to be changed and modified by users. Description how to [create new plugin](https://onflapp.github.io/LinCastorBrowserPlugins/).

## Troubleshooting

Most of these plugins require _Accessibility_ permissions to function correctly. To enable these permissions do the following:

- open **Security and Privacy** preferences
- make sure LinCastor Browser is enabled in the **Accessibility** section
- **Automation** should be enabled for MacOS 10.15

If you still have experience problems, try to remove the app and add it again.
