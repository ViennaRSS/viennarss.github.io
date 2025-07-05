---
layout: post
status: publish
published: true
title: If you are a Google Reader user…
author:
  display_name: barijaona
  login: barijaona
  email: vienna-rss.com@barijaona.com
  url: http://blog.barijaona.com
author_login: barijaona
author_email: vienna-rss.com@barijaona.com
author_url: http://blog.barijaona.com
wordpress_id: 401
wordpress_url: http://www.vienna-rss.com/?p=401
date: '2013-06-29 05:04:59 +1000'
date_gmt: '2013-06-29 05:04:59 +1000'
categories:
- Uncategorized
tags: []
comments: []
---
It is important that you save your Google Reader subscription list before the service shuts down on July 1st ! This can be done with [Google Takeout](https://www.google.com/takeout/#custom:reader). Do it as soon as possible !! The interesting part is the subscriptions.xml file, which is an OPML file.

The next version of Vienna will support the "[Open Reader API](http://rss-sync.github.io/Open-Reader-API/rssconsensus/)", allowing synchronization through services supporting it.

[Bazqux](http://bazqux.com) and [FeedHQ](https://feedhq.org) are the services I am currently testing with, and we made significant progresses in the last 48 hours. I'd like to thank Vladimir and Bruno for being so open-minded regarding interoperability and for their help.\
Bazqux and FeedHQ are also supported by Mr. Reader (iPad) and Feeddler Pro (iPhone).

If you prefer to wait before subscribing to a sync services, you can have your feeds set locally :\
\- save your Google Reader subscription list as described before,\
\- in Vienna Preferences, uncheck "Sync with Google Reader"\
\- To avoid duplicates, delete all feeds/folders marked with "\[G\]"\
\- use the "File->Import Subscriptions…" menu item and select the subscriptions.xml file
