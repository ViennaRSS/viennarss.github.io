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
wordpress_url: http://www.vienna-rss.org/?page_id=120
date: '2010-01-16 15:09:09 +1100'
date_gmt: '2010-01-16 15:09:09 +1100'
categories:
- Uncategorized
tags: []
comments:
- id: 13
  author: A Vienna 2.5 Sneak Peek&nbsp;|&nbsp;Vienna RSS
  author_email: ''
  author_url: http://www.vienna-rss.org/?p=201
  date: '2010-01-18 12:02:05 +1100'
  date_gmt: '2010-01-18 12:02:05 +1100'
  content: "[...] Creating Plugins (v2.5) [...]"
- id: 65
  author: Vienna 2.5 BETA&nbsp;|&nbsp;Vienna RSS
  author_email: ''
  author_url: http://www.vienna-rss.org/?p=237
  date: '2010-02-08 13:07:15 +1100'
  date_gmt: '2010-02-08 13:07:15 +1100'
  content: "[...] Creating Plugins (v2.5) [...]"
- id: 411
  author: Vienna 2.5 &#8211; The Social Sharing Edition&nbsp;|&nbsp;Vienna RSS
  author_email: ''
  author_url: http://www.vienna-rss.org/?p=285
  date: '2010-03-19 09:18:42 +1100'
  date_gmt: '2010-03-19 09:18:42 +1100'
  content: "[...] Creating Plugins (v2.5) [...]"
---
<p>Starting with v2.5 and later, Vienna supports plugins which are installed on the toolbar and can run defined actions. These plugins are XML-based and can be created by editing a simple <a href="http:&#47;&#47;developer.apple.com&#47;mac&#47;library&#47;documentation&#47;Cocoa&#47;Conceptual&#47;PropertyLists&#47;UnderstandXMLPlist&#47;UnderstandXMLPlist.html">.plist-file<&#47;a> without any knowledge of Cocoa programming, in as little as 15 minutes.  This section describes how to create your own plugins, which will look and work exactly like the built-in ones:<br />
<center><img alt="Vienna 2.5 supports user-creatable plugins" src="http:&#47;&#47;www.vienna-rss.org&#47;img&#47;plugins.png" title="Vienna 2.5 supports user-creatable plugins" width="327" height="77" &#47;><&#47;center></p>
<p><br><br />
<h2>Creating the Plugin Bundle<&#47;h2><br />
Vienna plugins are distributed in the form of folders with the extension "<strong>.viennaplugin<&#47;strong>", which OS X automatically treats as bundles. Simply create a new folder, named like your new plugin. Then edit its name and append ".viennaplugin". This registers the folder as a Vienna plugin folder so that it can be double-clicked or dragged-and-dropped on the Vienna application icon to automatically install it. After this step, you can view the folder's contents via control&#47;right-clicking and choosing "Show Package Contents" from the menu.</p>
<h2>Adding the Necessary Files<&#47;h2><br />
There are three types of plugins supported as of the time of writing: </p>
<ul>
<li>
<strong>Link plugins<&#47;strong> are simple sharing plugins that work with any web service that has a special URL for posting information. For example, if you wanted to share <em>"xyz.com"<&#47;em> (which has the page title "<em>XYZ<&#47;em>") <a href="http:&#47;&#47;www.facebook.com">Facebook's<&#47;a> "sharer.php" would be called like this:<br />
[html]http:&#47;&#47;www.facebook.com&#47;sharer.php?u=http:&#47;&#47;www.xyz.com&amp;amp;t=XYZ[&#47;html]<br />
In a Vienna link plugin, you would use special placeholders to represent this information:<br />
[html]http:&#47;&#47;www.facebook.com&#47;sharer.php?u=$ArticleLink$&amp;amp;t=$ArticleTitle$[&#47;html]<br />
<&#47;li></p>
<li><strong>Script plugins<&#47;strong> can run <a href="http:&#47;&#47;devworld.apple.com&#47;applescript&#47;">AppleScripts<&#47;a>, acting on the information that Vienna and other applications exposes to the user via their script suites.<&#47;li>
<li>
<strong>Blog Editor plugins<&#47;strong> are simple plugins that tell Vienna about any application that can use information about blog posts or websites that it sends to it via its export feature. These include <a href="http:&#47;&#47;www.red-sweater.com&#47;marsedit&#47;">MarsEdit<&#47;a>, <a href="http:&#47;&#47;illuminex.com&#47;ecto&#47;">Ecto<&#47;a>, <a href="http:&#47;&#47;codesorcery.net&#47;pukka">Pukka<&#47;a>, <a href="http:&#47;&#47;www.scifihifi.com&#47;cocoalicious&#47;">Cocoalicious<&#47;a> and many others. Quite a few of these are included in the standard distribution. To create your own plugin, you set <em>Type<&#47;em> to <em>BlogEditor<&#47;em> and <em>BundleIdentifier<&#47;em> to the application's <a href="http:&#47;&#47;developer.apple.com&#47;mac&#47;library&#47;documentation&#47;CoreFoundation&#47;Conceptual&#47;CFBundles&#47;BundleTypes&#47;BundleTypes.html">bundle identifier<&#47;a>, which you can find in the<em> info.plist<&#47;em> file inside the application bundle.<br />
<&#47;li></p>
<p><&#47;ul><br />
Each type requires: </p>
<ul>
<li>An <strong>info.plist<&#47;strong> file which defines the plugin's attributes.<&#47;li>
<li>An <strong>icon file<&#47;strong>, preferably a 16&times;16 TIFF without layers but with an alpha channel.<&#47;li><br />
<&#47;ul></p>
<p>Script plugins aditionally require:</p>
<ul>
<li><strong>The <a href="http:&#47;&#47;devworld.apple.com&#47;applescript&#47;">AppleScript<&#47;a> file<&#47;strong> which, for example, gets information out of Vienna and sends it to an other application.<&#47;li><&#47;ul></p>
<h2>Configuring your Plugin<&#47;h2><br />
The actual configuration of the plugin happens in its "info.plist". The following example completely describes Vienna's built-in Facebook plugin:</p>
<pre>[xml]<br />
<?xml version="1.0" encoding="UTF-8"?><br />
<!DOCTYPE plist PUBLIC "-&#47;&#47;Apple&#47;&#47;DTD PLIST 1.0&#47;&#47;EN" "http:&#47;&#47;www.apple.com&#47;DTDs&#47;PropertyList-1.0.dtd"></p>
<plist version="1.0">
<dict><br />
	<key>Name<&#47;key><br />
	<string>ShareWithFacebook<&#47;string><br />
	<key>Type<&#47;key><br />
	<string>Link<&#47;string><br />
	<key>URL<&#47;key><br />
	<string>http:&#47;&#47;www.facebook.com&#47;sharer.php?u=$ArticleLink$&amp;amp;t=$ArticleTitle$<&#47;string><br />
	<key>Default<&#47;key><br />
	<false&#47;><br />
	<key>FriendlyName<&#47;key><br />
	<string>Facebook<&#47;string><br />
	<key>Tooltip<&#47;key><br />
	<string>Share the current article on Facebook<&#47;string><br />
	<key>ButtonImage<&#47;key><br />
	<string>facebookButton<&#47;string><br />
	<key>MenuPath<&#47;key><br />
	<string>Share With Facebook<&#47;string><br />
	<key>ShortenURLs<&#47;key><br />
	<false&#47;><br />
