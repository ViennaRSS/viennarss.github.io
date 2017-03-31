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
<p>As of yesterday, Vienna development happens <a href="https://www.github.com/viennarss/vienna-rss">over at GitHub</a>. All our <a href="http://subversion.tigris.org/">Subversion</a> commit history going back to 2005 was migrated into a new <a href="http://www.git-scm.com/">Git</a> repository. The trunk will now always contain the version currently being worked on. Source for all previous releases will be available as separate tags (2.0.0 to 2.6.0). </p>
<p>To get the latest source, simply paste the following into a shell prompt: </p>
<blockquote><p>git clone git@github.com:ViennaRSS/vienna-rss.git</blockquote></p>
<p>To do this, you will need an up-to-date version of the Git version control system. I recommend installing it via <a href="http://mxcl.github.com/homebrew/">homebrew</a>, an awesome package manager for Mac OS X. Alternatively, you can use GitHub's freely available GUI client: <a href="http://mac.github.com">GitHub for Mac</a>. The latter will also optionally install the command line tools for you.</p>
<p>Have fun :-)</p>
