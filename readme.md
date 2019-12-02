# Datenschutz- und Verfahrensdokumentation dedica GmbH

dedica GmbH<br>
Ettighofferstr. 15<br>
53127 Bonn<br>

Sofern keine gesetzlichen Normen entgegenstehen, verfolgen wir das Prinzip der Datensparsamkeit und beachten bei der Erhebung, Speicherung, Verarbeitung, Veränderung oder Übermittlung personenbezogener Daten die Zulässigkeitsvoraussetzungen und Interessensabwägungen des § 28 BDSG und Art. 6 DSGVO.<br>

Bei der Planung und Konzeption informationstechnischer Sicherungseinrichtungen orientieren wir uns an den Empfehlungen des BSI. Das vorliegende Dokument beschreibt den aktuellen Zustand der implementierten technischen und organisatorischen Maßnahmen sowie interne Verhaltensrichtlinien und Mitarbeiteranweisungen.


## 1. Verantwortliche Ansprechpartner:
Dr. Daniel Pozzi daniel@dedica.team Tel 0177 274 54 89<br>
Matthias Molitor matthias@dedica.team

<small>Ein Datenschutzbeauftragter wird nach Artikel 37 GSDVO / 38 des BDSG nicht gestellt.</small>


## 2. Zwecke der Verarbeitung

### 2.1 Abwicklung von Beschäftigungsverhältnisen, Lohnbzw. Gehaltsabrechnungen

#### Betroffene Personen: 

Beschäftigte

#### Kategorien personenbezogener Daten

* Name und Adressen der Beschäftigten
* Bankverbindung der Beschäftigten
* Religionszugehörigkeit
* Kennzahlen zur Steuer- und Sozialversicherungs-Identifikation

#### Empfänger personenbezogener Daten

* Buchhaltung: Steuerberater Christian Klein, Zur Verlach 25b, 40723 Hilden
* Finanzamt
* Rentenversicherung
* ggf. Krankenkassen der Beschäftigten

#### Drittlandstransfer

Oben genannte Daten werden in unserem Auftrag ihn "Google Drive" des Anbieters Google LLC, 1600 Amphitheatre Parkway, Mountain View, CA 94043, USA gespeichert. Siehe https://policies.google.com/privacy


#### Löschfristen

DieLöschung erfolgt nach Ablauf der gesetzlichen Aufbewahrungsfristen.


## Technische und organisatorische Maßnahmen


### Zugangs- und Zutrittskontrolle

Wir unterhalten keine öffentlich zugänglichen Räume oder Ladenflächen. Der Zutritt von betriebsfremden Personen (z.B. Gäste) ist nur in Begleitung eines autorisierten Mitarbeiters möglich. Der Aufenthalt externer Dienstleister in unseren Räumlichkeiten ist nicht vorgesehen.

<br>
Wir betreiben keine eigenen Server-, Speicher- und Netzwerksysteme. Physikalischer Zugriff auf unsere Daten ist nur über die Arbeitsrechner der Mitarbeiter (s.u.) möglich.


### Datenträgerkontrolle

Für Datenträger gelten die im Abschnitt Zugriffskontrolle aufgeführten Anforderungen an Verschlüsselung.<br>
Wie im Abschnitt Verfügbarkeitskontrolle beschrieben, dürfen mobile Datenträger nicht mit Endgeräten verbunden werden.
Entsprechend sind keine leicht zu entfernenden Datenträger vorhanden, die gelesen, kopiert, entfernt oder verändert werden könnten.

### Speicherkontrolle

Die Kenntnisnahme personenbezogener Daten wird über die im Abschnitt Zugriffskontrolle beschriebenen Mechanismen gesteuert und unbefugte Kenntnisnahme verhindert.
Mitarbeiter sind auf den Umgang mit personenbezogenen Daten sensibilisiert und angewiesen, Unterstützungsleistungen gegenüber Dritten abzulehnen oder abzubrechen, wenn es hierdurch zu einer Übermittlung,
 unbefugten Kenntnisnahme oder sonstigen Verarbeitung personenbezogener Daten kommen sollte. Verantwortliche Dritte sind in diesem Zusammenhang aufgefordert, die Rechtmäßigkeit einer 
Verarbeitung glaubhaft zu machen, bevor Unterstützungsleistungen erbracht werden, bei denen personenbezogene Daten verarbeitet oder zur Kenntnis genommen werden.

### Benutzerkontrolle

Die Benutzerkontrolle wird über die im Abschnitt Zugriffskontrolle beschriebenen Mechanismen durchgesetzt, unabhängig davon, ob es sich um einen Zugriff per Datenfernübertragung oder standortlokal handelt.

### Zugriffskontrolle

