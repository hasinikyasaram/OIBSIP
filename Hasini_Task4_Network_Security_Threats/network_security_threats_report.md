# Research Report on Common Network Security Threats

**Prepared by:** Hasini Kyasaram  
**Domain:** Cyber Security  
**Organization:** Oasis Infobyte  

---

## 2. Introduction
Network security is the practice of protecting computer networks, devices, and data from unauthorized access, misuse, and cyberattacks. As organizations increasingly depend on digital infrastructure, network security has become essential for maintaining corporate survival and data protection.

Cyber threats directly undermine the **CIA Triad**, which is the foundational framework of information security:
* **Confidentiality:** Attacks like eavesdropping or interception expose private data to unauthorized individuals, breaking trust and privacy.
* **Integrity:** Unauthorized modifications or spoofing attacks alter data mid-transit, rendering information unreliable or corrupted.
* **Availability:** Flooding attacks disrupt infrastructure, ensuring that critical data, applications, and services are completely unreachable for legitimate users when needed.

---

## 3. Denial of Service (DoS) Attack
* **Definition:** A Denial of Service (DoS) attack is a malicious attempt to make a server, service, or network resource unavailable to its intended users.
* **How It Works:** An attacker sends a massive flood of malicious requests from a single machine to a target server. The server's processing capacity becomes completely overwhelmed trying to handle the fake traffic, causing it to crash or freeze. As a result, legitimate users are locked out and cannot access services.
* **Impact:** Severe service outages, operational business disruptions, and immediate revenue loss.
* **Real-World Example:** The infamous **2016 Dyn attack**, which crippled major internet platforms and services, featured massive components of traffic flooding that effectively brought down large portions of internet infrastructure on the US East Coast.
* **Prevention:** Implementing robust network Firewalls, enforcing Rate Limiting to limit maximum requests per IP, and setting up strict Traffic Filtering.

---

## 4. Distributed Denial of Service (DDoS)
* **Definition:** A Distributed Denial of Service (DDoS) attack is a large-scale attempt to disrupt server availability by flooding it with traffic originating from thousands of distributed sources simultaneously.
* **Difference between DoS and DDoS:** A DoS attack uses a single internet connection and machine to launch an attack, making the source easy to identify and block. A DDoS attack uses thousands of compromised devices scattered globally, making it exponentially harder to mitigate.
* **Botnets:** Attackers build a "botnet" by infecting vulnerable IoT devices, computers, and servers with malware. The attacker acts as a botmaster, commanding this army of infected "zombie" machines to attack a single target at once.
* **Real-World Example:** The **Mirai Botnet** systematically scanned the internet for poorly secured IoT devices (like security cameras and routers) using default passwords, bound them into a massive botnet, and launched historically devastating DDoS attacks.
* **Prevention Methods:** Deploying cloud-based DDoS mitigation services (such as Cloudflare or Akamai), scaling up network bandwidth, and configuring global load balancers.

---

## 5. Man-in-the-Middle (MITM) Attack
* **Definition:** A Man-in-the-Middle (MITM) attack occurs when a malicious actor secretly intercepts, relays, and alters the communication between two parties who believe they are talking directly to each other.
* **Working Process:** The attacker positions themselves silently within the communication path. All data packets pass directly through the attacker's machine before reaching the final destination. This setup allows the attacker to silently steal, view, or even modify the data in real time.
* **Impact:** Widespread credential theft, financial fraud, session hijacking, and severe data manipulation.
* **Example:** Public Wi-Fi attacks, where a hacker sets up a rogue, unencrypted access point named "Free Airport Wi-Fi" to capture all data typed by connected victims.
* **Prevention:** Uniform enforcement of HTTPS across websites, mandate the use of Virtual Private Networks (VPNs) on public networks, and implement end-to-end encryption.

---

