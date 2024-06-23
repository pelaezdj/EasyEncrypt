I'm not a programmer by trade but I'd like to share my nonsense.

How to use:

    format luks sde
Will...<BR>&nbsp;&nbsp;&nbsp;&nbsp;
    1. prompt the user to type "YES"<BR>&nbsp;&nbsp;&nbsp;&nbsp;
    2. ask for a password<BR>&nbsp;&nbsp;&nbsp;&nbsp;
    3. luksFormat the device<BR>&nbsp;&nbsp;&nbsp;&nbsp;
    4. luksOpen the device<BR>&nbsp;&nbsp;&nbsp;&nbsp;
    5. format the mapped (opened) device<BR>&nbsp;&nbsp;&nbsp;&nbsp;
    6. luksClose the device<BR>

Running...

    format luks sde
    format luks sde1
    format sde luks
    format crypt sde
    format luksFormat sde1
    ... and more
Will all do the same thing.


The script also supports normal format operations:

    format sde
Will run the command:

    mkfs.ext4 -F /dev/sde1

To format "/dev/sde1" in the FAT filesystem:

    format sde fat
or

    format fat sde

NTFS and BTRFS are supported as well!
