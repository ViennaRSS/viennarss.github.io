---
layout: page
status: publish
published: true
title: FAQs
author:
date: '2010-01-09 22:33:38 +1100'
categories:
---

* <a href="#What_does_Vienna_stand_for">What does the name Vienna mean?</a>
* <a href="#Where_do_I_get_the_Vienna_source_code">Where do I get the Vienna source code?</a>
* <a href="#I_found_a_problem_with_Vienna._How_do_I_report_it">I found a problem with Vienna. How do I report it?</a>
* <a href="#How_do_I_create_my_own_styles">How do I create my own styles?</a>
* <a href="#How_do_I_create_my_own_scripts">How do I create my own scripts?</a>
* <a href="#How_do_I_create_my_own_plugins">How do I create my own plugins?</a>
* <a href="#How_can_I_see_what_happened_when_my_subscriptions_are_refreshed">How can I see what happened when my subscriptions are refreshed?</a>
* <a href="#How_do_I_move_my_Vienna_database_to_another_folder">How do I move my Vienna database to another folder?</a>
* <a href="#One_of_my_subscriptions_reports_Error_parsing_XML_data_in_feed._What_does_this_mean">One of my subscriptions reports "Error parsing XML data in feed". What does this mean?</a>
* <a href="#Is_there_a_shortcut_key_for_going_to_the_next_article_marking_read_etc_">Is there a shortcut key for going to the next article, marking read, etc?</a>
* <a href="#How_do_I_use_Auto_Expire_and_what_does_it_do">How do I use Auto Expire and what does it do?</a>
* <a href="#How_do_I_request_an_enhancement_in_Vienna">How do I request an enhancement in Vienna?</a>

<h2>
	<a name="What_does_Vienna_stand_for" id="What_does_Vienna_stand_for">What does the name Vienna mean?</a>
</h2>

