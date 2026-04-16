# Packet Tracer - Identify MAC and IP Addresses

## Part 2

- What device has the destination MAC that is shown?  
  -> Der Router (Default Gateway)

---

## Reflection Questions

1. Were there different types of cables/media used to connect devices?  
-> Ja

2. Did the cables change the handling of the PDU in any way?  
-> Nein

3. Did the Hub lose any of the information that it received?  
-> Nein

4. What does the Hub do with MAC addresses and IP addresses?  
-> Ignoriert sie und sendet alles an alle Ports

5. Did the wireless Access Point do anything with the information given to it?  
-> Nein, es leitet nur weiter

6. Was any MAC or IP address lost during the wireless transfer?  
-> Nein

7. What was the highest OSI layer that the Hub and Access Point used?  
-> Layer 1 (Physical Layer)

8. Did the Hub or Access Point ever replicate a PDU that was rejected with a red “X”?  
-> Ja

9. When examining the PDU Details tab, which MAC address appeared first, the source or the destination?  
-> Destination MAC

10. Why would the MAC addresses appear in this order?  
-> Weil das Ziel zuerst definiert wird

11. Was there a pattern to the MAC addressing in the simulation?  
-> Ja, sie folgen den Geräten im Netzwerk

12. Did the switches ever replicate a PDU that was rejected with a red “X”?  
-> Nein

13. Every time that the PDU was sent between the 10 network and the 172 network, there was a point where the MAC addresses suddenly changed. Where did that occur?  
-> Beim Router

14. Which device uses MAC addresses that start with 00D0:BA?  
-> Der Router

15. What devices did the other MAC addresses belong to?  
-> PCs und Switches

16. Did the sending and receiving IPv4 addresses change fields in any of the PDUs?  
-> Nein

17. When you follow the reply to a ping, sometimes called a pong, do you see the sending and receiving IPv4 addresses switch?  
-> Ja

18. What is the pattern to the IPv4 addressing used in this simulation?  
-> Zwei verschiedene Netzwerke (172.x und 10.x)

19. Why do different IP networks need to be assigned to different ports of a router?  
-> Damit der Router zwischen Netzwerken routen kann

20. If this simulation was configured with IPv6 instead of IPv4, what would be different?  
-> Andere Adressformate und kein ARP, sondern NDP