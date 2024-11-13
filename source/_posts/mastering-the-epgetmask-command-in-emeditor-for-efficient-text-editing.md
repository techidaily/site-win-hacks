---
title: Mastering the EP_GET_MASK Command in EmEditor for Efficient Text Editing
date: 2024-11-07T00:42:45.283Z
updated: 2024-11-13T01:21:26.439Z
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
<li><a href="https://screen-video-capture.techidaily.com/new-2024-approved-simple-steps-to-document-online-meetings-on-os-xwindows/"><u>[New] 2024 Approved Simple Steps to Document Online Meetings on OS X/Windows</u></a></li>
<li><a href="https://fox-cloud.techidaily.com/updated-in-2024-sculpt-the-subject-mastering-the-art-of-background-takedown/"><u>[Updated] In 2024, Sculpt the Subject Mastering the Art of Background Takedown</u></a></li>
<li><a href="https://win-hacks.techidaily.com/befreit-ihre-geloschten-dateien-auf-externen-speichern-mit-diesen-sechs-restaurierungsmethoden/"><u>Befreit Ihre Gelöschten Dateien Auf Externen Speichern Mit Diesen Sechs Restaurierungsmethoden</u></a></li>
<li><a href="https://win-hacks.techidaily.com/comment-restaurer-efficacement-limage-du-systeme-sous-windows-10-8-ou-7-sur-un-autre-ordinateur/"><u>Comment Restaurer Efficacement L’image Du Système Sous Windows 10, 8 Ou 7 Sur Un Autre Ordinateur</u></a></li>
<li><a href="https://technical-tips.techidaily.com/easy-fixes-for-when-you-cant-locate-nsprnsp4dll-user-manual/"><u>Easy Fixes for When You Can't Locate Nsprnsp4.dll - User Manual</u></a></li>
<li><a href="https://some-knowledge.techidaily.com/evaluating-the-cost-of-producing-a-music-video-for-2024/"><u>Evaluating the Cost of Producing a Music Video for 2024</u></a></li>
<li><a href="https://win-hacks.techidaily.com/four-techniques-for-bootstrapping-windows-11-home-edition-on-new-hardware-without-linked-microsoft-id/"><u>Four Techniques for Bootstrapping Windows 11 Home Edition on New Hardware without Linked Microsoft ID</u></a></li>
<li><a href="https://blog-min.techidaily.com/free-conversion-of-ogv-video-files-easy-online-tools-by-movavi/"><u>Free Conversion of OGV Video Files: Easy Online Tools by Movavi</u></a></li>
<li><a href="https://hardware-updates.techidaily.com/free-download-latest-drivers-for-msi-z370-a-pro-motherboard/"><u>Free Download: Latest Drivers for MSI Z370-A Pro Motherboard</u></a></li>
<li><a href="https://sound-issues.techidaily.com/how-to-repair-a-non-functional-mic-on-steelseries-arctis-prime-headset/"><u>How to Repair a Non-Functional Mic on SteelSeries Arctis Prime Headset</u></a></li>
<li><a href="https://ios-location-track.techidaily.com/top-6-appsservices-to-trace-any-apple-iphone-6s-location-by-mobile-number-drfone-by-drfone-virtual-ios/"><u>Top 6 Apps/Services to Trace Any Apple iPhone 6s Location By Mobile Number | Dr.fone</u></a></li>
<li><a href="https://win-hacks.techidaily.com/top-rated-bitlocker-recovery-software-compatible-with-windows-1087-and-future-versions/"><u>Top Rated BitLocker Recovery Software Compatible with Windows 10/8/7 and Future Versions</u></a></li>
<li><a href="https://sound-tweaking.techidaily.com/updated-2024-approved-unlock-free-vocal-manipulation-expertise-with-in-depth-guide-to-voice-editing-via-filmora/"><u>Updated 2024 Approved Unlock Free Vocal Manipulation Expertise with In-Depth Guide to Voice Editing via Filmora</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2111981/7443" target="_top" id="2111981">
  <img src="//a.impactradius-go.com/display-ad/7443-2111981" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2111981/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

