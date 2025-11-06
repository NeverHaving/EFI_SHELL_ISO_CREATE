# EFI_SHELL_ISO_CREATE
Provide a method for creating bootable UEFI SHELL in Linux

- dd if=/dev/zero of=Shell.iso bs=1M count=50
- mkfs.fat -F 32 -n "SHELLISO" Shell.iso
- mmd -i Shell.iso ::EFI
- mmd -i Shell.iso ::EFI/BOOT
- mcopy -i Shell.iso Shell.efi ::EFI/BOOT/BOOTAA64.EFI
