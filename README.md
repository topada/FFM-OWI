# Frankfurt OWi Anzeige

Ein Codex-Skill, der aus Fotos eines möglichen Halt- oder Parkverstoßes eine nachvollziehbare Anzeige vorbereitet und das Onlineformular der Stadt Frankfurt am Main ausfüllt. Die fertigen Angaben werden zur Prüfung vorgelegt. **Eine Anzeige wird erst nach ausdrücklicher Bestätigung abgesendet.**

## Was macht der Skill?

- Er prüft die bereitgestellten Fotos auf Kennzeichen, Fahrzeugdetails, Standort, Verkehrszeichen und Markierungen.
- Er ermittelt belegbare Aufnahmezeitpunkte aus Original-Metadaten, sichtbaren Zeitstempeln oder deinen Angaben und kennzeichnet Unsicherheiten.
- Er gleicht plausible Verstöße mit amtlichen deutschen Rechtsquellen ab, erklärt die voraussichtlichen Regelsätze und lässt dich den passenden Vorwurf auswählen.
- Er formuliert den Sachverhalt auf Deutsch für die Behörde.
- Er schwärzt unbeteiligte Personen und fremde lesbare Kennzeichen in lokalen Upload-Kopien. Die Originalbilder bleiben unverändert.
- Er trägt die Angaben per Computer Use in das [Frankfurter Onlineformular](https://portal-civ.ekom21.de/civ.public/start.html?oe=00.00.PA.FFOrdA&mode=cc&cc_key=AnzeigeOwi) ein und zeigt vor dem Absenden die tatsächlichen Formulardaten und Anhänge zur Kontrolle.

Der Skill ist für den **ruhenden Verkehr in Frankfurt am Main** vorgesehen. Die rechtliche Einordnung bleibt vorläufig; über die Anzeige entscheidet die Behörde. Fehlende Tatsachen, Behinderungen oder Gefährdungen werden nicht erfunden. Die Unterhaltung folgt deiner Sprache, während Freitexte für die deutsche Behörde auf Deutsch verfasst werden.

## Voraussetzungen

- Codex mit Unterstützung für lokale Skills.
- Eine verfügbare Computer-Use-Anbindung (`cua_repl`) für die Bedienung des Portals. Der Skill selbst installiert diese Anbindung nicht.
- Internetzugriff für Rechtsquellen und das Onlineformular sowie lokale Werkzeuge zum Lesen von Bildmetadaten und zum Schwärzen von Upload-Kopien.
- Fotos des Vorfalls und ergänzende Angaben, soweit Ort, Zeitpunkt oder andere notwendige Tatsachen daraus nicht eindeutig hervorgehen.

## Installation

### Direkt in Codex

Bitte Codex, diesen Skill über den Skill-Installer zu installieren:

```text
Installiere den Skill aus https://github.com/topada/FFM-OWI.
Die SKILL.md liegt im Stammverzeichnis des Repositorys.
Verwende als lokalen Skill-Namen frankfurt-owi-anzeige.
```

Der Installer legt den Skill standardmäßig unter `~/.codex/skills/frankfurt-owi-anzeige` ab. Wenn `CODEX_HOME` gesetzt ist, wird stattdessen dessen Unterverzeichnis `skills/frankfurt-owi-anzeige` verwendet. Der Skill ist nach der Installation im nächsten Gesprächsschritt verfügbar.

### Alternativ mit Git

Führe in einem Terminal diese Befehle aus:

```sh
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
git clone https://github.com/topada/FFM-OWI.git \
  "${CODEX_HOME:-$HOME/.codex}/skills/frankfurt-owi-anzeige"
```

Der Zielordner darf noch nicht existieren. Wenn der Skill dort bereits installiert ist, aktualisiere ihn stattdessen wie unten beschrieben.

## Verwendung

Füge deine Fotos in Codex hinzu und rufe den Skill beispielsweise so auf:

```text
$frankfurt-owi-anzeige
Prüfe diese Fotos und bereite eine Anzeige für Frankfurt am Main vor.
Der Standort ist [Straße und Hausnummer oder Kreuzung].
Fülle das Formular für meine Prüfung aus.
```

Originaldateien sind hilfreich, wenn ihre Metadaten für Aufnahmezeit oder Standort benötigt werden. Beschreibe zusätzlich eigene Beobachtungen, die aus den Bildern nicht hervorgehen. Mehrere Fotos belegen zunächst einzelne Beobachtungen; eine durchgehende Standzeit darf nur mit entsprechender Tatsachengrundlage angenommen werden.

Der Skill fragt fehlende Angaben ab, stellt plausible Verstöße zur Auswahl und bereitet anschließend das Formular vor. Vor der Übermittlung erhältst du eine vollständige Übersicht einschließlich der Erklärung als Zeuge und der hochgeladenen Fotos. Erst deine ausdrückliche Bestätigung dieses Berichts erlaubt das Absenden.

## Persönliches Anzeigeprofil und Datenschutz

Beim ersten Einsatz fragt der Skill deine erforderlichen Anzeigedaten gesammelt ab und speichert daraus ein wiederverwendbares lokales Profil. Optionale Kontaktangaben können leer bleiben. Du trittst gegenüber der Behörde als namentlich benannter Zeuge auf; freiwillige Kontaktdaten können bei einer Akteneinsicht offengelegt werden.

Das Profil liegt **außerhalb dieses Repositorys**:

```text
$CODEX_HOME/profiles/frankfurt-owi-anzeige.json
```

Ohne gesetztes `CODEX_HOME` wird `~/.codex/profiles/frankfurt-owi-anzeige.json` verwendet. Der Skill sieht für die Profildatei private Zugriffsrechte (`0600`) und für das übergeordnete Profilverzeichnis `0700` vor, soweit das System dies unterstützt.

Die Datei [assets/local-profile.example.json](assets/local-profile.example.json) ist lediglich eine leere Vorlage. Trage keine persönlichen Daten in die geteilten Skill-Dateien ein und veröffentliche weder dein Profil noch Beweisfotos, Browseraufnahmen oder Falldaten in diesem Repository. Die Autorenadresse in der Skill-Beschreibung ist keine vorausgefüllte Kontaktadresse für Anzeigen.

## Aktualisierung

Wenn du den Skill mit Git installiert hast:

```sh
git -C "${CODEX_HOME:-$HOME/.codex}/skills/frankfurt-owi-anzeige" pull --ff-only
```

Dein außerhalb des Skill-Ordners gespeichertes Anzeigeprofil bleibt dabei erhalten.

## Dateien im Repository

| Datei | Inhalt |
| --- | --- |
| [SKILL.md](SKILL.md) | Arbeitsablauf, Beweisbewertung, Datenschutz und Bestätigungsregeln |
| [agents/openai.yaml](agents/openai.yaml) | Anzeigename und Aufrufvorschlag für Codex |
| [assets/local-profile.example.json](assets/local-profile.example.json) | Leere Vorlage für das lokale Anzeigeprofil |
| [references/form-catalog.md](references/form-catalog.md) | Dokumentierte Formularoptionen und Hinweise zur Einordnung |
| [references/form-catalog.json](references/form-catalog.json) | Strukturierter Katalog einschließlich Bußgeldschätzungen und Quellen |

Der Katalog dokumentiert einen beobachteten Portalstand. Formularoptionen und Rechtslage werden bei der Bearbeitung eines Falls erneut geprüft.
