---
title: Mastering the EP_GET_MASK Command in EmEditor for Efficient Text Editing
date: 2024-12-23T16:39:42.592Z
updated: 2024-12-30T00:53:26.476Z
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
<li><a href="https://facebook-video-footage.techidaily.com/new-mastering-video-privacy-directly-share-yt-clips-using-googleid/"><u>[New] Mastering Video Privacy Directly Share YT Clips Using GoogleID</u></a></li>
<li><a href="https://video-capture.techidaily.com/new-zombification-extravaganza-8-epic-titles-ranked-in-2024/"><u>[New] Zombification Extravaganza - 8 Epic Titles Ranked, In 2024</u></a></li>
<li><a href="https://screen-sharing-recording.techidaily.com/updated-2024-approved-decoding-durecorder-features-and-user-guide-review/"><u>[Updated] 2024 Approved Decoding DuRecorder Features and User Guide Review</u></a></li>
<li><a href="https://video-capture.techidaily.com/updated-2024-approved-uncovering-budget-friendly-video-conferencing-tools-for-all-systems/"><u>[Updated] 2024 Approved Uncovering Budget-Friendly Video Conferencing Tools for All Systems</u></a></li>
<li><a href="https://fox-boxes.techidaily.com/updated-top-tunes-choosing-best-offline-audio-to-text-tools-for-2024/"><u>[Updated] Top Tunes Choosing Best Offline Audio-to-Text Tools for 2024</u></a></li>
<li><a href="https://desktop-recording.techidaily.com/updated-unlock-superior-mac-gif-capture-with-these-apps/"><u>[Updated] Unlock Superior Mac GIF Capture with These Apps</u></a></li>
<li><a href="https://win-hacks.techidaily.com/1728495071563-hdd/"><u>解決策：巨大ファイルを外付けHDDに保存できず、代替手段</u></a></li>
<li><a href="https://android-pokemon-go.techidaily.com/here-are-some-reliable-ways-to-get-pokemon-go-friend-codes-for-oneplus-ace-2-pro-drfone-by-drfone-virtual-android/"><u>Here Are Some Reliable Ways to Get Pokemon Go Friend Codes For OnePlus Ace 2 Pro | Dr.fone</u></a></li>
<li><a href="https://win-hacks.techidaily.com/hoofdlijfjes-om-een-vlugger-winodocs-map-making-process-in-windows-11-te-laten-oplossen/"><u>Hoofdlijfjes Om Een Vlugger Winodocs Map Making Process in Windows 11 Te Laten Oplossen</u></a></li>
<li><a href="https://extra-information.techidaily.com/joke-junction-ultimate-free-comic-templates/"><u>Joke Junction Ultimate Free Comic Templates</u></a></li>
<li><a href="https://win-hacks.techidaily.com/reversing-file-removal-in-windows-n-procedure-uncover-5-strategies/"><u>Reversing File Removal in Windows N-Procedure: Uncover 5 Strategies</u></a></li>
<li><a href="https://ai-driven-video-production.techidaily.com/updated-in-2024-want-amazing-opening-effects-today-we-will-share-with-you-20-best-places-that-are-free-to-download-title-intro-templates-for-adobe-premiere-/"><u>Updated In 2024, Want Amazing Opening Effects? Today, We Will Share with You 20 Best Places that Are Free to Download Title, Intro Templates for Adobe Premiere Pro</u></a></li>
<li><a href="https://win-hacks.techidaily.com/use-appropriate-data-structures-like-arrays-or-lists-to-represent-each-number-with-each-element-corresponding-to-a-single-digit/"><u>Use Appropriate Data Structures (Like Arrays or Lists) to Represent Each Number, with Each Element Corresponding to a Single Digit.</u></a></li>
<li><a href="https://win-hacks.techidaily.com/windows-11108ssd/"><u>Windows 11/10/8和SSD的一体化搭配：不必重装就可实现</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/RJNYTGHVlLc?si=lhdUUVYMVQjzHXBh" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

