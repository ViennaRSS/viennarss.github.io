---
layout: post
status: publish
published: true
title: Vienna development moves to GitHub
author:
  display_name: Michael G. Ströck
  login: Michael Stroeck
  email: michael@stroeck.com
  url: http://www.twitter.com/mstroeck
author_login: Michael Stroeck
author_email: michael@stroeck.com
author_url: http://www.twitter.com/mstroeck
wordpress_id: 358
wordpress_url: http://www.vienna-rss.com/?p=358
date: '2011-08-29 21:03:49 +1000'
date_gmt: '2011-08-29 21:03:49 +1000'
categories:
- Blog
- News
- Programming
tags: []
---
As of yesterday, Vienna development happens [over at GitHub](https://www.github.com/viennarss/vienna-rss). All our [Subversion](http://subversion.tigris.org/) commit history going back to 2005 was migrated into a new [Git](http://www.git-scm.com/) repository. The trunk will now always contain the version currently being worked on. Source for all previous releases will be available as separate tags (2.0.0 to 2.6.0).

To get the latest source, simply paste the following into a shell prompt:

> git clone git@github.com:ViennaRSS/vienna-rss.git

To do this, you will need an up-to-date version of the Git version control system. I recommend installing it via [homebrew](http://mxcl.github.com/homebrew/), an awesome package manager for Mac OS X. Alternatively, you can use GitHub's freely available GUI client: [GitHub for Mac](http://mac.github.com). The latter will also optionally install the command line tools for you.

Have fun :-)
