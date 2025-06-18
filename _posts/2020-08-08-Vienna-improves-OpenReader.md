---
layout: post
title: 'Vienna 3.5.6 improves syncing support'
author:
  display_name: barijaona
categories:
- News
---
It has been a long time, but Vienna 3.5.6 is finally out.

The app is now notarised, so it will be much easier to install Vienna under macOS Catalina (10.15).

This version is also important if you intent to use Inoreader.com for syncing between the different devices you use to read feeds. We had problems with Inoreader which has put in place severe limitations of its services. In fact, Inoreader almost entirely blocked the use of Vienna on its servers.

Of course, you could still use TheOldReader.com, Bazqux.com, FeedHQ.org or any FreshRSS server as an alternative. But we disliked the situation.

Thankfully, we have been able to improve it with two changes. 

First, through the use of new algorithms, Vienna 3.5.6 is able to significantly reduce the network traffic between your Mac and any OpenReader server, including Inoreader. The gain is particularly noticeable if you privilege the actions present in the 'Folder' menu for marking articles read, rather than the actions present in the 'Article' menu.

For the time being, we recommend not to use the "*Mark current article read after a short delay*" setting in Preferences, if you are syncing with Inoreader. This could lead to a quick exhaustion of the daily quota of actions that Inoreader allocates to our app.

Instead, set "*Mark current article read after "Next Unread" command*" in the Preferences. Then, mainly use the "*Mark All Articles as Read*" or "*Skip Folder*" commands for updating your reading progression.

Another important change is that each Vienna user is now able to get his/her personal quota to be used with Inoreader, instead of using the very limited quota which has been assigned to us developers.

To do so, go with a web browser to the [https://www.inoreader.com/all_articles#preferences-developer](https://www.inoreader.com/all_articles#preferences-developer) section of your Inoreader account. Choose "New application", then select "Vienna" (or whatever you like) for application name,  "OS X" for platform. You can leave other values unchanged and validate.

Note the values __App ID:__ and __App key:__ which have been assigned to the newly created application.

You can then fire a Terminal session and type the two following commands :

    defaults write uk.co.opencommunity.vienna2 SyncingAppId <App ID:>

and :

    defaults write uk.co.opencommunity.vienna2 SyncingAppKey <App key:>
    
(Replace the quoted parts with the aforementioned values)

You can monitor your use of daily quotas by going back to the [https://www.inoreader.com/all_articles#preferences-developer](https://www.inoreader.com/all_articles#preferences-developer) section of your Inoreader account.
    












