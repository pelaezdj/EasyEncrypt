I'm not a programmer by trade but I'd like to share my nonsense.

How to use:

    format luks sde
Will...<BR>&nbsp;&nbsp;&nbsp;&nbsp;
prompt the user to type "YES"<BR>&nbsp;&nbsp;&nbsp;&nbsp;
    ask for a password<BR>&nbsp;&nbsp;&nbsp;&nbsp;
    luksFormat the device<BR>&nbsp;&nbsp;&nbsp;&nbsp;
    luksOpen the device<BR>&nbsp;&nbsp;&nbsp;&nbsp;
    format the mapped (opened) device<BR>&nbsp;&nbsp;&nbsp;&nbsp;
    and luksClose the device<BR>

Running...

    format luks sde
    format luks sde1
    format sde luks
    format crypt sde
    format luksFormat sde1
    ... and more
Will all produce the same set of commands.

The script also supports normal format operations:

    format sde
Will run the command:

    mkfs.ext4 -F /dev/sde1

To format in FAT:

    format sde fat
or

    format fat sde

NTFS and BTRFS are supported as well!
