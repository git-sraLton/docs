# Infsec

## Sicherheitsvokabular

### Schutzziele

#### Allgemein Akzeptierte Schutzziele (CIA Triade)

**Vertraulichkeit (Confidentiality)**  
*Daten nur für befugte Personen zugänglich*

**Integrität (Integrity)**  
*Daten/Programme/Funktionen werden in ihrem Soll-Zustand belassen*

**Verfügbarkeit (Availability)**  
*Steht dem Funktionsbezüger immer zur Verfügbarkeit*

#### Umstrittene Schutzziele

**Authenzität (authenticity)**  
*Echtheit / Überprüfbarkeit / Vertrauenswürdigkeit*

**Nicht-Abstreitbarkeit (non-repudiation)**
*Es kann nachgewiesen werden, dass eine Handlung tatsächlich Stattgefunden hat.*

### Grundlegendes

**Asset (Aktivposten)**  
*Etwas mit dem wir einen Wert verbinden (häufig Subjektiv)*

**Bedrohung (threat)**  
*Die Gefahr, dass ein Asset in seinen Schutzzielen beinträchtigt wird*

**Schwäche (vulnerability)**  
*Ein Zustand, durch die ein Asset gefährdet sein könnte*

### Risiko-Grundlagen

#### Schadensausmass

Der Wert der die Höhe des Schadensausmass bemisst.

#### Eintrittswarscheinlichkeit

Ein Faktor, welcher die Häufigkeit eines Ereignisses bestimmt. Diese Häufigkeit wird dann auf einen Bestimmten Zeitraum angegeben. (z.B. ein Jahr und 10 mal im Ø pro Jahr) dann ist die Eintrittswahrscheinlichkeit 10

#### Risiko

Das Produkt von Schadensausmass und Eintrittswahrscheinlichkeit. Dies ergibt einen Zahlenwert der den Ø-Geldbetrag über einen Zeitraum verkörpert.

**Bsp:**  
Schadensausmass 1000 CHF * Eintrittswahrscheinlichkeit/Jahr: 0.2 = 200CHF/Jahr

### Risikostrategien

#### Vermeidung

Kann oft nicht einfach vermieden werden, da für die Funktionalität die Risikaussetzung benötigt wird.

Bsp: Ein Webserver muss dem Internet angehängt sein, wass DOS-Attacken unvermeidbar macht

#### Reduktion/Optimierung

Dinge die gemacht werden können, damit die Eintrittswahrscheinlichkeit oder das Schadensausmass sinkt.

Falls mehr als der Optimale Wert (noch besser optimieren ist zu teuer) reduziert wird, nennt man das Risikoreduktion.

#### Transfer

Lohnt sich wenn das Risiko nicht durch eine Entität abgefangen werden kann. Dann wird das Risiko von mehreren Entitäten oder von der nächst grösseren getragen.  
Typischerweise wird dies bei tiefen Eintrettenswahrscheinlichkeiten und hohem Schadensausmass umgesetzt. Bsp. Versicherungen

## Gesetze

### FMG (Fernmeldegesetz)

Wer einen Fernmeldedienst für dritte betreibt muss dies dem Bundesamt für Kommunikation melden.

Der Bundesrat kann für Dienste mit geringer technischer und wirtschaftlicher Bedeutung Ausnahmen vorsehen.

Für Kantonale und Kommunale Behörden gibt es spezielle Gesetze und Überkantonale Verbunde sind gar nicht geregelt. Deshalb fällt die FHNW nicht unter dieses Gesetz.

### DSG

#### Personendaten

Angaben, die sich auf einen bestimmte oder bestimmbare natürliche Person beziehen.

#### Besonders Schützenswerte Personendaten

- Religiöse / politische Ansichten
- Krankheitsdaten / Rassenzugehörigkeit / Intimsphäre
- Genetische Daten
- Biometrische Daten
- Massnahmen der Sozialhilfe
- Verwaltungs/Strafrechtliche Verfolgungen/Sanktionen

#### Bekanntgabe ins Ausland

Daten dürfen ins Ausland gegeben werden, wenn der Bundesrat festgestellt hat, dass diese Land angemessenen Schutz gewährleistet.

Wenn Bundesrat nicht Entschieden hat, muss dieses Land andere Bedingungen erfüllen.

#### Auskunftsrecht

Jede Person kann Auskunft verlangen, ob ihre Daten verarbeitet werden.

Innerhalb von 30 Tagen und kostenlos (wenn Aufwand verhältnismässig).

#### Rechtsansprüche

Eine Person kann verlangen dass:
- Falsche Daten korrigiert werden (Ausser die Änderung ist verboten oder Archivzwecke)
- Bestimmte Datenbearbeitung verboten wird
- Bekanntgabe an drittparteien verbieten.
- Daten gelöscht oder vernichtet werden.

