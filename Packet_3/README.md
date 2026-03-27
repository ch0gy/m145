# Packet Tracer - Implement Basic Connectivity

## Part 1: Perform a Basic Configuration on S1 and S2

- How can you verify that both passwords were configured correctly?  
  -> Mit `exit` abmelden und prüfen, ob beim erneuten Zugriff das Console-Passwort verlangt wird. Danach mit `enable` prüfen, ob das Passwort für den privileged EXEC mode abgefragt wird.

- Which command do you issue to accomplish this step?  
  -> `copy running-config startup-config`

---

## Part 2: Configure the PCs

- Were you successful? Explain.  
  -> Nein, zuerst noch nicht. Der Ping auf S1 war anfangs nicht erfolgreich, weil auf dem Switch noch keine IP-Adresse auf dem Management Interface konfiguriert war.

---

## Part 3: Configure the Switch Management Interface

- If this is the case, why would we configure it with an IP address?  
  -> Damit der Switch über das Netzwerk verwaltet und getestet werden kann, zum Beispiel mit Ping oder später per SSH.

- Why do you enter the no shutdown command?  
  -> Damit das Interface aktiviert wird. Ohne `no shutdown` bleibt das Interface ausgeschaltet.

- Which command is used to save the configuration file in RAM to NVRAM?  
  -> `copy running-config startup-config`