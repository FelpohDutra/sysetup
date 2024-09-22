# Discord
Firstly, because Discord's official app for Linux is sort of terrible, I use [Vesktop](https://github.com/Vencord/Vesktop), which comes with the Vencord mod installed and also has a solution for screensharing with audio!
> (In my experience, it works fine, with the only major downside being that you can't share the audio of your entire screen when using with something that process your audio inputs, e.g [Easy Effects](https://github.com/wwmm/easyeffects))

#### Plugins
- NoDevtoolsWarning


![](https://cdn.discordapp.com/attachments/779555911634255932/1274870850071298178/image.png?ex=66f14f40&is=66effdc0&hm=7e205f00147ef8603ef4c93af181a33d37ae5ae269a6e9045f70329c667ee7a4&=)

If you're not a masochist, using this plugin is basically essential, otherwise your discord will keep logging you off every time you close the app *wrongly*. 

### ArRPC
> For this to work properly, start the server manually at least once. 

ArRPC allows Discord's Rich Presence to work on custom clients. This section is not about getting the [server up,](https://github.com/OpenAsar/arrpc) but actually to have it start with the system. For this I created a service using systemd.

First, create the .service file on user-level:

    nano ~/.config/systemd/user/arrpc.service

Inside the file, copy and paste this service template file

    [Unit]
    Description=arRPC Service
    After=network.target
    
    [Service]
    Type=simple
    ExecStart=/usr/bin/node /your_path_to_arrpc/src/
    Restart=on-failure
    
    [Install]
    WantedBy=default.target

After that, enable the service and start it.

    systemctl --user enable arrpc 
    systemctl --user start arrpc

### Theming
Indication of a cool theme that I usually use
> [system24](https://github.com/refact0r/system24), a tui-style discord theme.
![screenshot](https://github.com/refact0r/system24/raw/main/assets/screenshot3.png)

# Easy Effects
Easily one of the most important parts of my setup, as I'm addicted to listening to music, and having good audio just makes it even more addicting.

**Equalizer**

I have a Superlux HD681 with some really thick pads, so this preset was made with it in mind, with some inspiration from online presets. 

![](https://raw.githubusercontent.com/FelpohDutra/sysetup/refs/heads/main/images/Equalizer.png)
> [Download](https://raw.githubusercontent.com/FelpohDutra/sysetup/refs/heads/main/images/custom)

**Microphone**

Just two effects that makes my mic sound better and not too much robotic/filtered.

![](https://github.com/FelpohDutra/sysetup/blob/main/images/Mic1.png?raw=true)

![](https://github.com/FelpohDutra/sysetup/blob/main/images/Mic%202.png?raw=true)

# FastFetch
![](https://github.com/FelpohDutra/sysetup/blob/main/images/Sixel.png?raw=true)

With the **Blackbox** Terminal, images can be displayed when Sixel support is enabled 

That's how my fastfetch's *config.jsonc* looks like

    {
      "$schema": "https://github.com/fastfetch-cli/fastfetch/raw/dev/doc/json_schema.json",
      "logo": {
        "type": "sixel",
        "source": "/path_to_picture.whatever/"
    },
      "modules": [
        "title",
        "separator",
        "os",
        "host",
        "kernel",
        "shell",
        "display",
        "de",
        "wmtheme",
        "theme",
        "icons",
        "font",
        "cpu",
        "gpu",
        "memory",
        "break",
      ]
    }


# Fish
1. [Install Fish](https://github.com/fish-shell/fish-shell?tab=readme-ov-file)
2. [Install Fisher](https://github.com/jorgebucaran/fisher)
3. [Install Tide](https://github.com/IlanCosman/tide)
	
>**Tide** looks great!

![](https://github.com/IlanCosman/tide/raw/assets/images/header.png)



#### To have fastfetch welcome you every time you open the terminal, add `fastfetch`to `~/.config/fish/config.fish` 

# Black Box

1. On "**General**" , everything's ticked except for "*Show Head Bar*"
2. On "**Terminal**", set Opacity to "*75*"
3. On "**Advanced**", enable "*Sixel Support*" (Flatpak).

#### Open Black Box on Nautilus
1. Download **[dconf editor](https://apps.gnome.org/DconfEditor/)** 
2. Install [this](https://github.com/Stunkymonkey/nautilus-open-any-terminal) extension for Nautilus
3. Configure the extension like this:
![](https://github.com/FelpohDutra/sysetup/blob/main/images/Nautilus.png?raw=true)

# Sleepy Launcher

Although I barely play ZZZ nowadays, due to some issues with dxvk, this game has a really bad problem with VRAM leak, using this commands make the game not crash when you eventually get limited by VRAM

>This is mostly a problem for people with a graphics card with 8GB or less, so ymmv.

![](https://media.discordapp.net/attachments/779555911634255932/1287522985116307467/image.png?ex=66f1dab8&is=66f08938&hm=ed5d1dc8c426915774fbb326e91edecda13548537f8edac0ccc88f4e72dc046d&=&format=webp&quality=lossless&width=901&height=509)

# An Anime Game Launcher
Another game that I barely play nowadays, but when I do, I like it with mods (which is not the most straightforward thing to do with this launcher)

![](https://media.discordapp.net/attachments/779555911634255932/1287523698336600115/image.png?ex=66f1db62&is=66f089e2&hm=367d6481c5eac06d4b9216c7b24ed87d97088303070410b82326adf7bc14eff3&=&format=webp&quality=lossless&width=898&height=509)

- `gamemoderun ~/.local/share/anime-game-launcher/runners/your_wine_version/bin/wine64 launch.bat`;
- On your game folder, create this "*launch.bat*" file;
![](https://media.discordapp.net/attachments/779555911634255932/1287524046774210722/image.png?ex=66f1dbb5&is=66f08a35&hm=2ccc5d4928b4562affe7f30ccaab7fd42c22c3e5e62564555476391f5ab699ad&=&format=webp&quality=lossless&width=852&height=509)
- Inside, write this:
>You can't use "~/" here; replace "YOUR_USER" and "YOUR_DESIRED_FRAMERATE"

cd /home/YOUR_USER/.local/share/anime-game-launcher/prefix/drive_c/Program Files/3dmigoto
    start "" "3DMigoto Loader.exe"
    
    cd /home/YOUR_USER/.local/share/anime-game-launcher/Genshin Impact/
    start GenshinImpact.exe
    
    cd /home/YOUR_USER/.local/share/anime-game-launcher/fps_unlocker
    start fpsunlock.exe YOUR_DESIRED_FRAMERATE

- Install 3DMigoto on the path specified, also download this [DLL](https://cdn.discordapp.com/attachments/1132397027200868502/1142460757385162862/d3dcompiler_47.dll?ex=66f176fe&is=66f0257e&hm=42feaf1650de019d926a0e31a634c858c835cafc9f083a35db02e95849e1601e&) and place on the 3DMigoto folder;
- Download this [FPS Unlocker](https://codeberg.org/mkrsym1/fpsunlock) and install on the path specified too;
- Finally, on *"winecfg"*, add a DLL override for "*d3dcompiler_47*", and make sure it's configured as "*Native*".
 
![enter image description here](https://media.discordapp.net/attachments/779555911634255932/1287527953495883939/image.png?ex=66f1df59&is=66f08dd9&hm=04acad6771902ee0ba75651b738f3b274fcb6ba087d2dd63797f865846723c44&=&format=webp&quality=lossless&width=1004&height=509)
