---
title: Mastering the EP_GET_MASK Command in EmEditor for Efficient Text Editing
date: 2024-10-22T08:09:35.038Z
updated: 2024-10-29T03:46:29.572Z
tags:
  - product
categories:
  - emeditor
thumbnail: https://thmb.techidaily.com/720039bdcfeba97eefefa9824f21f9715183b78c763bbf782b71c474fcdd45b6.jpg
---

## Mastering the EP_GET_MASK Command in EmEditor for Efficient Text Editing

Viewing 3 posts - 1 through 3 (of 3 total)

* Author  
Posts
* January 7, 2010 at 9:45 am [#8026](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/ebe87191575d8a3f3b1fb12210cba2f0?s=80&d=identicon&r=g)CaptainFlint](https://www.emeditor.com/forums/users/captainflint/ "View CaptainFlint's profile")  
Participant  
In developing a plugin I met a problem with the toolbar icon. I followed the instructions in the help file and for 256-color icons I decided to make RGB(1, 1, 1) a transparent color. So, I designed an icon with 4 pixels in corners with this color (to make it look a bit rounded), and in the code I wrote:  
case EP_GET_MASK:  
		if  ((wParam & BITMAP_COLOR_MASK) == BITMAP_24BIT_COLOR)  
			lResult = CLR_NONE;  
		else if ((wParam & BITMAP_COLOR_MASK) == BITMAP_256_COLOR)  
			lResult = RGB(1, 1, 1);  
		break;  
 However, when I try the plugin in 256-color mode, its toolbar icon becomes garbled. Here is the screenshot of how the icon looks as itself and when shown by EmEditor:  
 EE 9.07; OS Vista Business SP2 x32 working in true-color mode.  
    
 I performed some more experiments and found the following:  
 1\. If I return CLR\_NONE instead of RGB(…), the color with index 0 from the image’s index table is used for transparency.  
 2\. The problem seems to lie in fact that my transparent color has index 0\. When I move it further in the index table, the problem seems to be gone.  
 The questions are: what are the “official” recommendations on creating transparent images, and why is all this not described in the help?  
January 7, 2010 at 6:17 pm [#8033](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
I think the issue is the color palette with 256-color mode. Even if your plug-in bitmap looks fine by itself, it becomes ugly with other plug-ins because the color palette must be adjusted with other bitmaps. For this reason, I would recommend you not adding 256-color bitmaps. Just use true-color bitmaps and 16-color bitmaps, and omit 256-color bitmaps. In most of my standard plug-ins, I don’t supply 256-color bitmaps any more for this reason. Most PCs now display true color, and 256-color mode is becoming obsolete. The 256-color mode feature might be taken out in the future.  
January 10, 2010 at 11:25 pm [#8040](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/ebe87191575d8a3f3b1fb12210cba2f0?s=80&d=identicon&r=g)CaptainFlint](https://www.emeditor.com/forums/users/captainflint/ "View CaptainFlint's profile")  
Participant  
I see, I’ll keep that in mind.  
 But even if the problem is in adjusting color palette, why simple repositioning of the transparent color fixes the problem completely? I don’t change the color itself, I don’t change colors of other pixels, I just move one color in the index table, and that’s all.  
 PS: Since I found how to eliminate the problem on the plugin’s side, it no longer bothers me as itself, but I’m concerned about possible bug in EmEditor which caused such strange behaviour.
* Author  
Posts

Viewing 3 posts - 1 through 3 (of 3 total)

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
<li><a href="https://fox-direct.techidaily.com/new-expert-techniques-for-capturing-minute-details-on-video-for-2024/"><u>[New] Expert Techniques for Capturing Minute Details on Video for 2024</u></a></li>
<li><a href="https://visual-screen-recording.techidaily.com/new-leading-tech-in-snap-capture-for-2024/"><u>[New] Leading Tech in Snap Capture for 2024</u></a></li>
<li><a href="https://eaxpv-info.techidaily.com/updated-2024-approved-elite-10-volume-augmenters-for-all-os/"><u>[Updated] 2024 Approved Elite 10 Volume Augmenters for All OS</u></a></li>
<li><a href="https://android-location.techidaily.com/3-effective-methods-to-fake-gps-location-on-android-for-your-infinix-hot-40-drfone-by-drfone-virtual/"><u>3 Effective Methods to Fake GPS location on Android For your Infinix Hot 40 | Dr.fone</u></a></li>
<li><a href="https://win-hacks.techidaily.com/best-iphone-data-retrieval-apps-for-pcmac-enthusiasts-a-comprehensive-guide/"><u>Best iPhone Data Retrieval Apps for PC/Mac Enthusiasts: A Comprehensive Guide</u></a></li>
<li><a href="https://blog-min.techidaily.com/diy-iphone-7-plus-ringtones-made-easy-a-comprehensive-tutorial/"><u>DIY iPhone 7 Plus Ringtones Made Easy – A Comprehensive Tutorial</u></a></li>
<li><a href="https://win-hacks.techidaily.com/foto-wiederherstellung-auf-einem-windows-11-pc-schritt-fur-schritt-anleitung/"><u>Foto-Wiederherstellung Auf Einem Windows 11 PC: Schritt-Für-Schritt-Anleitung</u></a></li>
<li><a href="https://win-hacks.techidaily.com/guide-pour-transferer-des-donnees-dun-disque-dur-a-un-ssd-par-commandes/"><u>Guide Pour Transférer Des Données D'un Disque Dur À Un SSD Par COMMANDES</u></a></li>
<li><a href="https://win-hacks.techidaily.com/how-to-restore-files-accidentally-emptied-into-trash-bin-a-quick-3-step-guide/"><u>How To Restore Files Accidentally Emptied Into Trash Bin - A Quick 3-Step Guide</u></a></li>
<li><a href="https://vp-tips.techidaily.com/in-2024-syncing-soundscapes-with-visuals-in-film-teasers/"><u>In 2024, Syncing Soundscapes with Visuals in Film Teasers</u></a></li>
<li><a href="https://tech-hub.techidaily.com/preserving-confidential-communications-how-to-securely-integrate-chatgpt-into-your-work-operations/"><u>Preserving Confidential Communications: How to Securely Integrate ChatGPT Into Your Work Operations</u></a></li>
<li><a href="https://win-hacks.techidaily.com/quick-start-guide-seamless-file-migration-between-synology-nas-and-computer-systems/"><u>Quick-Start Guide: Seamless File Migration Between Synology NAS and Computer Systems</u></a></li>
<li><a href="https://win-hacks.techidaily.com/step-by-step-tutorial-on-recovering-graphics-cards-post-driver-updates-mytechsavvy/"><u>Step-by-Step Tutorial on Recovering Graphics Cards Post Driver Updates - MyTechSavvy</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2027181/19272" target="_top" id="2027181">
  <img src="//a.impactradius-go.com/display-ad/19272-2027181" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2027181/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

