# i3-config

Hi everybody

this shall be a summary of my personal `i3`, `i3bar`, `xinit` etc config files that I personally use.
If you like something you see feel free to use it, if you see something you don't, feel free to comment
and suggest changes. And never forget to have fun!

***
![roarvo i3-config](https://raw.github.com/roarvo/i3-config/master/Screenshot.png "roarvo i3-config")
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

## conky

For installation on Arch Linux from `AUR` run
```shell
  sudo pacman -S conky
```
For the Icons download the ttf files and copy them to
```shell
  cp *.ttf ~/.local/share/fonts
```
and finally reload fonts
```shell
  fc-cache -fv
```

### set up conky in i3

copy `conky` to your i3 folder i. e. `.i3/` or in my case I have stored everything in `.config/i3/`

to enable `conky` in `i3bar` include the following into your i3 config in the section for bar`.config/i3/config`
```shell
	bar {
		...
		status_command $HOME/.config/i3/conky
		...
	}
```

## configure gpg for mutt
First create a pair of public/private keys:
```shell
	gpg --gen-key
```
Create a file in a **secure environment**
```
	~/.mutt
	***
	set my_pass = "<password>"
```
> Note: User defined variables **must** start with `my_`

Now encrypt the file:
```shell
	gpg -e -r '<name>' ~/.mutt
```
> Note: <name> must match the given name in key creation

You can now delete the file with cleartext password
```shell
	shred -xu ~/.mutt
```
`muttrc` is already set up right with `source ...` to load password, etc.

## zsh

`Zsh` is a powerful shell that operates as both an interactive shell and as a scripting language interpreter. It offers many advantages such as:

- Efficiency
- Improved tab completion
- Improved globbing
- Improved array handling
- Full customisability

The good part is you don't have to configure zsh from scratch for the configuration of zshrc see [oh-my-zsh] (https://github.com/robbyrussell/oh-my-zsh)
