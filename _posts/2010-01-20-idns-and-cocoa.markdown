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
<p>My family name contains an <a href="http://en.wikipedia.org/wiki/Umlaut">umlaut</a>, a fact that sometimes leads to confusion in the English-speaking world, especially when it comes to data-entry on shoddily coded websites. All my life, I have habitually used <em>Stroeck</em> instead of my actual name, and that's also my personal domain: <em>stroeck.com</em>. </p>
<p>Recently, support for<a href="http://en.wikipedia.org/wiki/Internationalized_domain_name"> Internationalized Domain Names</a> has been getting better, so I bought <em>ströck.com</em>. The first thing I did, of course, was typing it into Vienna's browser bar. Needless to say, it just failed silently :-) NSURL cannot handle IDNs, so in Vienna we now use a little hack to parse them. As far as I'm aware, <a href="http://developer.apple.com/mac/library/DOCUMENTATION/Cocoa/Reference/WebKit/Classes/WebView_Class/Reference/Reference.html#//apple_ref/occ/clm/WebView/URLFromPasteboard:">WebView's URLFromPasteboard:</a> is the only way to get this functionality in Cocoa without using private API or JavaScript trickery, which I was using before Jeff Johnson found this solution:<br />
<br></p>
<pre>[objc]<br />
NSURL *urlToLoad = nil;<br />
NSPasteboard * pasteboard = [NSPasteboard pasteboardWithName:@"ViennaIDNURLPb"];<br />
[pasteboard declareTypes:[NSArray arrayWithObject:NSStringPboardType] owner:nil];<br />
@try<br />
{<br />
	if ([pasteboard setString:theUrl forType:NSStringPboardType])<br />
		urlToLoad = [WebView URLFromPasteboard:pasteboard];<br />
}<br />
@catch (NSException * exception)<br />
{<br />
	urlToLoad = nil;<br />
	{<br />
		NSBeep();<br />
		NSLog(@"Can't create URL from string '%@'.", theUrl);<br />
	}<br />
}<br />
return urlToLoad;[/objc]</pre></p>
<p>For example, your user might type in  this URL:<br />
[html]http://www.ströck.com/Folder With Spaces/index.html[/html]<br />
Piping that through the above code will yield the following, which you can now plug into an <a href="http://developer.apple.com/mac/library/documentation/Cocoa/Reference/Foundation/Classes/NSURL_Class/Reference/Reference.html">NSURL</a>:<br />
[html]http://www.xn--strck-lua.com/Folder%20With%20Spaces/index.html[/html]</p>