## 6. IP Spoofing
* **Definition:** IP Spoofing is a technique where an attacker alters the source IP address in the header of an IP packet to impersonate a trusted computer system.
* **Risks:** * **Bypassing Security Controls:** Firewalls that rely solely on IP-based access control lists (ACLs) can be fooled into letting malicious packets into a secure local network.
  * **Launching Attacks Anonymously:** Masking the true origin of an attack prevents defenders from tracing it back to the true source.
* **Prevention:** Utilizing Ingress and Egress packet filtering, and requiring cryptographic authentication mechanisms for all remote data packets.

---

## 7. DNS Spoofing (DNS Cache Poisoning)
* **Definition:** DNS Spoofing is an attack where altered Domain Name System data is introduced into a DNS resolver's cache, causing the name server to return an incorrect IP address.
* **Impact:** * **Website Redirection:** Users typing a legitimate URL (like a bank website) are quietly redirected to a perfectly replicated malicious phishing website.
  * **Credential Theft & Malware Infections:** Once trapped on the fake site, users unwittingly hand over login credentials or download drive-by malware payloads.
* **Prevention:** Implementation of **DNSSEC** (DNS Security Extensions) to cryptographically sign data, and using highly secure, updated DNS services.

---

## 8. ARP Spoofing
* **Definition:** ARP Spoofing involves sending malicious Address Resolution Protocol (ARP) messages onto a local area network to link an attacker’s MAC address directly with the legitimate IP address of a target server or default gateway.
* **Impact:** * **Traffic Interception:** All data packets meant for the legitimate gateway flow directly through the attacker instead.
  * **Network Disruption:** Allows attackers to effortlessly launch local MITM attacks or execute LAN-wide denial of service.
* **Prevention:** Configuring Static ARP entries for critical infrastructure assets, and deploying continuous network monitoring tools to look for rogue ARP responses.

---

## 9. Comparison Table

| Threat | Description | Impact | Prevention |
| :--- | :--- | :--- | :--- |
| **DoS** | Single-source flooding attack | Service outage & downtime | Rate limiting, Firewalls |
| **DDoS** | Multi-source botnet flooding attack | Large-scale infrastructure disruption | Cloud DDoS protection, Load balancing |
| **MITM** | Intercepted communication path | Data theft, credential exposure | End-to-end Encryption, Corporate VPNs |
| **IP Spoofing** | Fake source IP address packet modification | Unauthorized access, identity hiding | Ingress/Egress Packet filtering |
| **DNS Spoofing** | Compromised and poisoned DNS cache entries | Website redirection, phishing exposure | DNSSEC validation protocols |
| **ARP Spoofing** | Fake ARP messages mapping MAC to local IP | Local traffic interception, LAN MITM | Static ARP entries, Network monitoring |

---

## 10. Best Practices for Network Security
To protect enterprise assets against complex threat vectors, organizations must implement a multi-layered security defense strategy:
* **Regular Software Updates:** Apply patches quickly to close existing security flaws before they are exploited.
* **Strong Passwords & Multi-Factor Authentication (MFA):** Eradicate default credentials and require multi-layered authentication steps across all accounts.
* **Firewalls & IDS/IPS:** Set up modern firewalls alongside Intrusion Detection and Prevention Systems to inspect incoming traffic for anomalies.
* **Network Segmentation:** Divide networks into smaller, isolated zones to stop attackers from moving laterally if they breach one section.
* **Employee Awareness Training:** Educate staff to notice anomalies, fake links, rogue networks, and phishing indicators.
* **Continuous Monitoring:** Run automated vulnerability scanners and log analytics to catch threats before they spread.

---

## 11. Conclusion
Network security threats continue to evolve as technology advances. Attacks such as DoS, DDoS, MITM, and spoofing can devastate businesses by exposing confidential data, wiping out consumer trust, and causing massive financial harm. By combining automated technical tools with disciplined network architecture and regular training, organizations can successfully lower their risk profile and keep their critical data safe.
