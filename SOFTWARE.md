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
