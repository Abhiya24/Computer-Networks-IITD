# Network Measurement and Traffic Analysis

This assignment involved analyzing network behavior using tools like `ping`, `traceroute`, and Wireshark. The objective was to study latency, protocol usage, packet flow, and performance across different network conditions and IP versions.

##  Tasks Performed

### 1. Latency Analysis (Ping)
- Compared average ping latencies to `google.com` and `sigcomm.org` using:
  - **IITD Network (IPv4 & IPv6)**
  - **Mobile Network (IPv4 & IPv6)**
- Observed:
  - Higher latency to `sigcomm.org` than `google.com`
  - Lower latency over IITD network than mobile network

### 2. Traceroute Analysis
- Traced route to both websites across networks
- Analyzed:
  - Number of hops
  - Autonomous System Numbers (ASNs)
  - Geographic locations of intermediate routers
  - Tier architecture (Tier 2 vs Tier 3)
- Found unusually low RTTs to international hops for Google (possible routing anomalies)

### 3. PCAP File Traffic Breakdown
- Analyzed traffic from a `.pcap` file (linked in report)
- Identified:
  - Predominantly IPv4 (99.9%)
  - Major protocols: UDP, STUN, RTP
  - Audio/Video packet count using RTP stream analysis
  - STUN usage suggested NAT traversal

### 4. Speed Test Traffic Classification
- Filtered and isolated speed test data from full network capture
- Calculated:
  - Download/upload throughput using `pyshark` and `pandas`
  - IO Graphs for speed test traffic vs. rest
  - Found approx. **58–66%** of packets belong to speed test

## ️ Tools & Techniques
- `ping`, `traceroute`
- Wireshark (filters, manual RTP decoding, IO Graphs)
- `pyshark`, `pandas` (Python-based PCAP analysis)
- ASN lookup and Geo-IP analysis

##  Files
- `report.pdf`: Detailed answers, figures, graphs, and Wireshark screenshots

##  Notes
- No code submission required
- PCAP files and supplementary plots are linked in the report

