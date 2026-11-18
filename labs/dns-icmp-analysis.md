# Lab: DNS and ICMP Traffic Analysis - Troubleshooting DNS Failure

## Scenario
User unable to resolve yummyrecipesforme.com

Scenario from the Google Cybersecurity Certificate course (Course 3 - Networks and Network Security) - practice lab, not a real incident.

## What I Did
- Analyzed tcpdump log: Client 192.51.100.15 sent UDP packet to DNS server 203.0.113.2 on Port 53 for A? yummyrecipesforme.com
- Server replied with ICMP "udp port 53 unreachable"

## Root Cause
DNS service not running or rejecting traffic on UDP Port 53 on the server. The server was reachable, but nothing was listening on that port, so it returned ICMP Port Unreachable.

## What I Learned
- DNS uses UDP Port 53 for queries
- UDP is connectionless, so errors are returned via ICMP
- How a SOC analyst uses packet capture to troubleshoot a network security incident

## Tools
tcpdump log analysis
