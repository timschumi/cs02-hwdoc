# Partitions

## Partition table

| #  | Offset (bytes) | Size (bytes) | Partition Name  | Flash Filename                 |
|----|----------------|--------------|-----------------|--------------------------------|
| 0  | 0x0            | 0x40000      | `BOOT`          | `BcmBoot.img`                  |
| 1  | 0x400000       | 0x100000     | `cal`           | -                              |
| 2  | 0x500000       | 0x40000      | `sysparm_dep`   | `sysparm_dep.img`              |
| 3  | 0x540000       | 0x40000      | `parm-spml_dep` | `sysparm2_dep_blob.img`        |
| 4  | 0x580000       | 0x40000      | `RF_CAL_FILE`   | `HEDGE_RF_LE_SS_HAWAII_00.bin` |
| 5  | 0x5c0000       | 0x800000     | `KERNEL`        | `boot.img`                     |
| 6  | 0xdc0000       | 0x800000     | `RECOVERY`      | `recovery.img`                 |
| 7  | 0x15c0000      | 0x12c0000    | `modem`         | `BcmCP.img`                    |
| 8  | 0x2880000      | 0x80000      | `reserved`      | -                              |
| 9  | 0x2900000      | 0x200000     | `SBL1`          | `sboot.bin`                    |
| 10 | 0x2b00000      | 0x200000     | `SBL2`          | -                              |
| 11 | 0x2d00000      | 0x800000     | `PARAM`         | `param.lfs`                    |
| 12 | 0x3500000      | 0x80000      | `DTSBK`         | -                              |
| 13 | 0x3580000      | 0x80000      | `DTS`           | `dt-blob`                      |
| 14 | 0x3600000      | 0x40000      | `FOTA_SIG`      | -                              |
| 15 | 0x3640000      | 0x1400000    | `efs`           | `efs.img`                      |
| 16 | 0x4a40000      | 0xc800000    | `CSC`           | `cache.img`                    |
| 17 | 0x11240000     | 0x482ae000   | `system`        | `system.img`                   |
| 18 | 0x594ee000     | 0x1e00000    | `HIDDEN`        | `hidden.img`                   |
| 19 | 0x5b2ee000     | ?            | `userdata`      | `userdata.img`                 |
| 20 | 0x4400         | 0x2000       | `PIT`           | `cs02.pit`                     |
| 21 | 0x6400         | 0x100000     | `MD5HDR`        | `md5.img`                      |


## PIT dump

The size of one partition block is 512 bytes.

