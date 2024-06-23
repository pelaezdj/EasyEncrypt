I'm not a programmer by trade but I'd like to share my nonsense.

How to use:

    format luks sde
Will prompt the user, ask for the password, luksFormat the device, luksOpen the device, format the mapped device, and luksClose the device

Running...

    format luks sde
    format luks sde1
    format sde luks
    format crypt sde
    format luksFormat sde1
    ... and more
Will all produce the same set of commands.

The script also supports regular encryption:

    format sde
Will run the command:

    mkfs.ext4 -F /dev/sde1

To format in FAT:

    format sde fat
or

    format fat sde

NTFS and BTRFS are supported as well!