Für die Zugriffssteuerung setzen wir ein differenziertes Berechtigungskonzept ein, das auf der Mitgliedschaft einzelner Mitarbeiter in verschiedenen Berechtigungsgruppen beruht. Die Standardrechte unterliegen hierbei maximalen Einschränkungen und werden nur bei Bedarf erweitert. Die Entscheidung über Vergabe und Entzug von Rechten obliegt der Geschäftsführung. Sofern Mitarbeiter das Unternehmen verlassen, werden unverzüglich alle Rechte entzogen – der zugehörige Active Directory Benutzer wird gesperrt.<br>


Für jeden Kunden – und bei Bedarf auch für einzelne Projekte – wird eine eigene Active Directory Sicherheitsgruppe erstellt. Der Zugriff auf die Daten eines Kunden wird auf Mitarbeiter eingeschränkt, 
die Mitglied in dieser Sicherheitsgruppe sind.<br


Für die  Benutzer-Authentifizierung werden individuelle Benutzerpasswörter mit mindestens 8 Zeichen verwendet, die Groß-/Kleinbuchstaben und Zahlen enthalten müssen. Die Verwendung von Sonderzeichen ist optional. 
Mitarbeiter sind aufgefordert, ihre individuellen Benutzerpasswörter nicht mehrfach zu verwenden. 

* Client-Systeme sollen bei der Inbetriebnahme neu installiert werden. Hierfür soll ein Ubuntu/Debian Image verwendet werden. Ziel ist ein sauberes System ohne Backdoors.

* Client-Systeme müssen mit einer Laufwerksverschlüsselung gesichert sein.

* Client-Systeme müssen bei Verlassen des Arbeitsplatzes gesperrt werden. Eine automatische Sperrung muß zudem nach längerer Inaktivität erfolgen.

* Zugangsdaten für Fremdsysteme (Kundensysteme, Online-Portale, Lieferantenshops, etc.) werden in einem zentralen multi-plattform und multi-user Passwortserver des Herstellers 1password
(zertifiziert nach SOC-2) gespeichert. Verbindungen zum Passwortserver sind SSL-verschlüsselt. Je nach Benutzerrecht, dürfen einzelne Zugangsdaten verwendet (ohne Preisgabe), gelesen, verändert oder neu angelegt werden.

Die Erstellung von Zugangsdaten für Fremdsysteme unterliegt den folgenden Richtlinien:

* Passwörter müssen zufallsgeneriert werden. Für die Erstellung soll der Passwort Generator des Passwortservers verwendet werden. Für die Verwaltung und Speicherung muß der Passwortserver verwendet werden. Passwörter sollen, wenn möglich, mit einem Verfallsdatum versehen werden.
* Passwörter dürfen nicht mehrfach für verschiedene Dienste verwendet werden.
* Falls der jeweilige Dienst dies unterstützt, sollen Passwörter mit mindestens 20 Zeichen, bestehend aus Groß-/Kleinbuchstaben, Zahlen und Sonderzeichen generiert werden.
* Zugriffsrechte müssen unmittelbar bei der Erstellung explizit gesetzt werden.

Die Basis der Firewall-Regelwerke sieht zunächst ein vollständiges Blockieren der gesamten Netzwerkkommunikation vor. Notwendige Kommunikation wird explizit freigegeben.
 Hierbei muß auf eine möglichst genaue Spezifikation der Kommunikationseigenschaften geachtet werden. Gewährende Firewall-Regeln sollen auf die zu erwartenden Nutzungszeiten eingeschränkt werden.<br>

Serverdienste wie zum Beispiel Webservices oder Datenbanken müssen – je nachdem ob eine Nutzung von intern, extern oder intern/extern erfolgen soll – auf unterschiedlichen Container-Hosts (Docker) ausgeführt werden. Container-Hosts sind eigenständige virtuelle Maschinen, auf denen ein minimales Linux-System zur Container-Virtualisierung ausgeführt wird. Diese Trennung ermöglicht die Durchsetzung von Zugriffsbeschränkungen auf Netzwerkebene und verhindert Zugriffe auf interne Systeme durch Rechteeskalation eines öffentlich zugänglichen Systems.

* Kundennetze, mobile Mitarbeiter und Home Offices werden per VPN angebunden. Für die Transportsicherung kommen IPsec oder TLS (SSL-VPN) zum Einsatz. 
* VPN-Verbindungen mobiler Mitarbeiter und Home Offices müssen Perfect Forward Secrecy (PFS) sowie gegenseitige X.509-zertifikatsbasierte Authentifizierung verwenden. Für die Anbindung von Kundennetzen soll PFS sowie zertifikatsbasierte Authentifizierung, vor dem Einsatz von Preshared-Keys, verwendet werden. Beim Einsatz von Preshared-Keys gelten die Richtlinien für die Erstellung von Zugangsdaten für Fremdsysteme sinngemäß für die Erstellung des Preshared-Key. Konkrete Verschlüsselungsalgorithmen und Hashfunktionen werden unter Abwägung eines zu erreichenden Sicherheitslevels und des benötigten Rechenaufwands ausgewählt.

