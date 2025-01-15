---
title: Mastering the EP_GET_MASK Command in EmEditor for Efficient Text Editing
date: 2025-01-08T02:54:50.999Z
updated: 2025-01-15T02:37:02.481Z
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
<li><a href="https://vimeo-videos.techidaily.com/new-crafting-an-auditory-ambiance-for-your-vimeo-video-pieces-for-2024/"><u>[New] Crafting an Auditory Ambiance for Your Vimeo Video Pieces for 2024</u></a></li>
<li><a href="https://some-skills.techidaily.com/new-the-blueprint-of-an-engaging-podcast-blurb/"><u>[New] The Blueprint of an Engaging Podcast Blurb</u></a></li>
<li><a href="https://instagram-clips.techidaily.com/updated-2024-approved-mastering-instagram-incorporating-music-in-videos-and-stories/"><u>[Updated] 2024 Approved Mastering Instagram Incorporating Music in Videos & Stories</u></a></li>
<li><a href="https://twitter-clips.techidaily.com/2024-approved-saving-the-fun-downloading-tweets-gif-content-easily/"><u>2024 Approved Saving the Fun Downloading Tweets' GIF Content Easily</u></a></li>
<li><a href="https://location-fake.techidaily.com/3-ways-to-fake-gps-without-root-on-apple-iphone-15-pro-max-drfone-by-drfone-virtual-ios/"><u>3 Ways to Fake GPS Without Root On Apple iPhone 15 Pro Max | Dr.fone</u></a></li>
<li><a href="https://mondly-stories.techidaily.com/1719579707441-accelerate-latvian-skills-10-minutes-per-day-maximum-effort/"><u>Accelerate Latvian Skills - 10 Minutes Per Day, Maximum Effort!</u></a></li>
<li><a href="https://win-hacks.techidaily.com/aomei-backupperoscpu/"><u>AOMEI Backupperソフトウェアに必要なOSとCPU要件 - 効率的バックアップ作成のためのガイド</u></a></li>
<li><a href="https://fox-making.techidaily.com/enhance-cpu-speeds-with-expert-advice-from-yl-software/"><u>Enhance CPU Speeds with Expert Advice From YL Software</u></a></li>
<li><a href="https://win-hacks.techidaily.com/how-to-duplicate-your-windows-10-boot-drive-on-an-ssd-two-effective-methods/"><u>How To Duplicate Your Windows 10 Boot Drive On an SSD - Two Effective Methods</u></a></li>
<li><a href="https://data-safeguard.techidaily.com/mastering-secure-deletion-invaluable-articles-and-best-practices-compiled-by-stellars-experts/"><u>Mastering Secure Deletion: Invaluable Articles & Best Practices Compiled by Stellar's Experts</u></a></li>
<li><a href="https://win-hacks.techidaily.com/passaggio-ottimale-di-windows-nella-tua-ssd-minima-strategie-e-consigli/"><u>Passaggio Ottimale Di Windows Nella Tua SSD Minima: Strategie E Consigli</u></a></li>
<li><a href="https://win-hacks.techidaily.com/seamless-transition-upgrading-from-windows/"><u>Seamless Transition: Upgrading From Windows</u></a></li>
<li><a href="https://win-hacks.techidaily.com/wie-man-musikspiele-erfolgreich-von-itunes-und-apple-music-auf-eine-disk-brennt/"><u>Wie Man Musikspiele Erfolgreich Von iTunes Und Apple Music Auf Eine Disk Brennt</u></a></li>
<li><a href="https://graphic-issues.techidaily.com/windows-11-new-level-of-display-customization-released/"><u>Windows 11: New Level of Display Customization Released</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/FLO5dwmJAVs?si=1OYH8rv8aPaMsCiU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

