---
id: teamspeak-server-installieren
title: Teamspeak Server installieren
sidebar_label: Teamspeak Server
---
Hier wird beschrieben, wie du auf deinem Windows oder Linux Server einen TeamSpeak Server installierst.

## Informationen
TeamSpeak ist eine Kommunikationssoftware, welche ermöglicht über das Internet per Sprache und Text zu kommunzieren und Dateien auszutauschen.


### 🐧 Linux Installation (Debian/Ubuntu)
1. Aktualisiere dein System und installiere einige Grundkomponenten

    ```sh
    $ apt update &&  apt upgrade -y
    $ apt install sudo bzip2
    ```
2. Lege einen Subuser für den Server an und melde dich an

    ```sh
    $ sudo adduser teamspeak --disabled-login
    $ sudo su teamspeak -l
    ```
3. Kopiere den Link für die neuste 64 Bit Linux Serverversion [auf der TeamSpeak Downloads Seite](https://www.teamspeak.com/en/downloads/#server)
4. Datei herunterladen entpacken und ins Verzeichnis navigieren, beispielsweise mit v3.13.3
    ```sh
   $ wget https://files.teamspeak-services.com/releases/server/3.13.3/teamspeak3-server_linux_amd64-3.13.3.tar.bz2
   $ tar xvfj teamspeak3-server_linux_amd64-3.13.3.tar.bz2
   $ cd teamspeak3-server_linux_amd64-3.13.3.tar.bz2
    ```
5. Über den Befehl `ls -l` siehst du nun die TeamSpeak Serverdateien. Jetzt noch Startfähig machen
   ```sh
   $ sudo chmod +x ts3server_startscript.sh
   $ ./ts3server_startscript.sh start
   ```


### 🐧 Windows Server Installation
Zuerst musst du alle nötigen Ports freigeben
1. Öffne das Programm `Windows-Firewall mit erweiterter Sicherheit` über die Windows Suche und erstelle folgende Regeln um die Ports zu erlauben:
    - 9987 - (UDP eingehend)
    - 2010 - (UDP ausgehend)
    - 30033, 10011, 41144 - (TCP eingehend)
    - 2008 - (TCP ausgehend)
     
   >[?] Wie erstellt man eine Regel?
   > Klicke in der linken Auswahl auf Eingehende bzw. Ausgehende Regeln und danach in der rechten Auswahl auf `Regel erstellen`. Als Regeltyp Port auswählen, TCP bzw. UDP auswählen und die bestimmten Ports angeben.
   >Danach auf Verbindung zulassen. Lasse im nächsten Schritt alle Profile aktiv und gib im letzten Schritt einen Namen für deine Regel an.

2. Lade dir das 64bit Server Zip Archiv [auf der TeamSpeak Downloads Seite](https://www.teamspeak.com/en/downloads/#server) herunter und entpacke sie auf dem Desktop deines Servers.

3. Entpache das Archiv und starte den Server über die ts3server.exe. 

4. Du wirst aufgefordert die Lizenz des Servers zu akzeptieren und erhälst danach deine Administratorzugänge. **Speichere dir diese ab.**


Der Server startet nun. 🎉

Bitte notiere dir den Server Query Admin Login und den Server Admin privilege key, damit du Administratorzugriff auf deinen Server hast.

### 🌎 Server mit Domain verbinden

Wie du deinen Server mit deiner Domain verbindest, erfährst du im Eintrag [SRV Record erstellen](srv-record-erstellen#-anlegen-von-srv-records-für-teamspeak).