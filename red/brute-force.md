# COMMANDS

## Check GPU

```bash
hashcat.exe -I
```

## 10 digits (Old Method)

```bash
hashcat.exe -m 2500 -a 3 10digit.hccapx ?d?d?d?d?d?d?d?d?d?d
```

## Increment WPA2 digits (Old Method)

```bash
hashcat.exe -m 2500 -a 3 10digit.hccapx --increment --increment-min 8 --increment-max 20 ?d?d?d?d?d?d?d?d?d?d?d?d?d?d?d?d?d?d?d?d
```

## 8 digits (New Method)

```bash
hashcat.exe -m 22000 8-digit-wpa2.hc22000 -a 3 ?d?d?d?d?d?d?d?d
```

## 10 digits (New Method)

```bash
hashcat.exe -m 22000 10-digit-wpa2.hc22000 -a 3 ?d?d?d?d?d?d?d?d?d?d
```

## 10 digits and alpha (New Method)

```bash
hashcat.exe -m 22000 10-digit-letters-wpa2.hc22000 -1 ?d?l?u -a 3 ?1?1?1?1?1?1?1?1?1?1
```

## Increment digits (New Method)

```bash
hashcat.exe -m 22000 hash.hc22000 -a 3 --increment --increment-min 8 --increment-max 18 ?d?d?d?d?d?d?d?d?d?d?d?d?d?d?d?d?d?d
```

## Increment digits and alpha (New Method)

```bash
hashcat.exe -m 22000 10-digit-letters-wpa2.hc22000 -1 ?d?l?u -a 3 --increment --increment-min 8 --increment-max 12 ?1?1?1?1?1?1?1?1?1?1?1?1
```
