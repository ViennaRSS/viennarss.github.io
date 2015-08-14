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
<p>Vienna supports a variety of different display styles for articles. These styles are provided on the Styles sub-menu off the View menu. A style is a combination of an <a href="http://en.wikipedia.org/wiki/HTML">HTML</a> template that is used to control the placement of various parts of the article and a <a href="http://en.wikipedia.org/wiki/Cascading_Style_Sheets">CSS</a> stylesheet that controls the appearance of the article.</p>
<h3>Creating New Styles</h3><br />
You can easily create your own custom styles with a little knowledge of HTML and CSS. This section explains how to do so. Create a folder called Styles under ~/Library/Application Support/Vienna. Under the styles folder, create a new folder and give it the name of the style. The folder name is what appears on the Styles sub-menu so keep it short and memorable. Within your new style folder, create two files: </p>
<ul>
<li><strong>template.html</strong>
<li><strong>stylesheet.css</strong></li><br />
</ul></p>
<p>You can have additional files such as images, but these two files must be present at a minimum for your style to work. The designe should be handled in <em>stylesheet.css</em>, while<em> template.html</em> contains the full HTML template for the article minus the head or body wrappers. A typical template appears below:</p>
<pre><code>
&lt;div&gt;
	&lt;div&gt;
		&lt;b&gt;&lt;a href=&quot;$ArticleLink$&quot;&gt;$ArticleTitle$&lt;/a&gt;&lt;/b&gt;
	&lt;/div&gt;&lt;/p&gt;
	&lt;div&gt;
		$ArticleBody$
	&lt;/div&gt;
	&lt;div&gt;
		&lt;span&gt;&lt;a href=&quot;$FeedLink$&quot;&gt;$FeedTitle$&lt;/a&gt;&lt;/span&gt; &lt;span&gt;$ArticleDate$&lt;/span&gt; &lt;span&gt;$ArticleAuthor$&lt;/span&gt;
	&lt;/div&gt;
&lt;/div&gt;
</code></pre>
<p>The parts in $...$ are special placeholders, called <strong>tags</strong>, that Vienna will fill in when it displays the article. After you have created your style, restart Vienna and your new style should appear on the Styles submenu. Switch to it see your finished work.</p>
<h3>Available Tags</h3><br />
The following is a complete list of the tags currently available to you. They are named to be self-explanatory. If you have an idea for a style that would need the application to expose additional information, please bring it up on the <a href="http://forums.cocoaforge.com/viewforum.php?f=20">Developer Forum</a> or create a new issue on <a href="https://github.com/ViennaRSS/vienna-rss/issues">GitHub</a>.</p>
<ul>
<li><code>$ArticleLink$</code></li>
<li><code>$ArticleTitle$</code></li>
<li><code>$ArticleBody$</code></li>
<li><code>$ArticleAuthor$</code></li>
<li><code>$ArticleDate$</code></li>
<li><code>$ArticleEnclosureLink$</code></li>
<li><code>$ArticleEnclosureFilename$</code></li>
<li><code>$FeedTitle$</code></li>
<li><code>$FeedLink$</code></li>
<li><code>$FeedDescription$</code></li><br />
</ul></p>
