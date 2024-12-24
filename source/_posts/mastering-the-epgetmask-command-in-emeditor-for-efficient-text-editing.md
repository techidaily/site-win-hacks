---
title: Mastering the EP_GET_MASK Command in EmEditor for Efficient Text Editing
date: 2024-12-21T08:44:34.770Z
updated: 2024-12-24T07:03:23.594Z
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
<li><a href="https://facebook-record-videos.techidaily.com/updated-double-the-joy-master-looping-of-youtube-media-on-televisions-for-2024/"><u>[Updated] Double the Joy Master Looping of YouTube Media on Televisions for 2024</u></a></li>
<li><a href="https://extra-approaches.techidaily.com/updated-inshot-vs-competitors-a-detailed-video-app-review/"><u>[Updated] InShot vs Competitors A Detailed Video App Review</u></a></li>
<li><a href="https://win-lab.techidaily.com/bantuannya-kebenaran-proses-restorasi-gambar-lemas-di-google-drive/"><u>Bantuannya Kebenaran, Proses Restorasi Gambar Lemas Di Google Drive</u></a></li>
<li><a href="https://win-hacks.techidaily.com/complete-guide-restoring-deleted-files-from-windows-11-recycle-bin-even-after-emptying/"><u>Complete Guide: Restoring Deleted Files From Windows 11 Recycle Bin Even After Emptying</u></a></li>
<li><a href="https://app-tips.techidaily.com/comprehensive-guide-syncing-your-chats-with-icloud-via-whatsapp/"><u>Comprehensive Guide: Syncing Your Chats with iCloud via WhatsApp</u></a></li>
<li><a href="https://win-hacks.techidaily.com/guide-de-configuration-du-sysreq-dans-lapplication-de-sauvegarde-centralisee-daomei/"><u>Guide De Configuration Du SysReq Dans L'Application De Sauvegarde Centralisée D’AOMEI</u></a></li>
<li><a href="https://android-unlock.techidaily.com/in-2024-how-to-show-wi-fi-password-on-vivo-s17-by-drfone-android/"><u>In 2024, How to Show Wi-Fi Password on Vivo S17</u></a></li>
<li><a href="https://win-hacks.techidaily.com/mastering-bilingual-documents-emeditor-and-its-superior-chinese-language-support/"><u>Mastering Bilingual Documents: EmEditor and Its Superior Chinese Language Support</u></a></li>
<li><a href="https://fox-blue.techidaily.com/premier-plans-exclusive-free-premiere-pro-samples-2023/"><u>Premier Plans - Exclusive Free Premiere Pro Samples 2023</u></a></li>
<li><a href="https://hardware-reviews.techidaily.com/1723341707040-solution-the-first-step-is-conducting-a-detailed-survey-to-understand-the-propertys-physical-features-and-constraints/"><u>Solution: The First Step Is Conducting a Detailed Survey to Understand the Property's Physical Features and Constraints.</u></a></li>
<li><a href="https://win-hacks.techidaily.com/solve-your-systems-snafu-expert-tips-to-repair-frozen-chkdsk-on-modern-windows-systems/"><u>Solve Your System's Snafu: Expert Tips to Repair Frozen Chkdsk on Modern Windows Systems</u></a></li>
<li><a href="https://win-hacks.techidaily.com/wiederauffinden-verschollener-festplattendaten-entdecke-verborgene-dateien-mit-myrecover/"><u>Wiederauffinden Verschollener Festplattendaten - Entdecke Verborgene Dateien Mit MyRecover</u></a></li>
<li><a href="https://vp-tips.techidaily.com/1725290009694-windows-11dvd5/"><u>Windows 11対応DVDダビング自由ソフトウェア5つ：初学者推薦版完全ガイド</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/YezPJZzPJ8Q?si=xF1t4BQHFquzvnzE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

