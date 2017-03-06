---
layout: page
status: publish
published: true
title: Creating Plugins
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
  author: A Vienna 2.5 Sneak Peek&nbsp;|&nbsp;Vienna RSS
  author_email: ''
  author_url: http://www.vienna-rss.com/?p=201
  date: '2010-01-18 12:02:05 +1100'
  date_gmt: '2010-01-18 12:02:05 +1100'
  content: "[...] Creating Plugins (v2.5) [...]"
- id: 65
  author: Vienna 2.5 BETA&nbsp;|&nbsp;Vienna RSS
  author_email: ''
  author_url: http://www.vienna-rss.com/?p=237
  date: '2010-02-08 13:07:15 +1100'
  date_gmt: '2010-02-08 13:07:15 +1100'
  content: "[...] Creating Plugins (v2.5) [...]"
- id: 411
  author: Vienna 2.5 &#8211; The Social Sharing Edition&nbsp;|&nbsp;Vienna RSS
  author_email: ''
  author_url: http://www.vienna-rss.com/?p=285
  date: '2010-03-19 09:18:42 +1100'
  date_gmt: '2010-03-19 09:18:42 +1100'
  content: "[...] Creating Plugins (v2.5) [...]"
---
<p>Starting with v2.5 and later, Vienna supports plugins which are installed on the toolbar and can run defined actions. These plugins are XML-based and can be created by editing a simple <a href="http://developer.apple.com/mac/library/documentation/Cocoa/Conceptual/PropertyLists/UnderstandXMLPlist/UnderstandXMLPlist.html">.plist-file</a> without any knowledge of Cocoa programming, in as little as 15 minutes.  This section describes how to create your own plugins, which will look and work exactly like the built-in ones:<br />
<center><img alt="Vienna 2.5 supports user-creatable plugins" src="http://www.vienna-rss.com/img/plugins.png" title="Vienna 2.5 supports user-creatable plugins" width="327" height="77" /></center></p>
<p><br><br />
<h2>Creating the Plugin Bundle</h2><br />
Vienna plugins are distributed in the form of folders with the extension "<strong>.viennaplugin</strong>", which OS X automatically treats as bundles. Simply create a new folder, named like your new plugin. Then edit its name and append ".viennaplugin". This registers the folder as a Vienna plugin folder so that it can be double-clicked or dragged-and-dropped on the Vienna application icon to automatically install it. After this step, you can view the folder's contents via control/right-clicking and choosing "Show Package Contents" from the menu.</p>
<h2>Adding the Necessary Files</h2><br />
There are three types of plugins supported as of the time of writing: </p>
<ul>
<li>
<strong>Link plugins</strong> are simple sharing plugins that work with any web service that has a special URL for posting information. For example, if you wanted to share <em>"xyz.com"</em> (which has the page title "<em>XYZ</em>") <a href="http://www.facebook.com">Facebook's</a> "sharer.php" would be called like this:<br />
[html]http://www.facebook.com/sharer.php?u=http://www.xyz.com&amp;t=XYZ[/html]<br />
In a Vienna link plugin, you would use special placeholders to represent this information:<br />
[html]http://www.facebook.com/sharer.php?u=$ArticleLink$&amp;t=$ArticleTitle$[/html]<br />
</li></p>
<li><strong>Script plugins</strong> can run <a href="http://devworld.apple.com/applescript/">AppleScripts</a>, acting on the information that Vienna and other applications exposes to the user via their script suites.</li>
<li>
<strong>Blog Editor plugins</strong> are simple plugins that tell Vienna about any application that can use information about blog posts or websites that it sends to it via its export feature. These include <a href="http://www.red-sweater.com/marsedit/">MarsEdit</a>, <a href="http://illuminex.com/ecto/">Ecto</a>, <a href="http://codesorcery.net/pukka">Pukka</a>, <a href="http://www.scifihifi.com/cocoalicious/">Cocoalicious</a> and many others. Quite a few of these are included in the standard distribution. To create your own plugin, you set <em>Type</em> to <em>BlogEditor</em> and <em>BundleIdentifier</em> to the application's <a href="http://developer.apple.com/mac/library/documentation/CoreFoundation/Conceptual/CFBundles/BundleTypes/BundleTypes.html">bundle identifier</a>, which you can find in the<em> info.plist</em> file inside the application bundle.<br />
</li></p>
<p></ul><br />
Each type requires: </p>
<ul>
<li>An <strong>info.plist</strong> file which defines the plugin's attributes.</li>
<li>An <strong>icon file</strong>, preferably a 16×16 TIFF without layers but with an alpha channel.</li><br />
</ul></p>
<p>Script plugins aditionally require:</p>
<ul>
<li><strong>The <a href="http://devworld.apple.com/applescript/">AppleScript</a> file</strong> which, for example, gets information out of Vienna and sends it to an other application.</li></ul></p>
<h2>Configuring your Plugin</h2><br />
The actual configuration of the plugin happens in its "info.plist". The following example completely describes Vienna's built-in Facebook plugin:

<pre><code>
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


<p>For more information on understanding and editing .plists, please go read <a href="http://developer.apple.com/mac/library/documentation/Cocoa/Conceptual/PropertyLists/UnderstandXMLPlist/UnderstandXMLPlist.htm">this document</a> at the Apple Developer Connection website.</p>
<h2>Configuration Entries</h2></p>
<ul>
<li><strong>Name</strong>: (mandatory) this is a short, internal, name that uniquely identifies the plugin. It is now displayed in the UI.</li>
<li><strong>Type</strong>: (mandatory) this specifies the plugin type. Three values are accepted: <strong>Link</strong>,  <strong>Script</strong> and <strong>BlogEditor</strong>.</li>
<li><strong>BundleIdentifier</strong>: Only used for BlogEditor plugins, this defines the identifier of the application that you want to be called.</li>
<li><strong>URL</strong>: (mandatory for link-type plugins) this is the URL that is browed when the plugin button is clicked. Vienna substitutes the $...$ placeholders with actual values from the current article being viewed. See <a href="http://www.vienna-rss.com/?page_id=65">here</a> for a list of placeholders.</li>
<li><strong>Script</strong>: (mandatory for script-type plugins) this is the name of the script file in the same folder as the info.plist.</li>
<li><strong>Default</strong>: if this is set to true then this plugin appears on the default toolbar.</li>
<li><strong>FriendlyName</strong>: this is the short name of the plugin that appears as the plugin button text on the toolbar. It should be kept as short as possible. If omitted, the internal name is used instead.</li>
<li><strong>Tooltip</strong>: this is the text of the tooltip that appears when you hover over the plugin button on the toolbar. If omitted, the friendly name is displayed instead.</li>
<li><strong>ButtonImage</strong>: (mandatory) this is the name of a 16x16 TIFF image in the same folder as the info.plist that will be used as the toolbar button image. For small buttons, Vienna takes this and reduces it to 12x12 automatically. However if you specify a TIFF image with the "small" prefix to the button image name then Vienna will use that for small buttons.</li>
<li><strong>ShortenURLs</strong>: for link type plugins, specifies whether Vienna shortens the URL before using it. Vienna uses the <a href="http://www.bit.ly">bit.ly</a> API to do this, there is nothing else you have to specify. To see it in action, try the built-in <a href="http://www.twitter.com">Twitter</a> plugin.</li>
<li><strong>MenuPath</strong>: specifies an optional name for the plugin at the end of the Article menu.
<li><strong>MenuKey</strong>: specifies an optional key association for the plugin in the menu. This should be one or more of: Cmd, Ctrl, Alt and Shift, separated by a '+' character and finally a single letter or number character.<br />
