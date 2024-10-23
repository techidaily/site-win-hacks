---
title: Mastering the EP_GET_MASK Command in EmEditor for Efficient Text Editing
date: 2024-10-22T06:51:51.389Z
updated: 2024-10-23T09:48:42.631Z
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
<li><a href="https://on-screen-recording.techidaily.com/new-maximize-communication-video-conferencing-tips-for-android-for-2024/"><u>[New] Maximize Communication Video Conferencing Tips for Android for 2024</u></a></li>
<li><a href="https://youtube-docs.techidaily.com/ed-premier-youtube-standards-for-all-viewers-for-2024/"><u>[Updated] Premier YouTube Standards for All Viewers for 2024</u></a></li>
<li><a href="https://youtube-tips.techidaily.com/ed-unlocking-the-potential-of-youtube-shorts-a-comprehensive-tutorial-for-2024/"><u>[Updated] Unlocking the Potential of YouTube Shorts A Comprehensive Tutorial for 2024</u></a></li>
<li><a href="https://win-hacks.techidaily.com/1728465925264-404/"><u>404エラー発生時に直すべき点を解説</u></a></li>
<li><a href="https://win-hacks.techidaily.com/copiar-disco-de-gratis-con-aomei-la-herramienta-sin-coste-para-clonar-unidades-guiadas/"><u>Copiar Disco De Gratis Con AOMEI - La Herramienta Sin Coste Para Clonar Unidades Guiadas</u></a></li>
<li><a href="https://hardware-updates.techidaily.com/effortless-driver-downloads-and-updates-for-lenovo-thinkpad-t-series-including-t500/"><u>Effortless Driver Downloads and Updates for Lenovo ThinkPad T Series, Including T500</u></a></li>
<li><a href="https://win-hacks.techidaily.com/gratuite-et-securite-le-meilleur-logiciel-de-sauvegarde-pour-ssd-crucial-simplifie/"><u>Gratuité Et Sécurité : Le Meilleur Logiciel De Sauvegarde Pour SSD Crucial Simplifié</u></a></li>
<li><a href="https://fox-hovers.techidaily.com/in-2024-gradual-dimming-of-sound-in-audacity-masterclass/"><u>In 2024, Gradual Dimming of Sound in Audacity Masterclass</u></a></li>
<li><a href="https://win-hacks.techidaily.com/optimal-disk-space-allocation-for-effective-system-shielding-how-much-is-enough/"><u>Optimal Disk Space Allocation for Effective System Shielding: How Much Is Enough?</u></a></li>
<li><a href="https://tech-revival.techidaily.com/resolving-your-ps4-pros-dvd-issue-in-5-easy-steps-a-comprehensive-fix-guide/"><u>Resolving Your PS4 Pro's DVD Issue in 5 Easy Steps: A Comprehensive Fix Guide</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://malaysia-healthcare-travel-council.pxf.io/c/5597632/1557746/17382" target="_top" id="1557746">
  <img src="//a.impactradius-go.com/display-ad/17382-1557746" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://malaysia-healthcare-travel-council.pxf.io/i/5597632/1557746/17382" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

