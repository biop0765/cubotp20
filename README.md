# cubotp20

#### dd the system

```shell
adb shell su -c dd if=/dev/block/mmcblk0p28 of=/storage/emulated/0/use_me_blk0p28-06-10-2020.img
```
#### enable user setup complete. See last 2 lines of bootstat.rc 
```shell
su -c cp -v /storage/emulated/0/bootstat.rc /etc/init/bootstat.rc
```

## change this

```shell
    exec u:r:shell:s0 shell shell input log adb sdcard_rw sdcard_r net_bt_admin net_bt inet net_bw_stats -- /system/bin/sh /system/bin/settings put global device_provisioned 1
    exec u:r:shell:s0 shell shell input log adb sdcard_rw sdcard_r net_bt_admin net_bt inet net_bw_stats -- /system/bin/sh /system/bin/settings put secure user_setup_complete 1
```
