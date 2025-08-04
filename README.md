# Task 1: Scan Your Local Network for Open Ports

## Objective
The objective of this task was to learn how to discover open ports on devices within my local network to understand network exposure.

## Tools Used
- Nmap 7.95  
- Wireshark 4.4.7 (for packet capture and analysis)

## Steps Performed
1. Identified my local network IP range as `192.168.29.0/24` using `ipconfig`.
2. Performed a TCP SYN scan on the local network using the command:  
nmap -sS 192.168.29.0/24 -oN scan_results.txt

text
3. Saved and analyzed the scan results.
4. Captured network traffic during the scan using Wireshark to observe the scan packets and corresponding responses.
5. Saved a packet capture file (`task1.pcapng`) and took screenshots for documentation.

## Scan Results Summary
- Scanned 256 IP addresses in the local network.
- Found 6 hosts active (responding).
- Open ports detected include:  
- HTTP (80), HTTPS (443), UPNP (1900), HTTP Proxy (8080), HTTPS-alt (8443) on devices such as `192.168.29.1` and `192.168.29.222`.
- Several devices had no open ports or were filtered, indicating a limited exposure and good network security practices.

## Wireshark Analysis
The Wireshark capture shows TCP SYN packets sent by Nmap and the corresponding SYN-ACK or RST responses from devices. This validates the status of ports as open, closed, or filtered. The included screenshot (`wireshark_screenshot.png`) in the screenshot directory provides visual evidence of this packet exchange.
