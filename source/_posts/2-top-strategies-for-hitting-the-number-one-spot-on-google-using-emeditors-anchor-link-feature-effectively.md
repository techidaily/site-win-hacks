---
title: "2. Top Strategies for Hitting the Number One Spot on Google: Using EmEditor's Anchor Link Feature Effectively"
date: 2024-10-14T16:00:43.543Z
updated: 2024-10-17T17:01:13.858Z
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
<li><a href="https://youtube-webster.techidaily.com/ed-2024-approved-your-iphones-mp3-fix-6-free-tools-to-convert-youtube-audio/"><u>[Updated] 2024 Approved Your iPhone's MP3 Fix 6 Free Tools to Convert YouTube Audio</u></a></li>
<li><a href="https://fox-links.techidaily.com/updated-installation-masterclass-transitioning-to-macos-sierra/"><u>[Updated] Installation Masterclass Transitioning to macOS Sierra</u></a></li>
<li><a href="https://video-screen-grab.techidaily.com/2024-approved-discover-the-evolution-of-video-technology-with-mycams-review/"><u>2024 Approved Discover the Evolution of Video Technology with MyCam's Review</u></a></li>
<li><a href="https://extra-lessons.techidaily.com/actionable-techniques-for-efficient-media-conversion-chains/"><u>Actionable Techniques for Efficient Media Conversion Chains</u></a></li>
<li><a href="https://win-hacks.techidaily.com/comment-accelerer-votre-ordinateur-avec-windows-11-guerisons-efficaces-pour-une-experience-plus-fluide-en-7-etapes/"><u>Comment Accélérer Votre Ordinateur Avec Windows 11 ? - Guérisons Efficaces Pour Une Expérience Plus Fluide en 7 Étapes!</u></a></li>
<li><a href="https://discover-exceptional.techidaily.com/easy-steps-to-enable-wmv-video-support-on-ios-devices/"><u>Easy Steps to Enable WMV Video Support on iOS Devices</u></a></li>
<li><a href="https://win-hacks.techidaily.com/expert-tips-for-enhancing-performance-how-to-swap-out-the-ssd-in-your-hp-spectre-x360/"><u>Expert Tips for Enhancing Performance: How to Swap Out the SSD in Your HP Spectre X360</u></a></li>
<li><a href="https://win-hacks.techidaily.com/get-started-with-cloudbacko-your-new-solution-for-google-drive-management/"><u>Get Started with CloudBacko: Your New Solution for Google Drive Management</u></a></li>
<li><a href="https://win-hacks.techidaily.com/how-to-resolve-windows-11-backup-tool-failures-effectively/"><u>How to Resolve Windows 11 Backup Tool Failures Effectively</u></a></li>
<li><a href="https://win-hacks.techidaily.com/restore-whats-gone-forever-explore-these-7-techniques-for-recovering-deleted-files-in-windows-11/"><u>Restore What's Gone Forever? Explore These 7 Techniques for Recovering Deleted Files in Windows 11</u></a></li>
<li><a href="https://activate-lock.techidaily.com/the-10-best-tools-to-bypass-icloud-activation-lock-from-iphone-6-you-should-try-out-by-drfone-ios/"><u>The 10 Best Tools to Bypass iCloud Activation Lock From iPhone 6 You Should Try Out</u></a></li>
<li><a href="https://howto.techidaily.com/why-your-xiaomi-redmi-12-5g-screen-might-be-unresponsive-and-how-to-fix-it-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Why Your Xiaomi Redmi 12 5G Screen Might be Unresponsive and How to Fix It | Dr.fone</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2036467/19272" target="_top" id="2036467">
  <img src="//a.impactradius-go.com/display-ad/19272-2036467" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2036467/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

