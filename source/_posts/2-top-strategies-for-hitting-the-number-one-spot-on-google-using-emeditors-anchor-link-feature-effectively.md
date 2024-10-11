---
title: "2. Top Strategies for Hitting the Number One Spot on Google: Using EmEditor's Anchor Link Feature Effectively"
date: 2024-10-07T16:13:05.899Z
updated: 2024-10-11T16:45:38.990Z
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
<li><a href="https://screen-recording.techidaily.com/new-2024-approved-top-10-best-webcam-covers-and-stickers/"><u>[New] 2024 Approved Top 10 Best Webcam Covers & Stickers</u></a></li>
<li><a href="https://facebook-clips.techidaily.com/updated-2024-approved-how-to-captivate-viewers-using-multiple-perspectives-on-fb-live/"><u>[Updated] 2024 Approved How to Captivate Viewers Using Multiple Perspectives on FB Live</u></a></li>
<li><a href="https://article-posts.techidaily.com/1718098795886-updated-how-much-will-it-cost-to-shoot-a-music-video/"><u>[Updated] How Much Will It Cost To Shoot A Music Video?</u></a></li>
<li><a href="https://win-hacks.techidaily.com/ai-demonstration-by-microsoft-embracing-the-loneliness-with-intelligent-technology-insights-from-zdnet/"><u>AI Demonstration by Microsoft: Embracing the Loneliness with Intelligent Technology - Insights From ZDNet</u></a></li>
<li><a href="https://tiktok-videos.techidaily.com/amplify-your-tiktok-content-with-current-trends-for-2024/"><u>Amplify Your TikTok Content with Current Trends for 2024</u></a></li>
<li><a href="https://win-hacks.techidaily.com/are-unsupported-devices-being-excluded-from-windows-11-update-rollouts-by-microsoft-techcrunch/"><u>Are Unsupported Devices Being Excluded From Windows 11 Update Rollouts by Microsoft? | TechCrunch</u></a></li>
<li><a href="https://win11.techidaily.com/breaking-barriers-windows-11-on-outdated-devices/"><u>Breaking Barriers: Windows 11 on Outdated Devices</u></a></li>
<li><a href="https://win-hacks.techidaily.com/expert-analysis-on-2024s-market-leaders-how-apple-dell-and-competitors-stack-up-reviewed-by-zdnet/"><u>Expert Analysis on 2024'S Market Leaders: How Apple, Dell, and Competitors Stack Up | Reviewed by ZDNET</u></a></li>
<li><a href="https://win-hacks.techidaily.com/explore-whats-new-with-windows-11-fresh-innovations-and-updates-unveiled-digital-trends/"><u>Explore What's New with Windows 11: Fresh Innovations and Updates Unveiled | Digital Trends</u></a></li>
<li><a href="https://win-hacks.techidaily.com/get-ready-microsofts-security-focused-copilot-hits-general-release-on-april-1-says-zdnet/"><u>Get Ready: Microsoft's Security-Focused Copilot Hits General Release on April 1, Says ZDNET</u></a></li>
<li><a href="https://review-topics.techidaily.com/in-2024-full-guide-to-fix-itoolab-anygo-not-working-on-vivo-g2-drfone-by-drfone-virtual-android/"><u>In 2024, Full Guide to Fix iToolab AnyGO Not Working On Vivo G2 | Dr.fone</u></a></li>
<li><a href="https://android-transfer.techidaily.com/in-2024-how-to-transfer-contacts-from-infinix-smart-8-pro-to-outlook-drfone-by-drfone-transfer-from-android-transfer-from-android/"><u>In 2024, How to Transfer Contacts from Infinix Smart 8 Pro to Outlook | Dr.fone</u></a></li>
<li><a href="https://win-hacks.techidaily.com/revolutionizing-microsofts-platform-exclusive-windows-on-arm-apps-unveiled-industry-watchers/"><u>Revolutionizing Microsoft's Platform: Exclusive Windows on Arm Apps Unveiled | Industry Watchers</u></a></li>
<li><a href="https://win-hacks.techidaily.com/top-choice-mom-appreciation-card-selections-ideal-for-mothers-day/"><u>Top Choice Mom Appreciation Card Selections - Ideal for Mother's Day</u></a></li>
<li><a href="https://buynow-reviews.techidaily.com/value-packed-review-why-the-microsoft-sculpt-ergonomic-keyboard-is-worth-every-penny/"><u>Value-Packed Review: Why the Microsoft Sculpt Ergonomic Keyboard Is Worth Every Penny</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2130875/7443" target="_top" id="2130875">
  <img src="//a.impactradius-go.com/display-ad/7443-2130875" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2130875/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

