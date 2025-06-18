---
layout: post
status: publish
published: true
title: IDNs and Cocoa
author:
  display_name: Michael G. Ströck
  login: Michael Stroeck
  email: michael@stroeck.com
  url: http://www.twitter.com/mstroeck
author_login: Michael Stroeck
author_email: michael@stroeck.com
author_url: http://www.twitter.com/mstroeck
wordpress_id: 215
wordpress_url: http://www.vienna-rss.com/?p=215
date: '2010-01-20 19:53:08 +1100'
date_gmt: '2010-01-20 19:53:08 +1100'
categories:
- Cocoa
- Programming
- Tips
tags: []
---
My family name contains an [umlaut](http://en.wikipedia.org/wiki/Umlaut), a fact that sometimes leads to confusion in the English-speaking world, especially when it comes to data-entry on shoddily coded websites. All my life, I have habitually used *Stroeck* instead of my actual name, and that's also my personal domain: *stroeck.com*.

Recently, support for[ Internationalized Domain Names](http://en.wikipedia.org/wiki/Internationalized_domain_name) has been getting better, so I bought *ströck.com*. The first thing I did, of course, was typing it into Vienna's browser bar. Needless to say, it just failed silently :-) NSURL cannot handle IDNs, so in Vienna we now use a little hack to parse them. As far as I'm aware, [WebView's URLFromPasteboard:](http://developer.apple.com/mac/library/DOCUMENTATION/Cocoa/Reference/WebKit/Classes/WebView_Class/Reference/Reference.html#//apple_ref/occ/clm/WebView/URLFromPasteboard:) is the only way to get this functionality in Cocoa without using private API or JavaScript trickery, which I was using before Jeff Johnson found this solution:

{% highlight objc %}
NSURL *urlToLoad = nil;
NSPasteboard * pasteboard = [NSPasteboard pasteboardWithName:@"ViennaIDNURLPb"];
[pasteboard declareTypes:[NSArray arrayWithObject:NSStringPboardType] owner:nil];
@try
{
	if ([pasteboard setString:theUrl forType:NSStringPboardType])
		urlToLoad = [WebView URLFromPasteboard:pasteboard];
}
@catch (NSException * exception)
{
	urlToLoad = nil;
	{
		NSBeep();
		NSLog(@"Can't create URL from string '%@'.", theUrl);
	}
}
return urlToLoad;
{% endhighlight %}

For example, your user might type in  this URL:

    http://www.ströck.com/Folder With Spaces/index.html

Piping that through the above code will yield the following, which you can now plug into an [NSURL](http://developer.apple.com/mac/library/documentation/Cocoa/Reference/Foundation/Classes/NSURL_Class/Reference/Reference.html):

    http://www.xn--strck-lua.com/Folder%20With%20Spaces/index.html
