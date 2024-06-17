********************
EFI Protocols survey
********************

This is a quick survey of the EFI Protocols usage.

EFI Protocols
=============

.. list-table:: Table of EFI Protocols
   :widths: 50 50
   :header-rows: 1

   * - EFI Protocol
     - Notes
   * - EFI_BLOCK_IO_PROTOCOL_
     - - EBBR v2.2.0: Required
       - U-Boot v2024.07-rc4: Implemented by efi_loader, installed on disks,
         also used in EFI_APP
       - Trammel OSFC 2019: mentioned
       - safeboot-loader 4c5ed91: TBD
   * - EFI_BUS_SPECIFIC_DRIVER_OVERRIDE_PROTOCOL_
     - - EBBR v2.2.0: Not required
   * - EFI_CC_MEASUREMENT_PROTOCOL_
     - - Linux v6.9.5: Use for trusted computing to retrieve event log and
         measure load options (command line) and initrd when available
       - GRUB v2.12: TBD
       - **Should we mention it in EBBR?**
   * - EFI_DECOMPRESS_PROTOCOL_
     - - EBBR v2.2.0: Not required
       - GRUB v2.12: TBD
   * - EFI_DEVICE_PATH_FROM_TEXT_PROTOCOL_
     - - Linux v6.9.5: Use for the ``initrd=`` and ``dtb=`` command line
         arguments
       - GRUB v2.12: TBD
       - **We should mention it in EBBR**
   * - EFI_DEVICE_PATH_PROTOCOL_
     - - EBBR v2.2.0: Required
       - U-Boot v2024.07-rc4: Implemented by efi_loader, installed on the root,
	 the disks, the initrd, the http boot ramdisk, the console, the network
	 interface and the running image, used by helloworld, also used in
         EFI_APP
       - safeboot-loader 4c5ed91: TBD
   * - EFI_DEVICE_PATH_TO_TEXT_PROTOCOL_
     - - EBBR v2.2.0: Required
       - U-Boot v2024.07-rc4: Implemented by efi_loader, installed on the root,
         also used in EFI_APP
       - GRUB v2.12: TBD
       - safeboot-loader 4c5ed91: TBD
   * - EFI_DEVICE_PATH_UTILITIES_PROTOCOL_
     - - EBBR v2.2.0: Required
       - U-Boot v2024.07-rc4: Implemented by efi_loader, installed on the root,
         also used in EFI_APP
       - GRUB v2.12: TBD
   * - EFI_DISK_IO_PROTOCOL_
     - - EBBR v2.2.0: Not required
   * - EFI_DRIVER_BINDING_PROTOCOL_
     - - U-Boot v2024.07-rc4: Implemented by efi_loader, installed on drivers
       - GRUB v2.12: TBD
       - **Should we mention it in EBBR?**
   * - EFI_DRIVER_FAMILY_OVERRIDE_PROTOCOL_
     - - EBBR v2.2.0: Not required
   * - EFI_DT_FIXUP_PROTOCOL_
     - - A U-Boot extension to UEFI
       - U-Boot v2024.07-rc4: Implemented by efi_loader, installed on the root
   * - EFI_FIRMWARE_MANAGEMENT_PROTOCOL_
     - - EBBR v2.2.0: Recommended
       - U-Boot v2024.07-rc4: Implemented by efi_loader, installed on the root
       - **Should we require in EBBR?**
   * - EFI_GRAPHICS_OUTPUT_PROTOCOL_
     - - EBBR v2.2.0: Not required
       - Linux v6.9.5: Use for graphics on UEFI framebuffer
       - U-Boot v2024.07-rc4: Implemented by efi_loader, installed when there is
         a video driver, also used in EFI_APP
       - **Should we recommend/require in EBBR?**
   * - EFI_HII_CONFIG_ACCESS_PROTOCOL_
     - - EBBR v2.2.0: Not required
       - U-Boot v2024.07-rc4: Not implemented (some unused sources left in
         efi_loader)
       - GRUB v2.12: TBD
   * - EFI_HII_CONFIG_ROUTING_PROTOCOL_
     - - EBBR v2.2.0: Not required
       - U-Boot v2024.07-rc4: Not implemented (some unused sources left in
         efi_loader)
       - GRUB v2.12: TBD
   * - EFI_HII_DATABASE_PROTOCOL_
     - - EBBR v2.2.0: Required
       - U-Boot v2024.07-rc4: Implemented by efi_loader, installed on the root
       - GRUB v2.12: TBD
   * - EFI_HII_PACKAGE_LIST_PROTOCOL_
     - - A package list header structure pointer as a protocol
       - EBBR v2.2.0: Not required
   * - EFI_HII_STRING_PROTOCOL_
     - - EBBR v2.2.0: Required
       - U-Boot v2024.07-rc4: Implemented by efi_loader, installed on the root
       - GRUB v2.12: TBD
   * - EFI_LOADED_IMAGE_DEVICE_PATH_PROTOCOL_
     - - EBBR v2.2.0: Required
       - U-Boot v2024.07-rc4: Implemented by efi_loader, installed on loaded
         images
   * - EFI_LOADED_IMAGE_PROTOCOL_
     - - EBBR v2.2.0: Required
       - Linux v6.9.5: Use to retrieve command line and for kernel (zboot)
         decompression
       - U-Boot v2024.07-rc4: Implemented by efi_loader, installed on loaded
         images, also used in EFI_APP
       - GRUB v2.12: TBD
   * - EFI_LOAD_FILE2_PROTOCOL_
     - - Linux v6.9.5: Use to load initrd from device path
       - U-Boot v2024.07-rc4: Implemented by efi_loader, installed on the initrd
       - GRUB v2.12: TBD
       - **We should recommend/require in EBBR**
   * - EFI_LOAD_FILE_PROTOCOL_
     - - U-Boot v2024.07-rc4: Not implemented but used by efi_loader to load
         images when available, for extensions (e.g. iPXE)
       - GRUB v2.12: TBD
       - **Should we mention it in EBBR?**
   * - EFI_FILE_PROTOCOL_
     - - U-Boot v2024.07-rc4: Implemented by efi_loader, installed on opened
         files
       - **Should we mention it in EBBR?**
   * - EFI_MANAGED_NETWORK_PROTOCOL_
     - - EBBR v2.2.0: Not required
   * - EFI_MEMORY_ATTRIBUTE_PROTOCOL_
     - - Linux v6.9.5: Use to remap kernel image with permissions
       - **Should we mention it in EBBR?**
   * - EFI_NETWORK_INTERFACE_IDENTIFIER_PROTOCOL_
     - - EBBR v2.2.0: Not required
   * - EFI_PCI_IO_PROTOCOL_
     - - EBBR v2.2.0: Not required
       - Linux v6.9.5: Use to disable PCI bus master (and for option ROMs and UGA)
   * - EFI_PLATFORM_DRIVER_OVERRIDE_PROTOCOL_
     - - EBBR v2.2.0: Not required
   * - EFI_PXE_BASE_CODE_PROTOCOL_
     - - EBBR v2.2.0: Not required
       - U-Boot v2024.07-rc4: Implemented by efi_loader, installed when there is
         a network interface
   * - EFI_RNG_PROTOCOL_
     - - EBBR v2.2.0: Required if hardware entropy source
       - Linux v6.9.5: Use for KASLR and random seed when available
       - U-Boot v2024.07-rc4: Implemented by efi_loader, installed when there is
         an RNG
       - GRUB v2.12: TBD
   * - EFI_XXX_SERVICE_BINDING_PROTOCOL_
     - - EBBR v2.2.0: Not required
   * - EFI_SIMPLE_FILE_SYSTEM_PROTOCOL_
     - - EBBR v2.2.0: Required if booting from block device
       - U-Boot v2024.07-rc4: Implemented by efi_loader, installed on the
         disks and partitions with a filesystem
       - GRUB v2.12: TBD
       - safeboot-loader 4c5ed91: TBD
   * - EFI_SIMPLE_NETWORK_PROTOCOL_
     - - EBBR v2.2.0: Required if network device
       - U-Boot v2024.07-rc4: Implemented by efi_loader, installed when there is
         a network interface
       - Trammel OSFC 2019: mentioned
       - safeboot-loader 4c5ed91: TBD
   * - EFI_SIMPLE_TEXT_INPUT_EX_PROTOCOL_
     - - EBBR v2.2.0: Required
       - U-Boot v2024.07-rc4: Implemented by efi_loader, installed on the
         console
       - GRUB v2.12: TBD
   * - EFI_SIMPLE_TEXT_INPUT_PROTOCOL_
     - - In System Table
       - EBBR v2.2.0: Required
       - U-Boot v2024.07-rc4: Implemented by efi_loader, installed on the
         console
       - GRUB v2.12: TBD
   * - EFI_SIMPLE_TEXT_OUTPUT_PROTOCOL_
     - - In System Table
       - EBBR v2.2.0: Required
       - U-Boot v2024.07-rc4: Implemented by efi_loader, installed on the
         console, also used in EFI_APP
       - GRUB v2.12: TBD
   * - EFI_SMBIOS_PROTOCOL_
     - - A UEFI PI protocol
       - Linux v6.9.5: Use to retrieve SMBIOS records (to get the SMCCC SoC ID
	 from type 4 records, to identify the system and determine if vamap
         quirks are needed)
       - **Recommend/require when SMBIOS has made it into EBBR**
   * - EFI_TCG_PROTOCOL_
     - - A TCG extension to UEFI, superceded by the TCG2 protocol
       - U-Boot v2024.07-rc4: Not implemented
       - **Mention as obsolete in EBBR?**
   * - EFI_TCG2_PROTOCOL_
     - - A TCG extension to UEFI
       - EBBR v2.2.0: Required if TPM
       - Linux v6.9.5: Use to retrieve event log and measure load options
         (command line) and initrd when available
       - U-Boot v2024.07-rc4: Implemented in efi_loader, registered when there
         is a TPM
       - Trammel OSFC 2019: mentioned
       - safeboot-loader 4c5ed91: TBD
   * - EFI_UNICODE_COLLATION_PROTOCOL_
     - - EBBR v2.2.0: Required
       - U-Boot v2024.07-rc4: Implemented by efi_loader, installed on the root
       - GRUB v2.12: TBD
   * - RISCV_EFI_BOOT_PROTOCOL_
     - - A RISC-V extension to UEFI
       - EBBR v2.2.0: Required on RISC-V
       - Linux v6.9.5: Use on RISC-V to retrieve boot hart id
       - U-Boot v2024.07-rc4: Implemented in efi_loader, registered on RISC-V
   * - `EFI_ABSOLUTE_POINTER_PROTOCOL`
     - - GRUB v2.12: TBD
   * - `EFI_COMPONENT_NAME2_PROTOCOL`
     - - GRUB v2.12: TBD
   * - `EFI_DEBUGPORT_PROTOCOL`
     - - GRUB v2.12: TBD
   * - `EFI_DEBUG_SUPPORT_PROTOCOL`
     - - GRUB v2.12: TBD
   * - `EFI_HII_FONT_PROTOCOL`
     - - GRUB v2.12: TBD
   * - `EFI_HII_IMAGE_PROTOCOL`
     - - GRUB v2.12: TBD
   * - `EFI_SCSI_IO_PROTOCOL`
     - - GRUB v2.12: TBD
   * - `EFI_SIMPLE_POINTER_PROTOCOL`
     - - GRUB v2.12: TBD
   * - `EFI_TAPE_IO_PROTOCOL`
     - - GRUB v2.12: TBD
   * - `EFI_USB2_HC_PROTOCOL`
     - - GRUB v2.12: TBD
   * - `EFI_USB_IO_PROTOCOL`
     - - GRUB v2.12: TBD
   * - `EFI_RAM_DISK_PROTOCOL`
     - - Trammel OSFC 2019: mentioned
       - safeboot-loader 4c5ed91: TBD
   * - `EFI_DHCP4_PROTOCOL`
     - - safeboot-loader 4c5ed91: TBD

