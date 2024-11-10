# Tmc_Wen-Tips
How can I create Clonezilla live iso file from clonezilla live zip file?
On a GNU/Linux system, download Clonezilla live zip file. Here we take clonezilla-live-2.5.5-38-amd6.iso as an example. Then run the following commands:
mkdir /tmp/zip2iso
unzip clonezilla-live-2.5.5-38-amd6.iso -d /tmp/zip2iso/
cd /tmp/zip2iso/
xorriso -as mkisofs -R -r -J -joliet-long -l -cache-inodes -iso-level 3 -isohybrid-mbr /usr/lib/ISOLINUX/isohdpfx.bin -partition_offset 16 -A 'Clonezilla live CD' -b syslinux/isolinux.bin -c syslinux/boot.cat -no-emul-boot -boot-load-size 4 -boot-info-table -eltorito-alt-boot --efi-boot boot/grub/efi.img -isohybrid-gpt-basdat -isohybrid-apm-hfsplus ./ > /tmp/clonezilla-live.iso
Then the created iso file clonezilla-live.iso is in the dir /tmp/.
来自已经403的官网
---
