### Fixing PCIE problem

I currently face a problem very similar to this [**one**](https://bbs.archlinux.org/viewtopic.php?id=271534).
So to "*fix*" it, I use this kernel parameter:

    pcie_aspm=off
> "_Active-State Power Management_ (ASPM) saves power in the _Peripheral Component Interconnect Express_ (PCI Express or PCIe) subsystem by setting a lower power state for PCIe links when the devices to which they connect are not in use. ASPM controls the power state at both ends of the link, and saves power in the link even when the device at the end of the link is in a fully powered-on state." [More here.](https://docs.redhat.com/en/documentation/red_hat_enterprise_linux/6/html/power_management_guide/aspm#ASPM) 

You can add this, and other, parameters by following this page from the Arch Wiki:

 - [GRUB](https://wiki.archlinux.org/title/Kernel_parameters#GRUB)
 - [SYSTEMD-BOOT](https://wiki.archlinux.org/title/Kernel_parameters#systemd-boot)

## Custom Kernel
Personally, I like to use a custom kernel. For this, I recommend the TKG kernel. Installing it is pretty easy so there's not a lot that I can say other than linking it's [Github](https://github.com/Frogging-Family/linux-tkg) page.

### Optional tweaks
Everything ***except*** for:

 - `ZFS` FPU
 - Provide own kernel  `.config`  file
