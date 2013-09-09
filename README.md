Install archlinux on your headless machine.


"arch-headless" is a script that takes an official archlinux installation iso image and modifies it in such a way that during the installation the root user is logged in automatically. The sshd.service starts automatically and root logins are allowed with an empty password.


APPLICATION
The script is written with just one purpose in mind:  Installation of archlinux on a headless server/computer, using a SSH connection.


REQUIREMENTS
- The headless computer/server has to boot from a CD/DVD.
- The headless computer/server connects automatically to the local network.
- The computer using the arch-headless script needs to have systemd installed.


INSTALLATION
No installation needed.


DEPENDENCIES
squachfs-tools (cammands: unsquashfs, mksquashfs)
cdrkit         (command:  genisoimage)
sed            (command:  sed)
