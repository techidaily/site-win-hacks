---
title: "2. Top Strategies for Hitting the Number One Spot on Google: Using EmEditor's Anchor Link Feature Effectively"
date: 2024-10-17T17:52:54.212Z
updated: 2024-10-23T07:15:18.662Z
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
<li><a href="https://article-helps.techidaily.com/new-in-2024-essential-tips-for-photosvideos-in-windows-10/"><u>[New] In 2024, Essential Tips for Photos/Videos in Windows 10</u></a></li>
<li><a href="https://win-hacks.techidaily.com/1728499815611-seagate/"><u>重新開機後，Seagate外置硬碟無法打開文件？解決之道有四：一步一步指南</u></a></li>
<li><a href="https://win-hacks.techidaily.com/aktiviere-dein-iphone-mit-diesen-8-einfachen-schritten-wenn-es-nicht-aktivierbar-scheint/"><u>Aktiviere Dein iPhone Mit Diesen 8 Einfachen Schritten, Wenn Es Nicht Aktivierbar Scheint</u></a></li>
<li><a href="https://win-hacks.techidaily.com/automatische-loschfunktion-in-outlook-deaktivieren-eine-detaillierte-losungskompass/"><u>Automatische Löschfunktion in Outlook Deaktivieren - Eine Detaillierte Lösungskompass</u></a></li>
<li><a href="https://change-location.techidaily.com/how-can-i-catch-the-regional-pokemon-without-traveling-on-vivo-v29-pro-drfone-by-drfone-virtual-android/"><u>How Can I Catch the Regional Pokémon without Traveling On Vivo V29 Pro | Dr.fone</u></a></li>
<li><a href="https://blog-min.techidaily.com/how-to-identify-some-outdated-drivers-with-windows-device-manager-on-windows-1110-by-drivereasy-guide/"><u>How to identify some outdated drivers with Windows Device Manager on Windows 11/10</u></a></li>
<li><a href="https://unlock-android.techidaily.com/how-to-unlock-infinix-zero-5g-2023-turbo-phone-pattern-lock-without-factory-reset-by-drfone-android/"><u>How to Unlock Infinix Zero 5G 2023 Turbo Phone Pattern Lock without Factory Reset</u></a></li>
<li><a href="https://bypass-frp.techidaily.com/in-2024-a-step-by-step-guide-on-using-adb-and-fastboot-to-remove-frp-lock-on-your-honor-play-40c-by-drfone-android/"><u>In 2024, A Step-by-Step Guide on Using ADB and Fastboot to Remove FRP Lock on your Honor Play 40C</u></a></li>
<li><a href="https://win-bytes.techidaily.com/mastering-pc-game-recording-a-comprehensive-tutorial-using-movavi-software/"><u>Mastering PC Game Recording: A Comprehensive Tutorial Using Movavi Software</u></a></li>
<li><a href="https://visual-screen-recording.techidaily.com/streamlining-the-demo-process-in-adobe-captivate-for-2024/"><u>Streamlining the Demo Process in Adobe Captivate for 2024</u></a></li>
<li><a href="https://win-hacks.techidaily.com/troubleshooting-fixed-correcting-authentication-issues-after-vmware-vcenter-update/"><u>Troubleshooting Fixed: Correcting Authentication Issues After VMware vCenter Update</u></a></li>
<li><a href="https://win-great.techidaily.com/uefi-secure-bootwindows-11/"><u>UEFI Secure Bootを使って、システムを安全にWindows 11更新する方法</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://unicoeye.pxf.io/c/5597632/2134240/18498" target="_top" id="2134240">
  <img src="//a.impactradius-go.com/display-ad/18498-2134240" border="0" alt="https://techidaily.com" width="540" height="90"/>
</a>
<img height="0" width="0" src="https://unicoeye.pxf.io/i/5597632/2134240/18498" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

