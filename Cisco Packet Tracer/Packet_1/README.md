# Packet Tracer - Navigate the IOS

### Objectives

Part 1: Establish Basic Connections, Access the CLI, and Explore Help
Part 2: Explore EXEC Modes
Part 3: Ser the Clock

## Part 1 – Verbindungen herstellen, CLI öffnen und Help nutzen

**Frage:** What is the setting for bits per second?  
**Antwort:** 9600  

**Frage:** What is the prompt displayed on the screen?  
**Antwort:** S1>  

**Frage:** Which command begins with the letter ‘C’?  
**Antwort:** connect  

**Frage:** Which commands are displayed? (S1> t?)  
**Antwort:** telnet, terminal, traceroute  

**Frage:** Which commands are displayed? (S1> te?)  
**Antwort:** telnet, terminal  

---

## Part 2 – EXEC Modes erkunden

**Frage:** What information is displayed for the enable command?  
**Antwort:** Aktiviert den privilegierten Modus (Turn on privileged commands)  

**Frage:** What displays after pressing the Tab key?  
**Antwort:** enable  

**Frage:** What would happen if you typed te<Tab> at the prompt?  
**Antwort:** Nichts, da der Befehl nicht eindeutig ist  

**Frage:** How does the prompt change?  
**Antwort:** S1#  

**Frage:** How many commands are displayed now that privileged EXEC mode is active?  
**Antwort:** Mehr Befehle als im User EXEC Mode  

**Frage:** What is the message that is displayed?  
**Antwort:** Enter configuration commands, one per line. End with CNTL/Z.  

**Frage:** How does the prompt change?  
**Antwort:** S1(config)#  

---

## Part 3 – Uhr einstellen

**Frage:** What information is displayed? What is the year that is displayed?  
**Antwort:** Aktuelle Uhrzeit und Datum werden angezeigt Sat Mar 13 1993  

**Frage:** What information is displayed? (S1# clock<ENTER>)  
**Antwort:** % Incomplete command  

**Frage:** What information is displayed? (S1# clock ?)  
**Antwort:** set  

**Frage:** What information is being requested?  
**Antwort:** Uhrzeit, Tag, Monat und Jahr  

**Frage:** What would have been displayed if only the clock set command had been entered?  
**Antwort:** % Incomplete command  

**Frage:** What information was returned? (S1# cl<Tab>)  
**Antwort:** clock  

**Frage:** What information was returned? (S1# clock)  
**Antwort:** % Incomplete command  

**Frage:** What information was returned? (S1# clock set 25:00:00)  
**Antwort:** % Invalid input  

**Frage:** What information was returned? (S1# clock set 15:00:00 32)  
**Antwort:** % Invalid input  