To Do
-----

- EBBR HTTP Boot protocols
- EBBR Byte stream device (UART) protocols
- EBBR USB bus protocols
- EBBR NVMe pass through protocols
- EBBR SCSI pass through protocols
- systemd-boot
- isolinux
- UEFI Shell
- iPXE
- u-root
- UKI
- Fuschia
- SONiC/ONIE
- `Android Generic Bootloader`_
- systemd-stub
- Finish GRUB details

.. _Android Generic Bootloader: https://resources.linaro.org/en/resource/8YxzJgiKff4sHXYXRg6yeL

See Also
========

- https://github.com/ARM-software/ebbr/wiki/Required-EFI-protocols
- `Trammel talk at OSFC 2019`_
- https://github.com/osresearch/safeboot-loader

.. _Trammel talk at OSFC 2019: https://www.osfc.io/2022/talks/linux-as-a-uefi-bootloader-and-kexecing-windows/
.. _EFI_BLOCK_IO_PROTOCOL: https://uefi.org/specs/UEFI/2.10/13_Protocols_Media_Access.html#efi-block-io-protocol
.. _EFI_BUS_SPECIFIC_DRIVER_OVERRIDE_PROTOCOL: https://uefi.org/specs/UEFI/2.10/11_Protocols_UEFI_Driver_Model.html#efi-bus-specific-driver-override-protocol-protocols-uefi-driver-model
.. _EFI_CC_MEASUREMENT_PROTOCOL: https://uefi.org/specs/UEFI/2.10/38_Confidential_Computing.html#efi-cc-measurement-protocol
.. _EFI_DECOMPRESS_PROTOCOL: https://uefi.org/specs/UEFI/2.10/19_Protocols_Compression_Algorithm_Specification.html#efi-decompress-protocol
.. _EFI_DEVICE_PATH_FROM_TEXT_PROTOCOL: https://uefi.org/specs/UEFI/2.10/10_Protocols_Device_Path_Protocol.html#efi-device-path-from-text-protocol
.. _EFI_DEVICE_PATH_TO_TEXT_PROTOCOL: https://uefi.org/specs/UEFI/2.10/10_Protocols_Device_Path_Protocol.html#efi-device-path-to-text-protocol
.. _EFI_DEVICE_PATH_UTILITIES_PROTOCOL: https://uefi.org/specs/UEFI/2.10/10_Protocols_Device_Path_Protocol.html#efi-device-path-utilities-protocol
.. _EFI_DISK_IO_PROTOCOL: https://uefi.org/specs/UEFI/2.10/13_Protocols_Media_Access.html#efi-disk-io-protocol
.. _EFI_FIRMWARE_MANAGEMENT_PROTOCOL: https://uefi.org/specs/UEFI/2.10/23_Firmware_Update_and_Reporting.html#efi-firmware-management-protocol
.. _EFI_GRAPHICS_OUTPUT_PROTOCOL: https://uefi.org/specs/UEFI/2.10/12_Protocols_Console_Support.html#efi-graphics-output-protocol
.. _EFI_HII_CONFIG_ROUTING_PROTOCOL: https://uefi.org/specs/UEFI/2.10/35_HII_Configuration_Processing_and_Browser_Protocol.html#efi-hii-config-routing-protocol
.. _EFI_HII_DATABASE_PROTOCOL: https://uefi.org/specs/UEFI/2.10/34_HII_Protocols.html#efi-hii-database-protocol
.. _EFI_HII_STRING_PROTOCOL: https://uefi.org/specs/UEFI/2.10/34_HII_Protocols.html#efi-hii-string-protocol
.. _EFI_RNG_PROTOCOL: https://uefi.org/specs/UEFI/2.10/37_Secure_Technologies.html#efi-rng-protocol
.. _EFI_SIMPLE_TEXT_INPUT_PROTOCOL: https://uefi.org/specs/UEFI/2.10/Apx_B_Console.html#efi-simple-text-input-protocol-and-efi-simple-text-input-ex-protocol
.. _EFI_SIMPLE_TEXT_INPUT_EX_PROTOCOL: https://uefi.org/specs/UEFI/2.10/Apx_B_Console.html#efi-simple-text-input-protocol-and-efi-simple-text-input-ex-protocol
.. _EFI_SIMPLE_TEXT_OUTPUT_PROTOCOL: https://uefi.org/specs/UEFI/2.10/Apx_B_Console.html#efi-simple-text-output-protocol-for-pc-ansi-or-ansi-x3-64-terminals
.. _EFI_SIMPLE_NETWORK_PROTOCOL: https://uefi.org/specs/UEFI/2.10/24_Network_Protocols_SNP_PXE_BIS.html#efi-simple-network-protocol
.. _EFI_SIMPLE_FILE_SYSTEM_PROTOCOL: https://uefi.org/specs/UEFI/2.10/13_Protocols_Media_Access.html#efi-simple-file-system-protocol
.. _EFI_DEVICE_PATH_PROTOCOL: https://uefi.org/specs/UEFI/2.10/10_Protocols_Device_Path_Protocol.html
.. _EFI_DRIVER_BINDING_PROTOCOL: https://uefi.org/specs/UEFI/2.10/11_Protocols_UEFI_Driver_Model.html#efi-driver-binding
.. _EFI_DRIVER_FAMILY_OVERRIDE_PROTOCOL: https://uefi.org/specs/UEFI/2.10/11_Protocols_UEFI_Driver_Model.html#efi-driver-family-override-protocol-protocols-uefi-driver-model
.. _EFI_PXE_BASE_CODE_PROTOCOL: https://uefi.org/specs/UEFI/2.10/24_Network_Protocols_SNP_PXE_BIS.html#efi-pxe-base-code-protocol
.. _EFI_PLATFORM_DRIVER_OVERRIDE_PROTOCOL: https://uefi.org/specs/UEFI/2.10/11_Protocols_UEFI_Driver_Model.html#efi-platform-driver-override-protocol
.. _EFI_PCI_IO_PROTOCOL: https://uefi.org/specs/UEFI/2.10/14_Protocols_PCI_Bus_Support.html#id32
.. _EFI_NETWORK_INTERFACE_IDENTIFIER_PROTOCOL: https://uefi.org/specs/UEFI/2.10/24_Network_Protocols_SNP_PXE_BIS.html#efi-network-interface-identifier-protocol
.. _RISCV_EFI_BOOT_PROTOCOL: https://github.com/riscv-non-isa/riscv-uefi/blob/main/boot_protocol.adoc
.. _EFI_TCG_PROTOCOL: https://trustedcomputinggroup.org/wp-content/uploads/TCG_EFI_Protocol_1_22_Final-v05.pdf
.. _EFI_TCG2_PROTOCOL: https://trustedcomputinggroup.org/wp-content/uploads/EFI-Protocol-Specification-rev13-160330final.pdf
.. _EFI_SMBIOS_PROTOCOL: https://uefi.org/specs/PI/1.8/V5_SMBIOS_Protocol.html#efi-smbios-protocol
.. _EFI_HII_CONFIG_ACCESS_PROTOCOL: https://uefi.org/specs/UEFI/2.10/35_HII_Configuration_Processing_and_Browser_Protocol.html#efi-hii-config-access-protocol
.. _EFI_LOADED_IMAGE_PROTOCOL: https://uefi.org/specs/UEFI/2.10/09_Protocols_EFI_Loaded_Image.html#id3
.. _EFI_LOADED_IMAGE_DEVICE_PATH_PROTOCOL: https://uefi.org/specs/UEFI/2.10/09_Protocols_EFI_Loaded_Image.html#id6
.. _EFI_LOAD_FILE_PROTOCOL: https://uefi.org/specs/UEFI/2.10/13_Protocols_Media_Access.html#efi-load-file-protocol
.. _EFI_LOAD_FILE2_PROTOCOL: https://uefi.org/specs/UEFI/2.10/13_Protocols_Media_Access.html#efi-load-file2-protocol
.. _EFI_MANAGED_NETWORK_PROTOCOL: https://uefi.org/specs/UEFI/2.10/25_Network_Protocols_Managed_Network.html#id4
.. _EFI_MEMORY_ATTRIBUTE_PROTOCOL: https://uefi.org/specs/UEFI/2.10/37_Secure_Technologies.html#efi-memory-attribute-protocol
.. _EFI_DT_FIXUP_PROTOCOL: https://github.com/U-Boot-EFI/EFI_DT_FIXUP_PROTOCOL
.. _EFI_UNICODE_COLLATION_PROTOCOL: https://uefi.org/specs/UEFI/2.10/21_Protocols_String_Services.html#efi-unicode-collation-protocol
.. _EFI_HII_PACKAGE_LIST_PROTOCOL: https://uefi.org/specs/UEFI/2.10/07_Services_Boot_Services.html#efi-boot-services-loadimage
.. _EFI_FILE_PROTOCOL: https://uefi.org/specs/UEFI/2.10/13_Protocols_Media_Access.html#efi-file-protocol
.. _EFI_XXX_SERVICE_BINDING_PROTOCOL: https://uefi.org/specs/UEFI/2.10/28_Network_Protocols_TCP_IP_and_Configuration.html#efi-ip4-service-binding-protocol
