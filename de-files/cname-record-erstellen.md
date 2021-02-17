---
id: cname-record-erstellen
title: CNAME Record erstellen
sidebar_label: CNAME Record
---
Hier wird dir erklärt wie du einen CNAME Record für deine Domain erstellst.

## Vorbereitung
Bevor wir mit dem A-Record beginnen können gehe bitte sicher, dass du die allgemeine Vorbereitung aus dem Punkt [DNS Verwaltung](dns-allgemein.md) befolgt hast!

### ℹ Wofür CNAME Records?
CNAME Records werden dafür benutzt um einen Alias für einen Domainname bereitzustellen.
Das kann zum Beispiel dazu genutzt werden, dass deinserverhost.de über dsh.domain.de erreichbar ist. 

Im Falle einer Änderung der IP-Adresse muss der CNAME Record nicht geändert werden und funktioniert weiterhin.

### 🚀 Anlegen von CNAME Records
Schritt für Schritt Anleitung:
1. Gehe in die Domainverwaltung in deinem Kundenbereich
2. Klicke in der Sidebar auf "DNS-Verwaltung". Wenn dir dieser Menüpunkt nicht angezeigt, kannst du unsere DNS Verwaltung kostenfrei über den Menüpunt "Erweiterungen" oder auf der Startseite aktivieren.
3. Klicke auf den Button zum Anlegen eines neuen Records
4. In der auswahl dann CNAME Record auswählen.
5. Du wirst nach einem Hostname gefragt. Dort kann entweder eine Subdomain, @ für die Domain selbst, oder ein * für die Domain und alle möglichen Subdomains angegeben werden. 
6. Im nächsten Schritt muss die Zieldomain angegeben werden. Der Inhalt dieser Zieldomain ist später über den CNAME Record erreichbar.
7. Mit Speichern bestätigen.

Der CNAME Record wurde erstellt. 🎉 