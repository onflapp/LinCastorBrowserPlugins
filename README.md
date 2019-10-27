# LinCastorBrowserPlugins

Useful plugins and samples for LinCastor Browser app.

There are two types of plugins; one that handles URLs (including custom schemes) and the other that uses currently selected text.
The URL handler plugins are usually used to open browsers or apps, whereas the text selection plugins do text lookups.

This repository includes plugins you can use "out of the box" or as a starting point for creating your own plugins.

The plugins must be placed into app's "Application Scripts" folder.

## Install plugins using GIT
```
git clone https://github.com/onflapp/LinCastorBrowserPlugins.git
cp ./LinCastorBrowserPlugins/* ~/Application\ Scripts/com.onflapp.LinCastor-Browser
```

## Download and install zipped plugins

1. download zip archive and unzip it into a directory
2. open scripts folder
3. copy contents of the zip archive to the scripts folder

## Working with selected text:

### AppleDictionary.scpt

Open selected text in Apple Directory app

### AppleMaps.scpt

Open selected text in Apple Maps

### DocumentBrowser.scpt

Search selected text in Google and opens the result in a web panel
