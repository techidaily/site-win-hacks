---
title: Mastering the EP_GET_MASK Command in EmEditor for Efficient Text Editing
date: 2024-12-05T11:23:54.039Z
updated: 2024-12-08T20:20:51.676Z
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
<li><a href="https://solve-helper.techidaily.com/movavi-aacmov/"><u>「Movaviで簡単! オンライン無料AAC形式へのMOVファイル変換」</u></a></li>
<li><a href="https://blog-min.techidaily.com/pof-movavi/"><u>線上無成本的POF翻譯 - 利用Movavi解決方案</u></a></li>
<li><a href="https://techno-recovery.techidaily.com/apple-watch-wont-sync-here-are-6-effective-fixes-to-try/"><u>Apple Watch Won't Sync? Here Are 6 Effective Fixes to Try</u></a></li>
<li><a href="https://extra-resources.techidaily.com/artful-stop-motion-animation-the-best-15-films-for-2024/"><u>Artful Stop-Motion Animation - The Best 15 Films for 2024</u></a></li>
<li><a href="https://win-hacks.techidaily.com/dive-into-digital-anatomy-exploring-key-computer-parts-through-yl-software-lens/"><u>Dive Into Digital Anatomy: Exploring Key Computer Parts Through YL Software Lens</u></a></li>
<li><a href="https://win-hacks.techidaily.com/effective-techniques-to-fix-issues-with-your-usb-drivers-guided-by-the-experts-at-yl-software/"><u>Effective Techniques to Fix Issues with Your USB Drivers, Guided by the Experts at YL Software</u></a></li>
<li><a href="https://facebook.techidaily.com/facebooks-bold-step-into-the-clubhouse-arena-with-audio-features/"><u>Facebook's Bold Step Into the Clubhouse Arena with Audio Features</u></a></li>
<li><a href="https://fox-glue.techidaily.com/highly-recommended-auto-cameras-for-vehicle-tracking-for-2024/"><u>Highly Recommended Auto Cameras for Vehicle Tracking for 2024</u></a></li>
<li><a href="https://win-hacks.techidaily.com/pcdjs-new-release-access-the-free-dex-361-beta-software-download/"><u>PCDJ's New Release: Access the Free DEX 3.6.1 Beta Software Download!</u></a></li>
<li><a href="https://techidaily.com/solutions-to-restore-deleted-files-from-x6-pro-by-fonelab-android-recover-data/"><u>Solutions to restore deleted files from X6 Pro</u></a></li>
<li><a href="https://win-hacks.techidaily.com/top-factors-leading-to-scanner-breakdowns-and-how-to-avoid-them-with-yl-technology-experts/"><u>Top Factors Leading to Scanner Breakdowns and How to Avoid Them with YL Technology Experts</u></a></li>
<li><a href="https://youtube-video-recordings.techidaily.com/unlocking-views-with-optimal-thumbnail-design/"><u>Unlocking Views with Optimal Thumbnail Design</u></a></li>
<li><a href="https://extra-hints.techidaily.com/unveiling-the-secret-sauce-for-massive-tiktok-content-grabs/"><u>Unveiling the Secret Sauce for Massive TikTok Content Grabs</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/xIP8ktrmOdg?si=zRnjbGzM6PDx2jCq" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

