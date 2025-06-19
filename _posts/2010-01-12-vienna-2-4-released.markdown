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
The Vienna team is happy to announce the release of Vienna 2.4! You can download it from SourceForge at [Vienna 2.4](http://sourceforge.net/projects/vienna-rss/files/ReleasedVersions/2.4.0/Vienna2.4.0.2401.zip/download "Vienna 2.4 Beta"). An English-only version can be [downloaded](http://sourceforge.net/projects/vienna-rss/files/ReleasedVersions/2.4.0/Vienna2.4.0.2401.en-us.zip/download) as well.

## Requirements

Vienna 2.4 requires Mac OS X 10.5 Leopard or higher to run. Sorry, we can no longer support Mac OS X 10.4 Tiger.

## Database upgrade

On the first launch, Vienna 2.4 will upgrade your database. Depending on the size of your database, the upgrade may take some time, so please be patient on first launch. Because of the database upgrade, we don't recommend that you switch back and forth between Vienna 2.4 and Vienna 2.3.

## Enhancements

- Gesture Support:
  - Enable navigating the built-in browser's back/forward-list via  left/right three-finger swipes.
  - Enable navigating feeds via left/right three-finger swipes: Left for "Go Back" and right for "View Next Unread".
  - Enable scrolling to the top/bottom of web pages and the article list via upwards/downwards three-finger swipes.
- The XML source for feeds is now saved, and there is a new menu item "Show XML Source" to display it.
- Add support for Internationalized Domain Names (IDN) in the built-in web browser.
- Many user interface improvements.
- Enable searching for text in the web browser. (Note that this required using the command-shift-g keyboard shortcut for "Find Previous", replacing the old shortcut for New Group Folder.)
- Enable printing of web pages.
- Double the number of simultaneous feed downloads during refreshing from 10 to 20.
- Minor speed improvements for some operations.
- An informative error page is displayed in the web browser when a page cannot be loaded.
- Add support for the blog editor Blogo.

## Fixes

- Fix a long standing bug where deleted articles would reappear after emptying the trash.
- Eliminate drawing artifacts in the Folders and Articles headers. (Patch from Dan Crosta)
- Fix a crash reported in Vienna forum topic 21303
- Fix a crash when sorting articles by enclosure URL.
- Fix a bug where clicking on a feed link launched Vienna but failed to subscribe to the feed.
- Fix the article view scrolling problem reported in Vienna forum topic 20814
- Fix the mark all read bug on Snow Leopard reported in Vienna forum topic 20877
- Prevent an infinite redirect loop. This was happening with the factcheck feedburner feed.
- Vienna's interface now correctly dims when the application is the background.
- Fix a bug where changing the layout would hide the tab bar until relaunch.
- Fix drawing errors and artifacts in the grey title bars.
- Check for https URLs as well as http on the pasteboard when adding a new subscription.
- Fix background drawing errors in main window and remove custom window background.
- Fix drawing errors in Downloads window and remove the custom background.
- Add a workaround for feeds that contain more than one item with the same guid. (For example, the WordPress Trac.)
- Fix "Help -> Keyboard shortcuts", which didn't work in some cases.
- Numerous fixes to localization of help pages and other strings in German, French, and other languages.
- Eliminate deprecated method warnings on Snow Leopard.
- Turn off animation of tab resizing. It was slow, superfluous and sometimes caused drawing errors in the tab bar background.
- Update SQLite to version 3.6.18
- Change "currentSelection" to "currentTextSelection" in Viennas Applescript terminology.
- Fix the filter field article selection problem reported [here](http://forums.cocoaforge.com/viewtopic.php?f=18&t=21665).