* Kundennetze werden als nicht-vertrauenswürdige Netze betrachtet und entsprechend behandelt.

### Weitergabekontrolle, Transportkontrolle und Übertragungskontrolle

Systeme, die zur Übertragung personenbezogener oder vertraulicher Daten eingesetzt werden, müssen mindestens eine Transportverschlüsselung einsetzen. 
Die damit zwingend einhergehenden Fehlererkennungs- und -korrekturverfahren sichern die Integrität der zu übermittelnden Daten. Mitarbeiter sollen Übertragungsweisen bevorzugen, 
die eine Ende-zu-Ende-Verschlüsselung unterstützen.

Protokolle ohne Transportsicherung dürfen nicht verwendet werden, wenn ein alternatives Protokoll mit Transportsicherung verfügbar ist (z.B für FTP, HTTP).

Für die Sicherung der Emailübertragung (IMAP und SMTP) setzen wir TLS ein.

Für die Übermittlung besonders sensibler oder vertraulicher Daten soll eine persönliche oder telefonische Kontaktaufnahme zur Verifikation der Empfängeridentität u stattfinden.

Im Falle von aufbewahrungspflichtigen Emails, erfolgt eine revisionssichere Speicherung (Archivierung) der Emails für eine Dauer von 6 respektive 10 Jahren (zur Erfüllung gesetzlicher Anforderungen der GoBD aus HGB und AO). Diese Speicherung/Archivierung wird über Google Retention-Policies umgesetzt.

Die Verwendung mobiler Datenträger (USB-Sticks, CDs/DVDs, mobile Festplatte, etc.) zum Transport personenbezogener Daten ist Mitarbeitern nicht gestattet. Die Annahme fremder mobiler Datenträger und deren Verwendung an unseren Datenverarbeitungssystemen ist Mitarbeitern ebenfalls untersagt.

Mitarbeiter sind im Rahmen ihres Arbeitsvertrags zur Geheimhaltung und auf das Datengeheimnis nach § 5 BDSG verpflichtet. Diese Verpflichtung überdauert das Arbeitsverhältnis und besteht auch nach dessen Beendigung fort.

### Eingabekontrolle

Die von uns eingesetzten Systeme zur Erhebung, Verarbeitung, Speicherung und Nutzung von Daten bestehen aus Google GSuite. Sie protokollieren vollumfänglich jede Änderung an Daten sowie administrative Tätigkeiten inklusive des durchführenden Benutzers.<br>


### Auftragskontrolle

Für den Betrieb unserer Datenspeicher und Maildienste für personenbezogene Date setzen wir folgende Dienstleister ein:

* Google GSuite

Für den Betrieb unserer sonstige Datenspeicher für ausschließlich **nicht personenbezogene Daten** nutzen wir außerden:

* GitHub
* Amazon AWS


Zum Zwecke der Buchführung und Erstellung von Jahresabschlüssen und deren Prüfung, ist nicht auszuschließen, dass personenbezogene Daten auf Belegen (Lieferscheine, Rechnungen, etc.) 
oder aus Fahrtenbüchern (Ansprechpartner eines Termins) an die Steuerberatungskanzlei CK Steuerberatung (Hilden) und die DATEV eG (Nürnberg) übermittelt werden. 
Die Datenschutzvereinbarung und das Verfahrensverzeichnis der DATEV eG befindet sich abrufbar unter: https://www.datev.de/web/de/m/ueber-datev/datenschutz/.
Mitarbeiter der CK Steuerberatung sind als Berufsgeheimnisträger zu besonderer Sorgfalt und Geheimhaltung verpflichtet.


### Verfügbarkeitskontrolle, Wiederherstellbarkeit, Zuverlässigkeit und Datenintegrität

Wiederherstellbarkeit, Zuverlässigkeit und Datenintegrität sind durch Google als Diensteanbieter gewährleistet. Zudem sind besonders wichtige Dokumente und auf Papier eingegangene Dokumente in unserem Büro in einem abschließbaren Schrank archiviert. 

### Umsetzung des Trennungsgebots

Zur Zeit werden personenbezogene Daten nicht zu unterschiedlichen Zwecken verarbeitet, insofern greift das Trennungsgebot nicht.<br>

Mitarbeiter sind in Rechtegruppen unterteilt (z.B. Buchhaltung, Service/Support, Geschäftsführung, etc.), die mit unterschiedlichen Zugriffsrechten unterschiedlichem Funktionsumfang innerhalb einzelner Dienste einhergehen.

