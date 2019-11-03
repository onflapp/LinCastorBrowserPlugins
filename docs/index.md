# Create new plugin

You can either use **Plugin Registration** dialog to create new plugin from a template. The dialog will create a temporary, read-only file that will have to be save or copied into the **Scripts folder**. This is quite important, otherwise MacOS may refuse to run the script.

Downloading and modifying one of the [sample plugins](https://github.com/onflapp/LinCastorBrowserPlugins) is good way to start start as well.

# Sample Plugin

The AppleScript plugin requires method called **handle_url** that will take a single argument. The argument is going to contain all URL variables as a record. Returning 1 indicates the handler has finished successfully. If method doesn’t return any value or returns 0, LinCastor Browser will execute to next plugin in line.

```
on handle_url(args)
  display dialog "handle url: " & |URL| of args
  return 1
end handle_url
```

The **args** record will contain different set of variable depending on whether this plugin is called to open URL or lookup a text.

### handling URL

```
URL           => my-http://myhost.domain.com:8080/mysite/a.html?search=blah#myanchor
URL_SCHEME    => my-http
URL_HOST      => myhost.domain.com
URL_PORT      => 8080
URL_PATH      => /mysite/a.html
URL_PATH_EXT  => html
URL_PATH_NAME => a.html
URL_QUERY     => ?search=blah
URL_FRAGMENT  => #myanchor
URL_VALUE     => everything that comes after the 'scheme:'
URL_B64VALUE  => the same as URL_VALUE but decoded using based64
```

URL query parameters (everything that comes after ?) is going to be expanded into variables. For example:

```
URL_QUERY_SEARCH => blah
URL_QUERY_FLAG   => 2
```

Note the upper case of parameter’s name

## handling selected text 

```
TEXT => the selected text used for a lookup
ENCODED_TEXT => the selected text encoded using url encoding
```

# Where do I find the Scripts folder?

The scripts folder is under your home folder **Library/Application Scripts/com.onflapp.LinCastor-Browser**

Use LinCastor's Help menu or the **Plugin Registration** dialog to go to it.

If you want to use Finder directly:

- select menu “Go”, then “Go to Folder”
- type in '~/Library/Application Scripts/com.onflapp.LinCastor-Browser'
- If this folder doesn’t exist already, create it.
