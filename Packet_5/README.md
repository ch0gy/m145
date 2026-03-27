# Packet Tracer - Examine the ARP Table

## Part 1: Examine an ARP Request

- Is this address listed in the table above?  
  -> Nein. Die Ziel-MAC ist die Broadcast-Adresse `FFFF.FFFF.FFFF` und diese steht nicht in der Tabelle.

- How many copies of the PDU did Switch1 make?  
  -> 2

- What is the IP address of the device that accepted the PDU?  
  -> 172.16.31.3

- What happened to the source and destination MAC addresses?  
  -> Die Source-MAC bleibt die vom sendenden Gerät. Die Destination-MAC ist die Broadcast-MAC `FFFF.FFFF.FFFF`.

- How many copies of the PDU did the switch make during the ARP reply?  
  -> 1

- Do the MAC addresses of the source and destination align with their IP addresses?  
  -> Ja

- To what IP address does the MAC address entry correspond?  
  -> 172.16.31.3

- In general, when does an end device issue an ARP request?  
  -> Wenn es die MAC-Adresse zu einer bekannten IPv4-Adresse im lokalen Netzwerk nicht kennt.

---

## Part 2: Examine a Switch MAC Address Table

- How many replies were sent and received?  
  -> 4 gesendet, 4 empfangen

- Do the entries correspond to those in the table above?  
  -> Ja

- Do the entries correspond to those in the table above?  
  -> Ja

- Why are two MAC addresses associated with one port?  
  -> Weil an diesem Port ein Access Point hängt und darüber mehrere Geräte erreichbar sind.

---

## Part 3: Examine the ARP Process in Remote Communications

- What is the IP address of the new ARP table entry?  
  -> 172.16.31.1

- How many PDUs appear?  
  -> 2

- What is the target destination IP destination address of the ARP request?  
  -> 172.16.31.1

- Why?  
  -> Weil das Ziel in einem fremden Netzwerk liegt. Darum wird nicht die MAC des Endgeräts gesucht, sondern die MAC des Default Gateways.

- How many MAC addresses are in the table? Why?  
  -> 0, weil Router keine switch MAC address table wie ein Switch führen.

- Is there an entry for 172.16.31.2?  
  -> Ja

- What happens to the first ping in a situation where the router responds to the ARP request?  
  -> Der erste Ping kann fehlschlagen oder verzögert sein, weil zuerst die ARP-Auflösung gemacht werden muss.