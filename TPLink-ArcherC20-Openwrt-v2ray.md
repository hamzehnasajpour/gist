## Installing V2ray on TPLink-ArcherC20 and openwrt

**This router has only 8MB flash and you can't install v2ray on it directly.**

### Solution

#### Using sshfs to mount a shared partition

1. Install/enable ssh server on one of your device in your network.
2. Create a directory on it to share the files. (I used a USB Flash 8G)
3. Extract `v2ray` binary files based on your cpu arch from here: https://github.com/hamzehnasajpour/v2ray-package/tree/main/openwrt.kuoruan.net/packages/releases          
  a. my device has a `MediaTek MT7628AN`: Cpu Type= `MIPS24KEc`           
  b. go to the related folder. (for me: https://github.com/hamzehnasajpour/v2ray-package/tree/main/openwrt.kuoruan.net/packages/releases/mipsel_24kc)         
  c. extract the binary files from `ipk` and copy them to the directory you created in (2).        
```bash
tar zxpvf v2ray-core_4.44.0-1_mipsel_24kc.ipk
tar xvf data.tar.gz 
```
4. Now you should have a file structure like this on the directory you created in (2).
```bash
.
├── control.tar.gz
├── data.tar.gz
└── usr
    ├── bin
    │   ├── v2ctl
    │   └── v2ray
    └── share
        └── v2ray
            ├── geoip.dat
            └── geosite.dat
```

5. Now you just need `config.json` for running the `v2ray`, so copy it in the directory.
6. On your router (form me TPLink-C20) run this command to mount the directory created in (2)
```bash
sshfs -o allow_other,default_permissions user@DEVICE_IP:/PATH/DIR/CREATED/IN/2 /mnt/
```
7. go to the path in your router and run the `v2ray`.
```bash
cd /mnt/
./usr/bin/v2ray run --config=config.json
V2Ray 4.44.0 (OpenWrt) R1 (go1.17.3 linux/mipsle)
A unified platform for anti-censorship.
2022/10/28 18:24:43 Using config from STDIN
2022/10/28 18:24:43 [Info] main/jsonem: Reading config: stdin:

```
