# Guidance

1. Check that /dev/ttyACM0 or any equal is existing
2. Run lsblk check that "sdc" is shown
3. Create a mount partition and place the bootloader in it:

mkdir -p /mnt/nano/
mount -t vfat /dev/sdc /mnt/nano

4. Copy the uf2 files into the mount
cp $bootloader_path /mnt/nano

5. Unmount the partition
umount /mnt/nano

# Helps
Unzip
7z x $filename $path

Display the output of the promicroboard
dmesg | tail
