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
comments:
- id: 17
  author: haschka
  author_email: haschka.spam@gmail.com
  author_url: ''
  date: '2010-01-21 01:20:42 +1100'
  date_gmt: '2010-01-21 01:20:42 +1100'
  content: "CFURLCreateStringByAddingPercentEscapes \r\n\r\nfound in http:&#47;&#47;developer.apple.com&#47;mac&#47;library&#47;documentation&#47;CoreFoundation&#47;Reference&#47;CFURLRef&#47;CFURLRef.pdf\r\n\r\nshould
    do it without invoking NSPasteboard which seems a bit ugly to me"
- id: 18
  author: Vienna Administrators
  author_email: vienna-rss-admins@sourceforge.net
  author_url: http://www.vienna-rss.com
  date: '2010-01-21 04:40:40 +1100'
  date_gmt: '2010-01-21 04:40:40 +1100'
  content: No, it doesn't. It only Percent-Escapes.
---
<p>My family name contains an <a href="http:&#47;&#47;en.wikipedia.org&#47;wiki&#47;Umlaut">umlaut<&#47;a>, a fact that sometimes leads to confusion in the English-speaking world, especially when it comes to data-entry on shoddily coded websites. All my life, I have habitually used <em>Stroeck<&#47;em> instead of my actual name, and that's also my personal domain: <em>stroeck.com<&#47;em>. </p>
<p>Recently, support for<a href="http:&#47;&#47;en.wikipedia.org&#47;wiki&#47;Internationalized_domain_name"> Internationalized Domain Names<&#47;a> has been getting better, so I bought <em>str&ouml;ck.com<&#47;em>. The first thing I did, of course, was typing it into Vienna's browser bar. Needless to say, it just failed silently :-) NSURL cannot handle IDNs, so in Vienna we now use a little hack to parse them. As far as I'm aware, <a href="http:&#47;&#47;developer.apple.com&#47;mac&#47;library&#47;DOCUMENTATION&#47;Cocoa&#47;Reference&#47;WebKit&#47;Classes&#47;WebView_Class&#47;Reference&#47;Reference.html#&#47;&#47;apple_ref&#47;occ&#47;clm&#47;WebView&#47;URLFromPasteboard:">WebView's URLFromPasteboard:<&#47;a> is the only way to get this functionality in Cocoa without using private API or JavaScript trickery, which I was using before Jeff Johnson found this solution:<br />
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
return urlToLoad;[&#47;objc]<&#47;pre></p>
<p>For example, your user might type in  this URL:<br />
[html]http:&#47;&#47;www.str&ouml;ck.com&#47;Folder With Spaces&#47;index.html[&#47;html]<br />
Piping that through the above code will yield the following, which you can now plug into an <a href="http:&#47;&#47;developer.apple.com&#47;mac&#47;library&#47;documentation&#47;Cocoa&#47;Reference&#47;Foundation&#47;Classes&#47;NSURL_Class&#47;Reference&#47;Reference.html">NSURL<&#47;a>:<br />
[html]http:&#47;&#47;www.xn--strck-lua.com&#47;Folder%20With%20Spaces&#47;index.html[&#47;html]</p>
