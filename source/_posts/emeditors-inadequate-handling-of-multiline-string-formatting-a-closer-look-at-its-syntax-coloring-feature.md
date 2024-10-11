---
title: "EmEditor's Inadequate Handling of Multiline String Formatting: A Closer Look at Its Syntax Coloring Feature"
date: 2024-10-10T16:38:24.355Z
updated: 2024-10-11T16:34:04.602Z
tags:
  - product
categories:
  - emeditor
thumbnail: https://thmb.techidaily.com/0004bab4ed76fb3b0e7b5e78faee5c8cd34739a5594338591ba06831ec971383.jpg
---

## EmEditor's Inadequate Handling of Multiline String Formatting: A Closer Look at Its Syntax Coloring Feature

Viewing 4 posts - 1 through 4 (of 4 total)

* Author  
Posts
* September 13, 2010 at 2:06 pm [#8947](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/05561bcf0e2ddd7cff592202c36eef4f?s=80&d=identicon&r=g)Jamil](https://www.emeditor.com/forums/users/jamil-cloud/ "View Jamil's profile")  
Participant  
I have an example SQL Server SQL script below:  
 DECLARE @SQL\_VAR VARCHAR(4000)  
 SET @SQL\_VAR = ‘SELECT \* FROM dbo.Table’  
 EXEC(@SQL\_VAR)  
 This script is colorized correctly as is.  
 However, if I modify the sript as follow, colorization breaks:  
 DECLARE @SQL\_VAR VARCHAR(4000)  
 SET @SQL\_VAR = ‘  
 SELECT \*  
 FROM dbo.Table  
 ‘  
 EXEC(@SQL\_VAR)  
 The script above is valid and colorized correctly with Microsoft’s SQL Server Management Studio. It appears EmEditor cannot handle a single string containing new lines.  
 I have reproduced this under the 32-bit and 64-bit versions of 10.0.1  
September 13, 2010 at 8:33 pm [#8948](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/c095e276d7d1f5ed27f91bf623e4e445?s=80&d=identicon&r=g)CrashNBurn](https://www.emeditor.com/forums/users/CrashNBurn/ "View CrashNBurn's profile")  
Member  
I’ve noticed this when attempting to create a custom CodeCollapse, that I was unable to use a multi-line regex… which really limits the whole idea of “replace match with string”  
 Since you can’t replace a match with a back-reference 1 2 etc if it’s a multi-line regex. :P  
September 14, 2010 at 6:26 am [#8967](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/ec03db8a2a7b8dea60b1c9f8f11901d9?s=80&d=identicon&r=g)Jibz](https://www.emeditor.com/forums/users/Jibz/ "View Jibz's profile")  
Member  
Try going into the properties for the EmEditor SQL configuration (Alt-Enter if you’re looking at the example at the moment), and on the Highlight (2) tab, under “String Enclosed by Quotation Marks”, check “Continue to Next Line”.  
 Seems to do the trick here.  
September 14, 2010 at 9:41 pm [#8974](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/05561bcf0e2ddd7cff592202c36eef4f?s=80&d=identicon&r=g)Jamil](https://www.emeditor.com/forums/users/jamil-cloud/ "View Jamil's profile")  
Participant  
Ah — I never noticed/realized the purpose of that option.  
 Yes — turning hat option on resolved this issue.  
 Thanks.
* Author  
Posts

Viewing 4 posts - 1 through 4 (of 4 total)

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
<li><a href="https://youtube-docs.techidaily.com/ed-2024-approved-streamlined-playback-controlling-youtube-video-delivery-speeds/"><u>[Updated] 2024 Approved Streamlined Playback Controlling YouTube Video Delivery Speeds</u></a></li>
<li><a href="https://video-capture.techidaily.com/1716042022241-updated-in-2024-top-6-minecraft-house-ideas-for-beginners/"><u>[Updated] In 2024, Top 6 Minecraft House Ideas [for Beginners]</u></a></li>
<li><a href="https://youtube-help.techidaily.com/2024-approved-navigating-copyright-on-youtube-and-cc/"><u>2024 Approved Navigating Copyright on YouTube & CC</u></a></li>
<li><a href="https://tech-haven.techidaily.com/can-chatgpt-adapt-through-interaction-learning-from-conversations/"><u>Can ChatGPT Adapt Through Interaction: Learning From Conversations?</u></a></li>
<li><a href="https://youtube-videos.techidaily.com/elevate-views-prime-seo-equipment-for-videos/"><u>Elevate Views Prime SEO Equipment for Videos</u></a></li>
<li><a href="https://win-hacks.techidaily.com/experience-copilot-pro-at-no-cost-the-ultimate-reasons-to-sign-up-today-insights-from-zdnet/"><u>Experience Copilot Pro at No Cost: The Ultimate Reasons to Sign Up Today – Insights From ZDNet</u></a></li>
<li><a href="https://win-hacks.techidaily.com/how-genai-is-revolutionizing-developer-workflow-insights-on-increased-productivity-in-software-projects/"><u>How GenAI Is Revolutionizing Developer Workflow: Insights on Increased Productivity in Software Projects</u></a></li>
<li><a href="https://win-hacks.techidaily.com/how-microsofts-ai-integration-in-surface-pro-and-laptop-poses-a-challenge-to-apple-zdnet-insight/"><u>How Microsoft's AI Integration in Surface Pro and Laptop Poses a Challenge to Apple - ZDNET Insight</u></a></li>
<li><a href="https://win-hacks.techidaily.com/how-windows-11-captivates-engineering-minds-according-to-microsoft-insights-from-zdnet/"><u>How Windows 11 Captivates Engineering Minds, According to Microsoft - Insights From ZDNet</u></a></li>
<li><a href="https://win-hacks.techidaily.com/mastering-your-microsoft-365-plan-in-the-world-of-windows-11-with-guidance-by-experts-at-zdnet/"><u>Mastering Your Microsoft 365 Plan in the World of Windows 11 with Guidance by Experts at ZDNET</u></a></li>
<li><a href="https://win-hacks.techidaily.com/maximizing-workplace-efficiency-revitalizing-a-traditional-office-layout-for-enhanced-teamwork-insights-from-zdnet/"><u>Maximizing Workplace Efficiency: Revitalizing a Traditional Office Layout for Enhanced Teamwork - Insights From ZDNet</u></a></li>
<li><a href="https://win-hacks.techidaily.com/microsoft-shifts-strategy-expected-price-tags-on-future-windows-10-updates-revealed-zdnet/"><u>Microsoft Shifts Strategy: Expected Price Tags on Future Windows 10 Updates Revealed | ZDNet</u></a></li>
<li><a href="https://network-issues.techidaily.com/revitalize-graphic-performance-seamlessly-update-intel-hd-graphics-3000-driver-for-w10/"><u>Revitalize Graphic Performance: Seamlessly Update Intel HD Graphics 3000 Driver for W10.</u></a></li>
<li><a href="https://tech-recovery.techidaily.com/selecting-an-ipad-understanding-which-versions-have-native-gps-functionality/"><u>Selecting an iPad: Understanding Which Versions Have Native GPS Functionality</u></a></li>
<li><a href="https://win-hacks.techidaily.com/simplifying-communication-across-sectors-with-microsoft-teams-the-combined-work-life-and-study-app-insights-from-zdnet/"><u>Simplifying Communication Across Sectors with Microsoft Teams: The Combined Work, Life, and Study App - Insights From ZDNet</u></a></li>
<li><a href="https://easy-unlock-android.techidaily.com/top-apps-and-online-tools-to-track-poco-c65-phone-withwithout-imei-number-by-drfone-android/"><u>Top Apps and Online Tools To Track Poco C65 Phone With/Without IMEI Number</u></a></li>
<li><a href="https://win-amazing.techidaily.com/up-to-date-nvidia-drivers-available-here-geforce-rtx-3080-for-windows-users/"><u>Up-to-Date NVIDIA Drivers Available Here: GeForce RTX 3#080 for Windows Users</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1896541/19272" target="_top" id="1896541">
  <img src="//a.impactradius-go.com/display-ad/19272-1896541" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1896541/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

