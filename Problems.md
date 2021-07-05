## **How to fix "Trial Version Expired"**

<http://oecake.wikia.com/wiki/Patch:_How_to_fix_%22Trial_Version_Expired%22>

## \[Solved\] Shader is not working (Acer laptop) Anytime

My OeCake is working fine, but i cannot get the shader to work. If i press 7 or use the Style: Shader, it will not work. I tried to find a picture of the oecake shader background and i found one but i tried to use it as my oecake background by clicking "Load Background" and i clicked on it, but it did'nt work.

## [ Game](/UserGdude2002.md "User:Gdude2002") hides half of the bottom screen (Windows Vista) Sunday, June 24, 2012

When I downloaded this game, I saved it to my SanDisk USB Thumbdrive (1.00 GB) and when I run it, the bottom of the screen where the physics are just dissapears. Also part of the top screen is white and when I create walls/water/anything from the menu, it spawns just 3 inches from where I want it to spawn. I would appreiate any assistance.

### Game runs too fast (MacOS) \[Solved\]

Apparently it was the TimeStepsPerFrame parameter that had changed itself. I want to request a function that allows to reset parameters to default. Nothing worse than parameters out of place, with no Return to Default function. Great game!

\_\_\_\_\_\_\_\_

Sometimes (now all the time), the game is running too fast. It's like playing a really old game on a really fast computer and everything just goes too fast. The water falls too quickly, your whole screen will be flooded with outflow in the matter of no time and.. yeah. I have played the game on windows without this problem, but on my mac (newest OS) it occurs. Shutting down the program and starting it again doesn't fix it. Also, as normal when a lot of physics come into play, the game is slowed down. So, if you're having a lot of water floating around it will slow down to normal speed. (Where it would normally turn laggy)

Solution: Make a big bar on the top of the screen and fill it fith water to create lag. This might just work!

[TobyBDK](/UserTobyBDK.md "User:TobyBDK") 21:56, August 7, 2010 (UTC)

## Open problems

### OE-Cake refuses to open on a Mac.

Oe Cake doesn't want to open on Snow Leopard Macbook 1.1 or Leopard Version 10.5.2.

Same thing happened to me too. Leopard Version 10.5.2.

Same. Any known fixes? I have the OLD demo, but I want to run the new version!

22:55, June 1, 2010 (UTC)22:55, June 1, 2010 (UTC)22:55, June 1, 2010 (UTC)[76.127.153.242](/SpecialContributions76.127.153.242.md "Special:Contributions/76.127.153.242") 22:55, June 1, 2010 (UTC)

The absolute new version (OECAKE 2 if you like) does NOT run on any mac or linux PCs, as far as I'm aware.
As this version goes, I have no idea. If you downloaded the copy we link to, it could just be that copy - look here: <http://www.mediafire.com/?m5oqzijemyx>

[Gdude2002](/UserGdude2002.md "User:Gdude2002") 14:31, June 3, 2010 (UTC)

I had about the same thing happen with 1.1.2b on Snow Leopard 10.6.4. Turned out the executable inside the .app bundle had lost its executable bit. Control-click the app, Show Package Contents, browse to Contents/MacOS/OE-CAKE!. Open Terminal and type in:

chmod +x

Note: space at the end of that. Now drag the OE-CAKE! from inside MacOS into Terminal to insert its full path. Press enter. Now try to run OE-Cake!.

Also, one zip I downloaded somewhere had a version that said it was expired when I run it. Either download a different one, or: Open the actual executable (in whatever.app/Contents/MacOS/) in a hex editor, search for "OE_EXPIRED" and change the date shortly before that to all # signs. My working executable's expiration date is "####-##-## 00:00:00 +0000".

### OE-Cake not showing on windows but using CPU power

So I was going to try and play OE-Cake today. But to my suprise it didn't work. I tried both a shortcut and the actual Executable. I also tried to start as administrator, no use. I tried to go on the net to seach for a solution but then my computer was VERY slow(and I have a monster rig). I checked task manager and saw several OE-Cake processes using lots of CPU power. I closed them all and downloaded a new OE-Cake incase my pack was broken. Same problem. Does anyone have a solution to this problem?

#### Solution

