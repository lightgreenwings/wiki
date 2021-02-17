---
id: aaaa-record-erstellen
title: AAAA Record erstellen
sidebar_label: AAAA Record
---
Hier wird dir erklärt wie du einen AAAA Record für deine Domain erstellst.

## Vorbereitung
Bevor wir mit dem A-Record beginnen können gehe bitte sicher, dass du die allgemeine Vorbereitung aus dem Punkt [DNS Verwaltung](dns-allgemein.md) befolgt hast!

### ℹ Wofür AAAA Records?
A Records werden dafür benutzt um Domainnamen, wie zum Beispiel deinserverhost.de, zu IPv6-Adressen aufzulösen.
Dies ist notwendig, wenn z. B. eine Webseite über eine Domain bereitgestellt werden soll.

### 🚀 Anlegen von AAAA Records
Schritt für Schritt Anleitung:
1. Gehe in die Domainverwaltung in deinem Kundenbereich
2. Klicke in der Sidebar auf "DNS-Verwaltung". Wenn dir dieser Menüpunkt nicht angezeigt, kannst du unsere DNS Verwaltung kostenfrei über den Menüpunt "Erweiterungen" oder auf der Startseite aktivieren.
3. Klicke auf den Button zum Anlegen eines neuen Records
4. In der auswahl dann AAAA Record auswählen.
5. Du wirst nach einem Hostname gefragt. Dort kann entweder eine Subdomain, @ für die Domain selbst, oder ein * für die Domain und alle möglichen Subdomains angegeben werden. 
6. Im nächsten Schritt muss eine IPv6-Adresse angegeben werden. Dies ist im Normalfall die IP-Adresse eures Servers oder Webspaces, z. B. 2a01:367:c204::31f:cf.
7. Mit Speichern bestätigen.

Der AAAA Record wurde erstellt. 🎉 