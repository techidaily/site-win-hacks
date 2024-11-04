---
title: "2. Top Strategies for Hitting the Number One Spot on Google: Using EmEditor's Anchor Link Feature Effectively"
date: 2024-10-31T21:32:04.771Z
updated: 2024-11-04T00:45:35.161Z
tags:
  - product
categories:
  - emeditor
thumbnail: https://thmb.techidaily.com/4d13682289fd093707f3e488098e8b68b405e6325695bb2b5c751424b8cb1104.jpeg
---

## 2. Top Strategies for Hitting the Number One Spot on Google: Using EmEditor's Anchor Link Feature Effectively

Viewing 6 posts - 1 through 6 (of 6 total)

* Author  
Posts
* April 5, 2011 at 5:53 pm [#9328](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/e4b3430962364a05c69af317cc2183cf?s=80&d=identicon&r=g)QiaoJiao](https://www.emeditor.com/forums/users/QiaoJiao/ "View QiaoJiao's profile")  
Participant  
Is there any possibilities to jump to specific search result in a given file?  
 For example:  
file://C:something.txt (s:1part) — clicking here will go to C:something.txt file and jump to first “1part” search result.  
 Or just (s:1part) – will jump to “1part” search result in this file.  
 Is it possible now? If not, it will be good in future versions. Just a kind of html’s anchors #gohere.  
April 6, 2011 at 4:20 am [#9331](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
No, it is not possible. I think you will need to write a macro for this purpose.  
April 7, 2011 at 5:33 am [#9333](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/e4b3430962364a05c69af317cc2183cf?s=80&d=identicon&r=g)QiaoJiao](https://www.emeditor.com/forums/users/QiaoJiao/ "View QiaoJiao's profile")  
Participant  
Yutaka, thank you for replaying.  
 I know how implement search in macros, but is it possible to do text clickable, so that it starts macros and passed file name and string for search to it?  
 We can do file://C:something.txt to go here. Is it possible to add something besides “file:” and adjust it for your own needs?  
 For example, using regexp to make search://C:something.txt(search this), so that “C:something.txt” and “search this” passed to macros and it will go to a file and search it.  
 I just want to now is it possible at all, because now I can not see a way to do it by macros.  
April 7, 2011 at 4:22 pm [#9334](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
Hi QiaoJiao,  
 No, I don’t think it is possible to parse the clickable text to macros.  
April 8, 2011 at 6:24 pm [#9335](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/e4b3430962364a05c69af317cc2183cf?s=80&d=identicon&r=g)QiaoJiao](https://www.emeditor.com/forums/users/QiaoJiao/ "View QiaoJiao's profile")  
Participant  
I think there is a way to do it by passing parameters to emeditor.exe like  
 file://C:emeditoremeditor.exe–open/c:file.txt–macros/c:macros.jsee–macros\_param/search\_for=search\\%20this&action=goto\_firstresult  
 But I agree that this is weird and have problems.  
 Still, it is interesting problem to solve.  
 I like connecting my text files. Links are a power.  
April 8, 2011 at 6:54 pm [#9336](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/e4b3430962364a05c69af317cc2183cf?s=80&d=identicon&r=g)QiaoJiao](https://www.emeditor.com/forums/users/QiaoJiao/ "View QiaoJiao's profile")  
Participant  
I Found solution!  
 1 Check “clicking url select whole string”  
 2 file://c:something.txt-s:search\_this — click it  
 3 launch macros (binded), that will get and parse selected text. It will open new file with given path and search and goto first match for -s parameter.  
 Only one additional step – launch script. Not a big deal.  
 Now it is all about macros possibilities, no core hacking.  
 But I still think it would be great if it will be possible to make regexp text clickable and bind it to macros. file: and http: works well and they are not special.
* Author  
Posts

Viewing 6 posts - 1 through 6 (of 6 total)

* You must be logged in to reply to this topic.

<ins class="adsbygoogle"
     style="display:block"
     data-ad-format="autorelaxed"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="1223367746"></ins>

<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="8358498916"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>

<span class="atpl-alsoreadstyle">Also read:</span>
<div><ul>
<li><a href="https://youtube-lab.techidaily.com/024-approved-unlock-youtubes-small-screen-image-magic/"><u>[New] 2024 Approved Unlock YouTube's Small Screen Image Magic</u></a></li>
<li><a href="https://win-hacks.techidaily.com/activate-windows-1110-offline-file-feature-three-effective-methods/"><u>Activate Windows 11/10 Offline File Feature: Three Effective Methods</u></a></li>
<li><a href="https://win-howtos.techidaily.com/addressing-missing-xinput13dll-for-smooth-performance/"><u>Addressing Missing XINPUT1_3.dll for Smooth Performance</u></a></li>
<li><a href="https://win-hacks.techidaily.com/comprehensive-guide-on-retrieving-lost-data-volumes-across-windows-operating-systems-11-10-8-and-cuisine-7/"><u>Comprehensive Guide on Retrieving Lost Data Volumes Across Windows Operating Systems (11, 10, 8 & Cuisine 7)</u></a></li>
<li><a href="https://win-hacks.techidaily.com/guide-de-configuration-du-sysreq-dans-lapplication-de-sauvegarde-centralisee-daomei/"><u>Guide De Configuration Du SysReq Dans L'Application De Sauvegarde Centralisée D’AOMEI</u></a></li>
<li><a href="https://some-techniques.techidaily.com/in-2024-grasping-the-nuances-in-youtube-viewer-reactions/"><u>In 2024, Grasping the Nuances in YouTube Viewer Reactions</u></a></li>
<li><a href="https://review-topics.techidaily.com/in-2024-how-to-fake-gps-on-vivo-y200e-5g-for-mobile-legends-drfone-by-drfone-virtual-android/"><u>In 2024, How To Fake GPS On Vivo Y200e 5G For Mobile Legends? | Dr.fone</u></a></li>
<li><a href="https://extra-guidance.techidaily.com/in-2024-simulate-hand-held-camera-effects-in-photoshop/"><u>In 2024, Simulate Hand-Held Camera Effects in Photoshop</u></a></li>
<li><a href="https://technical-tips.techidaily.com/ipad-pro-vs-macbook-air-showdown-determining-your-perfect-companion-for-work-and-play-digitalinsight/"><u>IPad Pro vs MacBook Air Showdown: Determining Your Perfect Companion for Work and Play | DigitalInsight</u></a></li>
<li><a href="https://win-hacks.techidaily.com/passaggio-ottimale-di-windows-nella-tua-ssd-minima-strategie-e-consigli/"><u>Passaggio Ottimale Di Windows Nella Tua SSD Minima: Strategie E Consigli</u></a></li>
<li><a href="https://win-hacks.techidaily.com/professionelle-strategien-zur-installation-von-windows-prise-on-ssd-erfolgreiche-tipps-und-tricks-fur-die-besten-methoden/"><u>Professionelle Strategien Zur Installation Von Windows Prise on SSD: Erfolgreiche Tipps Und Tricks Für Die Besten Methoden</u></a></li>
<li><a href="https://techidaily.com/recover-apple-iphone-7-plus-data-from-ios-icloud-drfone-by-drfone-ios-data-recovery-ios-data-recovery/"><u>Recover Apple iPhone 7 Plus Data From iOS iCloud | Dr.fone</u></a></li>
<li><a href="https://extra-skills.techidaily.com/step-by-step-techniques-building-animation-with-movie-maker-for-2024/"><u>Step-by-Step Techniques Building Animation with Movie Maker for 2024</u></a></li>
<li><a href="https://common-error.techidaily.com/valorant-screen-flickering-solutions-optimize-your-gameplay/"><u>Valorant Screen Flickering Solutions: Optimize Your Gameplay!</u></a></li>
<li><a href="https://win-hacks.techidaily.com/wie-man-musikspiele-erfolgreich-von-itunes-und-apple-music-auf-eine-disk-brennt/"><u>Wie Man Musikspiele Erfolgreich Von iTunes Und Apple Music Auf Eine Disk Brennt</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2144280/7443" target="_top" id="2144280">
  <img src="//a.impactradius-go.com/display-ad/7443-2144280" border="0" alt="https://techidaily.com" width="600" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2144280/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

