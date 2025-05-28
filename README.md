# 📄 Task 1 of the Elevate Labs Cybersecurity Internship
# Network Vulnerability Assessment Report

**Target Network:** 172.22.7.1/30  
**Scan Method:** TCP SYN Scan (`-sS`) with OS Detection (`-O`)  
**Scan Date:** May 27, 2025  
**Tool Used:** Nmap 7.93  
**Scan results:** (https://github.com/shivdev729/elevate_labs_task_01/blob/main/nmap_scan_results.txt)

![Target network](https://github.com/shivdev729/elevate_labs_task_01/blob/main/p1.JPG)

---

## Host: 172.22.7.1

### Open Ports and Services:
- **22/tcp (SSH)**: OpenSSH 7.2p2
- **80/tcp (HTTP)**: Apache httpd 2.4.18
- **3306/tcp (MySQL)**: MySQL 5.7.31

### Potential Vulnerabilities:
- **OpenSSH 7.2p2**: May be vulnerable to information disclosure and username enumeration 
- **Apache 2.4.18**: Outdated version, potential for vulnerabilities such as broken authentication.
- **MySQL 5.7.31**: Several known CVEs related to privilege escalation and information disclosure.

---

## Host: 172.22.7.2

### Open Ports and Services:
- **21/tcp (FTP)**: vsftpd 2.3.4
- **23/tcp (Telnet)**: Linux telnetd
- **139/tcp (NetBIOS)**: Samba smbd 3.X - 4.X
- **445/tcp (SMB)**: Samba smbd 4.3.11

### Potential Vulnerabilities:
- **vsftpd 2.3.4**: Contains a known backdoor vulnerability.
- **Telnet**: Insecure protocol, transmits data in plaintext.
- **Samba 4.3.11**: Vulnerable to EternalRed allowing RCE.

---

## Host: 172.22.7.3

### Open Ports and Services:
- **22/tcp (SSH)**: OpenSSH 6.6.1p1
- **80/tcp (HTTP)**: nginx 1.10.3
- **5432/tcp (PostgreSQL)**: PostgreSQL 9.5.21

### Potential Vulnerabilities:
- **OpenSSH 6.6.1p1**: Subject to CVEs related to weak default configurations
- **nginx 1.10.3**: Known directory traversal and buffer overflow vulnerabilities 
- **PostgreSQL 9.5.21**: Known vulnerabilities include privilege escalation

---

## Host: 172.22.7.4

### Open Ports and Services:
- **445/tcp (SMB)**: Samba smbd 4.1.6
- **3306/tcp (MySQL)**: MySQL 5.5.62
- **23/tcp (Telnet)**: Linux telnetd

### Potential Vulnerabilities:
- **Samba 4.1.6**: Subject to RCE via some CVE exploits.
- **MySQL 5.5.62**: Contains multiple CVEs including authentication bypass.
- **Telnet**: High risk due to lack of encryption.

---

__Submitted by__:- Shivang Shukla
