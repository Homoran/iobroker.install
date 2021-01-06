# iobroker.install
Doku preview



# Installation von ioBroker unter Linux
Die Installation von ioBroker unter Linux ist auch für jeden Einsteiger zu schaffen!

Bitte nicht von der Länge dieser Anleitung abschrecken lassen. Hier werden noch mehrere verschiedene Optionen beschrieben.

Im Prinzip besteht **jede** Installation aus zwei Schritten
* Installation eines Betriebssystems
* Installation von node.js und ioBroker über ```curl -sLf https://iobroker.net/install.sh | bash -```

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

Das gewünschte Betriebssystem wird in der zur Hardware passenden Version heruntergeladen und auf die SD-Karte / einen USB-Stick geschrieben.

Die SD-Karte wird in den Einplatinencomputer gesteckt, der Computer mit dem Netzwerk und mit der Stromversorgung verbunden.
