---
layout: page
status: publish
published: true
title: Creating Custom Styles
author:
  display_name: Vienna Administrators
  login: admin
  email: vienna-rss-admins@sourceforge.net
  url: http://www.vienna-rss.org
author_login: admin
author_email: vienna-rss-admins@sourceforge.net
author_url: http://www.vienna-rss.org
wordpress_id: 65
wordpress_url: http://www.vienna-rss.org/?page_id=65
date: '2010-01-09 12:52:14 +1100'
date_gmt: '2010-01-09 12:52:14 +1100'
categories:
- Uncategorized
tags: []
comments: []
---
<p>Vienna supports a variety of different display styles for articles. These styles are provided on the Styles sub-menu off the View menu. A style is a combination of an <a href="http:&#47;&#47;en.wikipedia.org&#47;wiki&#47;HTML">HTML<&#47;a> template that is used to control the placement of various parts of the article and a <a href="http:&#47;&#47;en.wikipedia.org&#47;wiki&#47;Cascading_Style_Sheets">CSS<&#47;a> stylesheet that controls the appearance of the article.</p>
<h3>Creating New Styles<&#47;h3><br />
You can easily create your own custom styles with a little knowledge of HTML and CSS. This section explains how to do so. Create a folder called Styles under ~&#47;Library&#47;Application Support&#47;Vienna. Under the styles folder, create a new folder and give it the name of the style. The folder name is what appears on the Styles sub-menu so keep it short and memorable. Within your new style folder, create two files: </p>
<ul>
<li><strong>template.html<&#47;strong>
<li><strong>stylesheet.css<&#47;strong><&#47;li><br />
<&#47;ul></p>
<p>You can have additional files such as images, but these two files must be present at a minimum for your style to work. The designe should be handled in <em>stylesheet.css<&#47;em>, while<em> template.html<&#47;em> contains the full HTML template for the article minus the head or body wrappers. A typical template appears below:</p>
<pre>[html]</p>
<div>
<div>
		<b><a href="$ArticleLink$">$ArticleTitle$<&#47;a><&#47;b><br />
	<&#47;div></p>
<div>
		$ArticleBody$<br />
	<&#47;div></p>
<div>
		<span><a href="$FeedLink$">$FeedTitle$<&#47;a><&#47;span> <span>$ArticleDate$<&#47;span> <span>$ArticleAuthor$<&#47;span><br />
	<&#47;div><br />
<&#47;div><br />
[&#47;html]<&#47;pre></p>
<p>The parts in $...$ are special placeholders, called <strong>tags<&#47;strong>, that Vienna will fill in when it displays the article. After you have created your style, restart Vienna and your new style should appear on the Styles submenu. Switch to it see your finished work.</p>
<h3>Available Tags<&#47;h3><br />
The following is a complete list of the tags currently available to you. They are named to be self-explanatory. If you have an idea for a style that would need the application to expose additional information, please bring it up on the <a href="http:&#47;&#47;forums.cocoaforge.com&#47;viewforum.php?f=20">Developer Forum<&#47;a> or create a new issue on <a href="https:&#47;&#47;github.com&#47;ViennaRSS&#47;vienna-rss&#47;issues">GitHub<&#47;a>.</p>
<ul>
<li> <code>$ArticleLink$<&#47;code><&#47;li>
<li><code>$ArticleTitle$<&#47;code><&#47;li>
<li><code>$ArticleBody$<&#47;code><&#47;li>
<li><code>$ArticleAuthor$<&#47;code><&#47;li>
<li><code>$ArticleDate$<&#47;code><&#47;li>
<li><code>$ArticleEnclosureLink$<&#47;code><&#47;li>
<li><code>$ArticleEnclosureFilename$<&#47;code><&#47;li>
<li><code>$FeedTitle$<&#47;code><&#47;li>
<li><code>$FeedLink$<&#47;code><&#47;li>
<li><code>$FeedDescription$<&#47;code><&#47;li><br />
<&#47;ul></p>
