# cisco_updates

deploy IOS updates to Cisco Devices

Deploys Cisco IOS/IOS-XE Code to devices. Checks MD5 checksum prior to actually installing/changing boot variables to ensure image is intact. May need to tweak transfer timeout variables for your environment, and depending on models of devices.

# currently supported/tested devices
- C9300-24U
- C9300-48U
- C9500-16X
- C9500-40X
- WS-C3560CX-12PC-S
- WS-C3560CG-8PC-S

Variables:
```
tftp_server: 10.205.101.38
tftp_blocksize: 1468 # theoretical best max for 1500 MTU network

# timeouts
ios_copy_timeout: 600
ios_reboot_timeout: 300

# versions for 3560CG Switches
ios_cg_version: "12.5(2)E10"
ios_file_3560_cg: c3560c405ex-universalk9-mz.152-2.E10.bin
ios_checksum_3560_cg: 6421c6090e78dda2bf5d8fb9b54bbb44

# versions for 3560CX Switches
ios_cx_version: "15.2(7)E2"
ios_file_3560_cx: c3560cx-universalk9-mz.152-7.E2.bin
ios_checksum_3560_cx: 17d91bba7d6f5780c491cd635685a260
```
