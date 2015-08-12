---
layout: page
status: publish
published: true
title: Development
author:
  display_name: Vienna Administrators
  login: admin
  email: vienna-rss-admins@sourceforge.net
  url: http://www.vienna-rss.org
author_login: admin
author_email: vienna-rss-admins@sourceforge.net
author_url: http://www.vienna-rss.org
wordpress_id: 16
wordpress_url: http://vienna-rss.sourceforge.net/?page_id=16
date: '2010-01-08 21:25:14 +1100'
date_gmt: '2010-01-08 21:25:14 +1100'
categories:
- Uncategorized
tags: []
comments: []
---
<p>The source code for Vienna lives at <a href="https:&#47;&#47;github.com&#47;viennarss">GitHub<&#47;a>. This section is intended to help you get started with downloading and building Vienna on your own machine. See the <a href="https:&#47;&#47;github.com&#47;viennarss&#47;vienna-rss"> Vienna GitHub Page<&#47;a> to quickly browse the Vienna sources. The rest of this page explains how to download the source to your machine.<&#47;p></p>
<h2>Getting the Source<&#47;h2>
<p>If you are already familiar with open source development for Mac OS X, <a href="https:&#47;&#47;github.com&#47;viennarss&#47;vienna-rss">browse the source<&#47;a> or just <a href="http:&#47;&#47;help.github.com&#47;fork-a-repo&#47;">fork<&#47;a> our <a href="https:&#47;&#47;github.com&#47;viennarss&#47;vienna-rss">Git repository<&#47;a> and get started.<&#47;p></p>
<h2>What You Need<&#47;h2></p>
<p>To build Vienna, you will need:<&#47;p></p>
<ul>
<li>
<p>Mac OSX 10.6 (Snow Leopard) and<a href="http:&#47;&#47;developer.apple.com&#47;technology&#47;xcode.html"> XCode 4<&#47;a>. <&#47;p><&#47;li></p>
<li>
<p>An <a href="http:&#47;&#47;git-scm.com&#47;">up-to-date Git client<&#47;a> and basic knowledge about using Git. GitHub provides a free GUI client that works quite well: <a href="http:&#47;&#47;mac.github.com&#47;">GitHub for Mac<&#47;a><&#47;li><br />
<&#47;ul></p>
<p>To make modifications to the Vienna source code, you will need a working knowledge of Objective-C and the Cocoa framework. See the <a href="http:&#47;&#47;developer.apple.com">Apple Developer's Web Site<&#47;a> for more information on XCode, Objective-C and Cocoa.<&#47;p></p>
<h2>Getting Started<&#47;h2></p>
<p><em>The Vienna source code has to be be checked out (or <em>cloned<&#47;em>, in Git terms) to a folder whose path does <b>not<&#47;b> contain spaces<&#47;em>. This is a limitation of the project file that will likely be fixed in the future but, for now, make sure the full path to the Vienna source folder does not have any spaces in it.<&#47;p>
<p>The trunk contains the current development version and all changes should be contributed to it.<&#47;p>GitHub makes contributing changes easy:</p>
<ul>
<li>Ideally, you should create an account at GitHub.<&#47;li>
<li>Then, simply <a href="http:&#47;&#47;help.github.com&#47;fork-a-repo&#47;">fork<&#47;a> our main repository: <a href="https:&#47;&#47;github.com&#47;viennarss&#47;vienna-rss">vienna-rss<&#47;a><&#47;li>
<li>Clone the repository to your local development machine.<&#47;li>
<li>Get coding, and send us a <a href="http:&#47;&#47;help.github.com&#47;send-pull-requests&#47;">pull request<&#47;a> from your GitHub repository when your patch is ready.<br />
<&#47;ul></p>
<h2>Contributing Changes<&#47;h2></p>
<p>We welcome improvements and bug fixes to the Vienna source code. While  you are free as per the terms of the <a href="http:&#47;&#47;www.apache.org&#47;licenses&#47;LICENSE-2.0.html">Apache 2.0 license<&#47;a> to reuse parts of the Vienna code in your own project, please consider contributing any improvements in Vienna itself back to us so we can review and add to the main source tree.<&#47;p>
<p>If you are looking for ideas to work on, please see the<a href="http:&#47;&#47;sourceforge.net&#47;tracker&#47;?group_id=142635&atid=753018">Vienna Bug Tracker<&#47;a> for bugs that need fixing or the file TODO in Vienna's source code folder for features that have been requested. Please let us know what you are working on by posting a note in the <a href="http:&#47;&#47;forums.cocoaforge.com&#47;viewforum.php?f=20">Vienna Development Forum<&#47;a>. Feel free as well to post any questions or comments you may have about Vienna development. We're happy to help, and we encourage developers to join the Vienna project.<&#47;p></p>
<h2>Documentation<&#47;h2>		</p>
<p>Vienna's source-code is very well documented. Read the (many, many...) comments  and use the debugger to work out which functions do what. If the code becomes large enough then we might write a high level architecture overview but right now the source code is documentation enough. If you are contributing changes, please ensure you follow the coding style used by the rest of the code. That means - function header style, nesting, spacing between keywords, etc. Consistency is important here.</p>
<h2>Development-related Discussion<&#47;h2></p>
<p>Vienna development is discussed in the <a href="http:&#47;&#47;forums.cocoaforge.com&#47;viewforum.php?f=20">Vienna Development Forum<&#47;a> on CocoaForge.<&#47;p></p>
<h2>Coding Guidelines<&#47;h2></p>
<p>We don't accept patches (<a href="http:&#47;&#47;help.github.com&#47;send-pull-requests&#47;">pull requests<&#47;a>, in Git lingo) unconditionally. While the license for Vienna permits you to make your own changes and redistribute them as you see fit, we have our own quality bar for changes that are submitted to the official build so please take a moment to read the below before you start making changes.<&#47;p></p>
<ul>
<li>
<p>Source code style is crucial. Look at the existing code and note the layout of the code, the use of tabs vs. spaces, braces, indents and spaces before and after parenthesis and pointers. We'll undertake minor cleanups if necessary but if your contribution is large and doesn't adhere to the style of the rest of the code, we'll bounce it back for cleanup.<&#47;p><&#47;li></p>
<li>
<p><em>Every<&#47;em> function has a comment block at the beginning. If you add new functions, add comments. They are there to help with future source code indexing and also to make sure that the intent and usage of the function is clear to anybody who maintains it in future.<&#47;p><&#47;li></p>
<li>
<p>If you want to pick something from the wish-list to implement then let us know first so we can mark it as "in progress" and avoid duplicate effort.<&#47;p><&#47;li></p>
<li>
<p>UI changes have a high bar and we recommend you discuss your idea with us first before going ahead and implementing.<&#47;p><&#47;li></p>
<li>
<p>Non-UI changes don't have such a high bar so if you have a patch or a nifty idea, feel free to code it up and send us a pull request<&#47;a>.<&#47;p><&#47;li></p>
<li>
<p>We review all patches before we accept them. For small bugs we'll probably make any fixes ourselves. Larger problems get bounced back for correction.<&#47;p><&#47;li><br />
<&#47;ul></p>
<h2>Localization<&#47;h2></p>
<p>We welcome volunteers who are willing to contribute by localizing Vienna  into other languages. The below table shows the current languages into which Vienna is already localized:<&#47;p></p>
<ul>
<li>English<&#47;li>
<li>Swedish<&#47;li>
<li>French<&#47;li>
<li>Italian<&#47;li>
<li>German<&#47;li>
<li>Dutch<&#47;li>
<li>Traditional Chinese<&#47;li>
<li>Spanish<&#47;li>
<li>Japanese<&#47;li>
<li>Korean<&#47;li>
<li>Brazilian Portuguese<&#47;li>
<li>Simplified Chinese<&#47;li>
<li>Danish<&#47;li>
<li>Czech<&#47;li>
<li>Euskara (Basque)<&#47;li>
<li>Russian<&#47;li>
<li>Ukrainian<&#47;li><br />
<&#47;ul></p>
<p>Additional languages planned for which volunteers are needed:<&#47;p></p>
<ul>
<li>Arabic<&#47;li>
<li>Polish<&#47;li>
<li>Portuguese<&#47;li>
<li>Hebrew<&#47;li><br />
<&#47;ul></p>
<p>If you wish to volunteer to localize Vienna for any of the above languages, contact us at the <a href="http:&#47;&#47;forums.cocoaforge.com&#47;viewforum.php?f=20">Developer Forum<&#47;a>.<&#47;p></p>
<h2>Tools<&#47;h2></p>
<p>To create localised versions of Vienna, you will need the same tools that are required to build Vienna. If you would prefer to work outside of Subversion, then an alternative approach is to copy the English.lproj file from the most recent build of Vienna and work on that.<&#47;p>
<p>Apple provides <a href="http:&#47;&#47;developer.apple.com&#47;intl&#47;localization&#47;tools.html">tools on its web site<&#47;a> that may help you with your efforts. Note that we don't mandate the use of any specific tools. It is up to you to use whatever you find works best for you.<&#47;p>
<p>You need Subversion to enlist in the source code and obtain the latest changes in the English.lproj folder for localization.<&#47;p></p>
