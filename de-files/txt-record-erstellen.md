---
id: txt-record-erstellen
title: TXT Record erstellen
sidebar_label: TXT Record
---
Hier wird dir erklärt wie du einen TXT Record für deine Domain erstellst.

## Vorbereitung
Bevor wir mit dem A-Record beginnen können gehe bitte sicher, dass du die allgemeine Vorbereitung aus dem Punkt [DNS Verwaltung](dns-allgemein.md) befolgt hast!

### ℹ Wofür TXT Records?
Über TXT Records können verschiedene Informationen in Form von Text bereitgestellt werden.
Das können zum einen Informationen zur Verifizierung des Besitzers der Domain sein, aber auch SPF, DKIM und DMARC Informationen zum Mailversand.

Eine Verifizierung des Domainbesitzers ist beispielsweise notwendig um ein SSL Zertifikat von Let's Encrypt anzufordern.


### 🚀 Anlegen von TXT Records
Schritt für Schritt Anleitung:
1. Gehe in die Domainverwaltung in deinem Kundenbereich
2. Klicke in der Sidebar auf "DNS-Verwaltung". Wenn dir dieser Menüpunkt nicht angezeigt, kannst du unsere DNS Verwaltung kostenfrei über den Menüpunt "Erweiterungen" oder auf der Startseite aktivieren.
3. Klicke auf den Button zum Anlegen eines neuen Records
4. In der auswahl dann TXT Record auswählen.
5. Du wirst nach einem Hostname gefragt. Dort kann entweder eine Subdomain, @ für die Domain selbst, oder ein * für die Domain und alle möglichen Subdomains angegeben werden. 
6. Im nächsten Schritt muss der gewünschte Text angegeben werden. Falls du einen TXT Record für ein Let’s Encrypt Zertifikat anlegen willst, wird dieser Text vom Server vorgegeben.
7. Mit Speichern bestätigen.

Der TXT Record wurde erstellt. 🎉 