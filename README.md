# Athanasius
#### Rice Manager

Athanasius is a set of bash utilities and themes to handle switching between rices easily. Athanasius links utilities like rofi and lemonbar and picom to a scripts folder which makes it easy to switch between rices without changeing invocation commands or config files. The rices included are aimed at [MMWM](https://github.com/kaugm/mmwm) but are somewhat compatible with other WM's. It aims to make ricing easy my making a scripts that can run on any machine by relying a config file called athanasius.conf. The included scripts make it easy to shift between machines and share configs by detecting the correct variables and frontloading the work of making your scripts compatible with other systems. For example, instead of sharing a bar script which detects whether the user is running pulseaudio or alsa, the scripts AWMgetvolume and AWMgetmute are already symlinked the correct script in the default_scripts directory.

The included themes make use of lemonbar-xft over polybar or yabar to cut down on system resource usage. Each theme includes a bar which can pull system information seamlessly without prior configuration. The bars update volume and battery in real time without the need for loops or external scripts by reading the output of acpi_listen.

## Usage
The setup script will automatically detect your battery, audioservice (pulseaudio or alsa), network interface, and WM and adjust its scripts accordingly.

#### AWMtheme

To set the current theme type AWMtheme 'themename'

example:
    $ AWMtheme leo

#### AWMmenu
The theme backend rices rofi by pointing to the correct config in a script called 'AWMtheme.' To use it just run:
    $AWMmenu

To get volume information or change volume

    $ AWMgetvolume

    $ AWMgetmute

    $ AWMaudioup

    $ AWMaudiodown

To change themes

    $ AWMtheme "theme"

To stop the current theme and all programs started by the theme

    $ AWMthemedown
#### Themes
To create a theme, simply add the config files you want to a directory in themes. The name of any theme is the name of the directory where config files are stored. Athanasius comes with five basic example themes to demonstrate the basic file structure.
## Michael
![michael](michael.png)
## Simeon
![simeon](simeon.png)
## Leo
![leo](leo.png)
## Bruno
![bruno](bruno.png)
## Akita
![akita](akita.png)


#### Theme Dependencies
    lemonbar-xft
    acpid
    rofi

    xdotool & xprop for michael theme


#### installation
1. clone the repo wherever you like
2. run the AWMsetup script
3. add 'AWMstart' to ~.xinitrc

Credits
------

#### Icon Font
The icon font is created entirely from free icons not made by me. The icon font is made up of the following:
[RemixIcons](https://remixicon.com/)
[Picol Icons](http://picol.org/)
[Font Awesome](http://fontawesome.io/)
[Ionicons](http://ionicons.com/)
[OctIcons](https://github.com/github/octicons)
[Elusive Icons](http://shoestrap.org/downloads/elusive-icons-webfont/)
[Minicons](http://www.webalys.com/minicons/icons-free-pack.php)
[Foundation Icons](http://zurb.com/playground/foundation-icon-fonts-3)
[Entypo](http://www.entypo.com/)
[Metrize](http://www.alessioatzeni.com/metrize-icons/)
[Iconic](http://www.somerandomdude.com/work/iconic/)
[Steadysheets](http://steadysets.com/)
[Other Icons](http://othericons.com/)

#### Wallpapers
Wallpaper Photo by [eberhard grossgasteiger](https://www.pexels.com/@eberhardgross) from Pexels
wallpaper Photo by [Min An](https://www.pexels.com/@minan1398?utm_content=attributionCopyText&utm_medium=referral&utm_source=pexels) from Pexels
Wallpaper Photo by [Anni Roenkae](https://www.pexels.com/@anniroenkae) from Pexels
Wallpaper by [Dark Indigo](https://www.pexels.com/@darkindigo?utm_content=attributionCopyText&utm_medium=referral&utm_source=pexels) from Pexels
Wallpaper from [Imgur](https://imgur.com/TS5S3)

#### Bar scripts
The bar scripts borrow work from [fsfg](https://gitlab.com/fsfg/dotfiles/) and [nan0s7](https://github.com/nan0s7/drowsylemon)