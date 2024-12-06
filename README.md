# EFI_SHELL_ISO_CREATE
Provide a method for creating bootable UEFI SHELL in Linux

- dd if=/dev/zero of=EFI/BOOT/Shell.iso bs=1M count=50
- mkfs.fat -F 32 -n "SHELLISO" EFI/BOOT/Shell.iso
- mmd -i EFI/BOOT/Shell.iso ::EFI
- mmd -i EFI/BOOT/Shell.iso ::EFI/BOOT
- mcopy -i EFI/BOOT/Shell.iso Shell.efi ::EFI/BOOT/BOOTAA64.EFI
