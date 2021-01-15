# My build of [dwm - the dynamic window manager](https://dwm.suckless.org/)

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

Available in the AUR as [dwm-monosans-git](https://aur.archlinux.org/packages/dwm-monosans-git/)
Add `exec dwm` to your `.xinitrc` file.

## Installation on other distributions

```
git clone https://github.com/monosans/dwm
cd dwm
sudo make clean install
```
Add `exec dwm` to your `.xinitrc` file.

## Note on emojis and special characters in status bar

If dwm crashes when displaying emojis, install [libxft-bgra](https://aur.archlinux.org/packages/libxft-bgra) or [libxft-bgra-git](https://aur.archlinux.org/packages/libxft-bgra-git) from the AUR.

## Note for multi-monitor users

Multi-monitor is disabled in `config.mk` by default. Also keybindings for multi-monitor setups are not set, but you can get them from the [original config](https://git.suckless.org/dwm/file/config.def.h.html).

## Note for OpenBSD users

Be sure to edit `config.mk` by commenting 18th line `FREETYPEINC = /usr/include/freetype2` and uncommenting 20th line.

## Uninstallation on Arch Linux

`sudo pacman -Rns dwm-monosans-git`

## Uninstallation on other distributions

```
git clone https://github.com/monosans/dwm
cd dwm
sudo make clean uninstall
```
Remove `exec dwm` from your `.xinitrc` file.
