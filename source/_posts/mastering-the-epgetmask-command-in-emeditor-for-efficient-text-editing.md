---
title: Mastering the EP_GET_MASK Command in EmEditor for Efficient Text Editing
date: 2024-11-18T23:46:45.023Z
updated: 2024-11-23T00:20:41.909Z
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
<li><a href="https://facebook-video-recording.techidaily.com/new-essential-fixes-for-disconnected-fb-live-feeds/"><u>[New] Essential Fixes for Disconnected FB Live Feeds</u></a></li>
<li><a href="https://win-hacks.techidaily.com/1-effortless-methods-sharing-images-from-your-desktop-computer-to-iphone-8/"><u>1. Effortless Methods: Sharing Images From Your Desktop Computer to iPhone 8</u></a></li>
<li><a href="https://location-fake.techidaily.com/6-ways-to-change-spotify-location-on-your-oppo-a56s-5g-drfone-by-drfone-virtual-android/"><u>6 Ways to Change Spotify Location On Your Oppo A56s 5G | Dr.fone</u></a></li>
<li><a href="https://youtube-tips.techidaily.com/p-by-step-guide-to-youtube-to-igtv-conversion-for-2024/"><u>A Step-by-Step Guide to YouTube to IGTV Conversion for 2024</u></a></li>
<li><a href="https://facebook.techidaily.com/boosting-quality-images-and-videos-in-fb-app/"><u>Boosting Quality Images & Videos in FB App</u></a></li>
<li><a href="https://facebook-video-content.techidaily.com/build-a-custom-facebook-coverage-for-2024/"><u>Build a Custom Facebook Coverage for 2024</u></a></li>
<li><a href="https://win-hacks.techidaily.com/die-besten-losungen-von-toshiba-fur-das-sichern-ihrer-daten-auf-externen-laufwerken-unter-windows-erfahren-sie-mehr-uber-die-top-2-optionen/"><u>Die Besten Lösungen Von Toshiba Für Das Sichern Ihrer Daten Auf Externen Laufwerken Unter Windows - Erfahren Sie Mehr Über Die Top 2 Optionen!</u></a></li>
<li><a href="https://facebook-video-share.techidaily.com/in-2024-how-to-share-a-private-youtube-video/"><u>In 2024, How to Share a Private YouTube Video?</u></a></li>
<li><a href="https://article-posts.techidaily.com/in-2024-prestigious-websites-elevating-youtube-content/"><u>In 2024, Prestigious Websites Elevating YouTube Content</u></a></li>
<li><a href="https://win-hacks.techidaily.com/solving-windows-10-update-problem-error-code-0x8-with-effective-methods-1-5/"><u>Solving Windows 10 Update Problem (Error Code: 0X8) with Effective Methods #1-5</u></a></li>
<li><a href="https://solve-lab.techidaily.com/1725288811885-winx-dvd/"><u>WinX DVD プラチナリッパーで動画をコピー出来ない？解決法見つけた！</u></a></li>
<li><a href="https://win-hacks.techidaily.com/1728496787011-windows-111087/"><u>データを失わない! Windows 11/10/8/7 互換性のある最適な無料リカバリプログラム【初心者のために教えます】</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/TJCye_oCTTw?si=6bVyBphcSgSFdyuq&autoplay=1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