#### Zusätze DSGVO

- Datenschutzbeauftragten nennen
- Verarbeitungstätigkeiten genau auflisten
- Einverständnis des Benutzers abholen
- Dem Benutzer die Möglichkeit geben sein Einverständnis zurückzuziehen
- Cookies müssen bewilligt und auf das technische Minimum beschränkt werden können.
- Personen-relevante Daten im Netz verschlüsseln
- Nachweisen wann wer sein Einverständnis gegeben hat.

#### Impressumspflicht

Sobald eine Webseite kommerziell ist braucht sie ein Impressum.

##### Anforderungen

- Vorname Name bzw. Firma des Anbieters
- Adresse von Wohnsitz bzw Firmensitz (kein Postfach)
- E-mail Adresse
- *Bei Fimen:* Rechtsform

## Verschlüsselungen

### Symmetrische Verschlüsselung

Zum ver- und entschlüsseln wird derselbe Schlüssel verwendet.

Einfache implementierung und schnelles Verfahren.

Wie kommt der Schlüssel vom Sender zum Empfänger.

#### Verfahren

- Camelia
- AES

#### Gebrochene Verfahren

- RC4
- DES
- 3DES

### Asymmetrische Verschlüsselung

Es braucht ein Schlüsselpaar, einer für die Verschlüsselung und der andere für die Entschlüsselung.

Aufwendiges mathematisches Verfahren und grosse Schlüssellängen.

#### Elliptische Kurven (Eliptic-curve Cryptography - ECC)

Es werden Punkte mit Linien verbunden und anschliessend gespiegelt.

Es werden wesentlich Kürzere Keys verwendet, als für RSA.

#### Verfahren

- RSA 4096+
- ECC 256+
- ElGammal

#### Gebrochene Verfahren

- RSA 1024
- RSA 2048 (vermutlich teilweise gebrochen)
- ECC 192

### Hashing

Einweg verschlüsselung, die nicht rückgängig gemacht werden kann (also nicht entschlüsselt werden kann).

Es kann bei einem guten Hash nicht bestimmt werden, was sich bei einer Änderung geändert hat.

#### Verfahren

- RIPE-MD 256+
- SHA2/3 256+

#### Gebrochene Verfahren

- MD5
- RIPE-MD 160
- SHA1

### Hybride Verschlüsselung

Es wird mit einem Assymetrischen Verfahren einen Symmetrischen Schlüssel übermittelt und danach nur noch mit diesem Verschlüsselt.

### Perfect Forward Secrecy

Es wird beim Schlüsselaustausch ein Langzeitschlüssel eingesetzt.

Falls dieser Langzeitschlüssel gebrochen wird, muss bei PFS gewährleistet sein, dass die Kommunikation nicht im Nachhinein entschlüsselt werden kann.

### Signieren

1. Vom Dokument wird ein Hash generiert.
2. Der Hash wird mit einem Privaten Schlüssel verschlüsselt.
3. Das Dokument (unverschlüsselt) wird mit dem verschlüsselten Hash und dem Öffentlichen Schlüssel versendet.
4. Der Empfänger kann mit dem PubKey den verschlüsselten Hash überprüfen.

### Zero Knowledge Proof

Peggy (Prüfer) legt in einem Commitment mehrere richtige Antworten vor.  
Victor (Verifizierer) darf eine Anschauen und verifizieren, dass die Antwort richtig ist.  
Das kann beliebig oft wiederholte werden, Peggy muss aber jedes mal ein neues Commitment vorlegen.

## Zertifikate

Vertrauenswerter, öffentlicher Schlüssel

Beinhaltet:

- Identifikation (SubjectDN & SubjectAlternateName)
- Öffentlicher Schlüssel
- Gültigkeitsdauer
- Verwendungszweck (z.B. Email / WebClients)

### Lebenszyklus

1. Schlüsselpaar wird erstellt
2. CSR (Certificate Signing Request) wird mindestens mit dem SubjectDN und dem PubKey erstellt.
3. Der PubKey wird von einer vertrauenswürdigen Instanz unterschrieben (Nun ist es ein Zertifikat).
4. (optional) CRL (Certificate Revocation List), welche ungültige Zertifikate beinhaltet.
5. (optional) Ablaufdatum

### Begriffe

#### Certificate Authority (CA)

Instanz die Zertifikate ausstellt.

#### Registration Authority (RA)

Instanz bei der Zertifikate beantragt werden können und diese Anträge überprüft.

#### Validation Authority (VA)

Instanz welche Zertifikate prüft. Dies ist vollautomatisch und läuft mit OSCP oder SCVP.

#### Certificate Policy (CP) (Dokument)

