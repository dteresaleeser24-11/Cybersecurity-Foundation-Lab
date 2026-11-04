
# Linux Command Cheat Sheet

## Cybersecurity Foundation Lab

This cheat sheet summarizes essential Linux commands used during the Foundation & Environment Setup Lab organized as part of the ApexPlanet cybersecurity learning task.

## 1. Navigation & File System

| Command | Description |
|---|---|
| `pwd` | Display the current working directory. |
| `ls` | List files and directories. |
| `ls -la` | List all files, including hidden files, with permissions. |
| `cd /etc` | Navigate to the /etc directory. |
| `cd ~` | Return to the home directory. |
| `mkdir test` | Create a directory named test. |
| `touch text.txt` | Create an empty file. |
| `cat text.txt` | Display file contents. |
| `cp file.txt backup.txt` | Copy a file. |
| `mv file.txt new.txt` | Rename or move a file. |

## 2. Permissions & Ownership

| Command | Description |
|---|---|
| `chmod 755 text.txt` | Set file permissions. |
| `chmod 644 text.txt` | Give owner read/write and others read access. |
| `ls -l` | Display file permissions and ownership. |
| `sudo chown root:root text.txt` | Change file owner and group to root. |

**Permission Reference:**
- 7 = Read + Write + Execute
- 6 = Read + Write
- 5 = Read + Execute
- 4 = Read only

## 3. Package Management (Kali Linux)

| Command | Description |
|---|---|
| `sudo apt update` | Refresh available package information. |
| `sudo apt upgrade` | Upgrade installed packages. |
| `sudo apt install nmap` | Install Nmap. |
| `sudo apt install netcat-traditional` | Install Netcat Traditional. |
| `dpkg -l` | List installed packages. |

## 4. Networking Commands

| Command | Description |
|---|---|
| `ip a` | Display network interfaces and IP addresses. |
| `ip route` | Display routing information. |
| `ping -c 4 <IP>` | Send four connectivity test packets. |
| `nslookup google.com` | Query DNS information. |
| `traceroute google.com` | Display the network path to a destination. |
| `netstat -tuln` | Display listening TCP and UDP ports. |

## 5. Cryptography (OpenSSL)

### Generate a SHA-256 Hash

```bash
sha256sum secret.txt
```

### Generate an MD5 Hash

```bash
md5sum secret.txt
```

### Encrypt a File

```bash
openssl enc -aes-256-cbc -salt -pbkdf2 -in secret.txt -out secret.enc
```

### Decrypt a File

```bash
openssl enc -d -aes-256-cbc -pbkdf2 -in secret.enc -out decrypted.txt
```

**Note:** OpenSSL will prompt for a password. Use a sample file for practice.

## 6. Cybersecurity Tools

| Tool | Purpose |
|---|---|
| Kali Linux | Security testing environment. |
| Nmap | Network discovery and security auditing. |
| Wireshark | Network packet analysis. |
| Burp Suite | Web application traffic inspection. |
| Netcat | Network connection and troubleshooting. |
| OpenSSL | Cryptographic operations. |

## 7. Important Concepts

- **CIA Triad:** Confidentiality, Integrity, Availability.
- **TCP/IP:** Communication protocol suite.
- **DNS:** Domain Name System.
- **HTTP/HTTPS:** Web communication protocols.
- **Hashing:** Producing a fixed-length digest of data.
- **Encryption:** Protecting information using cryptographic keys.
- **Host-Only Network:** Isolated virtual machine networking.

## Conclusion

These commands and concepts provide a foundation for Linux administration, networking, cryptography, and cybersecurity operations.

**Project:** Cybersecurity Foundation & Environment Setup  
**Organization:** ApexPlanet

