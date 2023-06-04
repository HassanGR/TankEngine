# Friday Night Funkin' - Tank Engine
A Psych Engine modification, intended to fix vanilla and Psych Engine version's many issues while keeping most of the casual play aspect of it.

# Installation:
You must have [the most up-to-date version of Haxe](https://haxe.org/download/) *(sometimes you have to downgrade though)*, seriously, stop using 4.1.5, it misses some stuff.

### Dependencies
• Git

• Haxe (Latest, not 4.2.X)

• VS Community (Windows only!. This guide provides instructions for installing VS!)

• 25 gigs of space (Windows only, due to Visual Studio and other shit)

• 1-5 gigs of space (Non-Windows)

• Some Command Line Knowledge (Ninjamuffin made a tutorial https://ninjamuffin99.newgrounds.com/news/post/1090480 or you can google)

**OPTIONAL Dependencies**

• VS Code [download](https://code.visualstudio.com/) *(for modifying code itself if you don't want to use VSC. VSC Isn't VS CODE!)*

• Sublime Text [download](https://www.sublimetext.com/)

### Recommended VS Code Extensions

• Lime

• HXCPP Debugger

• Tabline

# Downloads
## GIT
### Windows/Mac:

[Install Git](https://git-scm.com/downloads)

### Linux (Ubuntu/Debian based Distros):

*(replace apt with apt-get if necessary)*

```sudo apt update;sudo apt install git -y```

### Linux (Arch based Distros):

```sudo pacman -Sy git --noconfirm```


## Haxe

### Windows/Mac:

[Click here to download Haxe](https://haxe.org/download/)

### Linux (Ubuntu/Debian based Distros):

```
sudo add-apt-repository ppa:haxe/releases -y
sudo apt update
sudo apt install haxe -y
mkdir ~/haxelib && haxelib setup ~/haxelib
```


### Linux (Arch based Distros):

```
sudo pacman -Sy haxe --noconfirm
mkdir ~/haxelib;
haxelib setup ~/haxelib
```



## VS Community Setup(Windows Only)

***For Windows, you need to install Visual Studio Community from [here.](https://visualstudio.microsoft.com/downloads/). While installing VSC, don't click on any of the options to install workloads. Instead, go to the individual components tab and choose the following:***


• MSVC vXXX - C++ x64/x86 build tools

• Windows SDK (Latest version)

***It is recommended to reboot your PC once it finishes, but it's not required.***

## Terminal Setup & Compiling Game

• Windows: Press "Windows+R" and type in "cmd", if you don't like cmd, or you just use something different, open that program instead. Make sure to use normal CMD, not admin CMD

CMD is preinstalled, so it's easier to work with.

• Most Linux Distros: Usually you can find your Terminal in your applications menu, or press Ctrl+Alt+2-6 to open the TTY. Ctrl+Alt+7, Ctrl+Alt+1 or Ctrl+Alt+2 usually get you back to your desktop

• Mac: Press cmd+space and type "Terminal" into spotlight or open Launchpad and look for Terminal

Type in these commands:
```
haxelib git discord_rpc https://github.com/Aidan63/linc_discord-rpc
haxelib git linc_luajit https://github.com/superpowers04/linc_luajit
haxelib git hxvm-luajit https://github.com/nebulazorua/hxvm-luajit
haxelib install lime
haxelib install openfl
haxelib install flixel
haxelib install flixel-ui
haxelib install hscript
haxelib install flixel-tools
haxelib install flixel-addons
haxelib install actuate
haxelib install hxCodec
haxelib run lime setup
haxelib run lime setup flixel
haxelib run flixel-tools setup
```


***Read carefully when it prompts for you to do anything (like: setup the lime command, setup flixel tools, etc)***

`Run lime setup (PLATFORM)` (Replace (PLATFORM) with your device's platform. e.g windows, macos, linux, etc)

## Compiling Builds

To compile without running, run lime build (PLATFORM) (Replace platform with your device's platform)

Note that the first build will always be longer than the rest

If you get errors, refer to the forum posts in this channel before asking for help

**To compile & run, run `lime test PLATFORM`**

**Add a "-debug" flag at the end of your lime command**
### Examples:
`lime test windows`

`lime build linux -debug`

## Customization:

if you wish to disable things like *Lua Scripts* or *Video Cutscenes*, you can read over to `Project.xml`

inside `Project.xml`, you will find several variables to customize Psych Engine to your liking

to start you off, disabling Videos should be simple, simply Delete the line `"VIDEOS_ALLOWED"` or comment it out by wrapping the line in XML-like comments, like this `<!-- YOUR_LINE_HERE -->`

same goes for *Lua Scripts*, comment out or delete the line with `LUA_ALLOWED`, this and other customization options are all available within the `Project.xml` file

## Credits:
### * HassanGR - Modificator or somethin
* Shadow Mario - Programmer
* RiverOaken - Artist
* Yoshubs - Assistant Programmer

### Special Thanks
* bbpanzu - Ex-Programmer
* Yoshubs - New Input System
* SqirraRNG - Crash Handler and Base code for Chart Editor's Waveform
* KadeDev - Fixed some cool stuff on Chart Editor and other PRs
* iFlicky - Composer of Psync and Tea Time, also made the Dialogue Sounds
* PolybiusProxy - .MP4 Video Loader Library (hxCodec)
* Keoiki - Note Splash Animations
* Smokey - Sprite Atlas Support
* Nebula the Zorua - LUA JIT Fork and some Lua reworks
_____________________________________

# Features

## Attractive animated dialogue boxes:

![](https://user-images.githubusercontent.com/44785097/127706669-71cd5cdb-5c2a-4ecc-871b-98a276ae8070.gif)


## Mod Support
* Probably one of the main points of this engine, you can code in .lua files outside of the source code, making your own weeks without even messing with the source!
* Comes with a Mod Organizing/Disabling Menu.
