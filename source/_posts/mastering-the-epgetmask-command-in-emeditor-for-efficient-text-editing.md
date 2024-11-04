---
title: Mastering the EP_GET_MASK Command in EmEditor for Efficient Text Editing
date: 2024-10-28T01:18:04.283Z
updated: 2024-11-04T01:12:57.820Z
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
<li><a href="https://some-skills.techidaily.com/updated-top-10-audio-playback-accelerators-for-phones/"><u>[Updated] Top 10 Audio Playback Accelerators for Phones</u></a></li>
<li><a href="https://fox-boxes.techidaily.com/2024-approved-flawless-syncing-adding-soundtracks-to-inshot/"><u>2024 Approved Flawless Syncing Adding Soundtracks to Inshot</u></a></li>
<li><a href="https://extra-hints.techidaily.com/30-metaverse-phenomena-making-your-mark-with-memes-for-2024/"><u>30 Metaverse Phenomena Making Your Mark with Memes for 2024</u></a></li>
<li><a href="https://win-hacks.techidaily.com/1728480072657-ssd/"><u>重要SSD程序：頂尖二選和複製詳解</u></a></li>
<li><a href="https://facebook.techidaily.com/beyond-the-hype-dispelling-popular-facebook-misconceptions/"><u>Beyond the Hype: Dispelling Popular Facebook Misconceptions</u></a></li>
<li><a href="https://win-hacks.techidaily.com/comprehensive-walkthrough-restoring-your-computer-with-a-factory-reset-in-windows-vista/"><u>Comprehensive Walkthrough: Restoring Your Computer with a Factory Reset in Windows Vista</u></a></li>
<li><a href="https://win-hacks.techidaily.com/erstellen-eines-backups-fur-ihr-ipad-anleitung-zur-ubertragung-auf-einen-externen-speicher-einschliesslich-der-nutzung-und-umgehung-von-itunes/"><u>Erstellen Eines Backups Für Ihr iPad: Anleitung Zur Übertragung Auf Einen Externen Speicher, Einschließlich Der Nutzung Und Umgehung Von iTunes</u></a></li>
<li><a href="https://some-knowledge.techidaily.com/features-and-flaws-of-samsungs-image-editor-reviewed-for-2024/"><u>Features and Flaws of Samsung's Image Editor Reviewed for 2024</u></a></li>
<li><a href="https://android-transfer.techidaily.com/how-to-transfer-music-from-honor-x9b-to-ipod-drfone-by-drfone-transfer-from-android-transfer-from-android/"><u>How to Transfer Music from Honor X9b to iPod | Dr.fone</u></a></li>
<li><a href="https://win-hacks.techidaily.com/top-5-ersatzprodukte-fur-dropbox-im-jahr-2024-schritt-fur-schritt-anleitung/"><u>Top 5 Ersatzprodukte Für Dropbox Im Jahr 2024 - Schritt-Für-Schritt-Anleitung</u></a></li>
<li><a href="https://win-hacks.techidaily.com/transfer-von-windows-11-auf-samsung-ssd-neuladen-ohne-installation/"><u>Transfer Von Windows 11 Auf Samsung SSD - Neuladen Ohne Installation</u></a></li>
<li><a href="https://win-hacks.techidaily.com/ultimate-guide-on-shifting-ios-files-how-to-move-your-iphones-content-to-a-laptop-or-different-iphone-model/"><u>Ultimate Guide on Shifting iOS Files: How to Move Your iPhone's Content to a Laptop or Different iPhone Model</u></a></li>
<li><a href="https://technical-tips.techidaily.com/understanding-digital-acknowledgements-recognizing-when-your-text-messages-are-read/"><u>Understanding Digital Acknowledgements: Recognizing when Your Text Messages Are Read</u></a></li>
<li><a href="https://howto.techidaily.com/zte-blade-a73-5g-not-receiving-texts-10-hassle-free-solutions-here-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>ZTE Blade A73 5G Not Receiving Texts? 10 Hassle-Free Solutions Here | Dr.fone</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<span id="1993650">
					<video width="576" height="240" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1993650.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/22993-1993650">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1993650.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:360px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fhomestyler.sjv.io%2Fc%2F5597632%2F1993650%2F22993'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1993650/22993" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

