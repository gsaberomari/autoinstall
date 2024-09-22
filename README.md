# autoinstall
Ubuntu 24.10 Autoinstall Script
#Ubuntu 23.10 Autoinstall Script for testing only.

This `autoinstall.yaml` script streamlines the installation of Ubuntu 24.10 ("oracular oriole") with a focus on good sftuff, be ready to experience instability!

Note: Won't Recommend targeting kernel and nvidia version cause updates lurking around.(leave Ubuntu handle them)

## Features:

* **LVM:** Leverages Logical Volume Management for flexible disk partitioning.
* **Minimal Desktop:** Installs the full Ubuntu desktop environment for a balance of functionality and speed.
* **Essential Tools:** Includes `git`, `vim`, `htop`, and other useful utilities.


* **Performance Enhancements:**
    * ZRAM swap for improved memory management.
    * TRIM support for SSD optimization.
    * AppArmor profiles for Flatpak applications.
    * AMD microcode updates.

* **Additional Software:**
    * qBittorrent (via Flatpak)
    * VLC media player
    * fswatch 

## Usage:

1. **Create bootable USB:** Use a tool like BalenaEtcher or Startup Disk Creator to flash the Ubuntu 23.10 ISO to a USB drive.
2. **Place `autoinstall.yaml`:** Copy this `autoinstall.yaml` file to the root of the bootable USB drive.
3. **Boot from USB:** Boot your system from the USB drive and select the "Automated install" option.
4. **Point to `autoinstall.yaml`:** When prompted, select the `autoinstall.yaml` file on your USB drive.
5. **Relax:** The installation will proceed automatically.

## Customization:

* **Packages:** Add or remove packages in the `packages` section as needed.
* **NVIDIA Driver:** Adjust the version in the `late-commands` section if necessary.
* **User Account:** Modify the `users` section to change the username, password, or privileges.

## Disclaimer:

* **Backup your data:** Always back up important data before performing any system installations.
* **NVIDIA Compatibility:** Ensure your NVIDIA driver is compatible with the installed kernel.
* **Security:** Protect your `autoinstall.yaml` file, especially if it contains sensitive information like password hashes.

## Contributing:

Feel free to fork this basic work!
