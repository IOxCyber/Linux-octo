## Storage Management Concepts:
- RHEL default local file system: ` Extents File System (XFS)`
- For removable media use: `Extensible File Allocation Table (exFAT)`
- A block device is a file that provides low-level access to storage devices in `/dev directory`
- Block Device Naming: <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/9a90b06b-87a0-4f4e-90ba-253bd12a0e2b">
> With partitions, you can compartmentalize a disk.
- SATA-attached[^1] storage, the first partition is the /dev/sda1 disk & so on..
- Paravirtualized storage, the first partition is the /dev/vda1 & so on..
- NVMe[^2] storage devices, first disk is the /dev/nvme0n1p1.
- To display an overview of local and remote file-system devices, disk-filesystem: `df with -h or -H`
- For more detailed information about a specific directory tree space: `du with -h and -H`

## Mount & Unmount a device:
- To access the file system on a removable storage device, you must mount the storage device.
- Identify a block device: `lsblk`
- `mount` instructs the operating system to attach a file system at a specified directory.
- To `mount` the file system by `UUID` or with `device name in /dev` dir.
- To Unmount: `umount /mnt/data`
- 


- 

























[1^]: SATA (also referred to as Serial ATA) stands for Serial Advanced Technology Attachment, an industry-standard bus interface for connecting a computer's host bus adapter to storage devices such as hard disk drives (HDD), optical drives and solid-state drives (SSD).
[^2]: NVMe (Non-Volatile Memory Express) is a communications interface and driver that defines a command set and feature set for PCIe-based[^3] SSDs.
[^3]: PCIe, or peripheral component interconnect express, is an interface standard for connecting high-speed input output (HSIO) components. Every high-performance computer motherboard has a number of PCIe slots you can use to add GPUs, WiFi cards, or SSD (solid-state drive).
