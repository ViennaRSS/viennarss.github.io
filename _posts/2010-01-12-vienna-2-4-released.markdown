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
wordpress_url: http://www.vienna-rss.org/?p=108
date: '2010-01-12 17:56:45 +1100'
date_gmt: '2010-01-12 17:56:45 +1100'
categories:
- Blog
tags: []
comments:
- id: 3
  author: Nite
  author_email: 10nite10@gmail.com
  author_url: ''
  date: '2010-01-13 02:01:32 +1100'
  date_gmt: '2010-01-13 02:01:32 +1100'
  content: Awesome features! Rockin'! But, but, but, when is Google Reader sync coming??
- id: 4
  author: The Digital Productivity Blog
  author_email: ext+vienna-rss@digitivity.org
  author_url: http://digitivity.org
  date: '2010-01-13 15:35:55 +1100'
  date_gmt: '2010-01-13 15:35:55 +1100'
  content: "Congratulations on the release. \r\n\r\nIs Vienna a native OS X app?\r\n\r\nI'm
    putting together a list of recommended RSS clients for each platform for my blog
    readers."
- id: 6
  author: Michael Stroeck
  author_email: michael@stroeck.com
  author_url: ''
  date: '2010-01-14 10:30:37 +1100'
  date_gmt: '2010-01-14 10:30:37 +1100'
  content: Yes, Vienna is a completely native OS X app written in Objective-C with
    the Cocoa framework.
- id: 8
  author: The Digital Productivity Blog
  author_email: ext+vienna-rss@digitivity.org
  author_url: http://digitivity.org
  date: '2010-01-14 10:59:35 +1100'
  date_gmt: '2010-01-14 10:59:35 +1100'
  content: "That's great!\r\n\r\nI've updated my post at\r\nhttp:&#47;&#47;digitivity.org&#47;555&#47;what-is-rss\r\n\r\nI'm
    recommending Vienna as the default Mac-based open-source RSS aggregator."
- id: 9
  author: Axel Gschaider
  author_email: axel.gschaider@gmx.at
  author_url: ''
  date: '2010-01-14 11:17:08 +1100'
  date_gmt: '2010-01-14 11:17:08 +1100'
  content: "Hi there,ma\r\n\r\nnice update! Looks good and works great.\r\n\r\nThere's
    just one thing I still miss: I use flags to mark articles, I already read and
    want to archive.\r\nI would like to be able to mark an article while reading it.
    Right now, when wanting to flagg an article, I have to go back to the main view,
    search for the articles title and mark it there.\r\n\r\nIt's not a big thing but
    anyway ;)\r\n\r\nNon the less: Viennas the best rss-viewer ever! Thanks for all
    the work.\r\n\r\nregards Axel"
---
<p>The Vienna team is happy to announce the release of Vienna 2.4! You can download it from SourceForge at <a title="Vienna 2.4 Beta" href="http:&#47;&#47;sourceforge.net&#47;projects&#47;vienna-rss&#47;files&#47;ReleasedVersions&#47;2.4.0&#47;Vienna2.4.0.2401.zip&#47;download" target="_self">Vienna 2.4<&#47;a>. An English-only version can be <a href="http:&#47;&#47;sourceforge.net&#47;projects&#47;vienna-rss&#47;files&#47;ReleasedVersions&#47;2.4.0&#47;Vienna2.4.0.2401.en-us.zip&#47;download">downloaded<&#47;a> as well. </p>
<h2>Requirements<&#47;h2></p>
<p>Vienna 2.4 requires Mac OS X 10.5 Leopard or higher to run. Sorry, we can no longer support Mac OS X 10.4 Tiger.</p>
<h2>Database upgrade<&#47;h2></p>
<p>On the first launch, Vienna 2.4 will upgrade your database. Depending on the size of your database, the upgrade may take some time, so please be patient on first launch. Because of the database upgrade, we don't recommend that you switch back and forth between Vienna 2.4 and Vienna 2.3.</p>
<h2>Enhancements<&#47;h2></p>
<ul>
<li>Gesture Support:<&#47;li>
<ul>
<li>Enable navigating the built-in browser's back&#47;forward-list via  left&#47;right three-finger swipes.<&#47;li></p>
<li>Enable navigating feeds via left&#47;right three-finger swipes: Left for "Go Back" and right for "View Next Unread".<&#47;li>
<li>Enable scrolling to the top&#47;bottom of web pages and the article list via upwards&#47;downwards three-finger swipes.<&#47;li><&#47;ul>
<li> The XML source for feeds is now saved, and there is a new menu item "Show XML Source" to display it.<&#47;li>
<li>Add support for Internationalized Domain Names (IDN) in the built-in web browser.<&#47;li>
<li>Many user interface improvements.<&#47;li>
<li>Enable searching for text in the web browser. (Note that this required using the command-shift-g keyboard shortcut for "Find Previous", replacing the old shortcut for New Group Folder.)<&#47;li>
<li>Enable printing of web pages.<&#47;li>
<li>Double the number of simultaneous feed downloads during refreshing from 10 to 20.<&#47;li>
<li>Minor speed improvements for some operations.<&#47;li>
<li>An informative error page is displayed in the web browser when a page cannot be loaded.<&#47;li>
<li>Add support for the blog editor Blogo.<&#47;li><br />
<&#47;ul></p>
<h2>Fixes<&#47;h2></p>
<ul>
<li>Fix a long standing bug where deleted articles would reappear after emptying the trash.<&#47;li>
<li>Eliminate drawing artifacts in the Folders and Articles headers. (Patch from Dan Crosta)<&#47;li>
<li>Fix a crash reported in Vienna forum topic 21303<&#47;li>
<li>Fix a crash when sorting articles by enclosure URL.<&#47;li>
<li>Fix a bug where clicking on a feed link launched Vienna but failed to subscribe to the feed.<&#47;li>
<li>Fix the article view scrolling problem reported in Vienna forum topic 20814<&#47;li>
<li>Fix the mark all read bug on Snow Leopard reported in Vienna forum topic 20877<&#47;li>
<li>Prevent an infinite redirect loop. This was happening with the factcheck feedburner feed.<&#47;li>
<li>Vienna's interface now correctly dims when the application is the background.<&#47;li>
<li>Fix a bug where changing the layout would hide the tab bar until relaunch.<&#47;li>
<li>Fix drawing errors and artifacts in the grey title bars.<&#47;li>
<li>Check for https URLs as well as http on the pasteboard when adding a new subscription.<&#47;li>
<li>Fix background drawing errors in main window and remove custom window background.<&#47;li>
<li>Fix drawing errors in Downloads window and remove the custom background.<&#47;li>
<li>Add a workaround for feeds that contain more than one item with the same guid. (For example, the WordPress Trac.)<&#47;li>
<li>Fix "Help -> Keyboard shortcuts", which didn't work in some cases.<&#47;li>
<li>Numerous fixes to localization of help pages and other strings in German, French, and other languages.<&#47;li>
<li>Eliminate deprecated method warnings on Snow Leopard.<&#47;li>
<li>Turn off animation of tab resizing. It was slow, superfluous and sometimes caused drawing errors in the tab bar background.<&#47;li>
<li>Update SQLite to version 3.6.18<&#47;li>
<li>Change "currentSelection" to "currentTextSelection" in Viennas Applescript terminology.<&#47;li>
<li>Fix the filter field article selection problem reported <a href="http:&#47;&#47;forums.cocoaforge.com&#47;viewtopic.php?f=18&t=21665">here<&#47;a>. <&#47;li>
<p><&#47;ul></p>
