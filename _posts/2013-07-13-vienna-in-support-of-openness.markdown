---
layout: post
status: publish
published: true
title: Vienna, in support of openness
author:
  display_name: barijaona
  login: barijaona
  url: http://blog.barijaona.com
excerpt: Vienna can sync with BazQux and FeedHQ.
wordpress_id: 406
wordpress_url: http://www.vienna-rss.com/?p=406
date: '2013-07-13 06:58:07 +1000'
date_gmt: '2013-07-13 06:58:07 +1000'
categories:
- Uncategorized
tags: []
comments: []
---
We are very happy to present [Vienna 3 Beta 12](https://sourceforge.net/projects/vienna-rss/files/latest/download).

The announcement of the end of Google Reader was indeed a shock ; but it also opened to talented developers and entrepreneurs a new range of opportunities for presenting some alternatives. For Vienna users, the end result should be more choice.

Vienna started as a standalone RSS reader. It is still perfectly able to be used this way.

But in a world where the use of portable devices is frequent, total or partial synchronisation of reading lists was a much needed feature. Now, we are able to indicate  to Vienna’s users at least three working solutions :

- [Bazqux](http://www.bazqux.com)
- [FeedHQ](http://feedhq.org)
- any instance of FeedHQ running in the hosting environment of your choice (FeedHQ is an [open source project](https://github.com/feedhq/feedhq)).

Other services might work too, now or in the near future. We chose to support what is called the [Open Reader API](http://rss-sync.github.io/Open-Reader-API/rssconsensus/), which is best summarized by [this post by Marco Arment](http://www.marco.org/2013/03/14/baby-steps-replacing-google-reader). Bazqux and FeedHQ were considered a priority, because the commitment of their teams to this openness approach was clear. And they were very supportive of our efforts, providing ideas for current and future developments.

We will probably be able to add support of The Old Reader a little later. Feedly support might follow one day, but this is not yet a commitment, as a documentation review has yet to be done…

For mobile devices, we currently know of two applications which both support Bazqux and  FeedHQ :

- [Mr. Reader](https://itunes.apple.com/us/app/mr.-reader/id412874834?mt=8) (iPad only)
- [Feeddler Pro](https://itunes.apple.com/en/app/feeddler-rss-reader-pro/id365710282?mt=8).

Please, note that we haven’t tested these iOS apps ourselves. Other solutions will probably emerge.

There are other changes in Vienna Beta 12. Here are the most important :

- Renamed our layouts : Horizontal, Vertical and Unified
- The Unified layout has been completely rewritten. It now allows selection of an article (by use of a right click or a click in the left margin) for sharing it or marking it.
- Vienna’s integrated browser is now able to present the user a file selection dialog (for instance for uploading a file)
- Added a “Reindex Database” menu item
- Fix problems with icons in Leopard and Snow Leopard
- Visual tweaks and improvements
- Translation improvements (Brazilian Portuguese, Dutch, German, French, Korean)
- Many bugfixes

And please, if you have been an user of Vienna for a while, take a minute to answer [this poll on keyboard shortcuts](http://cocoaforge.com/viewtopic.php?t=26269&p=137020).
