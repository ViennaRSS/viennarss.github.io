---
layout: post
title: 'Celebrating 20 Years of Vienna RSS'
author:
  display_name: barijaona
categories:
- Blog
- News
---
Nine months ago, I noticed that the first public build of Vienna was published on Sourceforge on [July 7th of 2005](https://sourceforge.net/projects/vienna-rss/files/TestVersions/2.0.0.2000/). Promising to myself to collect memories and post a blog post, I added a reminder for today, expecting that, as I would be retired from my banking job, I would be more available to do that.

I am effectively retired now, but time is still flying, so I was in a hurry this week-end. But a promise is a promise: let's celebrate!

## From Aqua…

My long time accomplice [Josh](https://github.com/josh64x2) has almost always good advices when he reviews either my code or my ideas. In an email he sent me on Saturday, he wondered if it would be worth creating a virtual machine and taking screenshots of the v1.0.

Here we go, thanks to [archive.org](https://archive.org/details/mac104-tiger "Mac OS X 10.4 Tiger")! After some minor fiddling, I got the initial version of Vienna running on VirtualBox on [my retro hack](https://github.com/barijaona/OpenCore_GA-Z170X-Gaming5). But making it connect to today's World Wide Web and adding at least a feed to Vienna turned challenging. Most websites require Transport Layer Security 1.2 or better now, and even after installing the updated certificates, I could not make any https connection work from Mac OS X Tiger.

But thanks to [Protoweb](https://protoweb.org "Bringing Back The Information Super Highway!") and proxy settings, I was able to get a retro version of BBC's feed!

![Screenshot of initial Vienna RSS Beta - Horizontal layout](/images/20th//Vienna2-readingPaneBelow.png)

The toolbar position feels a bit strange, but all other things feel immediately natural and familiar…

I was quick to adapt the settings to me liking: just a few seconds to note that, in the "View" menu, instead of "Layout > Vertical", I had to choose "Reading Pane > On The Right".

![Screenshot of initial Vienna RSS Beta - Vertical layout](/images/20th/Vienna2-readingPaneRight.png)

The first [comment on Macupdate](https://vienna.macupdate.com/#comments) was published five days after the download was made available, and was:

> I've been using Vienna for a few days now, and I have to say it's the only client that comes the closest to being between NewsFire (my preferred GUI) and NetNewsWire Lite (my preferred feature set). Pluses: - Growl support - Fully customizable three-pane view - Smart folders - Flagged items - Open source and gratis Bugs: - No way to set an expiration date for headlines. They just keep accumulating, though there is a "Compact Database" option - Date sorting isn't always accurate - Takes extra clicks to mark messages read - Some feed [fav]icons displayed incorrectly What I'd like to see: - Podcast support - A bit more deafult spacing between feeds or alternating lines -- very cramped at the moment - Abitlity to open links in background - Bonjour support - Pool of included feeds (like NNWL) - More options and customization for individual feeds - More view styles - A better icon. That wavy V is fugly All in all, it's a great start. As an experiment of sorts, I removed NNWL from my dock when I installed Vienna and haven't returned to NNWL since.

The 2025 user I am would add: no integrated browser! It was added in September 2005, in version [2.0.0.2007](https://github.com/ViennaRSS/vienna-rss/blob/master/CHANGELOG.md#2002007)

## … To Liquid Glass

Let's stay above liquid elements, and let's swim from Aqua to Liquid Glass. This is how Vienna looks like when compiled and run on the developer preview of macOS Tahoe:

![Screenshot of macOS Tahoe preview running Vienna](/images/20th/macOS-Tahoe-Preview.png)

## But was there a Vienna 1 ?

All right, that was fine. But a mystery remained: why was the application named Vienna 2? Was there a Vienna 1, and if so, could July 7th 2005 still be considered as the official birthday of Vienna RSS?

I found the answer in the help files, which seemed familiar…  

![Screenshot of Help file](/images/20th/Vienna2-help.png)

… but contained some informations which differed from what we are used to.

This led me to the [archives](https://web.archive.org/web/20050206212851/http://opencommunity.co.uk/vienna.html) of the opencommunity.co.uk website provided the answer : Vienna 1 was an offline message reader for the [CIX conferencing service](https://en.wikipedia.org/wiki/CIX_(website)).

A new visit to [Sourceforge](https://cix-vienna.sourceforge.net) and an [installation](https://sourceforge.net/projects/cix-vienna/files/) confirmed that while Vienna for CIX and Vienna RSS shared some technical components, the goal of the former was really different.

![Screenshot of Vienna for CIX](/images/20th/Vienna1.png)

## Under the hood

[Github](https://github.com/ViennaRSS/vienna-rss/pulse) summarizes 20 years of involvement with the following graph:

![Histogram of line additions and deletions across the  time](/images/20th/code-frequency.png)

It's misleading. Changes in years 2011-2012 appear inflated, due to difficulties caused by migration from Subversion to Git of a code repository which was initially inited in CVS.

And even in what appears as a relatively calm period, the maintainers are busy, especially on week-ends… Cf. last 12 months:

![Weekly number of commits and means per week day](/images/20th/commits-last-12-months.png)

## Who contributed ?

Many people. I am particularly sorry being unable to give information on translators, but we can list number of commits by author, ignoring merge commits.

```shell
% git shortlog -sn --no-merges
  1716  Barijaona Ramaholimihaso
   891  Eitot
   652  stevewpalmer
   375  johnson1234
   255  mstroeck
   167  Tassilo Karge
   143  Josh
   112  Joshua Pore
    56  evands
    48  dak180
    45  Echelon9
    40  Jeff Johnson
    35  Nick Dazé
    33  Salvatore Ansani
    32  curtis-faith
    26  mteodori
    22  Jan Weiß
    20  György Tóth
    16  dkocher
     9  Barijaona Ramholimihaso
     9  Boris Dušek
     9  nielspl
     7  Andrew Herron
     7  leitinha
     6  Adam Hartford
     6  Sveinbjorn Thordarson
     4  biphuhn
     3  Dmitry Wolf
     3  Konstruktionist
     3  Matt Reagan
     3  Miguel Araújo
     3  ansani
     3  n
     3  renefk05
     2  Bavarious
     2  Jakub Stasiak
     2  Jean-Francois Moy
     2  Jesse Claven
     2  Josh Ringer
     2  Kang-min Liu
     2  Marco Zehe
     1  Adriano Marcondes Machado
     1  Ahmed Badran
     1  Andrew Hyatt
     1  Daniel Aleksandersen
     1  Daniel Cotton
     1  Devin Coughlin
     1  Emiliano Necciari
     1  Gerrit Beine
     1  Hiroaki ENDOH
     1  Making GitHub Delicious.
     1  Michael G. Ströck
     1  Neil Tiffin
     1  Nicolas Lœuillet
     1  Pete Cooper
     1  ReadmeCritic
     1  Rei Vilo
     1  Rinat
     1  Torsten Landsiedel
     1  William Bowling
     1  bavarious
     1  jfml
     1  no_author
     1  rj-p
     1  root
     1  カワリミ人形 
```
<br>
Some people appear under multiple names, and weight and complexity of different commits cannot be assessed arithmetically, but I chose to outline the role of a few people. 


### Steve Palmer

|![Icon of Vienna for CIX](/images/20th/icon1.png)|![Initial icon for Vienna RSS Beta](/images/20th/icon2-1.png)|Initial icons of Vienna for CIX and Vienna RSS|

Founding father of Vienna, Steve contributed mostly from 2004 to 2008, made a short comeback in 2010, and is definitely at the root of Vienna's ethics: making a clean, spartan, and highly useful app.

He almost never publicized his bio, but I finally found an ["About me"](https://web.archive.org/web/20041229120628/http://www.opencommunity.co.uk:80/About.html) (he was from the UK and a software developer working in the US for Microsoft Business Solutions), and some reflexions on  writing software : [part 2](https://web.archive.org/web/20051215061510/http://www.opencommunity.co.uk/blog/blog.html) and [part 1](https://web.archive.org/web/20050308113454/http://www.opencommunity.co.uk:80/makingsoftware.html).

|![First stable icon for Vienna RSS](/images/20th/icon2-2.png)| In September 2005, Vienna got a new icon by [Jasper Hauser](https://jasperhauser.nl).

### [Jeff Johnson](https://github.com/lapcat/)

I could contact him thanks to his Mastodon account [@lapcatsoftware@mastodon.social](https://mastodon.social/@lapcatsoftware):

> I give all credit to Steve Palmer, the creator of Vienna, who I believe started working on it in January 2004. Vienna was a model Mac app project, and I learned a lot from Steve's source code.

> I became a Vienna user in 2005 and continue to use it 20 years later. I had tried the various RSS readers available at the time and found Vienna best fit my requirements and workflow, which is still true. I've never seen anything better.

> I submitted my first source code patch to the Vienna project in February 2006. I was just learning Mac development, so Vienna was how I cut my teeth. For a while, before I got my first paying job as a developer, I was working on Vienna full time. Vienna actually helped me to get my first job, because my boss was also a user!

> In late 2006, Steve announced that he was stepping back from Vienna development, and I became the main developer.

> I worked on Vienna until 2010, when I announced my retirement from the project. I just didn’t have time to devote to it anymore.

### [Michael G. Ströck](https://github.com/mstroeck/)

Michael started his contributions in December 2006, with at first a focus on localization. He had for a time the crucial responsability of being the guardian of the temple. He moved the development from Sourceforge to Github: without him, the project would probably have died.

#### [Barijaona Ramaholimihaso](https://github.com/barijaona)

Mac user since 1986, I don't remember when I first encountered Vienna. After reading the [french edition](https://mac.developpez.com/cours/Xcode/become-xcoder/) of an online course titled _Become an Xcoder_, I took in 2012 a new year resolution: learning more by working on a real project.

My first satisfaction was achieving the transition to universal builds : at that time, that meant having the application run natively on both PowerPC, Intel 32 bits and Intel 64 bits.

As I was far from being confident with Apple's tools, [dak180](https://github.com/dak180) was key in starting reorganizing the on disk layout and fixing the release process.

While I was finishing the Google Reader support started by Adam Hartford and [Salvatore Ansani](https://github.com/ansani/), Google announced it would end Google Reader… That is far from being the single reason why Vienna 3 had 20 beta versions and 9 release candidate versions before being released in November 2014!

|![Current icon for Vienna RSS](/images/20th/icon2-3.png)|
A new icon authored by a forum user named @romiq and [Nick Dazé](https://github.com/nickdaze) was introduced in 2013|

### [Josh](https://github.com/josh64x2 @josh64@mastodon.social)

Joshua Pore started contributing in 2014. He was key in structuring our methodologies and remaking the website. Most importantly to me, he helped me defeat my reluctance to refactor things and to delve into Interface Builder!

He remains active, but somewhat regrets the good old times when Apple was focusing on AppKit and Objective-C.

### [Eitot](https://github.com/Eitot)

Eitot began contributing in 2017. He was the first to introduce Swift in our codebase, and is the main force behind current refactoring decisions. But he is also very attentive to details. He added the support for JSON Feed.

### [Tassilo Karge](https://github.com/Takeanice)

Tassilo began contributing in 2018. He is the main force behind the transition from old school WebView to WKWebView and the improvements to smart folders.

## What's next?

Stay tuned! You can participate in discussions [like this one](https://github.com/ViennaRSS/vienna-rss/issues/1476).

You can also follow me in Vienna, via this [RSS feed](https://mastodon.mg/@barijaona.rss) (which is not solely dedicated to Vienna).

If you have an account on the Fediverse (Mastodon, Pixelfed, …), you can react to this article by answering to this [toot](https://mastodon.mg/@barijaona/114813224912670424).




