---
layout: page
status: publish
published: true
title: FAQs
author:
date: '2010-01-09 22:33:38 +1100'
categories:
---

* [What does the name Vienna mean?](#What_does_Vienna_stand_for)
* [Where do I get the Vienna source code?](#Where_do_I_get_the_Vienna_source_code)
* [I found a problem with Vienna. How do I report it?](#I_found_a_problem_with_Vienna._How_do_I_report_it)
* [How do I create my own styles?](#How_do_I_create_my_own_styles)
* [How do I create my own scripts?](#How_do_I_create_my_own_scripts)
* [How do I create my own plug-ins?](#How_do_I_create_my_own_plugins)
* [How can I see what happened when my subscriptions are refreshed?](#How_can_I_see_what_happened_when_my_subscriptions_are_refreshed)
* [How do I move my Vienna database to another folder?](#How_do_I_move_my_Vienna_database_to_another_folder)
* [One of my subscriptions reports "Error parsing XML data in feed". What does this mean?](#One_of_my_subscriptions_reports_Error_parsing_XML_data_in_feed._What_does_this_mean)
* [Is there a shortcut key for going to the next article, marking read, etc?](#Is_there_a_shortcut_key_for_going_to_the_next_article_marking_read_etc_)
* [How do I use Auto Expire and what does it do?](#How_do_I_use_Auto_Expire_and_what_does_it_do)
* [How do I request an enhancement in Vienna?](#How_do_I_request_an_enhancement_in_Vienna)

## What does the name Vienna mean? {#What_does_Vienna_stand_for}

[Vienna](https://en.wikipedia.org/wiki/Vienna) is the capital city of [Austria](https://en.wikipedia.org/wiki/Austria). Project lead Steve Palmer says the about the name:

> "I honestly don't recall why I picked that particular name. I had it in mind as a codename for many years and when it came to pick a name for a newsreader, it simply stood out and the name stuck. And, yes, I am aware that Microsoft later picked Vienna as the codename for their successor to Vista.

## Where do I get the Vienna source code? {#Where_do_I_get_the_Vienna_source_code}

See the [Development page]({{ "/development" | prepend: site.baseurl }}) for instructions on getting the source code for Vienna. The source code is freely available if you're interested in learning how Vienna works, if you want to build your own copy of Vienna from scratch on your own machine or if you want to borrow portions for inclusion in your own project. The source is provided under the [Apache 2.0 license](http://www.apache.org/licenses/LICENSE-2.0.html).

## I found a problem with Vienna. How do I report it? {#I_found_a_problem_with_Vienna._How_do_I_report_it}

Create a new issue or start a discussion over on our [GitHub page]({{ site.app_github_url }}) and somebody will investigate or respond. Provide as much information about the problem as you can including: the build of Vienna (obtained from the About Vienna panel), steps to reproduce and what you expected to happen. If the problem occurs with a specific news feed, always include the URL of the feed. It is easier to fix problems that we can reproduce.

Make sure you're always running the most recent build of Vienna. The Check for Updates command will report if there's a newer build available than the one you have.

Fixes for bugs take priority over new features so if your problem is confirmed to be a bug with high impact and no simple workaround then we'll look at making a fix available as soon as reasonably possible.

## How do I create my own styles? {#How_do_I_create_my_own_styles}

See the [Custom Styles page]({{ "/development/creating-styles" | prepend: site.baseurl }}) for instructions.

## How do I create my own scripts? {#How_do_I_create_my_own_scripts}

Vienna's scripts are written using AppleScript. See [Mac Scripting Essentials](https://developer.apple.com/library/archive/documentation/LanguagesUtilities/Conceptual/MacAutomationScriptingGuide/index.html) and [Introduction to AppleScript Language Guide](https://developer.apple.com/library/archive/documentation/AppleScript/Conceptual/AppleScriptLangGuide/introduction/ASLR_intro.html) for more details. Also take a look at the Vienna scripting dictionary and examples of what you can accomplish.

To submit your own script, create an issue or a pull request on our [GitHub page]({{ site.site_github_url }}). After it has been reviewed and accepted, it will be made available on the Extras page.

## How do I create my own plug-ins? {#How_do_I_create_my_own_plugins}

You can create plug-ins as easily as editing a single plug-in file and no scripting needed. See the [Creating Plug-ins]({{ "/development/creating-plugins" | prepend: site.baseurl }}) page for more details. You can also package and share your plug-ins with others.

## How can I see what happened when my subscriptions are refreshed? {#How_can_I_see_what_happened_when_my_subscriptions_are_refreshed}

Open the Activity Window from the Window menu. The activity window shows all subscriptions and the status of the last time they were refreshed in that session. The bottom of the activity window shows more details include the HTTP headers and may be useful for debugging. (If the details pane is not visible, grab the split bar at the bottom of the Activity Window and drag it up to uncover the pane).

## How do I move my Vienna database to another folder? {#How_do_I_move_my_Vienna_database_to_another_folder}

By default, your Vienna database is the messages.db file which is located at ~/Library/Application Support/Vienna. You can move this to another folder if you wish. The following steps show how:

1. Shut down Vienna.
2. Open a console window and enter:

       defaults write uk.co.opencommunity.vienna2 "DefaultDatabase" '<path to new messages.db>'

   where `<path to new messages.db>` is the name of the folder that contains the messages.db file. The path itself should have the messages.db filename at the end.

   For example:

       defaults write uk.co.opencommunity.vienna2 "DefaultDatabase" '/Users/steve/mydata/messages.db'
3. Restart Vienna.

## One of my subscriptions reports "Error parsing XML data in feed". What does this mean? {#One_of_my_subscriptions_reports_Error_parsing_XML_data_in_feed._What_does_this_mean}

It means that Vienna got a feed back from the subscription that it couldn't interpret. There are several reasons for this:

1. The URL of the feed may not be pointing to an RSS or Atom feed but to a web page. Check the URL of the offending feed carefully.
2. The feed itself may contain malformed XML. Some subscriptions make a mistake in putting together the XML that makes up the feed and Vienna cannot interpret malformed XML. Use the Validate Feed command on the File menu to see if this is the case. Unfortunately you cannot do much about this in Vienna except wait for the feed itself to be corrected by the site.
3. The feed may be incomplete. If the refresh was interrupted then the XML data will be incomplete and will appear malformed in Vienna. A second refresh may correct this problem.

If none of the above explain the problem, create a issue on the [GitHub page]({{ site.app_github_url }}/issues) with the URL of the feed exhibiting the problem.

## Is there a shortcut key for going to the next article, marking read, etc? {#Is_there_a_shortcut_key_for_going_to_the_next_article_marking_read_etc_}

Probably. There are single key equivalents for some of the menu commands such as:

* Spacebar - goes to the next unread article. If the current article is several pages long, it will scroll through that article first. If you're at the end of the current article it will then go to the next unread article. By contrast the Next Unread command (Cmd+U) always goes straight to the next unread article.
* R - marks the current article read if it is unread, or unread if it is read.
* F - flags the current article if it isn't already flagged, or removes the existing flag if it is not.

Look in the Vienna Help file for more shortcuts.

## How do I use Auto Expire and what does it do? {#How_do_I_use_Auto_Expire_and_what_does_it_do}

Auto-expire moves articles older than a certain number of days to the Trash folder. It allows you to keep your folders manageable by only retaining articles that are recent. The auto-expire runs both when Vienna starts and after you have refreshed any subscriptions. To control the age of articles to auto-expire, change the "Expire articles older than" option in Preferences.

Auto-expire will NOT remove unread or flagged articles. It assumes that you haven't read these articles and thus leaves them alone.

## How do I request an enhancement in Vienna? {#How_do_I_request_an_enhancement_in_Vienna}

Start a discussion on our [GitHub Discussions]({{ site.app_github_url }}/discussions) page.
