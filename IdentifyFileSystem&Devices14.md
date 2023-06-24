## Storage Management Concepts:
- File System: the way in which files are named and where they are placed logically for storage and retrieval. 
- RHEL default local file system: ` Extents File System (XFS)`
- For removable media use: `Extensible File Allocation Table (exFAT)`
- A block device is a file that provides low-level access to storage devices in `/dev directory`
- Block Device Naming: <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/9a90b06b-87a0-4f4e-90ba-253bd12a0e2b">
> With partitions, you can compartmentalize a disk.
- SATA-attached[^1] storage, the first partition is the /dev/sda1 disk & so on..
- Paravirtualized storage, the first partition is the /dev/vda1 & so on..
- NVMe[^2] storage devices, first disk is the /dev/nvme0n1p1.
- To display an overview of local and remote file-system devices, disk-filesystem: `df with -h or -H`
- For Disk Usage: `du with -h and -H`

## Mount & Unmount a device:
- To access the file system on a removable storage device, you must mount the storage device.
- Identify a block device: `lsblk -fs`
- Query the UUID[^4] of the a device: `lsblk -fp PATH`
- `mount` instructs the operating system to attach a file system at a specified directory.
- To mount the file system: `mount DEV_PATH DIR_PATH`
- To Unmount: `umount /PATH`


## Locate/Find files on the System:
- To locate files(To search in pre-generated index): `locate KEYWORD`
> The locate database updates automatically every day but can be force by `updatedb`
- To find files(Search in real-time): `find LOCATION -name FILE_NAME`
- Search for Files Based on Ownership or Permission: `find -user developer`
- Find Files Based on Size: `find -size SIZE` (+/- for Greater/Less than)
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/180eab14-6046-4320-8a4a-93bfc0244c48">


























[1^]: SATA (also referred to as Serial ATA) stands for Serial Advanced Technology Attachment, an industry-standard bus interface for connecting a computer's host bus adapter to storage devices such as hard disk drives (HDD), optical drives and solid-state drives (SSD).
[^2]: NVMe (Non-Volatile Memory Express) is a communications interface and driver that defines a command set and feature set for PCIe-based[^3] SSDs.
[^3]: PCIe, or peripheral component interconnect express, is an interface standard for connecting high-speed input output (HSIO) components. Every high-performance computer motherboard has a number of PCIe slots you can use to add GPUs, WiFi cards, or SSD (solid-state drive).
[^4]: UUID (universally unique identifier) for unique labels. This is basically a unique string of characters that the operating system will use to identify your hard disk partitions and other storage components.
