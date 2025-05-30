# Stuff

Here I'm putting useful commands, dotfiles and links to remember. 

---

# Commands

To convert a bunch of images from one format to another via `ImageMagick`: 
```bash
mogrify -format jpg *.heic
```

---

# Dotfiles

<details open>
<summary>
Alacritty
</summary>

Located at `~/.config/alacritty/alacritty.toml`.
```toml
[env]
TERM = "xterm-256color"

[window]
opacity = 0.8
blur = true

[window.dimensions]
columns=100
lines=30

[font]
normal.family = "MesloLGS NF"
size = 12
```
</details>


