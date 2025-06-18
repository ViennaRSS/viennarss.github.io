---
layout: post
status: publish
published: true
title: Vienna 3 BETA with Google Reader Synch
author:
  display_name: Michael G. Ströck
  login: Michael Stroeck
  email: michael@stroeck.com
  url: http://www.twitter.com/mstroeck
author_login: Michael Stroeck
author_email: michael@stroeck.com
author_url: http://www.twitter.com/mstroeck
wordpress_id: 371
wordpress_url: http://www.vienna-rss.com/?p=371
date: '2012-09-15 11:57:42 +1000'
date_gmt: '2012-09-15 11:57:42 +1000'
categories:
- Uncategorized
tags: []
comments: []
---
*UPDATED Jan 2nd 2012  : download link has been updated and refers to 3.0.0 Beta 8*

Since I transferred [Vienna's development to GitHub](https://github.com/ViennaRSS/vienna-rss), we have been getting lots and lots of great contributions to the project. Chief among new contributors are [Salvatore Ansani](http://ansani.it/) and [Barijaona Ramaholimihaso](http://blog.barijaona.com/). Their work has led to a new release of Vienna, which you can now download here:

## [Download Vienna 3 BETA](http://sourceforge.net/projects/vienna-rss/files/TestVersions/3.0.0_beta8/Vienna3.0.0_beta8.tgz/download)

They have been working on a slew of bug-fixes and improvements (Google Reader support!) that you can now find in Vienna 3 BETA:

#### 3.0b.2819

- Fix other nasty crashes on Mountain Lion

#### 3.0b.2818

- Fix some nasty crashes on Mountain Lion which occurred when closing tabs
- Fix the “Check for newer versions of Vienna at startup” preference
- Make the knob of the vertical scrollbar more visible when reading long lists on Lion/Mountain Lion
- Other minor bugfixes and code cleaning

#### 3.0b.2817

- Fix fetching of icons associated to feeds.\
*Note* : users of previous versions are invited to use the “Refresh Folder Images” menu item
- Better accessibility for people with visual impairment through VoiceOver
- Completely logout from Google Reader when the “Sync with Google Reader” preference is unchecked
- Builds are now signed with Developer IDs delivered by Apple, to meet Mountain Lion’s Gatekeeper default requirements.

#### 3.0b.2816

- Google Reader support ! Each feed can either be local (especially authenticated feeds, which are not handled by Google Reader), or hosted on Google Reader
- 64 bit support
- Full Screen support on Mac OSX Lion and Mountain Lion
- Fixes running on Leopard and on PowerPC
- Fixes feeds whose titles are XHTML or contain linefeeds/carriage returns
- Fixes Atom feeds with relative links
- Stay on Discrete Graphics mode on Macs having dual graphics cards
- Improved web browser experience (persistent cookies)
- Some functions which were only available on Report or Condensed layout are now available on Unified layout
- Increased timeout for feeds refresh
- Larger use of multi-threading
- Compiled with LLVM
- Binaries are now signed to avoid blockade by Mountain Lion’s gatekeeper default settings (for first run, you’ll have to right click and select ‘Open’)
- Many other bugfixes
