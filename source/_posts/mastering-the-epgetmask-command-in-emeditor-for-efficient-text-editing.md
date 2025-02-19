---
title: Mastering the EP_GET_MASK Command in EmEditor for Efficient Text Editing
date: 2025-02-14T19:05:54.897Z
updated: 2025-02-18T17:25:35.988Z
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
<li><a href="https://fox-glue.techidaily.com/updated-effortless-editing-secrets-for-fresh-filmmakers/"><u>[Updated] Effortless Editing Secrets for Fresh Filmmakers</u></a></li>
<li><a href="https://fox-info.techidaily.com/updated-inject-photos-with-rotational-blur-effects-in-photosoph/"><u>[Updated] Inject Photos with Rotational Blur Effects in PHOTOSOPH</u></a></li>
<li><a href="https://win-hacks.techidaily.com/2-kostengunstige-und-leichte-methoden-zum-schutz-ihrer-computerdaten-auf-google-drive/"><u>2 Kostengünstige Und Leichte Methoden Zum Schutz Ihrer Computerdaten Auf Google Drive</u></a></li>
<li><a href="https://win-hacks.techidaily.com/1728496423979-windows-11usb/"><u>从Windows 11系统将照片传输至USB设备上：多样化的转移技巧分享</u></a></li>
<li><a href="https://win-hacks.techidaily.com/come-copiare-dischi-in-blocchi-diversi-facilmente-ed-efficientemente-guida-completa/"><u>Come Copiare Dischi in Blocchi Diversi Facilmente Ed Efficientemente - Guida Completa</u></a></li>
<li><a href="https://win-hacks.techidaily.com/contrasting-vmfs-by-vmware-with-the-standard-nfs-protocol-for-efficient-storage-solutions/"><u>Contrasting VMFS by VMware with the Standard NFS Protocol for Efficient Storage Solutions</u></a></li>
<li><a href="https://win-hacks.techidaily.com/discover-the-best-2-wd-zero-fill-software-solutions-compatible-with-all-windows-versions-start-your-risk-free-test-today/"><u>Discover the Best 2 WD Zero Fill Software Solutions Compatible with All Windows Versions - Start Your Risk-Free Test Today!</u></a></li>
<li><a href="https://blog-min.techidaily.com/how-i-transferred-messages-from-samsung-galaxy-a15-4g-to-iphone-12xs-max-in-seconds-drfone-by-drfone-transfer-from-android-transfer-from-android/"><u>How I Transferred Messages from Samsung Galaxy A15 4G to iPhone 12/XS (Max) in Seconds | Dr.fone</u></a></li>
<li><a href="https://win11-tips.techidaily.com/how-to-flip-mkv-to-mp4-in-windows-os/"><u>How to Flip MKV to MP4 in Windows OS</u></a></li>
<li><a href="https://win-hacks.techidaily.com/how-to-restore-factory-settings-on-laptops-running-windows-11-8-or-7/"><u>How to Restore Factory Settings on Laptops Running Windows 11, 8, or 7</u></a></li>
<li><a href="https://unlock-android.techidaily.com/in-2024-how-to-unlock-infinix-zero-30-5g-phone-with-broken-screen-by-drfone-android/"><u>In 2024, How to Unlock Infinix Zero 30 5G Phone with Broken Screen</u></a></li>
<li><a href="https://tiktok-video-files.techidaily.com/in-2024-tiktok-mastery-a-2023-elements-compendium/"><u>In 2024, TikTok Mastery A 2023 Elements Compendium</u></a></li>
<li><a href="https://android-pokemon-go.techidaily.com/in-2024-which-pokemon-can-evolve-with-a-moon-stone-for-oppo-find-x6-pro-drfone-by-drfone-virtual-android/"><u>In 2024, Which Pokémon can Evolve with a Moon Stone For Oppo Find X6 Pro? | Dr.fone</u></a></li>
<li><a href="https://win-hacks.techidaily.com/les-meilleurs-successeurs-du-kit-de-clonage-ssd-corsair-comparatif-complet-des-options-avant-gardistes/"><u>Les Meilleurs Successeurs Du Kit De Clonage SSD Corsair : Comparatif Complet Des Options Avant-Gardistes</u></a></li>
<li><a href="https://win-howtos.techidaily.com/overcoming-hp-laptop-webcam-glitches-in-windows-11-effective-solutions/"><u>Overcoming HP Laptop Webcam Glitches in Windows 11: Effective Solutions</u></a></li>
<li><a href="https://win-hacks.techidaily.com/resolvio-el-problema-del-error-dism-con-codigo-87-parametro-incorrecto-5-soluciones-efectivas/"><u>Resolvió El Problema Del Error 'DISM' Con Código 87: Parámetro Incorrecto - 5 Soluciones Efectivas</u></a></li>
<li><a href="https://fox-access.techidaily.com/the-most-massive-lifting-machines-in-the-sky/"><u>The Most Massive Lifting Machines in the Sky</u></a></li>
<li><a href="https://fox-cloud.techidaily.com/top-end-video-refresher-resolution-renaissance/"><u>Top-End Video Refresher Resolution Renaissance</u></a></li>
<li><a href="https://win-hacks.techidaily.com/ultimate-troubleshooting-guide-to-correcting-error-0x80n3712-on-your-pc-operating-system/"><u>Ultimate Troubleshooting Guide to Correcting Error 0X80n3712 on Your PC Operating System</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/ASUEYpqSP5E?si=0KOZxrTVexTuUkRn" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

