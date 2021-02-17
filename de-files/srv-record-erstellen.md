---
id: srv-record-erstellen
title: SRV Record erstellen
sidebar_label: SRV Record
---
Hier wird dir erklärt wie du einen SRV Record für deine Domain erstellst.

## Vorbereitung
Bevor wir mit dem SRV-Record beginnen können gehe bitte sicher, dass du die allgemeine Vorbereitung aus dem Punkt [DNS Verwaltung](dns-allgemein.md) befolgt hast!

### ℹ Wofür SRV Records?
SRV Records werden dafür benutzt um festzulegen welche Dienste über einen Domainnamen angeboten werden. 

Der Record wird häufig genutzt um bei Gameservern auf den Port verzichten zu können und um ein Loadbalancing zu realisieren.

Wenn beispielsweise ein Minecraft Server mit dem Port 25577 über die Domain deinserverhost.de erreichbar sein soll, ohne dass der Port hinter der Domain zum Verbinden angegeben werden muss, muss ein SRV Eintrag verwendet werden.

### ⚔ Anlegen von SRV Records für Minecraft
Schritt für Schritt Anleitung für einen SRV Record für einen Minecraft Server:

> Um einen SRV Record zu benutzen musst du zuerst einen [A Record](a-record-erstellen.md) bzw. einen [AAAA Record](aaaa-record-erstellen.md) erstellen. Der [A Record](a-record-erstellen.md) bzw. der [AAAA Record](aaaa-record-erstellen.md) muss auf die IP des Servers, auf welchem der Dienst läuft, zeigen.

1. Gehe in die Domainverwaltung in deinem Kundenbereich
2. Klicke in der Sidebar auf "DNS-Verwaltung". Wenn dir dieser Menüpunkt nicht angezeigt, kannst du unsere DNS Verwaltung kostenfrei über den Menüpunt "Erweiterungen" oder auf der Startseite aktivieren.
3. Klicke auf den Button zum Anlegen eines neuen Records
4. In der auswahl dann SRV Record auswählen.
5. Du wirst nach einem Dienst gefragt. Im Falle von einem Minecraftserver heißt dieser `minecraft`.
6. Im nächsten Schritt muss ein Typ bzw. ein Protokoll angegeben werden. Im Beispiel von Minecraft ist das `TCP`.            
7. Anschließend muss der Hostname angegeben werden unter dem der SRV Record verfügbar sein soll.
8. Die nächsten beiden Schritte sind, sofern ihr kein Loadbalancing nutzen wollt irrelevant. Dort kannst du eine beliebige Zahl angeben, z. B. 10.
9. Nun wirst du nach dem Port gefragt. Trage hier bitte den Port deines Minecraft Servers ein.
10. Im letzten Schritt musst du die vorhin bereits erstellte Subdomain angeben.
11. Mit Speichern bestätigen.

Der SRV Record wurde erstellt. 🎉 

### 📞 Anlegen von SRV Records für TeamSpeak
Schritt für Schritt Anleitung für einen SRV Record für einen TeamSpeak Server:

> Um einen SRV Record zu benutzen musst du zuerst einen [A Record](a-record-erstellen.md) bzw. einen [AAAA Record](aaaa-record-erstellen.md) erstellen. Der [A Record](a-record-erstellen.md) bzw. der [AAAA Record](aaaa-record-erstellen.md) muss auf die IP des Servers, auf welchem der Dienst läuft, zeigen.

Schritte 1 - 4 sind identisch.

Beim 5. Schritt gibst du anstatt des Dienstes minecraft, den Dienst `ts3` an.

Das Protokoll in Schritt 6 ersetzt du mit `UDP`.

Die Schritte 7-11 sind wieder identisch zum Erstellen eines SRV Records für einen Minecraftserver. Bei Schritt 9 muss dann der TeamSpeak Serverport angegeben werden.

### 🔫 Anlegen von SRV Records für FiveM

> Um einen SRV Record zu benutzen musst du zuerst einen [A Record](a-record-erstellen.md) bzw. einen [AAAA Record](aaaa-record-erstellen.md) erstellen. Der [A Record](a-record-erstellen.md) bzw. der [AAAA Record](aaaa-record-erstellen.md) muss auf die IP des Servers, auf welchem der Dienst läuft, zeigen.

Schritte 1 - 4 sind identisch wie beim Erstellen eines SRV Records für Minecraft.

Beim 5. Schritt gibst du anstatt des Dienstes minecraft, den Dienst `cfx` an.

Das Protokoll in Schritt 6 ersetzt du mit `UDP`.

Die Schritte 7-11 sind wieder identisch zum Erstellen eines SRV Records für einen Minecraftserver. Bei Schritt 9 muss dann der FiveM Serverport angegeben werden.