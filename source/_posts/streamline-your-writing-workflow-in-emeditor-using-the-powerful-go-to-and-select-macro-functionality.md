---
title: Streamline Your Writing Workflow in EmEditor Using the Powerful 'Go To and Select...' Macro Functionality.
date: 2024-10-08T16:54:39.700Z
updated: 2024-10-11T17:00:00.988Z
tags:
  - product
categories:
  - emeditor
thumbnail: https://thmb.techidaily.com/0313aeb6801c4ad054aee4b20ba488ff337dac52c595922f616f6d67ab2cd3c7.jpg
---

## Streamline Your Writing Workflow in EmEditor Using the Powerful 'Go To and Select...' Macro Functionality.

Viewing 2 posts - 1 through 2 (of 2 total)

* Author  
Posts
* July 27, 2012 at 2:13 pm [#10464](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/f29c043a3cc5c5dac8db4e62939893e9?s=80&d=identicon&r=g)Stefan](https://www.emeditor.com/forums/users/Stefan/ "View Stefan's profile")  
Participant  
 1.) GoTo and select   **n lines down or up**  
/*  
	Just an simple script to select an exact amount of lines.  
	    
	Useful e.g. to select next 1000 lines from an log to export.  
	Or to select always 10 header lines of an block to remove them.  
	Or to use with your file manager: export the list of file names,  
	paste them into EmEditor, use this script to select 30 lines,  
	copy them to the clipboard, ask your file manager  
	to "select from clipboard", done! ('TC' will do for example)  
	    
	How-to:  
	First put your cursor at the begin of an line.  
	Then execute this script and enter the amount of lines to select  
	and after an comma the direction to select to: down or up.  
	Note: the script will check for lower case char 'd' and 'u'.  
	The syntax for the command is: <number><comma><d/u> like: 5,d  
	Or just <number> or even < -number>.  
	*/  
	    
	//Ask the user what to do:  
	UserInput  = "Amount of lines to select and direction, ";  
	UserInput += "e.g.: 10,u  for 10 up, or 3,d for 3 down.";  
	UserInput  = prompt(UserInput, "10,d");  
	    
	//Check the user input:  
	if (UserInput == "") {quit();}  
	if (UserInput.indexOf(",") > -1){  
		CmdArray = UserInput.split(",");  
		cmdAmount = CmdArray[0];  
		  if (/^d*$/.test(cmdAmount)  == false){funcSyntax();}  
		cmdDirect = CmdArray[1];  
		  if (/^[ud]$/.test(cmdDirect) == false){funcSyntax();}  
	}else{  
		//simple form of user-input: just the amount of lines.  
		//Direction is 'd' as default:  
		cmdAmount = UserInput;  
		cmdDirect = "d";  

	    
	//Execute the command:  
	if (cmdDirect == 'd')  
		document.selection.LineDown(true,cmdAmount);  
	if (cmdDirect == 'u')  
		document.selection.LineUp(true,cmdAmount);  
	    
	//Used functions:  
	function funcSyntax(){  
		info  = "error: "+UserInput+"nnn";  
		info += "Use     "Amount-comma-direction",nn";  
		info += "e.g.:   "10,d"    to select 10 lines downn";  
		info += "   or    "3,u"     to select 3 line up."  
		alert(info);  
		quit();  

	July 28, 2012 at 2:15 pm [#10465](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/f29c043a3cc5c5dac8db4e62939893e9?s=80&d=identicon&r=g)Stefan](https://www.emeditor.com/forums/users/Stefan/ "View Stefan's profile")  
Participant  
 2.) GoTo and select   **to line X**  
 Purpose:  
 select the lines from start line to line number X.  
 Where X is a line number you entered to go to.  
 Tip; Line X can be below or above current line.  
 2a) EmEditor internal commands:  
 To select an block:  
 \* set your cursor on the start of the line you want  
 \* press F8 to set “begin of block marker”  
 \* press Ctrl+G and enter the line number to go to  
 (Tip: press ESC to leave selection mode)  
 To select whole lines:  
 \* same as above but press Ctrl+F8  
 To select an rectangular/vertical block:  
 \* set your cursor on the line and column you want  
 \* press Ctrl+Shift+F8 to set “begin of block marker”  
 \* press Ctrl+G and enter the line and column number to go to  
 (Tip: press ESC to leave selection mode)  
 Search the help for “F8”:  
> EmEditor Help – How to – Edit  
> To Select a Portion of a Document  
>  
> Click at the beginning of the selection,  
> move the mouse to the end of the selection while holding  
> the left mouse button down, and then release the mouse button.  
>  
> Tips  
> Alternatively, press arrow keys while pressing the SHIFT key.  
> Alternatively, press the F8 key, and then press arrow keys.  
> To select lines, click on the left edge of the window,  
> or press CTRL + F8\.  
> To select vertically (in a rectangular block), use the  
> mouse to select while pressing the ALT key,  
> or press SHIFT+ CTRL + F8.  
 2b) If you want to use an script for that,  
 the following code could be an start:  
 To select an block:  
 \* set your cursor on the line you want  
 \* execute this script and enter the line number to go to  
