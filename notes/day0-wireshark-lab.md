# Day 0 – Wireshark Mini Lab (HTTP on loopback)
**Goal:** capture and inspect basic HTTP traffic.

**What I did:**
1) Started Wireshark on macOS loopback (lo0).
2) Browsed to example.com and httpforever.com to generate HTTP requests.
3) Applied Wireshark filter `http` to focus only on HTTP packets.

**Findings (what I observed):**
- Saw HTTP GET requests with the Host and Request URI shown.
- Confirmed User-Agent string (my browser) in the packet details.
- Verified the 3-way TCP handshake happens before the HTTP request (SYN → SYN/ACK → ACK).

**Why this matters for a SOC analyst:**
- Being able to filter for protocols and read request details helps triage web-related alerts.
- Knowing how to locate Host, URI, and User-Agent is useful when investigating suspicious traffic.

**Evidence:**
- Screenshot: ../screenshots/Day0-wireshark-http.png
- PCAP: ../pcaps/day0-http.pcapng
