---
layout: post
title: 'Vienna syncs with FreshRSS'
author:
  display_name: barijaona
categories:
- News
---
Since Vienna 3, which introduced the ability to sync with a cloud based aggregator (à la Google Reader), Vienna developers team got requests to add support for many open source applications : Tiny RSS / Newsblur / ownCloud News…

Unfortunately, due to limited time, we were unable to satisfy these requests. We could only point to [FeedHQ](https://github.com/feedhq/feedhq) as a possible alternative for people wanting to have their own sync server. But FeedHQ’s technical requirements are slightly higher than what is most commonly provided by hosting companies.

I am therefore very happy to announce Vienna’s compatibility with [FreshRSS](https://freshrss.org) (version 1.13.0 and later).

FreshRSS is a free, self-hostable aggregator which just requires PHP/MySQL.

Special thanks to Alexandre Lapetite for his cooperation, and to Bish Erbas for testing.