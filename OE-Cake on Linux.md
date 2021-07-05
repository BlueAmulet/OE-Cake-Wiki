![OE-Cake working in Ubuntu 10.10 Desktop Edition.](/images/OE-Cake%20Linux%20Demo.png "OE-Cake working in Ubuntu 10.10 Desktop Edition.")I know this tutorial will be simple, but people think it will be a chore just to get OE-Cake running on a non-Windows OS. It's not a chore and this tutorial will help you.

<u>***STATUS:***</u>

-   ***OE-Cake*-**Works! You need to change your graphics mode on OE-Cake though.
-   ***Recipe Helper*-**Does NOT work, yet. The program will run, but it won't do anything.

## You will need...

-   The development release of WINE (free) or the latest version of Codeweaver's CrossOver or CrossOver Games (not free). WINE is an implementation of the Windows API for non-Windows OSes and CrossOver is the paid version of it, designed for the Mac, mostly. The development release was picked because you get the bugfixes and new features first with the dev release.
-   Linux or Mac OS X... isn't this the obvious one?
-   *If you have Linux, make sure your graphics card is Linux-capable and won't lag bad. I use a stupid Intel GMA card on my PC and it used to lag little on Windows but now on Linux? OpenGL needs to power everything, OE-Cake cannot run on OpenGL, but if your graphics card is crap, use the Circles options, they make a Minecraft feel on Linux instead of being circle for some reason!*

## Step 0.5: Get the development release of WINE.

WINE needs to be installed before you do anything. If you have the stable version, get rid of it! Look for your distribution and download it. It may give you different instructions (example: Ubuntu tells you to add a source to your software repositories.)

## Step 1: Install the Visual C++ 2005 Redistributable.

This is required by OE-Cake. Run the installer and check in "Uninstall WINE Software" for the redist.

## Step 2: Just run it!

With the new redistributable and the dev release of WINE, you now have OE-Cake

### **What works**

-   Basic drawing
-   Settings
-   Basically everything in OE-Cake

### **What doesn't work**

-   Circles are squares, but hey, it gives off a Minecraft-esque 8-bit feel that isn't 8-bit or Minecraft.
-   Blobs won't work. Nor the "textured" version.

## Other Options

OE-Cake is a relatively simple game. Performance under a Virtual Machine should be reasonable. If possible you should create an OSX machine to get a version of OE-Cake with more features. The [Darling Project](https://www.darlinghq.org) may be something to look into.
