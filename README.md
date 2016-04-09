# i3-config

Hi everybody

this shall be a summary of my personal `i3`, `i3bar`, `xinit` etc config files that I personally use.
If you like something you see feel free to use it, if you see something you don't, feel free to comment
and suggest changes. And never forget to have fun!

***

# Prerequisitse

## i3

`i3`is a dynamic tiling window manager for X-Server. To install `i3` on Arch Linux run
```shell
  sudo pacman -S i3
```
Enable `i3` by adding following to your `~/.xinitrc`
```shell
  exec i3
```

`i3status` is the most common tool to get system information to your panel. I use `i3blocks` to have different colours for each entry e. g. cpu usage

## i3blocks

For installation on Arch Linux from `AUR` run
```shell
  yaourt -S i3blocks.
```
For the Icons download the ttf files and copy them to
```shell
  cp *.ttf ~/.local/share/fonts
```
and finally reload fonts
```shell
  fc-cache -fv
```

## zsh

`Zsh` is a powerful shell that operates as both an interactive shell and as a scripting language interpreter. It offers many advantages such as:

- Efficiency
- Improved tab completion
- Improved globbing
- Improved array handling
- Full customisability

The good part is you don't have to configure zsh from scratch for the configuration of zshrc see [oh-my-zsh] (https://github.com/robbyrussell/oh-my-zsh)


## screenshot

![roarvo i3-config](https://raw.github.com/Soundsphere/i3-config/master/Screenshot2016-04-0711:58:00.png "roarvo i3-config")
