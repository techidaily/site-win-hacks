---
title: Mastering the EP_GET_MASK Command in EmEditor for Efficient Text Editing
date: 2024-10-04T16:46:27.414Z
updated: 2024-10-11T16:21:06.752Z
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
<li><a href="https://youtube-sure.techidaily.com/024-approved-guides-on-creating-cost-free-youtube-beginnings-and-conclusions/"><u>[New] 2024 Approved Guides on Creating Cost-Free YouTube Beginnings & Conclusions</u></a></li>
<li><a href="https://extra-resources.techidaily.com/new-budget-friendly-cloud-storage-pricing-guide-2024-update/"><u>[New] Budget-Friendly Cloud Storage Pricing Guide - 2024 Update</u></a></li>
<li><a href="https://on-screen-recording.techidaily.com/updated-the-grand-gaming-odyssey-our-list-of-best-action-adventures-for-2024/"><u>[Updated] The Grand Gaming Odyssey Our List of Best Action-Adventures for 2024</u></a></li>
<li><a href="https://instagram-video-recordings.techidaily.com/updated-the-leading-25-icons-setting-social-trends-on-insta/"><u>[Updated] The Leading 25 Icons Setting Social Trends on Insta</u></a></li>
<li><a href="https://screen-mirror.techidaily.com/8-best-apps-for-screen-mirroring-nokia-g22-pc-drfone-by-drfone-android/"><u>8 Best Apps for Screen Mirroring Nokia G22 PC | Dr.fone</u></a></li>
<li><a href="https://win-hot.techidaily.com/effortless-techniques-for-converting-pdf-tables-into-microsoft-excel-format/"><u>Effortless Techniques for Converting PDF Tables Into Microsoft Excel Format</u></a></li>
<li><a href="https://win-dash.techidaily.com/how-to-install-the-newest-intel-raid-drivers-on-your-windows-system-versions-for-w11-10-8-and-win7/"><u>How to Install the Newest Intel RAID Drivers on Your Windows System: Versions for W11, 10, 8 & Win7</u></a></li>
<li><a href="https://win-hacks.techidaily.com/how-to-resolve-issues-with-the-download-feature-at-flipbuildercom/"><u>How to Resolve Issues with the Download Feature at FlipBuilder.com</u></a></li>
<li><a href="https://win-hacks.techidaily.com/incorporating-your-brands-logo-into-a-flipbook-background-with-ease/"><u>Incorporating Your Brand's Logo Into a FlipBook Background with Ease</u></a></li>
<li><a href="https://win-hacks.techidaily.com/integrating-page-turn-audio-effects-into-your-digital-flipbooks-with-flipbuilder/"><u>Integrating Page-Turn Audio Effects Into Your Digital Flipbooks with FlipBuilder</u></a></li>
<li><a href="https://win-hacks.techidaily.com/masterful-presentation-creation-with-flip-powerpoint-pro-seamlessly-integrate-multimedia-and-create-interactive-book-style-slideshows-explore-at-flipbuilder16/"><u>Masterful Presentation Creation with Flip PowerPoint Pro: Seamlessly Integrate Multimedia and Create Interactive Book-Style Slideshows [Explore at FlipBuilder.com]</u></a></li>
<li><a href="https://win-hacks.techidaily.com/mastering-flipoffice-pro-upgrades-a-comprehensive-walkthrough-for-importing-themes-easily-expert-advice-from-flipbuilder/"><u>Mastering FlipOffice Pro Upgrades: A Comprehensive Walkthrough for Importing Themes Easily | Expert Advice From FlipBuilder</u></a></li>
<li><a href="https://win-hacks.techidaily.com/mastering-image-comments-for-your-online-galleries-using-flipbuilders-tools/"><u>Mastering Image Comments for Your Online Galleries Using FlipBuilder's Tools</u></a></li>
<li><a href="https://hardware-help.techidaily.com/revive-your-lenovo-docking-station-with-the-latest-driver-software-step-by-step-instructions/"><u>Revive Your Lenovo Docking Station with the Latest Driver Software: Step-by-Step Instructions</u></a></li>
<li><a href="https://tech-haven.techidaily.com/unlock-the-power-of-bing-chat-on-android-the-ultimate-walkthrough/"><u>Unlock the Power of Bing Chat on Android: The Ultimate Walkthrough</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1885947/19272" target="_top" id="1885947">
  <img src="//a.impactradius-go.com/display-ad/19272-1885947" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1885947/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

