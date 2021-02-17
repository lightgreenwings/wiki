---
id: nomachine-grafische-oberfläche-installieren
title: NoMachine Server installieren
sidebar_label: NoMachine (Grafische Oberfläche)
---
Hier wird beschrieben, wie du auf deinem Linux Server NoMachine als Headless Desktopumgebung installierst.

## Informationen
NoMachine ist eine Software, die es ermöglicht einen Linux Remotedesktop in hoher Qualität und einfach zu erreichen.

### 🐧 Installation Server

Melde dich zuerst per SSH als root Benutzer auf deinem Server an.

1. Aktualisieren des Systems

   ```sh
   $ apt update && apt upgrade -y
   ```
   
2. Benötigte Software installieren und vorbereiten

   ```sh
   $ apt install x-window-system gdm3 cups -y
   ```
   
3. Gnome als Desktopoberfläche installieren
    
   ```sh
   $ apt install gnome -y
   ```

4. NoMachine herunterladen und installieren
   
   ```sh
   $ wget https://download.nomachine.com/download/7.0/Linux/nomachine_7.0.211_4_amd64.deb
   $ dpkg -i nomachine_7.0.211_4_amd64.deb
   ``` 
     
   > Die neueste Version lässt sich immer [auf der Downloadseite von nomachine.com](https://www.nomachine.com/de/download/download&id=1) herausfinden.

Der NoMachine Server wurde nun installiert ✔

### 💻 Installation Client

Lade dir [auf nomachine.com](https://www.nomachine.com/de) den NoMachine Client herunter und installiere ihn.


Öffne den Client und klicke oben auf `Neu`

![img](/img/nomachine/1.png)

### ⚙ Konfiguration der Verbindung  

1. Belasse das Protokoll bei `NX`
2. Setze den Host als `IP deines Servers`, der Port bleibt bei 4000
3. Wähle als Authentifizierungsmethode `Passwort` aus, damit du dich einfach mit dem root Benutzer anmelden kannst 
4. Die Proxieinstellung ebenfalls bei `Keinen Proxy verwenden` lassen
5. Gib der Verbindung einen Namen

Die Verbindung wurde konfiguriert ✔

### 〰 Verbindung herstellen

Doppelklicke auf die neu erstellte Verbindung im Startbildschirm von NoMachine.

Du wirst nach der Authentizität deines Servers gefragt. Klicke hier auf `Ja`

![img](/img/nomachine/2.png)

Du wirst nach deinem Login gefragt. Trage deine Verbindungsdetails einfach in die Felder ein.

![img](/img/nomachine/3.png)

Auf dem Server wird keine Anzeige erkannt. Klicke hier ebenfalls wieder auf `Ja`, damit eine neue Anzeige erstellt wird.

![img](/img/nomachine/4.png)

Sobald die Verbindung erfolgreich hergestellt wurde, werden dir noch einige Tipps und Hinweise angezeigt.

Die Installation ist nun abgeschlossen ✔