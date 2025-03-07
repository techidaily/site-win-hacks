---
title: Mastering the EP_GET_MASK Command in EmEditor for Efficient Text Editing
date: 2025-03-04T18:53:19.593Z
updated: 2025-03-07T17:04:38.530Z
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
<li><a href="https://fox-cloud.techidaily.com/updated-2024-approved-t5-unboxed-the-revolution-in-action-filming/"><u>[Updated] 2024 Approved T5 Unboxed - The Revolution in Action Filming</u></a></li>
<li><a href="https://screen-mirroring-recording.techidaily.com/updated-ultimate-drivers-delight-5-top-race-games/"><u>[Updated] Ultimate Driver's Delight 5 Top Race Games</u></a></li>
<li><a href="https://win-hacks.techidaily.com/1-risoluzione-del-problema-disco-ignoto-non-inizializzato-trovato-su-windows-11/"><u>1. Risoluzione Del Problema: Disco Ignoto Non Inizializzato Trovato Su Windows 11</u></a></li>
<li><a href="https://win-hacks.techidaily.com/como-recuperar-informacion-eliminada-accidentalmente-en-una-unidad-de-memoria-sandisk-con-seguridad-integrada/"><u>Cómo Recuperar Información Eliminada Accidentalmente en Una Unidad De Memoria SanDisk Con Seguridad Integrada</u></a></li>
<li><a href="https://location-social.techidaily.com/edit-and-send-fake-location-on-telegram-for-your-samsung-galaxy-m14-5g-in-3-ways-drfone-by-drfone-virtual-android/"><u>Edit and Send Fake Location on Telegram For your Samsung Galaxy M14 5G in 3 Ways | Dr.fone</u></a></li>
<li><a href="https://apple-account.techidaily.com/how-to-sign-out-of-apple-id-on-iphone-12-pro-max-without-password-by-drfone-ios/"><u>How to Sign Out of Apple ID On iPhone 12 Pro Max without Password?</u></a></li>
<li><a href="https://win-hacks.techidaily.com/identify-all-sentences-that-mention-architectural-features-eg-built-in-wardrobes-fireplaces/"><u>Identify All Sentences that Mention Architectural Features (E.g., Built-In Wardrobes, Fireplaces).</u></a></li>
<li><a href="https://instagram-video-files.techidaily.com/in-2024-reach-new-heights-on-igtv-top-tactics-for-expanding-your-audience/"><u>In 2024, Reach New Heights on IGTV Top Tactics for Expanding Your Audience</u></a></li>
<li><a href="https://buynow-help.techidaily.com/the-ultimate-guide-to-using-the-powerful-beatit-bt-d11-jump-starter-a-thorough-review/"><u>The Ultimate Guide to Using the Powerful Beatit BT-D11 Jump Starter - A Thorough Review</u></a></li>
<li><a href="https://win-hacks.techidaily.com/tips-dan-teknik-cara-cara-membuat-ulang-partisi-ssd-dengan-efisien/"><u>Tips Dan Teknik Cara Cara Membuat Ulang Partisi SSD Dengan Efisien</u></a></li>
<li><a href="https://win-hacks.techidaily.com/ubersetzen-von-daten-zwei-methoden-zum-migrieren-von-hdd-auf-ssd-unter-windows-11/"><u>Übersetzen Von Daten: Zwei Methoden Zum Migrieren Von HDD Auf SSD Unter Windows 11</u></a></li>
<li><a href="https://win-hacks.techidaily.com/unlocking-effective-solutions-post-m3-drive-intrusion-and-recovery-tool-exploits/"><u>Unlocking Effective Solutions Post-M3 Drive Intrusion & Recovery Tool Exploits</u></a></li>
<li><a href="https://tech-savvy.techidaily.com/vanguard-ai-tech-for-optimal-web-data-hunting/"><u>Vanguard AI Tech for Optimal Web Data Hunting</u></a></li>
</ul></div>

