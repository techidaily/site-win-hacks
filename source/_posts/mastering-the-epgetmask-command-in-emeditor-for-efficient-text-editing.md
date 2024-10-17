---
title: Mastering the EP_GET_MASK Command in EmEditor for Efficient Text Editing
date: 2024-10-15T17:42:08.580Z
updated: 2024-10-17T16:29:25.789Z
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
<li><a href="https://youtube-zero.techidaily.com/rofessional-level-content-structure-with-expert-templates/"><u>[New] Professional-Level Content Structure with Expert Templates</u></a></li>
<li><a href="https://win-hacks.techidaily.com/44cm44oh44oi44oq44o844k544og44kj44od44kv44gr5asx44kp44km44gf44oh44o844k44gu5b6p5rs75oml6acg44cn/"><u>「メモリースティックに失われたデータの復活手順」</u></a></li>
<li><a href="https://win-hacks.techidaily.com/beginners-guide-to-mastering-gpu-passthrough-in-microsoft-hyper-v-a-step-by-step-tutorial/"><u>Beginner's Guide to Mastering GPU Passthrough in Microsoft Hyper-V: A Step-by-Step Tutorial</u></a></li>
<li><a href="https://extra-resources.techidaily.com/combatting-blurry-and-warped-youtube-videos/"><u>Combatting Blurry and Warped YouTube Videos</u></a></li>
<li><a href="https://win-hacks.techidaily.com/complete-aomei-backupper-qanda-expert-answers-and-tips-for-your-data-protection-needs/"><u>Complete AOMEI Backupper Q&A - Expert Answers and Tips for Your Data Protection Needs</u></a></li>
<li><a href="https://phone-solutions.techidaily.com/easy-steps-to-recover-deleted-videos-from-z50s-pro-by-fonelab-android-recover-video/"><u>Easy steps to recover deleted videos from Z50S Pro</u></a></li>
<li><a href="https://extra-tips.techidaily.com/hardware-hurdles-whats-necessary-for-big-sur/"><u>Hardware Hurdles What's Necessary for Big Sur?</u></a></li>
<li><a href="https://screen-mirror.techidaily.com/how-to-mirror-realme-12-proplus-5g-to-mac-drfone-by-drfone-android/"><u>How to Mirror Realme 12 Pro+ 5G to Mac? | Dr.fone</u></a></li>
<li><a href="https://android-transfer.techidaily.com/how-to-transfer-videos-from-asus-rog-phone-7-ultimate-to-ipad-drfone-by-drfone-transfer-from-android-transfer-from-android/"><u>How to Transfer Videos from Asus ROG Phone 7 Ultimate to iPad | Dr.fone</u></a></li>
<li><a href="https://android-transfer.techidaily.com/in-2024-5-techniques-to-transfer-data-from-itel-p40plus-to-iphone-15141312-drfone-by-drfone-transfer-from-android-transfer-from-android/"><u>In 2024, 5 Techniques to Transfer Data from Itel P40+ to iPhone 15/14/13/12 | Dr.fone</u></a></li>
<li><a href="https://eaxpv-info.techidaily.com/mehr-klarheit-in-ihren-filmen-steigerung-der-videodatenqualitat-auf-hd-bzw-4k-ebene-unter-windows-and-mac-os-x/"><u>Mehr Klarheit in Ihren Filmen: Steigerung Der Videodatenqualität Auf HD- Bzw. 4K-Ebene Unter Windows & Mac OS X</u></a></li>
<li><a href="https://win-hacks.techidaily.com/page-cannot-be-located-http-404-error/"><u>Page Cannot Be Located: HTTP 404 Error</u></a></li>
<li><a href="https://fox-boxes.techidaily.com/prospective-leaders-in-titling-the-top-5-online-masters-revealed/"><u>Prospective Leaders in Titling The Top 5 Online Masters Revealed</u></a></li>
<li><a href="https://win-hacks.techidaily.com/seamless-steps-for-cloning-a-dynamic-disk-under-windows-7/"><u>Seamless Steps for Cloning a Dynamic Disk Under Windows 7</u></a></li>
<li><a href="https://win-hacks.techidaily.com/titre-techniques-simplifiees-pour-sauvegarder-et-configurer-les-ordinateurs-developpement-professionnel-avec-windows/"><u>Titre: Techniques Simplifiées Pour Sauvegarder Et Configurer Les Ordinateurs Développement Professionnel Avec Windows</u></a></li>
<li><a href="https://win-hacks.techidaily.com/top-clone-ssd-software-entierement-integre-sans-risque-de-pertes-de-donnees/"><u>Top Clone SSD Software: Entièrement Intégré Sans Risque De Pertes De Données</u></a></li>
<li><a href="https://win-hacks.techidaily.com/ubersetzen-sie-videos-vom-pc-direkt-auf-ihre-iphone-kamera-rolle/"><u>Übersetzen Sie Videos Vom PC Direkt Auf Ihre iPhone Kamera Rolle</u></a></li>
<li><a href="https://howto.techidaily.com/what-to-do-if-google-play-services-keeps-stopping-on-motorola-g54-5g-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>What to Do if Google Play Services Keeps Stopping on Motorola G54 5G | Dr.fone</u></a></li>
<li><a href="https://win-hacks.techidaily.com/1728478556044-windows-11/"><u>Windows 11初回ログインパスワード削除手順３通り</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135400/19272" target="_top" id="2135400">
  <img src="//a.impactradius-go.com/display-ad/19272-2135400" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135400/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

