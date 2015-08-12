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
wordpress_url: http://www.vienna-rss.org/?p=358
date: '2011-08-29 21:03:49 +1000'
date_gmt: '2011-08-29 21:03:49 +1000'
categories:
- Blog
- News
- Programming
tags: []
comments:
- id: 5304
  author: TomDV
  author_email: arioch@penumbra.be
  author_url: http://blog.penumbra.be
  date: '2011-08-31 10:24:59 +1000'
  date_gmt: '2011-08-31 10:24:59 +1000'
  content: "I couldn't find it on homebrew...\r\n\r\n$ sudo brew update\r\nFrom http:&#47;&#47;github.com&#47;mxcl&#47;homebrew\r\n
    * branch            master     -> FETCH_HEAD\r\nAlready up-to-date.\r\n$ brew
    search vienna\r\n$"
- id: 5305
  author: TomDV
  author_email: arioch@penumbra.be
  author_url: http://blog.penumbra.be
  date: '2011-08-31 10:26:20 +1000'
  date_gmt: '2011-08-31 10:26:20 +1000'
  content: "Oh wait... never mind.\r\nYou were referring to git, not vienna."
- id: 5319
  author: Vienna Administrators
  author_email: vienna-rss-admins@sourceforge.net
  author_url: http://www.vienna-rss.org
  date: '2011-09-22 08:57:31 +1000'
  date_gmt: '2011-09-22 08:57:31 +1000'
  content: |-
    $ brew install github

    That's what I meant :-) You can install Git via homebrew, not Vienna -)
---
<p>As of yesterday, Vienna development happens <a href="https:&#47;&#47;www.github.com&#47;viennarss&#47;vienna-rss">over at GitHub<&#47;a>. All our <a href="http:&#47;&#47;subversion.tigris.org&#47;">Subversion<&#47;a> commit history going back to 2005 was migrated into a new <a href="http:&#47;&#47;www.git-scm.com&#47;">Git<&#47;a> repository. The trunk will now always contain the version currently being worked on. Source for all previous releases will be available as separate tags (2.0.0 to 2.6.0). </p>
<p>To get the latest source, simply paste the following into a shell prompt: </p>
<blockquote><p>git clone git@github.com:ViennaRSS&#47;vienna-rss.git<&#47;blockquote></p>
<p>To do this, you will need an up-to-date version of the Git version control system. I recommend installing it via <a href="http:&#47;&#47;mxcl.github.com&#47;homebrew&#47;">homebrew<&#47;a>, an awesome package manager for Mac OS X. Alternatively, you can use GitHub's freely available GUI client: <a href="http:&#47;&#47;mac.github.com">GitHub for Mac<&#47;a>. The latter will also optionally install the command line tools for you.</p>
<p>Have fun :-)</p>
