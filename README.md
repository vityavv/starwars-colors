# My dotfiles for starwars colors

### You can view my setup [here](https://imgur.com/gallery/tzppTdc)

Shoutout to `u/f_s_f_g_` of reddit for letting me use and modify their openbox config, and to `simonizor` on discord ([Discord Linux](https://discord.gg/discord-linux) for getting me into opensuse in the first place and getting me through all of the hard parts. Without them, this setup would not exist and my computer would probably be broken/unusable for a while.

The `SUSE-setup-rough-instructions.txt` is mostly notes for myself, but you can use them if you want

## How to set up all of this stuff
Make sure you have fira mono installed. If you do not like this font, I also recommend using Anonymous Pro, although that breaks with the newest version of URxvt

### ATOM

1. Copy `atom/starwars-syntax` to `~/.atom/packages/starwars-syntax`
2. Copy `atom/styles.less` to `~/.atom/styles.less`
3. Install Seti-UI and minimap
4. Set font to fira mono

### URxvt

1. Copy `.Xresources` to `~/.Xresources`
2. Run `xrdb ~/.Xresources`

### Openbox

1. In `~/.config/openbox/autostart`, set the wallpaper. I used `feh`, like this: `feh --bg-scale path/to/wallpaper.png`. The wallpaper can be found in `gvcci-out/wallpaper`, and it is a 2560x1440 jpeg.
2. Open obconf. Select `Create a theme archive (.obt)...`, and navigate to the folder that is *this repo* (*not* `openbox-3`). Press OK. Then, press `Install a new theme...`, and navigate to the `.obt` file you just created (it will probably be in your home folder). Finally, select this bt from the theme menu.
3. In obconf, under the `Appearance` panel, select `Windows retain a border when undecorated`
4. Edit `~/.config/openbox/rc.xml`. Under `<applications>`, put `<application class="*"><decor>no</decor></application>`
5. Run `openbox --reconfigure`

### rofi

1. Copy `config.rasi` to `~/.config/rofi/config.rasi`
2. That's it

### Polybar

1. Copy `polybar-config` to `~/.config/polybar/config`
2. Run `polybar victor`. You can also put `polybar victor &` into your openbox autostart (`~/.config/openbox/autostart`)

### Micro (not shown)

Micro is a terminal-based text editor that I've grown to like a lot. While I don't like the colorshceme I made for micro here, you can use it if you want.

1. In the micro folder there are three colorschemes. Use starwars3 if you have the terminal colors set to starwars colors. Otherwise, use starwars2. I don't know why I keep these around.
2. Move one of these colorschemes to `~/.config/micro/colorschemes`.
3. In micro, go into the prompt (Control-E) and type `set colorscheme starwars3`, using the name of the version you chose

### Editors other than Atom and Micro

I have included a `starwars.tmTheme` so you can use this theme with editors like sublime text or convert this file into a theme for the editor of your choice.

### Terminals other than URxvt

In `gvcci-out` there are colors in several different forms which you can apply to your favorite terminal
