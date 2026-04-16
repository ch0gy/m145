# Packet Tracer – Subnet an IPv4 Network

## Part 1: Design an IPv4 Network Subnetting Scheme

- How many host addresses are needed in the largest required subnet?  
  -> 50

- What is the minimum number of subnets required?  
  -> 4

- The network that you are tasked to subnet is 192.168.0.0/24. What is the /24 subnet mask in binary?  
  -> 11111111.11111111.11111111.00000000

- In the network mask, what do the ones represent?  
  -> Den Netzwerkteil

- In the network mask, what do the zeros represent?  
  -> Den Hostteil

---

### 1) (/25) 11111111.11111111.11111111.10000000
- Dotted decimal subnet mask equivalent:  
  -> 255.255.255.128
- Number of subnets? Number of hosts?  
  -> 2 Subnetze, 126 Hosts

### 2) (/26) 11111111.11111111.11111111.11000000
- Dotted decimal subnet mask equivalent:  
  -> 255.255.255.192
- Number of subnets? Number of hosts?  
  -> 4 Subnetze, 62 Hosts

### 3) (/27) 11111111.11111111.11111111.11100000
- Dotted decimal subnet mask equivalent:  
  -> 255.255.255.224
- Number of subnets? Number of hosts?  
  -> 8 Subnetze, 30 Hosts

### 4) (/28) 11111111.11111111.11111111.11110000
- Dotted decimal subnet mask equivalent:  
  -> 255.255.255.240
- Number of subnets? Number of hosts?  
  -> 16 Subnetze, 14 Hosts

### 5) (/29) 11111111.11111111.11111111.11111000
- Dotted decimal subnet mask equivalent:  
  -> 255.255.255.248
- Number of subnets? Number of hosts?  
  -> 32 Subnetze, 6 Hosts

### 6) (/30) 11111111.11111111.11111111.11111100
- Dotted decimal subnet mask equivalent:  
  -> 255.255.255.252
- Number of subnets? Number of hosts?  
  -> 64 Subnetze, 2 Hosts

---

- Considering your answers above, which subnet masks meet the required number of minimum host addresses?  
  -> /25 und /26

- Considering your answers above, which subnet masks meets the minimum number of subnets required?  
  -> /26, /27, /28, /29, /30

- Considering your answers above, which subnet mask meets both the required minimum number of hosts and the minimum number of subnets required?  
  -> /26

---

## Derived Subnets

| Subnet Address | Prefix | Subnet Mask |
|---|---|---|
| 192.168.0.0 | /26 | 255.255.255.192 |
| 192.168.0.64 | /26 | 255.255.255.192 |
| 192.168.0.128 | /26 | 255.255.255.192 |
| 192.168.0.192 | /26 | 255.255.255.192 |

---

## Addressing Table (completed)

| Device | Interface | IP Address | Subnet Mask | Default Gateway |
|---|---|---|---|---|
| CustomerRouter | G0/0 | 192.168.0.1 | 255.255.255.192 | N/A |
| CustomerRouter | G0/1 | 192.168.0.65 | 255.255.255.192 | N/A |
| CustomerRouter | S0/1/0 | 209.165.201.2 | 255.255.255.252 | N/A |
| LAN-A Switch | VLAN1 | 192.168.0.2 | 255.255.255.192 | 192.168.0.1 |
| LAN-B Switch | VLAN1 | 192.168.0.66 | 255.255.255.192 | 192.168.0.65 |
| PC-A | NIC | 192.168.0.62 | 255.255.255.192 | 192.168.0.1 |
| PC-B | NIC | 192.168.0.126 | 255.255.255.192 | 192.168.0.65 |

---

## Part 3: Test and Troubleshoot the Network

- Determine if PC-A can communicate with its default gateway. Do you get a reply?  
  -> Ja

- Determine if PC-B can communicate with its default gateway. Do you get a reply?  
  -> Ja

- Determine if PC-A can communicate with PC-B. Do you get a reply?  
  -> Ja