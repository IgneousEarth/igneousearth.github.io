# Useful stuff

Here I'm putting useful commands, dotfiles and links to remember. 

---

# Links

I love:
- [Owls in Towels](https://owlsintowels.org/)
- [Electron Band Structure In Germanium, My Ass](https://web.archive.org/web/20001031193257/http://www.cs.wisc.edu/~kovar/hall.html)
- [Max Carr's PCT blog](https://pct.maxcarr.com)


---

# Commands

To convert a bunch of images from one format to another via `ImageMagick`
```bash
mogrify -format jpg *.heic
```

To convert some audio files from one sample/depth to another via `sox`
```bash
mkdir converted; for flac in *.[Ff][Ll][Aa][Cc]; do sox -S "$flac" -R -G -b 16 converted/"$flac" rate -v -L 44100 dither; done
```

To enable scientific notation in `qalc`
```bash
set exp # set exp 0 to disable
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

<details>
<summary>
Last command in Fish (!!)
</summary>

Put in `~/.config/fish/config.fish`.
```
function last_history_item; echo $history[1]; end
abbr -a !! --position anywhere --function last_history_item
```
</details>
