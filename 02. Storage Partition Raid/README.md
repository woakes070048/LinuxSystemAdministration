<p align="center"><a href="https://softuni.bg/">
<img src="https://raw.githubusercontent.com/velialarm/PHP-and-MySQL/master/softuni.png" /></a></p>

Linux Commands
=========================


/dev/mapper/lu-system on /system type ext3 (rw)
/dev/mapper/lu-homes on /home type ext3 (rw)
/dev/mapper/lu-tmp on /tmp type reiserfs (rw,noexec,nosuid,nodev,noatime)
/dev/mapper/lu-storage on /system/storage type ext3 (rw)

root@wolf:~# fdisk -l /dev/sda
Disk /dev/sda: 120.0 GB, 120030944768 bytes
255 heads, 63 sectors/track, 14592 cylinders
Units = cylinders of 16065 * 512 = 8225280 bytes

Device Boot Start End Blocks Id System
/dev/sda1 * 1 14592 117210208+ 8e Linux LVM

root@wolf:~# pvdisplay
--- Physical volume ---
PV Name /dev/sda1
VG Name lu
PV Size 111.78 GB / not usable 0
Allocatable yes
PE Size (KByte) 4096
Total PE 28615
Free PE 3658
Allocated PE 24957
PV UUID d6iLHy-0izS-JAMp-l4XG-3E0k-H4YO-PfEWhT

root@wolf:~# vgdisplay
--- Volume group ---
VG Name lu
System ID
Format lvm2
Metadata Areas 1
Metadata Sequence No 7
VG Access read/write
VG Status resizable
MAX LV 0
Cur LV 5
Open LV 5
Max PV 0
Cur PV 1
Act PV 1
VG Size 111.78 GB
PE Size 4.00 MB
Total PE 28615
Alloc PE / Size 24957 / 97.49 GB
Free PE / Size 3658 / 14.29 GB
VG UUID iGizW3-4jEt-aUrh-KmZg-erD1-zCAs-mYecuG

root@wolf:~# lvdisplay
--- Logical volume ---
LV Name /dev/lu/storage
VG Name lu
LV UUID HPwRcZ-sp6t-bjam-tQmr-Rm2X-vjoo-j1VHgv
LV Write Access read/write
LV Status available
# open 1
LV Size 80.00 GB
Current LE 20480
Segments 1
Allocation inherit
Read ahead sectors 0
Block device 253:0

--- Logical volume ---
LV Name /dev/lu/tmp
VG Name lu
LV UUID E3NU1f-aIrs-JTy8-TV8b-szOP-VcYy-7GgLn8
LV Write Access read/write
LV Status available
# open 2
LV Size 2.00 GB
Current LE 512
Segments 1
Allocation inherit
Read ahead sectors 0
Block device 253:1

--- Logical volume ---
LV Name /dev/lu/homes
VG Name lu
LV UUID oq0AIB-91Ut-b3H7-h8PV-sqlp-iT5y-puIJgj
LV Write Access read/write
LV Status available
# open 1
LV Size 7.00 GB
Current LE 1792
Segments 1
Allocation inherit
Read ahead sectors 0
Block device 253:2

--- Logical volume ---
LV Name /dev/lu/system
VG Name lu
LV UUID 4pJOpM-QPI5-XhAi-gYF2-7Iy3-bfL3-k2TUUb
LV Write Access read/write
LV Status available
# open 1
LV Size 8.00 GB
Current LE 2048
Segments 1
Allocation inherit
Read ahead sectors 0
Block device 253:3

--- Logical volume ---
LV Name /dev/lu/swap
VG Name lu
LV UUID LJs944-VrsD-OgHJ-IkIT-60cP-ZVk6-A9LQmN
LV Write Access read/write
LV Status available
# open 1
LV Size 500.00 MB
Current LE 125
Segments 1
Allocation inherit
Read ahead sectors 0
Block device 253:4


http://en.wikipedia.org/wiki/Logical_Volume_Manager_%28Linux%29
http://en.wikipedia.org/wiki/Universally_Unique_Identifier
http://en.wikipedia.org/wiki/Device_mapper
http://en.wikipedia.org/wiki/Physical_extent
http://en.wikipedia.org/wiki/Logical_extent
http://sources.redhat.com/lvm2/

