---
layout: post
status: publish
published: true
title: Vienna 2.5 - The Social Sharing Edition
author:
  display_name: Michael G. Ströck
  login: Michael Stroeck
  email: michael@stroeck.com
  url: http://www.twitter.com/mstroeck
author_login: Michael Stroeck
author_email: michael@stroeck.com
author_url: http://www.twitter.com/mstroeck
wordpress_id: 285
wordpress_url: http://www.vienna-rss.com/?p=285
date: '2010-03-19 09:18:39 +1100'
date_gmt: '2010-03-19 09:18:39 +1100'
categories:
- Blog
- News
tags: []
---
The Vienna Dev Team is proud to announce the release of Vienna 2.5. Among other things, it adds extendability via a new [plugin development API]({{ '/development/creating-plugins' | prepend: site.baseurl }}) and fixes a small number of bugs. To be more precise, the new plugins make it extremely simple to extend Vienna with sharing capabilities that leverage social networking sites like [Facebook](http://www.facebook.com) and [Twitter](http://www.twitter.com/ViennaRSS). Special thanks go to [Curtis Faith](http://www.curtisfaith.com), who contributed bug fixes for this release.

[![Vienna 2.5 supports user-creatable plugins]({{ '/images/plugins.png' | prepend: site.baseurl }} "Vienna 2.5 supports user-creatable plugins")](http://sourceforge.net/projects/vienna-rss/files/ReleasedVersions/2.5.0/Vienna2.5.0.2501.zip/download)
{: style="text-align: center;"}

### Click to download: [**Vienna 2.5**](http://sourceforge.net/projects/vienna-rss/files/ReleasedVersions/2.5.0/Vienna2.5.0.2501.zip/download)
{: style="text-align: center;"}

### Requirements

This release requires **Mac OS X 10.5 (Leopard)** to run.

### Changes

- User Interface refresh: Removed the grey headers, made the vertical divider easier to grab and made filtering more discoverable.
- Added support for plugins.
- Added support for search engine plugins and the ability to do web-searches from the toolbar.
- Added support for blog editor plugins.
- Added support for sharing plugins that work like bookmarklets for social websites.
- Added support for script plugins.
- Added Share With Facebook button.
- Added Share With Evernote button.
- Added Share With Twitter button with automatic URL shortening via bit.ly.
- Added user contributed "Share with Delicious" plugin to the core distribution. Thanks to forum user czanderna.
- Update to the current version of Sparkle, which prevents auto-updating to a version of Vienna which will not run on the user's system.
- Fix bug where deleting a feed in Unified view mode would cause Vienna to stop working correctly.
- Fix bug where changing the article font size would crash Vienna.
- Fix bug that caused zombiefied update spinners (thanks to Curtis Faith).
- Fix bug that caused the reading position to be lost upon refresh (thanks to Curtis Faith).
