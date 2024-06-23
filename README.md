I'm not a programmer by trade but I'd like to share my nonsense.

How to use:

    format luks sde
Will...<BR>
    prompt the user to type "YES"<BR>
    ask for a password<BR>
    luksFormat the device<BR>
    luksOpen the device<BR>
    format the mapped (opened) device<BR>
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
