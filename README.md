# My build of dwm - the dynamic window manager

The [dynamic window manager (dwm)](https://dwm.suckless.org/) with some additional features.

## Features

+ New clients attach at the bottom of the stack instead of the top.
+ System tray.
+ Bar is shown when Super key is pressed.

## Main bindings

+ **dmenu** - `Super+d`
+ **st** - `Super+Enter`
+ **Kill client** - `Super+Shift+q`
+ **View tag** - `Super+TagNumber`
+ **Move client to other tag** - `Super+Shift+TagNumber`
+ **Change client's size** - `Super+{h, l}`
+ **Swap stack with master** - `Super+s`
+ **Change number of masters** - `Super+{i, o}`
+ **Toggle floating** - `Super+Shift+Space`
+ **Change focus** - `Super+{j, k}`
+ **Toggle bar** - `Super+p` or hold `Super`
+ **Resize floating client** - `Super+ClickMouseWheel`
+ **Move floating client** - `Super+LeftMouseButton`
+ **Quit dwm** - `Super+Shift+Ctrl+c`

## Installation on Arch Linux and Arch Linux based distributions

Available in AUR as [dwm-monosans-git](https://aur.archlinux.org/packages/dwm-monosans-git/)

## Installation on other distributions

```
git clone https://github.com/monosans/dwm
cd dwm
sudo make clean install
```

## Note for multi-monitor users

Multi-monitor is disabled in `config.mk` by default. There is also no keybindings for multi-monitor setups, but you can get them from the [original config](https://git.suckless.org/dwm/file/config.def.h.html).

## Note for OpenBSD users

Be sure to edit `config.mk` by commenting 19th line `FREETYPEINC = /usr/include/freetype2` and uncommenting 21th line.

## Uninstallation on Arch Linux

`sudo pacman -Rns dwm-monosans-git`

## Uninstallation on other distributions

```
git clone https://github.com/monosans/dwm
cd dwm
sudo make clean uninstall
```
