# Note
These customizations were done on **GNOME 46.5**, they weren't tested yet on GNOME 47.
The current state of the Extensions mentioned are described below their respective names *(Sep 27th 2024)*

> On upgrading to GNOME 47, 19 out of 23 currently installed extensions will be compatible (82%).
> 
# Tweaks
Starting by *GNOME Tweaks*, tweaks :wink:.

Under **Appearance**, the following is installed:

 - [Cursor](https://www.gnome-look.org/p/1503665)
- [Icons](https://www.gnome-look.org/p/1256209/)
- [Shell](https://www.gnome-look.org/p/1977647)

All available colors for *Shell* and *Icons* were installed, this way, whenever I feel like changing the color scheme, it's easily doable.

Installing these are fairly easy:

 - For *Cursors* and *Icons*, extract the compressed files inside ~/.icons
 - For *Shell*, extract the files inside ~/.themes
 
 >"Shell" option requires extension mentioned in the next section 

# Extensions
First things first, install the **[Extension Manager](https://aur.archlinux.org/packages/extension-manager)** from the AUR (or Flathub). It makes life 100x easier.

**System extensions**
Enable "**User Themes**"

For **"User-Installed Extensions"**, you can install the extensions in any order, as you may want.

 ### 1. Custom Accent Colors @ demiskp
 > Supported: No
 (Apparently supported natively on GNOME 47)
 

 1. **Accent Color:** Choose whatever you want. I always like to match it with the desktop wallpaper.
 2. **Enable all the Extra Options**

### 2. Blur my Shell @ aunetx
 > Supported: Yes


 1. **Leave everything on default**, except for:
	 -  Panel: Switch **Blur type** to **Dynamic** 
	 - Applications: Turn it **ON**; Set **"Sigma"** to **1**; **"Brightness"** and **"Opacity"** to **Maximum** possible; **"Opaque focused window"** and **"Enable all by default"** **ON** and **"Blur on overview"** **OFF**.

### 3. ArcMenu @ arcmenu
 > Supported: Yes


 1. **Leave everything on default**, except for:
 -  Menu: **Menu Layout** > **Windows** (under **"Modern Layout Menus"**).

### 4. Just Perfection @ just-perfection
> Supported: Yes

Customize as you wish, but it's essential for my specific look to change **"Panel Position"**, inside **Customize**, to **"Bottom"**  .

### 5. App Icons Taskbar @ aztaskbar
 > Supported: Yes


 - Leave everything on default.

### 6. AppIndicator and KstatusNotifierItem Support @ rgcjonas
 > Supported: Yes

 - Leave everything on default.

### 7. Arch Linux @ RapahelRochet
> Supported: Yes

Under **Advanced settings**, change the "**Command to update packages**" to

    flatpak run com.raggesilver.BlackBox -c "paru ; echo Done - Press enter to exit; read _" 

### 8. Desktop Icons NG (DING) @ rastersoft
 > Supported: No


 - Leave everything on default.
 
### 9. Show Desktop Button @ amivaleo
 > Supported: No


Change **"Indicator position on panel"** to **"Far Right"**.

### 10. Transparent Window Moving @ noobsai
 > Supported: No


 1. **"Opacity"**: **200**

# Example

The final result will look something like this:

![same from the main page](https://raw.githubusercontent.com/FelpohDutra/sysetup/main/images/gnome-my-first-rice-ever-v1.webp)

![enter image description here](https://raw.githubusercontent.com/FelpohDutra/sysetup/refs/heads/main/images/Updated.png)

By editing a little bit more, you can even get something that looks a bit more with "Windows"! (*uncanny valley territory to be honest*)

![what](https://github.com/FelpohDutra/sysetup/blob/main/images/Screenshot-from-2024-08-25-16-48-32.png?raw=true)