<&#47;dict><br />
<&#47;plist><br />
[&#47;xml]<&#47;pre></p>
<p>For more information on understanding and editing .plists, please go read <a href="http:&#47;&#47;developer.apple.com&#47;mac&#47;library&#47;documentation&#47;Cocoa&#47;Conceptual&#47;PropertyLists&#47;UnderstandXMLPlist&#47;UnderstandXMLPlist.htm">this document<&#47;a> at the Apple Developer Connection website.</p>
<h2>Configuration Entries<&#47;h2></p>
<ul>
<li><strong>Name<&#47;strong>: (mandatory) this is a short, internal, name that uniquely identifies the plugin. It is now displayed in the UI.<&#47;li>
<li><strong>Type<&#47;strong>: (mandatory) this specifies the plugin type. Three values are accepted: <strong>Link<&#47;strong>,  <strong>Script<&#47;strong> and <strong>BlogEditor<&#47;strong>.<&#47;li>
<li><strong>BundleIdentifier<&#47;strong>: Only used for BlogEditor plugins, this defines the identifier of the application that you want to be called.<&#47;li>
<li><strong>URL<&#47;strong>: (mandatory for link-type plugins) this is the URL that is browed when the plugin button is clicked. Vienna substitutes the $...$ placeholders with actual values from the current article being viewed. See <a href="http:&#47;&#47;www.vienna-rss.org&#47;?page_id=65">here<&#47;a> for a list of placeholders.<&#47;li>
<li><strong>Script<&#47;strong>: (mandatory for script-type plugins) this is the name of the script file in the same folder as the info.plist.<&#47;li>
<li><strong>Default<&#47;strong>: if this is set to true then this plugin appears on the default toolbar.<&#47;li>
<li><strong>FriendlyName<&#47;strong>: this is the short name of the plugin that appears as the plugin button text on the toolbar. It should be kept as short as possible. If omitted, the internal name is used instead.<&#47;li>
<li><strong>Tooltip<&#47;strong>: this is the text of the tooltip that appears when you hover over the plugin button on the toolbar. If omitted, the friendly name is displayed instead.<&#47;li>
<li><strong>ButtonImage<&#47;strong>: (mandatory) this is the name of a 16x16 TIFF image in the same folder as the info.plist that will be used as the toolbar button image. For small buttons, Vienna takes this and reduces it to 12x12 automatically. However if you specify a TIFF image with the "small" prefix to the button image name then Vienna will use that for small buttons.<&#47;li>
<li><strong>ShortenURLs<&#47;strong>: for link type plugins, specifies whether Vienna shortens the URL before using it. Vienna uses the <a href="http:&#47;&#47;www.bit.ly">bit.ly<&#47;a> API to do this, there is nothing else you have to specify. To see it in action, try the built-in <a href="http:&#47;&#47;www.twitter.com">Twitter<&#47;a> plugin.<&#47;li>
<li><strong>MenuPath<&#47;strong>: specifies an optional name for the plugin at the end of the Article menu.
<li><strong>MenuKey<&#47;strong>: specifies an optional key association for the plugin in the menu. This should be one or more of: Cmd, Ctrl, Alt and Shift, separated by a '+' character and finally a single letter or number character.<br />
