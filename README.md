# Athanasius
#### Rice Manager

Athanasius is a set of bash utilities and themes to handle switching between rices easily. Athanasius links utilities like rofi and lemonbar and picom to a scripts folder which makes it easy to switch between rices without changeing invocation commands or config files. The rices included are aimed at [MMWM](https://github.com/kaugm/mmwm) but are somewhat compatible with other WM's.

#### Usage
The setup script will automatically detect your battery, audioservice (pulseaudio or alsa), and network interface and adjust its scripts accordingly.

To get volume information or change volume

    $ AWMgetvolume

    $ AWMgetmute

    $ AWMaudioup

    $ AWMaudiodown

To change themes

    $ AWMtheme "theme"

To stop the current theme and all programs started by the theme

    $ AWMthemedown

#### installation
1. clone the repo to ~/.config/athanasius/
2. run the AWMsetup script in ~/.config/athanasius/scripts/
3. add 'AWMstart' to ~.xinitrc