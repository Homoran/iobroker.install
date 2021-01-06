# iobroker.install
Doku preview



# Installation von ioBroker unter Linux
Die Installation von ioBroker unter Linux ist auch für jeden Einsteiger zu schaffen!

Bitte nicht von der Länge dieser Anleitung abschrecken lassen. Hier werden noch mehrere verschiedene Optionen beschrieben.

Im Prinzip besteht **jede** Installation nur aus zwei Schritten
* Installation eines Betriebssystems
* Installation von node.js und ioBroker über `curl -sLf https://iobroker.net/install.sh | bash -`

Die weitere Verfahrensweise ist anschließend überall gleich.

### benötigte Software/Hardware
Für die Installation und die spätere Administrierung des Systems werden noch folgende Komponenten benötigt:
* SD-Card Reader
* Schreibprogramm für SD-Karten (z.B. Balena etcher)
* Terminalprogramm für SSH-Zugriff (z.B. puTTY)

## Betriebssysteme
Als Betriebssystem sollte ein Serverbetriebssystem, basierend auf Debian ohne grafische Oberfläche installiert werden.

Empfohlene Betriebssysteme sind:
* für einem (mini-) PC: https://www.debian.org/distrib/
* für einen Raspberry Pi: https://www.raspberrypi.org/software/operating-systems/
* für andere ARM-basierte Einplatinencomputer: https://www.armbian.com/download/

### Einplatinencomputer (SBC)

#### Vorbereitung
Das gewünschte Betriebssystem wird in der zur Hardware passenden Version heruntergeladen und auf die SD-Karte geschrieben.

Die SD-Karte wird in den Einplatinencomputer gesteckt, der Computer mit dem Netzwerk und mit der Stromversorgung verbunden.

Nach kurzer Zeit ist der SBC im Netzwerk erreichbar. Im Router nach der IP-Adresse sehen, und diese dabei direkt an den SBC binden.

#### Verbindung vom PC zum SBC über Terminalprogramm
* Über das Terminalprogramm zum SBC verbinden, indem die IP des SBC unter Port 22 aufgerufen wird.
* Die Zugangsdaten eingeben

#### Einrichtung und Aktualisierung des Systems
##### User anlegen
Sollte in dem System der Zugang mit *root* stattfinden und noch kein normaler User angelegt sein, muss dieser angelegt werden mit `adduser UserName` wobei UserName durch den gewünschen Usernamen ersetzt werden muss.

Anschließend das Passwort vergeben, wiederholen und bestätigen, dann mit `exit` ausloggen und eine neue Verbindung als User aufbauen.

##### Aktualisierung des Systems
Auch wenn das Betriebssystem neu heruntergeladen wurde sollte es auf Aktualisierung überprüft werden. Dies geschieht mit `sudo apt update && sudo apt upgrade`

Anschließend noch bestätigen.

Nach einiger Zeit ist das System auf dem neuesten Stand.

##### Konfiguration des Systems
Wichtige Einstellungen wie z.B.
* Zeitzone
* Sprache
* Servername
müssen über dem Aufruf `sudo raspi-config` bzw. `sudo armbian-config` eingestellt werden.
Danach nochmals rebooten mit `sudo reboot`

### Debian-PC
* Das Betriebssystem wird auf einen Bootfähigen USB-Stick geschrieben.
* Im BIOS wird
  * der Boot von USB aktiviert 
  * Auf ein "Legacy-Betriebssystem" umgestellt
  
Anschließend vom USB-Stick booten und der geführten Installation folgen.

Auch hier sollte keine grafische Oberfläche installiert werden.

## Installation von node.js und ioBroker

ioBroker wird mit dem Befehl `curl -sLf https://iobroker.net/install.sh | bash - ` installiert

Auf einem neuen System, auf dem sich noch kein node.js befindet wird dieses in der jeweils aktuell empfohlenen Version mit installiert.

---

## Nutzung von ioBroker
Die erfolgreiche Installation endet mit der Information unter welcher IP ioBroker aufgerufen werden soll. Unter dieser <IP>:8081 ist die Bedienoberfläche (der Admin) von ioBroker in jedem Browser aufrufbar.
