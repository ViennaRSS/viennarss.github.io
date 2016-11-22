---
layout: page
status: publish
published: true
title: Development
author:
date: '2010-01-08 21:25:14 +1100'
categories:
---

The source code for Vienna lives at [GitHub](https://github.com/viennarss). This section is intended to help you get started with downloading and building Vienna on your own machine. See the [Vienna GitHub Page](https://github.com/viennarss/vienna-rss) to quickly browse the Vienna sources. The rest of this page explains how to download the source to your machine.

<script src="https://www.openhub.net/p/vienna-rss/widgets/project_factoids?format=js"></script>

## Getting the Source
If you are already familiar with open source development for Mac OS X, <a href="https://github.com/viennarss/vienna-rss">browse the source</a> or just <a href="http://help.github.com/fork-a-repo/">fork</a> our <a href="https://github.com/viennarss/vienna-rss">Git repository</a> and get started.

## What You Need
To build Vienna, you will need:

* macOS 10.12 (Sierra) and [Xcode 8.1](https://developer.apple.com/xcode/).
* An [up-to-date Git client](http://git-scm.com/) and basic knowledge about using Git. GitHub provides a free GUI client that works quite well: [GitHub Desktop](https://desktop.github.com/)

To make modifications to the Vienna source code, you will need a working knowledge of Objective-C and the Cocoa framework. See the [Apple Developer's Web Site](https://developer.apple.com) for more information on Xcode, Objective-C and Cocoa.

##	Getting Started
The Vienna source code has to be be *checked out* (or *cloned*, in Git terms) to a folder whose path does **not** contain spaces. This is a limitation of the project file that will likely be fixed in the future but, for now, make sure the full path to the Vienna source folder does not have any spaces in it.

The trunk contains the current development version and all changes should be contributed to it.

GitHub makes contributing changes easy:

* Ideally, you should create an account at GitHub.
* Then, simply [fork](https://help.github.com/articles/fork-a-repo/) our main repository: [vienna-rss](https://github.com/viennarss/vienna-rss)
* Clone the repository to your local development machine.
* Get coding, and send us a [pull request](https://help.github.com/articles/creating-a-pull-request-from-a-fork/) from your GitHub repository when your patch is ready.

## Contributing Changes
We welcome improvements and bug fixes to the Vienna source code. While you are free as per the terms of the [Apache 2.0 license](http://www.apache.org/licenses/LICENSE-2.0.html) to reuse parts of the Vienna code in your own project, please consider contributing any improvements in Vienna itself back to us so we can review and add to the main source tree.

If you are looking for ideas to work on, please see the [GitHub issues page](https://github.com/ViennaRSS/vienna-rss/issues) for bugs that need fixing or the file TODO in Vienna's source code folder for features that have been requested. Please let us know what you are working on by posting a note in the [Vienna Development Forum](http://forums.cocoaforge.com/viewforum.php?f=18). Feel free as well to post any questions or comments you may have about Vienna development. We're happy to help, and we encourage developers to join the Vienna project.

## Documentation
Vienna's source-code is very well documented. Read the (many, many...) comments and use the debugger to work out which functions do what. If the code becomes large enough then we might write a high level architecture overview but right now the source code is documentation enough. If you are contributing changes, please ensure you follow the coding style used by the rest of the code. That means - function header style, nesting, spacing between keywords, etc. Consistency is important here.

## Development-related Discussion
Vienna development is discussed in the [Developer Forum](https://forums.cocoaforge.com/viewforum.php?f=18) on CocoaForge or on GitHub.

## Coding Guidelines
We don't accept patches ([pull requests](https://help.github.com/articles/creating-a-pull-request-from-a-fork/), in Git lingo) unconditionally. While the license for Vienna permits you to make your own changes and redistribute them as you see fit, we have our own quality bar for changes that are submitted to the official build so please take a moment to read the below before you start making changes.

* Source code style is crucial. For Objective-C code, please try to follow the [Spotify Objective-C Coding Style](https://github.com/spotify/ios-style) and for Swift code, please try to follow the [GitHub Swift Style Guide](https://github.com/github/swift-style-guide).
* If you want to pick something from the wish-list to implement then let us know first so we can mark it as "in progress" and avoid duplicate effort.
* UI changes have a high bar and we recommend you discuss your idea with us first before going ahead and implementing.
* Non-UI changes don't have such a high bar so if you have a patch or a nifty idea, feel free to code it up and send us a pull request.
* We review all pull requests before we accept them. For small bugs we'll probably make any fixes ourselves. Larger problems get bounced back for correction.

## Localisation
We welcome volunteers who are willing to contribute by localizing Vienna into other languages. The below table shows the current languages into which Vienna is already localized:

* English
* Swedish
* French
* Italian
* German
* Dutch
* Traditional Chinese
* Spanish
* Japanese
* Korean
* Brazilian Portuguese
* Simplified Chinese
* Danish
* Czech
* Euskara (Basque)
* Russian
* Ukrainian

Additional languages planned for which volunteers are needed:

* Arabic
* Polish
* Portuguese
* Hebrew

If you wish to volunteer to localise Vienna for any of the above languages, please [create a new issue on GitHub](https://github.com/ViennaRSS/vienna-rss/issues/new), or contact us at the [Developer Forum](https://forums.cocoaforge.com/viewforum.php?f=18).

## Tools
To create localised versions of Vienna, you will need the same tools that are required to build Vienna. If you would prefer to work outside of Subversion, then an alternative approach is to copy the English.lproj file from the most recent build of Vienna and work on that.

Apple provides [tools on its web site](https://developer.apple.com/internationalization/) that may help you with your efforts. Note that we don't mandate the use of any specific tools. It is up to you to use whatever you find works best for you.

You will need a git client as mentioned above to download the source code and obtain the latest UI changes in the English.lproj folder for localisation.

