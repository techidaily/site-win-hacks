---
title: Mastering the EP_GET_MASK Command in EmEditor for Efficient Text Editing
date: 2024-12-14T06:04:20.912Z
updated: 2024-12-14T17:34:12.335Z
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
<li><a href="https://remote-screen-capture.techidaily.com/new-2024-approved-a-comprehensive-list-of-best-skype-recorder-models/"><u>[New] 2024 Approved A Comprehensive List of Best Skype Recorder Models</u></a></li>
<li><a href="https://win-hacks.techidaily.com/decoding-electronic-buzz-understanding-unexpected-audio-alerts-in-your-system-with-yl-software-expertise/"><u>Decoding Electronic Buzz: Understanding Unexpected Audio Alerts in Your System with YL Software Expertise</u></a></li>
<li><a href="https://driver-download.techidaily.com/directly-access-the-latest-nvidia-quadro-rtx-8000-drivers-for-all-supported-win-versions-10-8-7/"><u>Directly Access the Latest Nvidia Quadro RTX 8000 Drivers for All Supported Win Versions (10, 8, 7)</u></a></li>
<li><a href="https://win-hacks.techidaily.com/effortless-tech-tips-by-yl-software-a-how-to-on-deleting-redundant-applications/"><u>Effortless Tech Tips by YL Software: A How-To on Deleting Redundant Applications</u></a></li>
<li><a href="https://novels-ebooks.techidaily.com/138597640-9781462040650-energy-in-motion/"><u>Energy in Motion | Free Book</u></a></li>
<li><a href="https://win-hacks.techidaily.com/exploring-the-impact-of-overclocking-on-system-memory-insights-from-yl-computing-and-yl-software/"><u>Exploring the Impact of Overclocking on System Memory: Insights From YL Computing and YL Software</u></a></li>
<li><a href="https://extra-lessons.techidaily.com/in-2024-crafting-ae-titles-with-maximum-impression/"><u>In 2024, Crafting AE Titles with Maximum Impression</u></a></li>
<li><a href="https://fox-info.techidaily.com/in-2024-ink-your-photos-leading-apps-for-captioning-iosandroid/"><u>In 2024, Ink Your Photos Leading Apps for Captioning (iOS/Android)</u></a></li>
<li><a href="https://some-knowledge.techidaily.com/mp3-to-m4r-iphone/"><u>MP3 to M4R変換 - iPhone用着信音作りガイドと手順</u></a></li>
<li><a href="https://win-forum.techidaily.com/social-media-giants-unveiled-exploring-facebook-twitter-instagram-and-youtubes-influence/"><u>Social Media Giants Unveiled: Exploring Facebook, Twitter, Instagram, and YouTube's Influence</u></a></li>
<li><a href="https://win-hacks.techidaily.com/unlock-endless-melodies-exclusive-song-selection-on-party-tyme-karaoke-service-subscribe-now-perfect-for-djs/"><u>Unlock Endless Melodies: Exclusive Song Selection on Party Tyme Karaoke Service (Subscribe Now!) - Perfect for DJs!</u></a></li>
<li><a href="https://win-hacks.techidaily.com/unlocking-control-panel-how-to-navigate-and-modify-windows-defender-firewall-settings/"><u>Unlocking Control Panel: How to Navigate and Modify Windows Defender Firewall Settings</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/XVsiIO7hWOc?si=UvWnqxaI_yHwEr74" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

