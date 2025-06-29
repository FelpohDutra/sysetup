### Fixing PCIE problem

I currently face a problem very similar to this [**one**](https://bbs.archlinux.org/viewtopic.php?id=271534).
So to "*fix*" it, I use this kernel parameter:

    pcie_aspm=off
> "_Active-State Power Management_ (ASPM) saves power in the _Peripheral Component Interconnect Express_ (PCI Express or PCIe) subsystem by setting a lower power state for PCIe links when the devices to which they connect are not in use. ASPM controls the power state at both ends of the link, and saves power in the link even when the device at the end of the link is in a fully powered-on state." [More here.](https://docs.redhat.com/en/documentation/red_hat_enterprise_linux/6/html/power_management_guide/aspm#ASPM) 

