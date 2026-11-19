# Lab 2: SYN Flood (DoS) Attack Analysis - Travel Agency Website Outage

## Scenario
Employees of a travel agency could not open the company's sales webpage. Their browsers showed a connection timeout error, and the monitoring system raised an alert for the web server.

Scenario from the Google Cybersecurity Certificate course - practice lab, not a real incident.

## What I Observed
The packet capture showed a very large number of TCP SYN requests coming from one unfamiliar IP address. The server answered each request with a SYN-ACK, but the connections stayed half-open because the final ACK never arrived.

## Root Cause
A TCP SYN flood, which is a type of Denial of Service (DoS) attack. The attacker sent thousands of fake connection requests to fill the server's connection table, leaving no room for real visitors.

## How the Attack Works
A normal TCP three-way handshake has three steps:

1. Client to server: SYN
2. Server to client: SYN-ACK (the server reserves memory for the connection)
3. Client to server: ACK (the connection is established)

In this attack, the attacker sends only step 1 and never completes step 3. The server keeps waiting for the missing ACK while the half-open connections pile up and use all available slots. Legitimate users then cannot connect and get a timeout.

## Impact
- The sales webpage became completely unavailable, not just slow
- Employees could not search vacation packages for customers
- Lost sales and reduced customer trust
- The server had to be taken offline temporarily to recover

## What I Did
- Took the server offline temporarily so it could recover
- Blocked the attacker's IP address in the firewall
- Noted that blocking an IP is not enough on its own, because the attacker can spoof a new IP address and continue

## How to Prevent This in Future
- Enable SYN cookies
- Configure SYN rate limiting on the firewall
- Use an Intrusion Prevention System (IPS) to detect abnormal SYN rates
- Use a load balancer or a DDoS protection service

## DoS vs DDoS
A DoS attack comes from a single source, as in this case. A DDoS (Distributed Denial of Service) attack comes from many machines at the same time, which makes it much harder to block.
