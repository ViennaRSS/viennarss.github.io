---
layout: post
status: publish
published: true
title: Vienna 2.4 Released
author:
  display_name: Michael G. Ströck
  login: Michael Stroeck
  email: michael@stroeck.com
  url: http://www.twitter.com/mstroeck
author_login: Michael Stroeck
author_email: michael@stroeck.com
author_url: http://www.twitter.com/mstroeck
wordpress_id: 108
wordpress_url: http://www.vienna-rss.com/?p=108
date: '2010-01-12 17:56:45 +1100'
date_gmt: '2010-01-12 17:56:45 +1100'
categories:
- Blog
tags: []
---
<p>The Vienna team is happy to announce the release of Vienna 2.4! You can download it from SourceForge at <a title="Vienna 2.4 Beta" href="http://sourceforge.net/projects/vienna-rss/files/ReleasedVersions/2.4.0/Vienna2.4.0.2401.zip/download" target="_self">Vienna 2.4</a>. An English-only version can be <a href="http://sourceforge.net/projects/vienna-rss/files/ReleasedVersions/2.4.0/Vienna2.4.0.2401.en-us.zip/download">downloaded</a> as well. </p>
<h2>Requirements</h2></p>
<p>Vienna 2.4 requires Mac OS X 10.5 Leopard or higher to run. Sorry, we can no longer support Mac OS X 10.4 Tiger.</p>
<h2>Database upgrade</h2></p>
<p>On the first launch, Vienna 2.4 will upgrade your database. Depending on the size of your database, the upgrade may take some time, so please be patient on first launch. Because of the database upgrade, we don't recommend that you switch back and forth between Vienna 2.4 and Vienna 2.3.</p>
<h2>Enhancements</h2></p>
<ul>
<li>Gesture Support:</li>
<ul>
<li>Enable navigating the built-in browser's back/forward-list via  left/right three-finger swipes.</li></p>
<li>Enable navigating feeds via left/right three-finger swipes: Left for "Go Back" and right for "View Next Unread".</li>
<li>Enable scrolling to the top/bottom of web pages and the article list via upwards/downwards three-finger swipes.</li></ul>
<li> The XML source for feeds is now saved, and there is a new menu item "Show XML Source" to display it.</li>
<li>Add support for Internationalized Domain Names (IDN) in the built-in web browser.</li>
<li>Many user interface improvements.</li>
<li>Enable searching for text in the web browser. (Note that this required using the command-shift-g keyboard shortcut for "Find Previous", replacing the old shortcut for New Group Folder.)</li>
<li>Enable printing of web pages.</li>
<li>Double the number of simultaneous feed downloads during refreshing from 10 to 20.</li>
<li>Minor speed improvements for some operations.</li>
<li>An informative error page is displayed in the web browser when a page cannot be loaded.</li>
<li>Add support for the blog editor Blogo.</li><br />
</ul></p>
<h2>Fixes</h2></p>
<ul>
<li>Fix a long standing bug where deleted articles would reappear after emptying the trash.</li>
<li>Eliminate drawing artifacts in the Folders and Articles headers. (Patch from Dan Crosta)</li>
<li>Fix a crash reported in Vienna forum topic 21303</li>
<li>Fix a crash when sorting articles by enclosure URL.</li>
<li>Fix a bug where clicking on a feed link launched Vienna but failed to subscribe to the feed.</li>
<li>Fix the article view scrolling problem reported in Vienna forum topic 20814</li>
<li>Fix the mark all read bug on Snow Leopard reported in Vienna forum topic 20877</li>
<li>Prevent an infinite redirect loop. This was happening with the factcheck feedburner feed.</li>
<li>Vienna's interface now correctly dims when the application is the background.</li>
<li>Fix a bug where changing the layout would hide the tab bar until relaunch.</li>
<li>Fix drawing errors and artifacts in the grey title bars.</li>
<li>Check for https URLs as well as http on the pasteboard when adding a new subscription.</li>
<li>Fix background drawing errors in main window and remove custom window background.</li>
<li>Fix drawing errors in Downloads window and remove the custom background.</li>
<li>Add a workaround for feeds that contain more than one item with the same guid. (For example, the WordPress Trac.)</li>
<li>Fix "Help -> Keyboard shortcuts", which didn't work in some cases.</li>
<li>Numerous fixes to localization of help pages and other strings in German, French, and other languages.</li>
<li>Eliminate deprecated method warnings on Snow Leopard.</li>
<li>Turn off animation of tab resizing. It was slow, superfluous and sometimes caused drawing errors in the tab bar background.</li>
<li>Update SQLite to version 3.6.18</li>
<li>Change "currentSelection" to "currentTextSelection" in Viennas Applescript terminology.</li>
<li>Fix the filter field article selection problem reported <a href="http://forums.cocoaforge.com/viewtopic.php?f=18&t=21665">here</a>. </li>
<p></ul></p>
