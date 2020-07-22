<div align='center'>
	<h1>AwesomeWM</h1>
</div>

## My Setup ##

![](./images/screenshot.png)

## Connotation ##

- [My Setup](#my-setup)
- [Connotation](#connotation)
- [OS Details](#os-details)
- [About](#about)
- [Dependencies](#dependencies)
	- [Some Other Dependencies](#some-other-dependencies)
	- [Fonts](#fonts)
- [Installing](#installing)
- [File Structure](#file-structure)
- [Upcoming](#upcoming)

<a name='details'><a>
## OS Details ##
+ **OS**      : Fedora Workstation 32
+ **Shell**   : oh-my-zsh
+ **WM**      : awesomewm
+ **Theme**   : Juno gtk3 theme
+ **Icons**   : Tela Green
+ **Cursor**  : Adwaita
+ **Terminal**: kitty
+ **Editor**  : micro

<a name='about'></a>
## About ##
+ Lighter than usual desktop environments
+ Less RAM Usage and highly customizable
+ Very few dependencies required
+ Based on a programming langauge
+ No need to learn entire language
+ This configuration is based on the stable release of the awesomewm

<a name='dependencies'></a>
## Dependencies ##
The dependencies are kept as low as possible and are common for all distros so the
config can be used by anyone willing to use awesomewm. Also these packages will most likey be available in the package manager of your linux distro.

| Dependency package name | What it does? |
| :---------------------:| :-----------------:|
| `awesome` | Window Manager |
| `feh` | Command line tool for setting up the wallpaper |
| `picom` | Composite manager for window managers |
| `rofi` | Application launcher or menu |
| `ImageMagick` | Used for theming and wallpaper | 


### Some Other Dependencies ###

```bash  
xfce4-power-manager
```
This will be the extension for the battery management for the people using laptops.

```bash
nautilus
```
The file manager for our system. Alternatively, we can go for other apps as well like thunar but this is my preferred one.

```bash
bluez blueman
```
The bluetooth module for our system.

```bash
xbacklight
```
A module to control the brightness. But this has to be configured accoring to your machine. If it works out of the box, perfect but if not use this [guide](https://askubuntu.com/questions/823669/volume-sound-and-screen-brightness-controls-not-working).


### Fonts ###

The system font that has been used is [SF Text](https://github.com/perrychan1/fonts.git) or you can download from official Apple website.

Terminal Font is Fira Code by default. It is possible that the font is available in the official repositories of your distro so you can install it from there or you can download from [here](https://github.com/tonsky/FiraCode)

<a name='installing'></a>
## Installing ##

The installation of my awesomewm config is very simple if you met all the dependencies and the fonts.
To install, clone this repository onto your system and place all the files into 

```bash
~/.config/awesome
```
And here you go, enjoy your awesomewm journey!

<a name='file-structure'></a>
## File Structure ##

1. `apps.lua` : This file contains all the details about the apps. The default apps can be changed in the defaul.apps object and the apps that run on start-up can be changed on the run_on_start_up object.

2. `rc.lua`: This is actually the main file for awesomewm which connects all lua files in the directory. Alternatively, we can write all the contents of all the files into the rc.lua file but that will be very messy and lengthy so dividing it into multiple files makes it easier to maintain and understand what each module is responsible for. The theme for the awesomewm can be changed through `.Xresources` file saved in your home directory. If not, create one for your own theme.

3. `tags.lua`: This file is only for the numbering of workspaces. IF you want to change the text on the workspace indicator on the top panel, you just need to change the .png files in the `icons/tags` directory and it will show on the top panel.

4. `keys.lua`: This file contains the keybindings of the spawning and resizing of apps and the mod key. You can change everything by changing the name of the keyboard button.

5. `rules.lua`: This file contains the rules for window spawning, the window borders and the look of the windows. This file can also be used for declaring rules specific to a particular window.

6. `theme.lua`: This file contains the rules for the current theme and the dpi of gaps and if the gaps should be present if only a single window is spawned in a workspace. This file can also be used for declaring and using your own custom layout icons, by placing the icons in `icons/layouts` directory.

<a name='upcoming'></a>
## Upcoming ##

1. I will be updating the themes according to the wallpaper color schemes and will probably create a new branch for the newly themed version.

2. I will also document the code a little bit more and will explain the file structure for the beginners.

3. Will also be working on other wm configurations as I rice them XD