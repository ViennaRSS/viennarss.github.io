---
layout: post
status: publish
published: true
title: If you are a Google Reader user&hellip;
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
<p>It is important that you save your Google Reader subscription list before the service shuts down on July 1st ! This can be done with <a href="https://www.google.com/takeout/#custom:reader">Google Takeout</a>. Do it as soon as possible !!<br />
The interesting part is the subscriptions.xml file, which is an OPML file.</p>
<p>The next version of Vienna will support the "<a href="http://rss-sync.github.io/Open-Reader-API/rssconsensus/">Open Reader API</a>", allowing synchronization through services supporting it.</p>
<p><a href="http://bazqux.com">Bazqux</a> and <a href="https://feedhq.org">FeedHQ</a> are the services I am currently testing with, and we made significant progresses in the last 48 hours. I'd like to thank Vladimir and Bruno for being so open-minded regarding interoperability and for their help.<br />
Bazqux and FeedHQ are also supported by Mr. Reader (iPad) and Feeddler Pro (iPhone).</p>
<p>If you prefer to wait before subscribing to a sync services, you can have your feeds set locally :<br />
- save your Google Reader subscription list as described before,<br />
- in Vienna Preferences, uncheck "Sync with Google Reader"<br />
- To avoid duplicates, delete all feeds/folders marked with "[G]"<br />
- use the "File->Import Subscriptions…" menu item and select the subscriptions.xml file</p>
