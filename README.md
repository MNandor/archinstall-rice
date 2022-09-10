# Archinstall Rice

A set of files to be gnu `stow`-ed when I reintall my OS.
`linux`

Please do both the cloning and the stowing as root so the ownership is set correctly.

`us` is an existing keyboard layout file. We need to remove it so stow can override it with out own.
```
sudo rm /usr/share/x11/xkc/symbols/us
```

```
sudo stow target=/ --simulate .
sudo stow target=/ .
```

To set the GTK theme:
```
lxappearance
```
I use `Full-Dark-Red` for the theme and `HighContrast` icons.

The greeter is configured separately:
```
sudo lightdm-gtk-greeter-settings
```

*Note: this repo is meant to be used together with archinstall-ntprogram and dotfiles. Things might break if you use them reparately.*
