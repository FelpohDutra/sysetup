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
 (This will, apparently, be added in GNOME 47, so you might not need to install this one depending on the time you're reading this)
 

 1. **Accent Color:** Choose whatever you want. I always like to match it with the desktop wallpaper.
 2. **Enable all the Extra Options**

### 2. Blur my Shell @ aunetx

 1. **Leave everything on default**, expect for:
	 -  Panel: Switch **Blur type** to **Dynamic** 
	 - Applications: Turn it **ON**; Set **"Sigma"** to **1**; **"Brightness"** and **"Opacity"** to **Maximum** possible; **"Opaque focused window"** and **"Enable all by default"** **ON** and **"Blur on overview"** **OFF**.

### 3. ArcMenu @ arcmenu

 1. **Leave everything on default**, expect for:
 -  Menu: **Menu Layout** > **Windows** (under **"Modern Layout Menus"**).

### 4. Just Perfection @ just-perfection

Customize as you wish, but it's essential for my specific look to change **"Panel Position"**, inside **Customize**, to **"Bottom"**  .

### 5. App Icons Taskbar @ aztaskbar

 - Leave everything on default.

### 6. AppIndicator and KstatusNotifierItem Support @ rgcjonas

 - Leave everything on default.

### 7. Arch Linux @ RapahelRochet

Under **Advanced settings**, change the "**Command to update packages**" to

    flatpak run com.raggesilver.BlackBox -c "paru ; echo Done - Press enter to exit; read _" 

### 8. Desktop Icons NG (DING) @ rastersoft

 - Leave everything on default.
 
### 9. Show Desktop Button (DING) @ amivaleo

Change **"Indicator position on panel"** to **"Far Right"**.

### 10. Transparent Window Moving @ noobsai

 1. **"Opacity"**: **200**

# Example

The final result will look something like this:

![same from the main page](https://preview.redd.it/gnome-my-first-rice-ever-v0-ijj3mwimoijd1.png?width=1080&crop=smart&auto=webp&s=2098995565cba837ec83626dbf7215d2943ec17a)

By editing a little bit more, you can even get something that looks a bit more with "Windows"! (*uncanny valley territory to be honest*)

![what](https://i.ibb.co/2yFsrJ7/Screenshot-from-2024-08-25-16-48-32.png)
