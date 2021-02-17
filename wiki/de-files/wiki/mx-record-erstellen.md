---
id: mx-record-erstellen
title: MX Record erstellen
sidebar_label: MX Record
---
Hier wird dir erklärt wie du einen MX Record für deine Domain erstellst.

## Vorbereitung
Bevor wir mit dem MX-Record beginnen können gehe bitte sicher, dass du die allgemeine Vorbereitung aus dem Punkt [DNS Verwaltung](dns-allgemein.md) befolgt hast!

### ℹ Wofür MX Records?
MX Records werden ausschließlich für E-Mail Dienste genutzt.

Wenn zum Beispiel eine E-Mail an kontakt@deinserverhost.de gesendet wird überprüft der Mailserver des Senders, ob auf der Domain deinserverhost.de ein MX Record existiert.

Falls ja, gibt dieser MX Record den FQDN (Fully Qualified Domain Name) des empfangenden Mailservers an. Über diesen FQDN kann anhand der dafür angelegten A/AAAA Records die IP-Adresse des Mailservers ermittelt werden und somit die E-Mail zugestellt werden.
### 🚀 Anlegen von MX Records
Schritt für Schritt Anleitung:
1. Gehe in die Domainverwaltung in deinem Kundenbereich
2. Klicke in der Sidebar auf "DNS-Verwaltung". Wenn dir dieser Menüpunkt nicht angezeigt, kannst du unsere DNS Verwaltung kostenfrei über den Menüpunt "Erweiterungen" oder auf der Startseite aktivieren.
3. Klicke auf den Button zum Anlegen eines neuen Records
4. In der auswahl dann MX Record auswählen.
5. Du wirst nach einem Hostname gefragt. Dort kann entweder eine Subdomain, @ für die Domain selbst, oder ein * für die Domain und alle möglichen Subdomains angegeben werden. Bei MX Records ist hier meistens @ gewollt.
6. Im nächsten Schritt muss der FQDN (Fully Qualified Domain Name) des Mailservers angeben werden. Der FQDN ist der Domainname unter dem der Mailserver erreichbar ist und ist meistens eine Subdomain (mail.domain.de).            
7. MX Records benötigen eine Priorität. Bei nur einem MX Rexord kann diese eine beliebige Zahl sein.
7. Mit Speichern bestätigen.

Der MX Record wurde erstellt. 🎉 