```
Entry Count: 22
Unknown 1: 1598902083
Unknown 2: 844251476
Unknown 3: 21315
Unknown 4: 12848
Unknown 5: 0
Unknown 6: 0
Unknown 7: 0
Unknown 8: 0


--- Entry #0 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 80
Attributes: 2 (STL Read-Only)
Update Attributes: 1 (FOTA)
Partition Block Size/Offset: 0
Partition Block Count: 512
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: BOOT
Flash Filename: BcmBoot.img
FOTA Filename: 


--- Entry #1 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 1
Attributes: 5 (Read/Write)
Update Attributes: 1 (FOTA)
Partition Block Size/Offset: 8192
Partition Block Count: 2048
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: cal
Flash Filename: 
FOTA Filename: 


--- Entry #2 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 2
Attributes: 5 (Read/Write)
Update Attributes: 1 (FOTA)
Partition Block Size/Offset: 10240
Partition Block Count: 512
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: sysparm_dep
Flash Filename: sysparm_dep.img
FOTA Filename: 


--- Entry #3 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 3
Attributes: 5 (Read/Write)
Update Attributes: 1 (FOTA)
Partition Block Size/Offset: 10752
Partition Block Count: 512
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: parm-spml_dep
Flash Filename: sysparm2_dep_blob.img
FOTA Filename: 


--- Entry #4 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 4
Attributes: 5 (Read/Write)
Update Attributes: 1 (FOTA)
Partition Block Size/Offset: 11264
Partition Block Count: 512
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: RF_CAL_FILE
Flash Filename: HEDGE_RF_LE_SS_HAWAII_00.bin
FOTA Filename: 


--- Entry #5 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 5
Attributes: 5 (Read/Write)
Update Attributes: 1 (FOTA)
Partition Block Size/Offset: 11776
Partition Block Count: 16384
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: KERNEL
Flash Filename: boot.img
FOTA Filename: 


--- Entry #6 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 6
Attributes: 5 (Read/Write)
Update Attributes: 1 (FOTA)
Partition Block Size/Offset: 28160
Partition Block Count: 16384
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: RECOVERY
Flash Filename: recovery.img
FOTA Filename: 


--- Entry #7 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 7
Attributes: 5 (Read/Write)
Update Attributes: 1 (FOTA)
Partition Block Size/Offset: 44544
Partition Block Count: 38400
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: modem
Flash Filename: BcmCP.img
FOTA Filename: 


--- Entry #8 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 8
Attributes: 5 (Read/Write)
Update Attributes: 1 (FOTA)
Partition Block Size/Offset: 82944
Partition Block Count: 1024
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: reserved
Flash Filename: 
FOTA Filename: 


--- Entry #9 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 9
Attributes: 5 (Read/Write)
Update Attributes: 1 (FOTA)
Partition Block Size/Offset: 83968
Partition Block Count: 4096
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: SBL1
Flash Filename: sboot.bin
FOTA Filename: 


--- Entry #10 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 10
Attributes: 5 (Read/Write)
Update Attributes: 1 (FOTA)
Partition Block Size/Offset: 88064
Partition Block Count: 4096
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: SBL2
Flash Filename: 
FOTA Filename: 


--- Entry #11 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 11
Attributes: 5 (Read/Write)
Update Attributes: 1 (FOTA)
Partition Block Size/Offset: 92160
Partition Block Count: 16384
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: PARAM
Flash Filename: param.lfs
FOTA Filename: 


--- Entry #12 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 12
Attributes: 5 (Read/Write)
Update Attributes: 1 (FOTA)
Partition Block Size/Offset: 108544
Partition Block Count: 1024
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: DTSBK
Flash Filename: 
FOTA Filename: 


--- Entry #13 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 13
Attributes: 5 (Read/Write)
Update Attributes: 1 (FOTA)
Partition Block Size/Offset: 109568
Partition Block Count: 1024
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: DTS
Flash Filename: dt-blob
FOTA Filename: 


--- Entry #14 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 14
Attributes: 5 (Read/Write)
Update Attributes: 1 (FOTA)
Partition Block Size/Offset: 110592
Partition Block Count: 512
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: FOTA_SIG
Flash Filename: 
FOTA Filename: 


--- Entry #15 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 15
Attributes: 5 (Read/Write)
Update Attributes: 5 (FOTA)
Partition Block Size/Offset: 111104
Partition Block Count: 40960
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: efs
Flash Filename: efs.img
FOTA Filename: 


--- Entry #16 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 16
Attributes: 5 (Read/Write)
Update Attributes: 5 (FOTA)
Partition Block Size/Offset: 152064
Partition Block Count: 409600
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: CSC
Flash Filename: cache.img
FOTA Filename: 


--- Entry #17 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 17
Attributes: 5 (Read/Write)
Update Attributes: 5 (FOTA)
Partition Block Size/Offset: 561664
Partition Block Count: 2364784
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: system
Flash Filename: system.img
FOTA Filename: 


--- Entry #18 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 18
Attributes: 5 (Read/Write)
Update Attributes: 5 (FOTA)
Partition Block Size/Offset: 2926448
Partition Block Count: 61440
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: HIDDEN
Flash Filename: hidden.img
FOTA Filename: 


--- Entry #19 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 19
Attributes: 5 (Read/Write)
Update Attributes: 5 (FOTA)
Partition Block Size/Offset: 2987888
Partition Block Count: 0
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: userdata
Flash Filename: userdata.img
FOTA Filename: remained


--- Entry #20 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 70
Attributes: 5 (Read/Write)
Update Attributes: 1 (FOTA)
Partition Block Size/Offset: 34
Partition Block Count: 16
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: PIT
Flash Filename: cs02.pit
FOTA Filename: 


--- Entry #21 ---
Binary Type: 0 (AP)
Device Type: 2 (MMC)
Identifier: 71
Attributes: 5 (Read/Write)
Update Attributes: 1 (FOTA)
Partition Block Size/Offset: 50
Partition Block Count: 2048
File Offset (Obsolete): 0
File Size (Obsolete): 0
Partition Name: MD5HDR
Flash Filename: md5.img
FOTA Filename: 
```
