# Active Reconnaissance - Ethical Hacking

## Overview

This repository contains documentation and steps followed during the **Active Reconnaissance** task from the Ethical Hacking course (02193) at DTU. The objective was to explore, analyze, and extract sensitive information using various reconnaissance techniques.

## Steps Followed

### 1. Identifying Backup Files

- Navigated to the target website: `https://dtu.shelltrail.io`
- Found `.bak` files containing potentially sensitive information:
  - `SECURITY.bak`
  - `SYSTEM.bak`
  - `SAM.bak`

### 2. Exploiting File Access

- Renamed `.bak` files to `.txt` for easier retrieval.
- Used the command:
  ```
  1.1.1.1 && copy SYSTEM.bak SYSTEM.bak.txt
  ```

### 3. Extracting Hashes

- Used `impacket-secretsdump` in Kali Linux to extract system hashes:
  ```
  impacket-secretsdump -system SYSTEM.bak -security SECURITY.bak -sam SAM.bak
  ```
- Retrieved local SAM hashes and system bootkey.

### 4. Cracking the Hashes

- Uploaded extracted hashes to [Hashes.com](https://hashes.com/)
- Successfully cracked a hash, retrieving the password: **Havfrue1**

## Tools Used

- Kali Linux
- `impacket-secretsdump`
- Hashes.com

## Disclaimer

This project was conducted for **educational purposes only** as part of an ethical hacking course. Unauthorized penetration testing or exploitation of systems without permission is illegal and unethical.

## Author



VASUDEV GOUD BIKKI
