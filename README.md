*Note: this repo is meant to be used together with archinstall-ntprogram and dotfiles. Things might break if you use them reparately.*

Note: `us` is an existing keyboard layout file. We need to remove it so stow can override it with out own.
```
sudo rm /usr/share/x11/xkc/symbols/us
```
This file is also the reason we need root privileges. Probably shoulnd't be using it but ¯\\_(ツ)_/¯.

```
sudo stow target=/ --simulate .
sudo stow target=/ .
```

To set the GTK theme:
```
lxappearance
```
I use `Full-Dark-Red` for the theme and `HighContrast` icons.
