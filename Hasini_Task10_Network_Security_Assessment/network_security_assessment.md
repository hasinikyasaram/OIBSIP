# Network Security Assessment Report

## Executive Summary

A network security assessment was conducted on a Windows system using Nmap and Wireshark. The objective was to identify open ports, running services, and analyze network traffic.

---

## Scope

Target Host: 192.168.1.15

Assessment Type: Local Network Assessment

---

## Tools Used

- Nmap
- Wireshark

---

## Nmap Scan Results

### Command Used

```bash
nmap -sV 192.168.1.15
```

### Open Ports and Services

| Port | Service | Version |
|--------|---------|---------|
| 135 | msrpc | Microsoft Windows RPC |
| 139 | netbios-ssn | Microsoft NetBIOS |
| 445 | microsoft-ds | SMB Service |
| 2869 | http | Microsoft HTTPAPI 2.0 |
| 3306 | mysql | MySQL |
| 6646 | tcpwrapped | Protected Service |
| 12345 | netbus? | Unknown/Remote Access |

---

## Port Analysis

### Port 135 (MSRPC)

Used by Windows applications and services for communication.

### Port 139 (NetBIOS)

Supports network file and printer sharing.

### Port 445 (SMB)

Provides file-sharing functionality and should be monitored due to common exploitation attempts.

### Port 2869 (HTTPAPI)

Associated with UPnP and SSDP device discovery services.

### Port 3306 (MySQL)

Database service port that should be protected with strong authentication.

### Port 6646 (tcpwrapped)

Protected service that restricts unauthorized access.

### Port 12345 (NetBus?)

Potential remote access service that should be investigated further.

---

## Wireshark Traffic Analysis

Network traffic was captured during normal browsing activities.

### Protocols Observed

- DNS
- TCP
- ARP
- TLSv1.2

### DNS Traffic

Observed DNS requests resolving domain names to IP addresses.

### ARP Traffic

ARP packets were used for communication between local network devices.

### TLSv1.2 Traffic

Encrypted web traffic was observed, indicating secure HTTPS communications.

### TCP Traffic

TCP packets established and maintained connections between systems.

---

## Security Concerns

1. SMB service exposed on Port 445.
2. MySQL service available on Port 3306.
3. UPnP-related service running on Port 2869.
4. Port 12345 requires verification.

---

## Recommendations

- Close unnecessary ports.
- Enable firewall protection.
- Restrict SMB access.
- Secure MySQL with strong passwords.
- Regularly update the operating system.
- Perform routine vulnerability assessments.

---

## Conclusion

The assessment successfully identified active services and normal network traffic patterns. While encrypted communication was observed, several open ports should be reviewed to reduce the overall attack surface and improve network security.
