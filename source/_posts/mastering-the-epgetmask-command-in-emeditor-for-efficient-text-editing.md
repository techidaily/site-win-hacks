---
title: Mastering the EP_GET_MASK Command in EmEditor for Efficient Text Editing
date: 2025-01-22T23:13:23.311Z
updated: 2025-01-26T21:16:13.292Z
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
<li><a href="https://digital-screen-recording.techidaily.com/new-sustainable-screen-tech-best-picks-reviewed-for-2024/"><u>[New] Sustainable Screen Tech Best Picks Reviewed for 2024</u></a></li>
<li><a href="https://fox-http.techidaily.com/new-voice-over-techniques-that-transform-video-storytelling-for-2024/"><u>[New] Voice Over Techniques That Transform Video Storytelling for 2024</u></a></li>
<li><a href="https://win-hacks.techidaily.com/360-hard-drive-capacity/"><u>360 Hard Drive Capacity!</u></a></li>
<li><a href="https://win-solutions.techidaily.com/constraint-a-use-only-the-c-major-scale-for-representation/"><u>Constraint A: Use only the C-Major Scale for Representation.</u></a></li>
<li><a href="https://win-hacks.techidaily.com/effiziente-methoden-zur-reparatur-einer-defekten-datentrageroberflache/"><u>Effiziente Methoden Zur Reparatur Einer Defekten Datenträgeroberfläche</u></a></li>
<li><a href="https://win-amazing.techidaily.com/gratis-online-converteren-van-videe-aan-mkv-wijzenmovavis/"><u>Gratis Online Converteren Van VIDEE Aan MKV - WijzenMOVavis</u></a></li>
<li><a href="https://phone-solutions.techidaily.com/in-2024-the-best-8-vpn-hardware-devices-reviewed-on-oppo-a1-5g-drfone-by-drfone-virtual-android/"><u>In 2024, The Best 8 VPN Hardware Devices Reviewed On Oppo A1 5G | Dr.fone</u></a></li>
<li><a href="https://win-hacks.techidaily.com/iniciando-el-recovery-mode-en-windows-11-una-guia-completa-para-tecnicos-avanzados/"><u>Iniciando El Recovery Mode en Windows 11: Una Guía Completa Para Técnicos Avanzados</u></a></li>
<li><a href="https://win-hacks.techidaily.com/problembehandlung-nicht-vollstandige-speicherkapazitat-auf-festplatte-in-windows-10-erkennen/"><u>Problembehandlung: Nicht Vollständige Speicherkapazität Auf Festplatte in Windows 10 Erkennen</u></a></li>
<li><a href="https://win-special.techidaily.com/recuperacion-de-particion-olvidada-tecnicas-esenciales-con-pasos-a-seguir-para-windows-11-y-versiones-anteriores/"><u>Recuperación De Partición Olvidada: Técnicas Esenciales Con Pasos a Seguir Para Windows 11 Y Versiones Anteriores</u></a></li>
<li><a href="https://win-hacks.techidaily.com/regler-les-problemes-dincompatibilite-avec-windows-11-installation-et-mise-a-niveau-effortless-guide/"><u>Règler Les Problèmes D'Incompatibilité Avec Windows 11 Installation Et Mise À Niveau Effortless Guide</u></a></li>
<li><a href="https://youtube-videos.techidaily.com/unlocking-elusive-footage-the-systematic-guide-to-youtube-secrets/"><u>Unlocking Elusive Footage The Systematic Guide to YouTube Secrets</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/hXIq2G0nShk?si=5Z4Fwv7ZB6oKWsdd" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