Anforderungen an CA. Es dient Dritten zur analyse der Vertrauenswürdigkeit.

#### Certificate Practice Statements (CPS) (Dokument)

Beschreibt Praktische umsetzung des CP Dokuments in die Praxis.

## Angriffe

### Kategorisierung

- Ereignis
  - natürlich
  - künstlich
    - harmlos
    - bösartig
      - gerichtet
      - zufällig

### Nicht technische Angriffe

Angriffe die ein Schutzziel beinträchtigen können und keine technische Anlage als Ziel haben.

Mögliche Ziele:  
- Menschen
- Prozesse
- Zustände

#### Dumpster Diving

Vertrauliche Informationen landen im Abfall / Altpapier / aussortierte Hardware und werden dort gesammelt.

Sonderform: es werden im Webarchiv Informationen gesucht, welche damals öffentlich und heute vertraulich sind.

#### Spying

Informationen werden durch Beobachten und ohne manipulation von Entitäten beschafft.

*Sonderform "Eavesdropping":* mitschneiden von legitimen Datenflüssen

#### Social Engineering

- Impersonation:  
  Ich bin euer neuer Supportmitarbeiter und helfe bei ihrem Problem von dem sie nichts wissen
- Tailgating:  
  Ich komme direkt mit ihnen durch die Schleuse
- Phishing/Vishing/Whaling  
  Ich bin arm, bitte senden sie mir Geld / Kontoinformationen
- Popup Fenster  
  Wir haben 1200 Viren auf ihrem System gefunden
- Intressante Applikationen  
  Coole App mit tollen Features
- Hoaxing  
  Machen Sie ihren Computer kaputt weil ich selbst zu blöd bin einen Virus zu schreiben.

##### Typische Arbeitsmethoden

- Dringlichkeit
- Authorität
- Vertraulichkeit
- Vertrautheit
- Schuldgefühl (Quid pro quo / Piggybacking / Tailgating)
- Gier oder Faulheit (Baiting)

##### Kanäle

Alles mögliche (Tel, mail, post, Social Media, etc.)

##### Fishing

- Phishing: password Fishing  
- Vishing: fishing over VOIP
- Smishing: fishing over SMS
- Spearing: Spear Phishing (Phishing auf kleine Zielgruppe, mit besserer Qualität)
- Whaling: Phishing auf grosse Fische

##### Gängige Angriffe

- Enkeltrick
- Romance Scam
- Sextortion
- CEO Fraud
- Advance Scam Fraud

##### Gegenmassnahmen

- Ausbildung Beteiligter
- Etablieren von geeigneten Prozessen

### Technische Angriffe

#### Gegenmassnahmen

- Verhindern (Zugriff auf system limitieren)
- Erschweren (Angriffsfläche gering halten)
- Entdecken (Schadaktivitäten erkennen)
- Ableiten, Erholen (Schaden gering halten)

#### Man in the middle

#### Dos (Denial of Service)

- Einfach: teile des Systems überlasten
- Fortgeschritten: Daten/Programm/HW zerstören

#### Zero Day Exploits

Die Schwachstelle wird zum Zeitpunkt der Entdeckung bereits ausgenutzt, deshalb muss sie auch nicht geheim gehalten werden und braucht ein sofortiger Patch.

#### Security through Obscurity

Sicherheit durch geheimhaltung der Funktionsweise des Systems.

#### Full Disclosure

Der Sicherheitsforscher, der die Schwachstelle gefunden hat legt die Schwachstelle öffentlich. Das Unternehmen ist unter Zeitdruck und das Image wird geschwächt.

#### Responsible Disclosure

Es wird nur öffentlich gemacht, dass eine Schwachstelle existiert. Die genauen Details werden nur dem Hersteller zugekommen lassen, damit diese genügend Zeit haben die Schwachstelle zu beheben, bis sie ganz veröffentlicht wird.

#### Supply Chain Attacken

#### Exploits

##### Kategorien

- Remote Code Execution
- Local Privilege escalation
- Information disclosure/manipulation

##### Weitere Attribute

- Full Chain Break
- Zero Click

#### Cache Poisoning

mittels falscher Informationen Datenströme umleiten

- DNS Poisoning
- ARP-Spoofing
- DHCP Poisoning

#### Privilege escalation

Sicherheitsbarrieren umgehen, mithilfe der Übernahme der Rechten von hochpriviligierten Prozessen oder durch die Überwindung von Sicherheitsbarrieren.

#### Webbasierte Angriffe

- Drive by Infektionen
- Injection

#### Angriff Entdecken

##### Indikatoren

- Versagen eines Dienstes / Assets
- Geänderte Leistung eines Subsystems
- Geändertes Verhalten eines Systems/Subsystems

