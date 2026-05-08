# Fragen und Antworten

## Wie lautet die Netzwerkadresse vom Standort Samedan?

`192.168.3.0/24`

---

## Auf welcher IP-Adresse befindet sich der AccessPoint in Bellinzona?

`192.168.4.30`

---

## In welchem VLAN befinden sich die Arbeitsplatz-PCs?

`VLAN-2: Office`

---

## Über welche IP-Adresse erreicht man den Manageable-Switch am Standort Chur?

`192.168.2.253`

---

## Welche IP-Adressen LAN-seitig und tunnelseitig ist der VPN-Gateway am Standort Bellinzona konfiguriert?

LAN-seitig: `192.168.4.1`

Tunnelseitig: `172.200.4.2/24`

---

## Wie lautet der am Standort Samedan an den Arbeitsplatz-PCs eingetragene Standardgateway?

`192.168.3.1`

---

## Ein Aussendienstmitarbeiter benötigt Zugriff auf das Firmennetzwerk. Wie muss er seine VPN-SW IP-mässig konfigurieren?

Remote-Access läuft über `VPN-C`.

Der VPN-Gateway in Chur hat `172.200.5.1/24`.

Der Client braucht eine freie Adresse im Netz `172.200.5.0/24`, z.B. `172.200.5.2/24`, mit Ziel/Gateway `172.200.5.1`.

---

## Wer hat im Büro CAD Wasserbau die VoIP-Telefone installiert?

`abisang`

---

## Wann wurde im Bistro der AccessPoint installiert?

Am `23.7.14`

---

## Der IT-Mitarbeiter Rene Sauter (rsauter) verlässt die Firma. Welche Arbeiten bzw. Verantwortlichkeiten sind davon betroffen? Wen würden Sie als zukünftigen Ansprechpartner bei Problemen vorschlagen?

Betroffen sind Einträge, die von `rsauter` gemacht wurden:

- Arbeitsplatz-PC Empfang `E1/1`
- CAD Workstation CAD Tiefbau `E2/1`
- MF-Kopierer Bauleiterbüro `E3/2`
- AccessPoint Bistro `E8/1`

Als Ansprechpartner würde ich je nach Problem wählen:

- `blaeuchli` für Arbeitsplatz/Hardware/Netzwerkanschlüsse
- `abisang` für VoIP-Telefone

---

## Wieviele RJ45-Steckdosen stehen Ihnen im Bauleiterbüro zur Verfügung und wieviele davon sind zurzeit noch nicht belegt?

Total `8` RJ45-Anschlüsse:

`E3/1`, `E3/2`, `E4/1`, `E4/2`, `E5/1`, `E5/2`, `E6/1`, `E6/2`

Frei sind `2`:

`E3/1` und `E6/2`

---

## Im Büro CAD Tiefbau muss ein weiteres VoIP-Telefon zur Verfügung stehen. Wie soll diese Verbindung gepatched werden? Verlangt wird die Patchpanelbelegung und der Switch-Port.

Freier Anschluss im CAD Tiefbau: `E2/2`

Patchen:

- Patchpanel: `E2/2`
- Switch-Port: freier Port im `VLAN-1 Telefon`
- Telefon-Portbereich: `24–47`

Da kein exakter freier Switch-Port dokumentiert ist, würde ich z.B. den nächsten freien Telefon-Port verwenden, etwa `Port 33`, falls Ports `24–32` bereits belegt sind.

---

## Im Bistro soll eine Projektpräsentation stattfinden. Dafür muss ein Ethernetkabelverbindung bereitgestellt werden.

Im Bistro ist `E8/1` vom AccessPoint belegt.

Frei sind:

- `E8/2`
- `E9/1`
- `E9/2`

Ich würde z.B. `E8/2` verwenden und auf einen freien Switch-Port im `VLAN-2 Office`, also Portbereich `1–23`, patchen.

---

## Im Büro CAD Wasserbau soll temporär ein weiterer Arbeitsplatz eingereichtet werden. Wie werden sie diese Aufgabe lösen?

Im CAD Wasserbau sind laut Belegung alle Anschlüsse `E10/1–E10/4` und `E11/1–E11/4` belegt.

Für temporär:

- Kleinen Switch an einen bestehenden Arbeitsplatz-Anschluss hängen, z.B. an `E10/4` oder `E11/4`
- Bestehenden PC und temporären Arbeitsplatz am kleinen Switch anschliessen

Sauberer wäre langfristig eine zusätzliche Dose/Leitung.

---

## Wieviele Switchs stehen ihnen am Standort Chur zur Verfügung?

`2` Switches, als Stack:

`2 ZyXEL XGS1910-24`

---

## Frau Sommer arbeitet an der CAD-Workstation und meldet ihnen, dass sie keine Verbindung ins Internet mehr hat. Was werden sie überprüfen?

CAD Workstation ist `E2/1` im CAD Tiefbau.

Prüfen:

- Netzwerkkabel am PC
- Netzwerkdose `E2/1`
- Patchpanel `E2/1`
- Switch-Port im `VLAN-2 Office`
- Link-LED am Switch
- IP-Adresse im Netz `192.168.2.0/24`
- Gateway `192.168.2.1`
- DNS `192.168.2.3`
- Ping auf Switch `192.168.2.253`
- Ping auf Gateway `192.168.2.1`
- Danach externe Verbindung/Router prüfen

---

## Wie lautet die SSID des Churer-AccessPoint?

Nicht genau ersichtlich.

In der Doku steht beim Churer AccessPoint nur:

- Modell: `ZyXEL NWA1123-AC`
- IP: `192.168.2.30`
- VLAN: `VLAN-3`
- Port: `48`

Eine SSID wird in diesem PDF nicht klar angegeben.