o = document.selection;  
	yPos = o.GetActivePointY(eePosLogical);  
	TargetLine = prompt("Select to line:","");  
	o.LineDown(true, (TargetLine - yPos));  
 To select whole lines:  
 – start at begin of line  
 – at the end hold Shift-key and press End-key  
 Or add this to the end of the script:  
 document.selection.EndOfLine(true, eeLineLogical);  
 To select an rectangular/vertical block:  
 – i will post next…  
 .
* Author  
Posts

Viewing 2 posts - 1 through 2 (of 2 total)

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
<li><a href="https://facebook-record-videos.techidaily.com/new-unlock-mastery-the-beginners-guide-to-editing-excellence/"><u>[New] Unlock Mastery The Beginner's Guide to Editing Excellence</u></a></li>
<li><a href="https://voice-adjusting.techidaily.com/2024-approved-the-elite-selection-of-virtual-audio-editing-experts/"><u>2024 Approved The Elite Selection of Virtual Audio Editing Experts</u></a></li>
<li><a href="https://hardware-help.techidaily.com/dark-mode-vs-light-mode-adjust-your-androids-background-settings-with-ease/"><u>Dark Mode Vs. Light Mode: Adjust Your Android's Background Settings with Ease</u></a></li>
<li><a href="https://screen-activity-recording.techidaily.com/download-verbatim-excerpt/"><u>Download Verbatim Excerpt</u></a></li>
<li><a href="https://win-hacks.techidaily.com/effortless-conversion-free-software-for-changing-powerpoint-presentations-into-flash-swf-files/"><u>Effortless Conversion: Free Software for Changing PowerPoint Presentations Into Flash (.swf) Files</u></a></li>
<li><a href="https://win-hacks.techidaily.com/expert-tips-for-not-displaying-flipbuilder-sites-in-your-ebooks-web-address/"><u>Expert Tips for Not Displaying FlipBuilder Sites in Your eBook's Web Address</u></a></li>
<li><a href="https://win-hacks.techidaily.com/guide-to-setting-up-downloadable-ebooks-on-your-website-via-flipbuilder/"><u>Guide to Setting Up Downloadable eBooks on Your Website via FlipBuilder</u></a></li>
<li><a href="https://techno-recovery.techidaily.com/hook-up-disney-plus-streaming-service-to-google-chromecast-a-simple-how-to/"><u>Hook Up Disney Plus Streaming Service to Google Chromecast - A Simple How-To</u></a></li>
<li><a href="https://win-hacks.techidaily.com/how-to-batch-convert-your-ppt-presentations-into-digital-flipbooks-with-ease-discover-flipbuilders-powerful-feature/"><u>How to Batch Convert Your PPT Presentations Into Digital Flipbooks with Ease - Discover FlipBuilder's Powerful Feature</u></a></li>
<li><a href="https://win-hacks.techidaily.com/how-to-create-an-engaging-flipbook-ebook-with-images-by-using-txt-files-on-flipbuildercom/"><u>How to Create an Engaging Flipbook EBook with Images by Using TXT Files on FlipBuilder.com</u></a></li>
<li><a href="https://win-hacks.techidaily.com/how-to-resolve-issues-with-the-download-feature-at-flipbuildercom/"><u>How to Resolve Issues with the Download Feature at FlipBuilder.com</u></a></li>
<li><a href="https://techidaily.com/how-to-transfer-data-from-apple-iphone-14-pro-max-to-others-ios-devices-drfone-by-drfone-transfer-data-from-ios-transfer-data-from-ios/"><u>How To Transfer Data From Apple iPhone 14 Pro Max To Others ios devices? | Dr.fone</u></a></li>
<li><a href="https://win-hacks.techidaily.com/incorporating-your-brands-logo-into-a-flipbook-background-with-ease/"><u>Incorporating Your Brand's Logo Into a FlipBook Background with Ease</u></a></li>
<li><a href="https://tech-revival.techidaily.com/protecting-your-child-online-5-essential-practices-for-safe-usage-of-chatgpt/"><u>Protecting Your Child Online: 5 Essential Practices for Safe Usage of ChatGPT</u></a></li>
<li><a href="https://win-howtos.techidaily.com/1723208693075-unlocking-success-expert-advice-for-tackling-and-repairing-error-1603-on-your-device/"><u>Unlocking Success: Expert Advice for Tackling and Repairing Error 1603 on Your Device.</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2137413/7443" target="_top" id="2137413">
  <img src="//a.impactradius-go.com/display-ad/7443-2137413" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2137413/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

