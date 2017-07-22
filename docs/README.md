# caja-scripts
This is a repository for Caja scripts created by me. The same scripts may be used for Nautilus with minor modifications.

### Dependencies
On a debian machine with MATE desktop, I haven't installed anything specific. For interactive menus and messages, `zenity` is used. If you don't have `zenity`, please install it.

### Installation:
1. Copy the scripts to `~/.config/caja/scripts/`
2. Make sure that the script files have executable permission.

### Disclaimer:
	I haven't tested this software extensively. Please report bugs and help me fix them.
	Pull requests are always welcome.

### Details of each script is given below

# Checksum

View the checksum`(md5sum, sha1sum, sha256sum, sha512sum)` of any file from Caja itself.

# Open Terminal

Open `mate-terminal` from any location.

# Unmount FUSE volumes

This script can unmount any fuse mounts *(sshfs/encfs)* mounts within the Caja window itself. Once executed, the script will show a list of fuse mounts, and the user can select the one he wish to unmount.

### Background
Caja supports *ssfhs* mounts from the GUI. But it does not support unmounting from Caja window (See [Caja bug report](https://github.com/mate-desktop/caja/issues/53)). Nautilus also has the same problem.

There are two workarounds I found in the Internet, but I dont like any of them
1. Open terminal and execute `fusermount -u <mountpoint>`.

    If Caja supports mounting the sshfs from GUI, it should be removable from GUI. It should be that simple.
2. Use *gvfs*.

    A *gvfs* mount does not behave like a local folder. Some application does not work properly. eg. VLC cannot play with public key authentication. (See [VLC bug report](https://forum.videolan.org/viewtopic.php?t=130355)).

