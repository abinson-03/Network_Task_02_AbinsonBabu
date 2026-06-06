\# Networking Task 02: Network Devices \& IP Addressing



\## 📌 Project Overview

This project focuses on researching core network hardware devices, understanding IPv4 address classification structures, tracking packet communication flows, and executing local DNS diagnostic exercises.



\---



\## 🛠️ Part A: Network Devices Research

| Device | Purpose | How it Works | Real-World Usage |

| :--- | :--- | :--- | :--- |

| \*\*Router\*\* | Connects entirely different networks together. | Inspects destination IPs and forwards packets across routing tables. | Home or college Wi-Fi gateways routing to the Internet. |

| \*\*Switch\*\* | Connects multiple devices within the same local network (LAN). | Maps hardware MAC addresses to point-to-point data packets directly. | Linking computers together inside a college computer laboratory. |

| \*\*Hub\*\* | Connects multiple network devices via a basic layer. | Blindly broadcasts any incoming data packet out to all available ports. | Outdated infrastructure, legacy data tracking environments. |

| \*\*Access Point\*\* | Extends a wired local area network wirelessly. | Plugs into a switch via Ethernet and broadcasts a local Wi-Fi signal. | Ceiling-mounted Wi-Fi units in academic or office hallways. |

| \*\*Firewall\*\* | Establishes a security boundary for filtering traffic. | Analyzes incoming/outgoing packets against established security parameters. | Securing institutional servers against external malicious entities. |

| \*\*Modem\*\* | Translates network data between an ISP and a local router. | Performs signal modulation and demodulation (digital <-> analog conversions). | Broadband box provided by telecom companies (Jio, BSNL, etc.). |



\---



\## 🏷️ Part B: IP Address Classification

1\. \*\*192.168.1.10:\*\* \*\*Private\*\* — Fits inside the Class C private block (`192.168.0.0` - `192.168.255.255`).

2\. \*\*10.0.0.5:\*\* \*\*Private\*\* — Fits inside the Class A private block (`10.0.0.0` - `10.255.255.255`).

3\. \*\*172.16.5.20:\*\* \*\*Private\*\* — Fits inside the Class B private block (`172.16.0.0` - `172.31.255.255`).

4\. \*\*8.8.8.8:\*\* \*\*Public\*\* — Sits outside all private registry ranges; registers globally to Google's Public DNS.

5\. \*\*1.1.1.1:\*\* \*\*Public\*\* — Sits outside all private registry ranges; registers globally to Cloudflare's Public DNS.

6\. \*\*192.168.100.1:\*\* \*\*Private\*\* — Fits inside the Class C private block; widely utilized as a local router configuration address.



\---



\## 💻 Part C: Understanding Your Network

\* \*\*Local Subnet Range:\*\* Class A Private Range (`10.0.0.0` to `10.255.255.255`).

\* \*\*Addressing Nature:\*\* Private IP Address.

\* \*\*Router Role:\*\* Handles Network Address Translation (NAT) to safely map local device metrics to an external public IP, while acting as the default entry/exit gateway.

\* \*\*DNS Failure Implication:\*\* Internet routes remain connected, but human-readable address resolution drops. Users cannot browse via domain labels (like `google.com`) and must use raw public IP references directly instead.



\---



\## 🗺️ Part D: Network Communication Flow

Below is the sequential operational chain triggered when accessing a web resource domain:



!\[Network Communication Flow](./diagrams/communication\_flow.png)



1\. \*\*Local Cache Check:\*\* The web browser checks its internal and operating system caches for recent DNS mapping records.

2\. \*\*Gateway Transport:\*\* Unresolved requests fold into standard packets and hop over Wi-Fi directly to the Default Gateway router.

3\. \*\*DNS Query:\*\* The gateway loops the request out to an ISP or configured DNS directory server to resolve the domain string into an IP address.

4\. \*\*TCP Handshake:\*\* The host system establishes a direct transport line with the target server across public routing lines.

5\. \*\*Data Stream Response:\*\* The web server receives the application request and streams back the HTML/CSS/JS page resources to load the site.



\---



\## ⚡ Part E: Practical Command Exercise

\### Diagnostic Overview

\* \*\*Resolved Google IP Address (DNS):\*\* `2404:6800:4007:81b::200e` (IPv6 Native)

\* \*\*Ping Connectivity Status:\*\* Successful (4 Packets Transmitted, 4 Packets Received, 0% Packet Loss, 126ms Average Latency).

\* \*\*Pre-Communication DNS Importance:\*\* Systems route packets using binary patterns and numeric IP coordinates, not word structures. DNS must resolve these domain strings first so that the initial network packet can map out its target path before any application processing takes place.



\---



\## 🖼️ Verification Artifacts

\* Complete Local Configuration Data: `screenshots/IP1.jpeg`, `screenshots/IP2.jpeg`, `screenshots/IP3.jpeg`

\* Connectivity Outputs (`ping`/`tracert`): `screenshots/Screenshot 2026-06-06 171512.png`



\---



\## 🛠️ Tools Used

\* \*\*Command Line Diagnostics:\*\* ipconfig /all, nslookup, ping.

\* \*\*Documentation Engine:\*\* Markdown Markdown Tables, Git/GitHub.

