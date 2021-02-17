---
id: mariadb-installieren
title: MariaDB installieren
sidebar_label: MariaDB Server
---
Hier erfährst du, wie du auf deinem Linux Server MariaDB bzw. MySQL installieren kannst.

> Dieser Eintrag richtet sich dabei an Debian und Ubuntu Server.

## Information
Der Datenbankserver MariaDB ist eine Abspaltung von MySQL und löst dises immer stärker ab. 

### 🖥 Installation
Verbinde dich per SSH zu deinem Server. Dafür kannst du Programme wie zum Beispiel PuTTY oder MobaXterm benutzen.

1. Aktualisiere dein System und installiere den Datenbankserver
    
    ```sh
    $ apt update &&  apt upgrade -y
    $ apt install mariadb-server -y
    ```
2. Starte das Setup des MariaDB Servers. In diesem Beispiel wird das root-Passwort des MariaDB Servers gesetzt, der Login als anonymer Benutzer und als root Benutzer, aus dem öffentlichen Netzwerk, gesperrt. Die Datenbank, die MariaDB nach der Installation automatisch anlegt löschen wir ebenfalls.

    ```sh
    $ mysql_secure_installation
    ```

3. Beginn des Setups

    Du bekommst eine Ausgabe, wie im Screenshot gezeigt. Hier musst du zuerst Enter drücken.

    ![img](/img/mariadb/1.png)

4. Root Passwort ändern

    Jetzt wirst du gefragt, ob du das root-Passwort ändern willst. Bestätige das mit `Y`.

    ![img](/img/mariadb/2.png)
 
5. Neues Root Passwort setzen

    Anschließend wirst du nach dem neuen root-Passwort gefragt. Wähle ein sicheres Passwort und gib es zur Bestätigung ein zweites Mal ein.
    >Das Passwort wird bei der Eingabe nicht angezeigt.

    ![img](/img/mariadb/3.png)
 
6. Anonymen Login sperren
 
    Jetzt kannst du den Login als anonymen Benutzer sperren. Das verhindert, dass sich Personen ohne Benutzername und Passwort auf deinem MariaDB Server anmelden können. Bestätige die Abfrage mit `Y`.
     
    ![img](/img/mariadb/4.png)

7. Öffentlichen root Zugriff deaktivieren

    Danach wirst du gefragt, ob du den Login als root Benutzer vom öffentlichen Netzwerk sperren willst. Bestätigt das ebenfalls wieder mit `Y`.
    
    ![img](/img/mariadb/5.png)

8.  Entfernen der Testdatenbank

    Nun wird noch die Testdatenbank, die bei der Installation vom MariaDB automatisch erstellt wird, gelöscht. Hier du ebenfalls mit `Y` bestätigen.
    
    ![img](/img/mariadb/6.png)
 
9. Benutzerrechte neu laden
 
    Abschließend werden die Tabellen, in denen die Berechtigungen abgelegt werden, neu geladen. Das stellt sicher, dass alle Änderungen übernommen werden.
     
    ![img](/img/mariadb/7.png) 
 
Der MariaDB Server ist nun fertig konfiguriert und abgesichert 🎉

### 🚀 Erstellen einer Datenbank mit Administrator Benutzer
1. Am Datenbankserver anmelden
   ```sh
   $ mysql -u root -p
   ```
   Hier müsst ihr zuerst euer vorher gesetztes Passwort eingeben. 
  
2. Datenbank und administrativen Benutzer erstellen

    Ersetzt dabei den Datenbanknamen mit einem von euch gewähltem, ebenso den Benutzernamen und das Passwort. Bestätigt diese Befehle nach dem Semikolon mit Enter.
    ```sh
   CREATE DATABASE datenbank;
   CREATE USER 'benutzername'@'localhost' IDENTIFIED BY 'Passwort1234!';
   GRANT ALL PRIVILEGES ON datenbank.* TO 'benutzername'@'localhost';
   FLUSH PRIVILEGES;
    ```
    Nun hast du eine Datenbank und einen Benutzer erstellt. Der Benutzer hat hierber Vollzugriff auf die Datenbank 🎉

3. Abmelden
    ```ssh
    quit
   ```
   
#### 🚨 Einen weiteren Benutzer mit vollem Zugriff erstellen

So kannst du einen Administrativen Benutzer **für alle Datenbanken** erstellen:
1. Nur mit lokalem Zugriff
    ```sh
    CREATE USER 'admin'@'localhost' IDENTIFIED BY 'Passwort1234!';
    GRANT ALL PRIVILEGES ON *.* TO 'admin'@'localhost';
   FLUSH PRIVILEGES;
    ```
2. Mit Remotezugriff
    ```sh
    CREATE USER 'admin'@'%' IDENTIFIED BY 'Passwort1234!';
    GRANT ALL PRIVILEGES ON *.* TO 'admin'@'%';
   FLUSH PRIVILEGES;
    ```
   
### 🔥 Verbinden   
Du kannst deine Anwendungen auf dem Server mit der Datenbank verbinden, indem du die Adresse „localhost:3306“, den von euch gewähltem Benutzernamen und das Passwort angibst.

> [!] Wenn du auf deine Datenbank von extern Zugreifen willst, musst du die Datenbank und den Nutzer wie folgt erstellen: 
>```sh
>CREATE DATABASE datenbank;
>CREATE USER 'benutzername'@'%' IDENTIFIED BY 'Passwort1234!';
>GRANT ALL PRIVILEGES ON datenbank.* TO 'benutzername'@'%';
>FLUSH PRIVILEGES;
> ```