[Vienna](https://en.wikipedia.org/wiki/Vienna) is the capital city of [Austria](https://en.wikipedia.org/wiki/Austria). Project lead Steve Palmer says the about the name:

> "I honestly don't recall why I picked that particular name. I had it in mind as a codename for many years and when it came to pick a name for a newsreader, it simply stood out and the name stuck. And, yes, I am aware that Microsoft later picked Vienna as the codename for their successor to Vista.

<h2>
	<a name="Where_do_I_get_the_Vienna_source_code" id="Where_do_I_get_the_Vienna_source_code">Where do I get the Vienna source code?</a>
</h2>

See the [Development page](http://www.vienna-rss.com/?page_id=16) for instructions on getting the source code for Vienna. The source code is freely available if you're interested in learning how Vienna works, if you want to build your own copy of Vienna from scratch on your own machine or if you want to borrow portions for inclusion in your own project. The source is provided under the [Apache 2.0 license](http://www.apache.org/licenses/LICENSE-2.0.html).

<h2>
	<a name="I_found_a_problem_with_Vienna._How_do_I_report_it" id="I_found_a_problem_with_Vienna._How_do_I_report_it">I found a problem with Vienna. How do I report it?</a>
</h2>

Create a new issue or start a discussion over on our [GitHub page]({{ site.app_github_url }}) and somebody will investigate or respond. Provide as much information about the problem as you can including: the build of Vienna (obtained from the About Vienna panel), steps to reproduce and what you expected to happen. If the problem occurs with a specific news feed, always include the URL of the feed. It is easier to fix problems that we can reproduce.

Make sure you're always running the most recent build of Vienna. The Check for Updates command will report if there's a newer build available than the one you have.

Fixes for bugs take priority over new features so if your problem is confirmed to be a bug with high impact and no simple workaround then we'll look at making a fix available as soon as reasonably possible.

<h2>
	<a name="How_do_I_create_my_own_styles" id="How_do_I_create_my_own_styles">How do I create my own styles?</a>
</h2>

See the [Custom Styles page](http://www.vienna-rss.com/?page_id=65) for instructions.

<h2>
	<a name="How_do_I_create_my_own_scripts" id="How_do_I_create_my_own_scripts">How do I create my own scripts?</a>
</h2>

Vienna's scripts are written using AppleScript. See the [Apple resource page](http://www.apple.com/macosx/features/applescript/resources.html) for more details. Also take a look at the Vienna scripting dictionary and examples of what you can accomplish.

To submit your own script, create an issue or a pull request on our [GitHub page]({{ site.site_github_url }}). After it has been reviewed and accepted, it will be made available on the Extras page.

<h2>
	<a name="How_do_I_create_my_own_plugins" id="How_do_I_create_my_own_plugins">How do I create my own plugins?</a>
</h2>

You can create plugins as easily as editing a single plugin file and no scripting needed. See the [Creating Plugins](http://www.vienna-rss.com/?page_id=120) page for more details. You can also package and share your plugins with others.

<h2>
	<a name="How_can_I_see_what_happened_when_my_subscriptions_are_refreshed" id="How_can_I_see_what_happened_when_my_subscriptions_are_refreshed">How can I see what happened when my subscriptions are refreshed?</a>
</h2>

Open the Activity Window from the Window menu. The activity window shows all subscriptions and the status of the last time they were refreshed in that session. The bottom of the activity window shows more details include the HTTP headers and may be useful for debugging. (If the details pane is not visible, grab the split bar at the bottom of the Activity Window and drag it up to uncover the pane).

<h2>
	<a name="How_do_I_move_my_Vienna_database_to_another_folder" id="How_do_I_move_my_Vienna_database_to_another_folder">How do I move my Vienna database to another folder?</a>
</h2>

By default, your Vienna database is the messages.db file which is located at ~/Library/Application Support/Vienna. You can move this to another folder if you wish. The following steps show how:

1. Shut down Vienna.
2. Open a console window and enter:

`defaults write uk.co.opencommunity.vienna2 "DefaultDatabase" '<path to new messages.db>'` 
	where
`<path to new messages.db>` is the name of the folder that contains the messages.db file. The path itself should have the messages.db filename at the end. 
	
	For example: `defaults write uk.co.opencommunity.vienna2 "DefaultDatabase" '/Users/steve/mydata/messages.db'`
3. Restart Vienna.

<h2>
	<a name="One_of_my_subscriptions_reports_Error_parsing_XML_data_in_feed._What_does_this_mean" id="One_of_my_subscriptions_reports_Error_parsing_XML_data_in_feed._What_does_this_mean">One of my subscriptions reports "Error parsing XML data in feed". What does this mean?</a>
</h2>

It means that Vienna got a feed back from the subscription that it couldn't interpret. There are several reasons for this:

1. The URL of the feed may not be pointing to an RSS or Atom feed but to a web page. Check the URL of the offending feed carefully.<br />
2. The feed itself may contain malformed XML. Some subscriptions make a mistake in putting together the XML that makes up the feed and Vienna cannot interpret malformed XML. Use the Validate Feed command on the File menu to see if this is the case. Unfortunately you cannot do much about this in Vienna except wait for the feed itself to be corrected by the site.<br />
3. The feed may be incomplete. If the refresh was interrupted then the XML data will be incomplete and will appear malformed in Vienna. A second refresh may correct this problem.

If none of the above explain the problem, create a issue on the [GitHub page]({{ site.app_github_url }}/issues) with the URL of the feed exhibiting the problem.

<h2>
	<a name="Is_there_a_shortcut_key_for_going_to_the_next_article_marking_read_etc_" id="Is_there_a_shortcut_key_for_going_to_the_next_article_marking_read_etc_">Is there a shortcut key for going to the next article, marking read, etc?</a>
</h2>

Probably. There are single key equivalents for some of the menu commands such as:

* Spacebar - goes to the next unread article. If the current article is several pages long, it will scroll through that article first. If you're at the end of the current article it will then go to the next unread article. By contrast the Next Unread command (Cmd+U) always goes straight to the next unread article.
* R - marks the current article read if it is unread, or unread if it is read.<br />
* F - flags the current article if it isn't already flagged, or removes the existing flag if it is not.<br />

Look in the Vienna Help file for more shortcuts.

<h2>
	<a name="How_do_I_use_Auto_Expire_and_what_does_it_do" id="How_do_I_use_Auto_Expire_and_what_does_it_do">How do I use Auto Expire and what does it do?</a>
</h2>

Auto-expire moves articles older than a certain number of days to the Trash folder. It allows you to keep your folders manageable by only retaining articles that are recent. The auto-expire runs both when Vienna starts and after you have refreshed any subscriptions. To control the age of articles to auto-expire, change the "Expire articles older than" option in Preferences.

Auto-expire will NOT remove unread or flagged articles. It assumes that you haven't read these articles and thus leaves them alone.

<h2>
	<a name="How_do_I_request_an_enhancement_in_Vienna" id="How_do_I_request_an_enhancement_in_Vienna">How do I request an enhancement in Vienna?</a>
</h2>

Start a discussion on our [GitHub Discussions]({{ site.app_github_url }}/discussions) page.
