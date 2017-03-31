---
layout: page
status: publish
published: true
title: Creating Custom Styles
author:
  display_name: Vienna Administrators
  login: admin
  email: vienna-rss-admins@sourceforge.net
  url: http://www.vienna-rss.com
author_login: admin
author_email: vienna-rss-admins@sourceforge.net
author_url: http://www.vienna-rss.com
wordpress_id: 65
wordpress_url: http://www.vienna-rss.com/?page_id=65
date: '2010-01-09 12:52:14 +1100'
date_gmt: '2010-01-09 12:52:14 +1100'
categories:
- Uncategorized
tags: []
comments: []
---

Vienna supports a variety of different display styles for articles. These styles are provided on the Styles sub-menu off the View menu. A style is a combination of an [HTML](http://en.wikipedia.org/wiki/HTML) template that is used to control the placement of various parts of the article and a [CSS](http://en.wikipedia.org/wiki/Cascading_Style_Sheets) stylesheet that controls the appearance of the article.

### Creating New Styles
You can easily create your own custom styles with a little knowledge of HTML and CSS. This section explains how to do so. Create a folder called Styles under the path `~/Library/Application Support/Vienna`. Under the styles folder, create a new folder and give it the name of the style. The folder name is what appears on the Styles sub-menu so keep it short and memorable. Within your new style folder, create two files:

* template.html
* stylesheet.css

You can have additional files such as images, but these two files must be present at a minimum for your style to work. The design should be handled in *stylesheet.css*, while *template.html* contains the full HTML template for the article minus the head or body wrappers. A typical template appears below:

{% highlight html %}
<div>
	<div>
		<b><a href="$ArticleLink$">$ArticleTitle$</a></b>
	</div></p>
	<div>
		$ArticleBody$
	</div>
	<div>
		<span><a href="$FeedLink$">$FeedTitle$</a></span> <span>$ArticleDate$</span> <span>$ArticleAuthor$</span>
	</div>
</div>
{% endhighlight %}

The parts in `$...$` are special placeholders, called **tags**, that Vienna will fill in when it displays the article. After you have created your style, restart Vienna and your new style should appear on the Styles submenu. Switch to it see your finished work.

### Available Tags
The following is a complete list of the tags currently available to you. They are named to be self-explanatory. If you have an idea for a style that would need the application to expose additional information, please bring it up on the [Developer Forum](https://forums.cocoaforge.com/viewforum.php?f=18) or create a new issue on [GitHub](https://github.com/ViennaRSS/vienna-rss/issues).

* `$ArticleLink$`
* `$ArticleTitle$`
* `$ArticleBody$`
* `$ArticleAuthor$`
* `$ArticleDate$`
* `$ArticleEnclosureLink$`
* `$ArticleEnclosureFilename$`
* `$FeedTitle$`
* `$FeedLink$`
* `$FeedDescription$`

