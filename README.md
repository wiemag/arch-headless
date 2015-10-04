Install archlinux on your headless machine.
-------------------------------------------


"arch-headless" is a script that takes an official archlinux installation iso image and modifies it in such a way that during the installation the root user is logged in automatically. The sshd.service starts automatically and root logins are allowed with an empty password.

With version 0.97 unnecessary architecture files are removed from the iso image, and the resulting iso-image file name is changed to show the modified-image architecture.
Version 1.11 adds time zone and locale configuration.
Version 1.12 allows adding your own scripts/files to the installation media.
Version 1.13 works with the new archiso structure (new structure from 201510)

APPLICATION

The script is written with just one purpose in mind:  Installation of archlinux on a headless server/computer, using a SSH connection.


EXTRA APPLICATION NOTE

Not tested with (U)EFI. A silent assumption was made that the modified iso image would be used only with BIOS based computers.


REQUIREMENTS

- The headless computer/server has to boot from a CD/DVD. (If USB read man pages.)
- The headless computer/server connects automatically to the local network.
- The computer using the arch-headless script needs to have systemd installed.


INSTALLATION

No installation needed. The script has been simplified and does not install missing dependencies any longer, just informs that a dependency is missing and exits.

There is a PKGBUILD availavble on Arch linux AUR and on https://github/wiemag/PKGBUILDs


DEPENDENCIES

- squachfs-tools (cammands: unsquashfs, mksquashfs)
- cdrkit         (command:  genisoimage)
- sed            (command:  sed)
- util-linux     (command:  mount, umount)
- coreutils      (command:  wc, md5sum, ln, cp, echo)
- gawk           (command:  awk)
- kbd            (command:  loadkeys, setfont)

'cdrkit' conflicts with 'cdrtools'. Modify PKGBUILD if you prefer 'cdrtools'.
