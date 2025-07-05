---
layout: page
status: publish
published: true
title: Creating Plug-ins
author:
  display_name: Steve Palmer
  login: Steve Palmer
  email: stevewpalmer@gmail.com
  url: ''
author_login: Steve Palmer
author_email: stevewpalmer@gmail.com
wordpress_id: 120
wordpress_url: http://www.vienna-rss.com/?page_id=120
date: '2010-01-16 15:09:09 +1100'
date_gmt: '2010-01-16 15:09:09 +1100'
categories:
- Uncategorized
tags: []
comments:
- id: 13
  author: A Vienna 2.5 Sneak Peek | Vienna RSS
  author_email: ''
  author_url: http://www.vienna-rss.com/?p=201
  date: '2010-01-18 12:02:05 +1100'
  date_gmt: '2010-01-18 12:02:05 +1100'
  content: "[...] Creating Plugins (v2.5) [...]"
- id: 65
  author: Vienna 2.5 BETA | Vienna RSS
  author_email: ''
  author_url: http://www.vienna-rss.com/?p=237
  date: '2010-02-08 13:07:15 +1100'
  date_gmt: '2010-02-08 13:07:15 +1100'
  content: "[...] Creating Plugins (v2.5) [...]"
- id: 411
  author: Vienna 2.5 – The Social Sharing Edition | Vienna RSS
  author_email: ''
  author_url: http://www.vienna-rss.com/?p=285
  date: '2010-03-19 09:18:42 +1100'
  date_gmt: '2010-03-19 09:18:42 +1100'
  content: "[...] Creating Plugins (v2.5) [...]"
redirect_from:
  - /development/creating-plugins-for-vienna-2-5/
---
Starting with v2.5 and later, Vienna supports plugins which are installed on the toolbar and can run defined actions. These plugins are XML-based and can be created by editing a simple [.plist-file](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/PropertyLists/UnderstandXMLPlist/UnderstandXMLPlist.html) without any knowledge of Cocoa programming, in as little as 15 minutes.  This section describes how to create your own plugins, which will look and work exactly like the built-in ones:

![Vienna 2.5 supports user-creatable plugins]({{ '/images/plugins.png' | prepend: site.baseurl }} "Vienna 2.5 supports user-creatable plugins")
{: style="text-align: center;"}

## Creating the Plug-in Bundle

Vienna plugins are distributed in the form of folders with the extension "**.viennaplugin**", which OS X automatically treats as bundles. Simply create a new folder, named like your new plugin. Then edit its name and append ".viennaplugin". This registers the folder as a Vienna plugin folder so that it can be double-clicked or dragged-and-dropped on the Vienna application icon to automatically install it. After this step, you can view the folder's contents via control/right-clicking and choosing "Show Package Contents" from the menu.

## Adding the Necessary Files

There are three types of plugins supported as of the time of writing:

- **Link plugins** are simple sharing plugins that work with any web service that has a special URL for posting information. For example, if you wanted to share *"xyz.com"* (which has the page title "*XYZ*") [Facebook's](http://www.facebook.com) "sharer.php" would be called like this:

      http://www.facebook.com/sharer.php?u=http://www.xyz.com&amp;t=XYZ

  In a Vienna link plugin, you would use special placeholders to represent this information:

      http://www.facebook.com/sharer.php?u=$ArticleLink$&amp;t=$ArticleTitle$

- **Script plugins** can run [AppleScripts](https://developer.apple.com/library/archive/documentation/AppleScript/Conceptual/AppleScriptX/AppleScriptX.html), acting on the information that Vienna and other applications exposes to the user via their script suites.
- **Blog Editor plugins** are simple plugins that tell Vienna about any application that can use information about blog posts or websites that it sends to it via its export feature. These include [MarsEdit](http://www.red-sweater.com/marsedit/), [Ecto](http://illuminex.com/ecto/), [Pukka](http://codesorcery.net/pukka), [Cocoalicious](http://www.scifihifi.com/cocoalicious/) and many others. Quite a few of these are included in the standard distribution. To create your own plugin, you set *Type* to *BlogEditor* and *BundleIdentifier* to the application's [bundle identifier](https://developer.apple.com/library/archive/documentation/CoreFoundation/Conceptual/CFBundles/BundleTypes/BundleTypes.html), which you can find in the *Info.plist* file inside the application bundle.

Each type requires:

- An **Info.plist** file which defines the plugin's attributes.
- An **icon file**, preferably a 16×16 TIFF without layers but with an alpha channel.

Script plugins aditionally require:

- **The [AppleScript](https://developer.apple.com/library/archive/documentation/AppleScript/Conceptual/AppleScriptX/AppleScriptX.html) file** which, for example, gets information out of Vienna and sends it to an other application.

## Configuring your Plug-in

The actual configuration of the plugin happens in its "Info.plist". The following example completely describes Vienna's built-in Facebook plugin:

{% highlight xml %}
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
	<key>Name</key>
	<string>ShareWithFacebook</string>
	<key>Type</key>
	<string>Link</string>
	<key>URL</key>
	<string>http://www.facebook.com/sharer.php?u=$ArticleLink$&amp;t=$ArticleTitle$</string>
	<key>Default</key>
	<false/>
	<key>FriendlyName</key>
	<string>Facebook</string>
	<key>Tooltip</key>
	<string>Share the current article on Facebook</string>
	<key>ButtonImage</key>
	<string>facebookButton</string>
	<key>MenuPath</key>
	<string>Share With Facebook</string>
	<key>ShortenURLs</key>
	<false/>
</dict>
</plist>
{% endhighlight %}

For more information on understanding and editing .plists, please go read [this document](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/PropertyLists/UnderstandXMLPlist/UnderstandXMLPlist.html) at the Apple Developer Connection website.

## Configuration Entries

- **Name**: (mandatory) this is a short, internal, name that uniquely identifies the plugin. It is now displayed in the UI.
- **Type**: (mandatory) this specifies the plugin type. Three values are accepted: **Link**,  **Script** and **BlogEditor**.
- **BundleIdentifier**: Only used for BlogEditor plugins, this defines the identifier of the application that you want to be called.
- **URL**: (mandatory for link-type plugins) this is the URL that is browed when the plugin button is clicked. Vienna substitutes the $...$ placeholders with actual values from the current article being viewed. See [here]({{ '/development/creating-styles' | prepend: site.baseurl }}) for a list of placeholders.
- **Script**: (mandatory for script-type plugins) this is the name of the script file in the same folder as the Info.plist.
- **Default**: if this is set to true then this plugin appears on the default toolbar.
- **FriendlyName**: this is the short name of the plugin that appears as the plugin button text on the toolbar. It should be kept as short as possible. If omitted, the internal name is used instead.
- **Tooltip**: this is the text of the tooltip that appears when you hover over the plugin button on the toolbar. If omitted, the friendly name is displayed instead.
- **ButtonImage**: (mandatory) this is the name of a 16x16 TIFF image in the same folder as the Info.plist that will be used as the toolbar button image. For small buttons, Vienna takes this and reduces it to 12x12 automatically. However if you specify a TIFF image with the "small" prefix to the button image name then Vienna will use that for small buttons.
- **MenuPath**: specifies an optional name for the plugin at the end of the Article menu.
- **MenuKey**: specifies an optional key association for the plugin in the menu. This should be one or more of: Cmd, Ctrl, Alt and Shift, separated by a '+' character and finally a single letter or number character.