Mac- force quit
windows- control- alt - delete, processes tab, hit the "process name" sorting option, find [OEC.exe](/OEC.exe.md "OEC.exe") and click it then right click and choose "show process". this solved it for me. [\~if at first you don't suceed skydiving is not your sport](/UserVoldemort1.md "User:Voldemort1") 23:16, November 29, 2009 (UTC)

[87.248.19.122Robtherobot](/SpecialContributions87.248.19.122.md "Special:Contributions/87.248.19.122")[87.248.19.122](/SpecialContributions87.248.19.122.md "Special:Contributions/87.248.19.122")

## Lag Problem

For some reason my OE cake lags like hell. It takes atleast 10 seconds to have a dot of wall appear, let alone filling a cup with water. Is there any way to fix this, or is my computer just really bad? Thanks in advance, -[Mannface](/UserUnclever%20Name.md "User:Unclever Name") 01:51, January 13, 2012 (UTC)

Solution

Make OeCake smaller by putting the cursor on the top of the screen. Then, do the same with the sides. If this does'nt work, click the two squares in the top right corner. This shoild work.

## Solved Problems

### Windows package has invalid files

I downloaded OeCakeWin.7z today and found that files in the main folder are all of 0 bytes:

`> 7za l OeCakeWin.7z`  
  
`7-Zip (A) 4.65  Copyright (c) 1999-2009 Igor Pavlov  2009-02-03`  
  
`Listing archive: OeCakeWin.7z`  
  
`Method = LZMA`  
`Solid = -`  
`Blocks = 59`  
`Physical Size = 2100333`  
`Headers Size = 1590`  
  
`   Date      Time    Attr         Size   Compressed  Name`  
`------------------- ----- ------------ ------------  ------------------------`  
`2008-04-17 12:49:22 ....A        63344         7934  demo\action.oec`  
`...`  
`2008-04-24 14:09:12 ....A        51266        42591  demo\woods.tiff`  
`                    .....            0            0  glew32.dll`  
`                    .....            0            0  mfc80.dll`  
`                    .....            0            0  mfc80u.dll`  
`                    .....            0            0  mfcm80.dll`  
`                    .....            0            0  mfcm80u.dll`  
`                    .....            0            0  Microsoft.VC80.MFC.manifest`  
`                    .....            0            0  OE-CAKE!âwâïâv.chm`  
`                    .....            0            0  OE-CAKE!Ägùpïûæ°î_û±Åæ.pdf`  
`                    .....            0            0  OECake.exe`  
`                    .....            0            0  Äné_é+é¿ôAé▌é¡é¥é▌éó.txt`  
`2009-06-01 23:00:15 D....            0            0  demo`  
`------------------- ----- ------------ ------------  ------------------------                               7908812      2098743  69 files, 1 folders`

Please fix the Windows package.

[192.163.20.231](/SpecialContributions192.163.20.231.md "Special:Contributions/192.163.20.231") 05:58, September 4, 2009 (UTC)

---
I'll go take a look now. Did you try extracting them?
[Gdude2002](/UserGdude2002.md "User:Gdude2002")15:16, September 4, 2009 (UTC)
---

Yep, you're right. I'm reuploading them as .zip files, seems like my machine isn't fond of 7zip :P
I'll post here when the page is updated. If it doesn't work after that, then please clear your cache and reload the page.
[Gdude2002](/UserGdude2002.md "User:Gdude2002") 15:25, September 4, 2009 (UTC)

---

Okay, I've added mediafire mirrors. The system's a bit odd right now, as we moved to a VPS and te indexing isn't working yet.

Thanks for your patience.

Please refresh the page here and you'll find the links: <http://www.pearsoncoles.com/gareth/oecake.htm>

[Gdude2002](/UserGdude2002.md "User:Gdude2002") 15:47, September 4, 2009 (UTC)

---

Hi,

Thanks for re-uploading. However, the new URL shows 404 page: <http://www.pearsoncoles.com/files/oecake/Oe-cake_win.zip%C2%A0>;:(

I hope this URL is correct.

Please help!

[59.92.205.224](/SpecialContributions59.92.205.224.md "Special:Contributions/59.92.205.224") 12:58, September 5, 2009 (UTC)

---

No, the link is fine. But go to <http://www.pearsoncles.com/gareth> and click on OE-Cake, and you'll find mediafire mirrors.

[Gdude2002](/UserGdude2002.md "User:Gdude2002") 20:43, September 5, 2009 (UTC)

---

It's working. Thanks!

[59.92.156.73](/SpecialContributions59.92.156.73.md "Special:Contributions/59.92.156.73") 03:40, September 6, 2009 (UTC)

---

You're welcome! Thanks for visiting :P

[Gdude2002](/UserGdude2002.md "User:Gdude2002") 08:30, September 7, 2009 (UTC)

### **OE-Cake show Error message that says "Trial Version Expired"**

**i have use OE-CAKE for 2 month**

  
Set your PC Time back to before November 5th [Kilandor](/UserKilandor.md "User:Kilandor") 08:05, November 21, 2009 (UTC)

<!-- -->

  
oddly it says that the trial version is expired on November 5th, 2008, but any time before November 5th will work.

Also, it is oddly it will work in 2010, so you can set time forward too.\\

(=== Problem on the date of 11/6/11 === )

I try to open OECake and it gives the same error message, I have tried to downlaod it from different places, but it still doesn't work.

===

(===OE-CAKE just stopped running 11/6/10**===)**

  
I played OE-CAKE just fine two days ago, but now I am getting the "Trial Version Expired" message. I run OE-CAKE on my flash drive at a public library computer, so I can't change the system time. Is there another fix I could try?

UPDATE: Just tried to start up OE-CAKE today (12/4/10) and now it works again for some reason. I hope it keeps working!

UPDATE: Nope. Dead again today. (12/6/10)

## <u>Shader graphic is pitch black</u> and only solids and fires particles (the things that come up from the fire) show up

What do I do?

(11/2/10)  
I have this same problem too. Help!

ANSWERGUY SAYS:

The answer is that your physical computer has a out-dated graphic card.

---

**My OE-CAKE says "Driver mismatch componets"**

my problem is that the shader does not work (not shown the effects of light and shadow that was to appear, I put shader and the blob is in the style and texture), I was looking at the readme file and I saw something about OpenGL and pixel shader, which is that if varsao them?

---

when i try to run oe cake all it says is "application failed to initialize click ok to terminate the application" but when i click ok another window pops up and says "oe cake has stopped working windows will try to look for a solution" and then it doesn't give me a solution it just closes i got windows vista.

[Category:My OE-Cake can't run on blur, blur with texture, shader or even circles with lagging please help.](/CategoryMy%20OE-Cake%20can%27t%20run%20on%20blur%2C%20blur%20with%20texture%2C%20shader%20or%20even%20circles%20with%20lagging%20please%20help.md "Category:My OE-Cake can't run on blur, blur with texture, shader or even circles with lagging please help.")
