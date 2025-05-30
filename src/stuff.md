# Stuff

Here I'm putting useful commands, dotfiles and links to remember. 

---

# Links

I love:
- [Owls in Towels](https://owlsintowels.org/)
- [Electron Band Structure In Germanium, My Ass](https://web.archive.org/web/20001031193257/http://www.cs.wisc.edu/~kovar/hall.html)
- [Max Carr's PCT blog](https://pct.maxcarr.com/posts)


---

# Commands

To convert a bunch of images from one format to another via `ImageMagick`: 
```bash
mogrify -format jpg *.heic
```

---

# Dotfiles

<details>
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


