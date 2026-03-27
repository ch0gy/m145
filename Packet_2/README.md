# Packet Tracer - Configure Initial Switch Settings

## Part 1: Verify the Default Switch Configuration

- Fast Ethernet Interfaces: 24  
- Gigabit Ethernet Interfaces: 2  
- VTY Lines: 0–15  

- Which command will display the current contents of non-volatile random-access memory (NVRAM)?  
  -> show startup-config  

- Why does the switch respond with “startup-config is not present?”  
  -> Es wurde noch keine Konfiguration gespeichert.

---

## Part 2: Basic Switch Configuration

### Why is the login command required?  
-> Damit das gesetzte Passwort auch abgefragt wird. Ohne login wird kein Passwort verlangt.

---

### What is displayed for the enable secret password?  
-> Ein verschlüsselter Hash-Wert

### Why is the enable secret password displayed differently from what we configured?  
-> Weil das Passwort verschlüsselt gespeichert wird und nicht im Klartext sichtbar ist.

---

### If you configure any more passwords on the switch, will they be displayed in the configuration file as plain text or in encrypted form? Explain.  
-> Sie werden verschlüsselt angezeigt, weil der Befehl service password-encryption aktiviert wurde.

---

## Part 3: MOTD Banner

### When will this banner be displayed?  
-> Beim Verbinden bzw. Einloggen auf den Switch.

### Why should every switch have a MOTD banner?  
-> Um unbefugte Benutzer zu warnen und klarzustellen, dass der Zugriff eingeschränkt ist.

---

## Part 4: Save Configuration

### What is the shortest, abbreviated version of the copy running-config startup-config command?  
-> write  

### Which command will display the contents of NVRAM?  
-> show startup-config  

### Are all the changes that were entered recorded in the file?  
-> Ja, alle Änderungen wurden gespeichert.
---

## Part 5: Configure S2

- Hostname: S2  
- Console password: letmein  
- Enable password: c1$c0  
- Enable secret: itsasecret  
- MOTD banner configured  
- Password encryption enabled  
- Configuration saved  