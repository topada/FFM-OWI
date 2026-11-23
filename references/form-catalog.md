# Frankfurt OWi form option catalog

Observed through Computer Use on 2026-11-19. Source: [Frankfurt ekom21 portal](https://portal-civ.ekom21.de/civ.public/start.html?oe=00.00.PA.FFOrdA&mode=cc&cc_key=AnzeigeOwi).

Read the relevant group before selecting an offence. These are exact observed portal labels, including spelling errors. The UI labels are distinct from the sourced likely-fine estimates below; neither determines the authority's eventual decision. Recheck the live page if labels or available branches differ.

## Contents

- Vehicle dropdowns: Fahrzeugtyp, Kennzeichen Land, Marke des Fahrzeuges
- Incident-page schemas and shared upload constraints
- Groups 1–8: every specific offence route, its obstruction controls, and time fields
- Likely fines, official sources and estimation rules
- Portal requirements and UI limitations

## Vehicle dropdowns

### Fahrzeugtyp (19)

- Anhänger
- Elektrokleinstfahrzeug
- Kraftomnibus
- Kraftomnibus mit Anhänger
- Kraftomnibus mit Fahrgästen
- Kraftrad
- Kraftrad mit Anhänger
- Kraftroller
- LKW
- LKW mit Anhänger
- Leichtkraftfahrzeug
- Leichtkraftrad
- Mofa
- PKW
- PKW mit Anhänger
- Sattelzuganhänger
- Sattelzugmaschine
- Wohnmobil
- Wohnmobil mit Anhänger

### Kennzeichen Land (31)

- Deutschland
- Belgien
- Bulgarien
- Dänemark
- Estland
- Finnland
- Frankreich
- Griechenland
- Irland
- Island
- Italien
- Kroatien
- Lettland
- Liechtenstein
- Litauen
- Luxemburg
- Malta
- Niederlande
- Norwegen
- Österreich
- Polen
- Portugal
- Rumänien
- Schweden
- Schweiz
- Slowakische Republik
- Slowenien
- Spanien
- Tschechien
- Ungarn
- Zypern

### Marke des Fahrzeuges (64)

- Alfa Lancia
- Alfa Romeo
- Aston Martin
- Audi
- Austin
- BMW
- Bugatti
- Chevrolet
- Chrysler
- Citroën
- Dacia
- Daewoo
- DAF
- Daihatsu
- Delta Motor
- Ferrari
- Fiat
- Ford
- General Motors
- Harley-Davidson
- Honda
- Husqvarna
- Hyundai
- Isuzu
- Iveco
- Jaguar
- Jeep
- Kässbohrer
- Kawasaki
- Kia
- Lamborghini
- Lancia
- MAN
- Maserati
- Mazda
- mbk
- Mercedes-Benz
- MG
- Mitsubishi
- Moto Guzzi
- Nissan
- Opel
- Peugeot
- Piaggio
- Pontiac
- Porsche
- Renault
- Rolls-Royce
- Rover
- Saab
- Samsung
- Scania
- Seat
- Skoda
- Smart
- Subaru
- Suzuki
- Tesla
- Toyota
- Vespa
- Volvo
- Volkswagen
- Yamaha
- Sonstiges

The blank selection and disabled “Bitte auswählen...” placeholder are not substantive options. The country list contains no “other” choice; do not invent an unavailable country or choose Deutschland for an unsupported plate. Marke includes “Sonstiges”. Fahrzeugmodell and Farbe are free-text fields, not dropdown lists. The entrypoint’s photo-evidence rules and PKW default still apply.

## Incident schemas and shared requirements

- **Single time:** required Straße und Hausnummer, eventuell Konkretisierung; Tattag (Datum); Tatzeit (Zeitpunkt).
- **Interval:** required Straße und Hausnummer, eventuell Konkretisierung; Tattag (Datum); Beginn Tatzeit; Ende Tatzeit.
- Time format: `hh:mm`; preserve EXIF seconds in the case analysis and, where available, an appropriate comments field. Do not invent a comments field: none was observed on these 72 incident screens.
- Both schemas offer optional further witnesses via “Eintrag hinzufügen”.
- Both require a Beweis-Übersichtsfoto and a Beweis-Fahrzeugfoto. Each upload section allows at most 5 files, PDF/JPEG/JPG/PNG, maximum 10 MB per file.
- Interval pages instruct that reports crossing a day boundary use only one day’s times, e.g. `22:00–23:59` or `00:00–06:00`.
- A displayed obstruction description is required and limited to 1000 characters. A Ja/Nein question can reveal it; some routes require it directly without offering Ja/Nein. Follow the precise row below.
- “Personal Ja/Nein” means the actual question “Wurden Sie behindert?*”, with Ja/Nein choices. Ja requires the description; Nein hides it. “Rescue Ja/Nein” means “Wurde ein Rettungsfahrzeug im Einsatz behindert?*”. Do not treat these questions as interchangeable.

## Likely fines: sources and interpretation

Verified on **2026-11-19** against the [current BKatV annex](https://www.gesetze-im-internet.de/bkatv_2013/anlage.html) and the KBA's [08.10.2026 database](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bet_datenbank_08102026_txt.txt?__blob=publicationFile&v=9), with page-level checks in the [official 15.1 print catalog, 22.08.2024](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2). Related [October 2026 amendment](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/aenderungsverzeichnis_datenbank_2b_08_10_2026.pdf?__blob=publicationFile&v=3). All referenced current amounts were cross-checked with [weg.li charges](https://www.weg.li/charges) using its [public charge data](https://www.weg.li/charges.json). The live official entries take priority over weg.li's 2024 edition description.

- Values are **likely standard Verwarnungs-/Bußgeld amounts**, in EUR, for the stated proven facts, not a promise of prosecution or a final sanction. [BKatV § 1](https://www.gesetze-im-internet.de/bkatv_2013/__1.html) and [§ 3](https://www.gesetze-im-internet.de/bkatv_2013/__3.html) govern standard-case assessment and possible changes. [§ 2](https://www.gesetze-im-internet.de/bkatv_2013/__2.html) addresses warnings.
- Figures exclude possible procedural fees/expenses, towing or other separate costs. Administrative fine proceedings can add [fees and expenses under § 107 OWiG](https://www.gesetze-im-internet.de/owig_1968/__107.html). Do not automatically add such charges to every warning.
- Mapping the portal label to a KBA TBNR is a reasoned semantic match: the Frankfurt UI does **not** expose the TBNR it sends. TBNRs and BKat numbers are different identifiers. Where a KBA entry has `-- BKat`, the detailed official catalog supplies the warning amount even though the BKatV annex lacks a dedicated numbered entry.
- The additional amount depends on **actual legally relevant obstruction**, not merely selecting Ja or entering the saved description. A forced detour, concrete danger, blocking a taxi, and hindering an emergency vehicle in action are different facts. Never choose the offence with the largest fine to maximize an allegation.
- Use the actual duration, including thresholds the portal does not offer as distinct radios: **over 15 minutes** (second row), **over one hour**, or **over three hours**. Equality at the threshold is not “longer than”. A generic Parken route can still trigger a duration tariff.
- Country and brand alone have no separate tariff. The listed defaults generally assume a PKW and a valid applicable prohibition. For another vehicle class, permission, supplementary sign or exception, verify applicability first; an allowed vehicle has no violation merely because a similarly worded route exists. No reliable weight-based fine can be inferred from appearance alone.
- When a route has no obstruction radio, the “mit Behinderung” figure below is still a legal variant **only if the evidence supports it**; its presence in this catalog does not add a control to the portal.
- Do not add the figures in different rows together for the same conduct. The [BKatV § 2(6)](https://www.gesetze-im-internet.de/bkatv_2013/__2.html) and [§ 3(5)](https://www.gesetze-im-internet.de/bkatv_2013/__3.html) contain rules for overlapping offences.
- Recheck current official sources when running the skill after the verification date, and the version applicable on the incident date. If facts do not establish which variant applies, show the conditional amounts or an explicit uncertainty rather than invent a single fine.

The route tables show **basic / obstruction** values for the lowest applicable duration in that route. Longer-duration variants and special conditions appear in the adjacent notes. The following page links are the actual pages containing the cited TBNRs, not generic search results.

## 1. Radweg/Radfahrstreifen

Selection order and labels follow the portal. The route IDs below are local catalog references, not Tatbestandsnummern.

| Route | Exact choice sequence | Obstruction controls | Incident times | Likely EUR (basic / obstruction) | Fine conditions / official reference |
|---|---|---|---|---|---|
| G01-R01 | Halten → auf einem Radweg (Zeichen 237). | Personal Ja/Nein; Ja → description | Single time | 55 / 70 | KBA TBNR [141070](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=222); [141071](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=222); no dedicated BKat number. |
| G01-R02 | Halten → auf einem gemeinsamen Geh- und Radweg (Zeichen 240). | No obstruction input observed | Single time | 50 / 55 | PKW-Regelfall. Bei einer Einordnung als Befahren/Halten im gesperrten Bereich können Fahrzeugklasse und zulässige Gesamtmasse maßgeblich sein: 141166 / 141159 / 141737 (50 / 55 / 100 EUR). Ein PKW-Standardwert ersetzt keine Gewichts- oder Zulassungsfeststellung. KBA TBNR [141090](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=223); [141091](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=223); no dedicated BKat number. |
| G01-R03 | Halten → auf einem getrennten Geh- und Radweg (Zeichen 241). | No obstruction input observed | Single time | 50 / 55 | PKW-Regelfall. Bei einer Einordnung als Befahren/Halten im gesperrten Bereich können Fahrzeugklasse und zulässige Gesamtmasse maßgeblich sein: 141166 / 141159 / 141737 (50 / 55 / 100 EUR). Ein PKW-Standardwert ersetzt keine Gewichts- oder Zulassungsfeststellung. KBA TBNR [141090](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=223); [141091](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=223); no dedicated BKat number. |
| G01-R04 | Halten → auf einer Fahrradstraße (Zeichen 244.1). | Personal Ja/Nein; Ja → description | Single time | 55 / 70 | Nur wenn die Benutzung/Halteposition tatsächlich unzulässig ist. Eine Fahrradstraße allein begründet kein pauschales Parkverbot für dort zugelassenen Fahrzeugverkehr; Zusatzzeichen und Berechtigung prüfen. KBA TBNR [141020](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=226); [141021](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=226); no dedicated BKat number. |
| G01-R05 | Halten → verbotswidrig auf einem Schutzstreifen für den Radverkehr (Zeichen 340). | Personal Ja/Nein; Ja → description | Single time | 55 / 70 | Kein eigener Daueraufschlag in dieser Familie: ein längerer Aufenthalt allein rechtfertigt nicht automatisch mehr als 55 EUR. Die 70-EUR-Variante verlangt tatsächliche Behinderung; die Portalwahl Halten verkürzt den im Sachverhalt dokumentierten Aufenthalt nicht. KBA TBNR [142170](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=276); [142671](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=276). BKat 54a, 54a.1. |
| G01-R06 | Parken → auf einem Radweg (Zeichen 237). | Personal Ja/Nein; Ja → description | Start + end | 55 / 70 | Länger als 1 Stunde, ohne zusätzliche Behinderung: 70 EUR. Länger als 1 Stunde, mit nachgewiesener Behinderung: 80 EUR. KBA TBNR [141174](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=222); [141775](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=222); [141776](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=222); [141777](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=222). BKat 52a, 52a.1, 52a.2, 52a.2.1. |
| G01-R07 | Parken → auf einem gemeinsamen Geh- und Radweg (Zeichen 240). | Personal Ja/Nein; Ja → description | Start + end | 55 / 70 | Länger als 1 Stunde, ohne zusätzliche Behinderung: 70 EUR. Länger als 1 Stunde, mit nachgewiesener Behinderung: 80 EUR. 52a-Zuordnung für Geh-/Radwegparken. Bei einer stattdessen auf das gesperrte Verkehrsgebiet bezogenen Ahndung nach BKat 144 gelten 55 / 70 EUR und die 3-Stunden-Variante; nicht allein aus dem UI-Label eine 1-Stunden-Erhöhung garantieren. KBA TBNR [141194](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=223); [141795](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=224); [141796](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=224); [141797](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=224). BKat 52a, 52a.1, 52a.2, 52a.2.1. |
| G01-R08 | Parken → auf einem getrennten Geh- und Radweg (Zeichen 241). | Personal Ja/Nein; Ja → description | Start + end | 55 / 70 | Länger als 1 Stunde, ohne zusätzliche Behinderung: 70 EUR. Länger als 1 Stunde, mit nachgewiesener Behinderung: 80 EUR. 52a-Zuordnung für Geh-/Radwegparken. Bei einer stattdessen auf das gesperrte Verkehrsgebiet bezogenen Ahndung nach BKat 144 gelten 55 / 70 EUR und die 3-Stunden-Variante; nicht allein aus dem UI-Label eine 1-Stunden-Erhöhung garantieren. KBA TBNR [141194](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=223); [141795](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=224); [141796](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=224); [141797](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=224). BKat 52a, 52a.1, 52a.2, 52a.2.1. |
| G01-R09 | Parken → auf einer Fahrradstraße (Zeichen 244.1). | Personal Ja/Nein; Ja → description | Start + end | 55 / 70 | Länger als 1 Stunde, ohne zusätzliche Behinderung: 70 EUR. Länger als 1 Stunde, mit nachgewiesener Behinderung: 80 EUR. Nur bei tatsächlich unzulässiger Nutzung/Position; zugelassener Kfz-Verkehr darf nicht allein wegen Zeichen 244.1 als Falschparken bewertet werden. KBA TBNR [141124](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=226); [141525](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=226); [141526](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=226); [141527](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=226); no dedicated BKat number. |
| G01-R10 | Parken länger als 1 Stunde → auf einem Radweg (Zeichen 237). | Personal Ja/Nein; Ja → description | Start + end | 70 / 80 | Route already requires >1 h. KBA TBNR [141776](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=222); [141777](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=222). BKat 52a.2, 52a.2.1. |
| G01-R11 | Parken länger als 1 Stunde → auf einem gemeinsamen Geh- und Radweg (Zeichen 240). | Personal Ja/Nein; Ja → description | Start + end | 70 / 80 | Route already requires >1 h. 52a-Zuordnung für Geh-/Radwegparken. Bei einer stattdessen auf das gesperrte Verkehrsgebiet bezogenen Ahndung nach BKat 144 gelten 55 / 70 EUR und die 3-Stunden-Variante; nicht allein aus dem UI-Label eine 1-Stunden-Erhöhung garantieren. KBA TBNR [141796](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=224); [141797](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=224). BKat 52a.2, 52a.2.1. |
| G01-R12 | Parken länger als 1 Stunde → auf einem getrennten Geh- und Radweg (Zeichen 241). | Personal Ja/Nein; Ja → description | Start + end | 70 / 80 | Route already requires >1 h. 52a-Zuordnung für Geh-/Radwegparken. Bei einer stattdessen auf das gesperrte Verkehrsgebiet bezogenen Ahndung nach BKat 144 gelten 55 / 70 EUR und die 3-Stunden-Variante; nicht allein aus dem UI-Label eine 1-Stunden-Erhöhung garantieren. KBA TBNR [141796](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=224); [141797](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=224). BKat 52a.2, 52a.2.1. |
| G01-R13 | Parken länger als 1 Stunde → auf einer Fahrradstraße (Zeichen 244.1). | Personal Ja/Nein; Ja → description | Start + end | 70 / 80 | Route already requires >1 h. Nur bei tatsächlich unzulässiger Nutzung/Position; zugelassener Kfz-Verkehr darf nicht allein wegen Zeichen 244.1 als Falschparken bewertet werden. KBA TBNR [141526](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=226); [141527](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=226); no dedicated BKat number. |

Exact conditional field prompts:

- Bitte wählen Sie aus:*
- Wurden Sie behindert?*

## 2. Gehweg/Fußgängerüberweg/Fußgängerfurt

Selection order and labels follow the portal. The route IDs below are local catalog references, not Tatbestandsnummern.

| Route | Exact choice sequence | Obstruction controls | Incident times | Likely EUR (basic / obstruction) | Fine conditions / official reference |
|---|---|---|---|---|---|
| G02-R01 | Halten → verbotswidrig auf dem Gehweg. | No obstruction input observed | Single time | 50 / 55 | KBA TBNR [112050](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=109); [112051](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=109); no dedicated BKat number. |
| G02-R02 | Halten → auf dem Fußgängerüberweg. | No obstruction input observed | Single time | 20 / 35 | KBA TBNR [141290](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=209); [141291](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=209). BKat 51, 51.1. |
| G02-R03 | Parken → verbotswidrig auf dem Gehweg. | Personal Ja/Nein; Ja → description | Start + end | 55 / 70 | Länger als 1 Stunde, ohne zusätzliche Behinderung: 70 EUR. Länger als 1 Stunde, mit nachgewiesener Behinderung: 80 EUR. KBA TBNR [112454](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=110); [112655](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=110); [112656](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=110); [112657](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=110). BKat 52a, 52a.1, 52a.2, 52a.2.1. |
| G02-R04 | Parken → auf einem Gehweg entgegen der durch Zeichen 315 vorgeschriebenen Aufstellungsart. | Personal Ja/Nein; Ja → description | Start + end | 10 / 15 | Länger als 3 Stunden, ohne zusätzliche Behinderung: 20 EUR. Länger als 3 Stunden, mit nachgewiesener Behinderung: 30 EUR. KBA TBNR [142222](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=274); [142223](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=274); [142224](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=274); [142225](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=274). BKat 54, 54.1, 54.2, 54.2.1. |
| G02-R05 | Parken → auf dem Gehweg (Zeichen 239), der durch dieses Zeichen gesperrt war. | Personal Ja/Nein; Ja → description | Start + end | 55 / 70 | Länger als 3 Stunden: 70 EUR. BKat 144 ist nicht die 1-Stunden-Familie 52a. Bei Behinderung und mehr als drei Stunden keinen unbelegten zusätzlichen Aufschlag addieren. KBA TBNR [141184](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=223); [141785](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=223); [141786](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=223). BKat 144, 144.1, 144.2. |
| G02-R06 | Parken → auf einem gemeinsamen Geh- und Radweg (Zeichen 240). | Personal Ja/Nein; Ja → description | Start + end | 55 / 70 | Länger als 1 Stunde, ohne zusätzliche Behinderung: 70 EUR. Länger als 1 Stunde, mit nachgewiesener Behinderung: 80 EUR. 52a-Zuordnung für Geh-/Radwegparken. Bei einer stattdessen auf das gesperrte Verkehrsgebiet bezogenen Ahndung nach BKat 144 gelten 55 / 70 EUR und die 3-Stunden-Variante; nicht allein aus dem UI-Label eine 1-Stunden-Erhöhung garantieren. KBA TBNR [141194](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=223); [141795](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=224); [141796](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=224); [141797](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=224). BKat 52a, 52a.1, 52a.2, 52a.2.1. |
| G02-R07 | Parken → auf einem getrennten Geh- und Radweg (Zeichen 241). | Personal Ja/Nein; Ja → description | Start + end | 55 / 70 | Länger als 1 Stunde, ohne zusätzliche Behinderung: 70 EUR. Länger als 1 Stunde, mit nachgewiesener Behinderung: 80 EUR. 52a-Zuordnung für Geh-/Radwegparken. Bei einer stattdessen auf das gesperrte Verkehrsgebiet bezogenen Ahndung nach BKat 144 gelten 55 / 70 EUR und die 3-Stunden-Variante; nicht allein aus dem UI-Label eine 1-Stunden-Erhöhung garantieren. KBA TBNR [141194](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=223); [141795](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=224); [141796](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=224); [141797](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=224). BKat 52a, 52a.1, 52a.2, 52a.2.1. |
| G02-R08 | Parken → im Bereich einer Fußgängerzone (Zeichen 242.1), der durch dieses Zeichen gesperrt war. | Personal Ja/Nein; Ja → description | Start + end | 55 / 70 | Länger als 3 Stunden: 70 EUR. BKat 144 ist nicht die 1-Stunden-Familie 52a. Bei Behinderung und mehr als drei Stunden keinen unbelegten zusätzlichen Aufschlag addieren. KBA TBNR [141184](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=223); [141785](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=223); [141786](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=223). BKat 144, 144.1, 144.2. |
| G02-R09 | Parken → auf dem Fußgängerüberweg. | Personal Ja/Nein; Ja → description | Start + end | 25 / 40 | Länger als 1 Stunde, ohne zusätzliche Behinderung: 40 EUR. Länger als 1 Stunde, mit nachgewiesener Behinderung: 50 EUR. KBA TBNR [141292](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=209); [141293](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=209); [141294](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=209); [141295](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=210). BKat 52, 52.1, 52.2, 52.2.1. |
| G02-R10 | Parken → Abstand von weniger als 5 Metern vor einem Fußgängerüberweg. | Personal Ja/Nein; Ja → description | Start + end | 25 / 40 | Länger als 1 Stunde, ohne zusätzliche Behinderung: 40 EUR. Länger als 1 Stunde, mit nachgewiesener Behinderung: 50 EUR. KBA TBNR [141302](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=210); [141303](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=210); [141304](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=210); [141305](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=210). BKat 52, 52.1, 52.2, 52.2.1. |
| G02-R11 | Parken → auf einer Fußgängerfurt (Eine Fußgängerfurt ist eine durch Markierungen fast ausschließlich an Ampelanlagen gekennzeichnete Fläche auf der Straße). | Description always required; no Ja/Nein | Start + end | 20 (obstruction required) | Die Behinderung ist Tatbestandsvoraussetzung, kein bloßer Aufschlag. Ohne belegte Behinderung lässt sich aus dieser Route kein pauschaler 20-EUR-Verstoß ableiten. Nicht mit dem Fußgängerüberweg/Zebrastreifen verwechseln. KBA TBNR [101048](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=17); no dedicated BKat number. |
| G02-R12 | Parken länger als 1 Stunde verbotswidrig auf dem Gehweg | Personal Ja/Nein; Ja → description | Start + end | 70 / 80 | Route already requires >1 h. KBA TBNR [112656](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=110); [112657](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=110). BKat 52a.2, 52a.2.1. |

Exact conditional field prompts:

- Bitte wählen Sie aus:*
- Das Fahrzeugt parkte:*
- Wurden Sie behindert?*

## 3. Haltverbot/gesperrter Bereich/Sonderparkplätze

Selection order and labels follow the portal. The route IDs below are local catalog references, not Tatbestandsnummern.

| Route | Exact choice sequence | Obstruction controls | Incident times | Likely EUR (basic / obstruction) | Fine conditions / official reference |
|---|---|---|---|---|---|
| G03-R01 | im Haltverbot. → unzulässig im eingeschränkten Haltverbot (Zeichen 286). → Parken | Personal Ja/Nein; Ja → description | Start + end | 25 / 40 | Länger als 1 Stunde, ohne zusätzliche Behinderung: 40 EUR. Länger als 1 Stunde, mit nachgewiesener Behinderung: 50 EUR. KBA TBNR [141322](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=211); [141323](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=211); [141324](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=211); [141325](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=211). BKat 52, 52.1, 52.2, 52.2.1. |
| G03-R02 | im Haltverbot. → unzulässig im eingeschränkten Haltverbot (Zeichen 286). → Parken länger als 1 Stunde | Personal Ja/Nein; Ja → description | Start + end | 40 / 50 | Route already requires >1 h. KBA TBNR [141324](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=211); [141325](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=211). BKat 52.2, 52.2.1. |
| G03-R03 | im Haltverbot. → im absoluten Haltverbot (Zeichen 283). → Parken | Personal Ja/Nein; Ja → description | Start + end | 25 / 40 | Länger als 1 Stunde, ohne zusätzliche Behinderung: 40 EUR. Länger als 1 Stunde, mit nachgewiesener Behinderung: 50 EUR. KBA TBNR [141312](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=210); [141313](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=210); [141314](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=211); [141315](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=211). BKat 52, 52.1, 52.2, 52.2.1. |
| G03-R04 | im Haltverbot. → im absoluten Haltverbot (Zeichen 283). → Parken länger als 1 Stunde | Personal Ja/Nein; Ja → description | Start + end | 40 / 50 | Route already requires >1 h. KBA TBNR [141314](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=211); [141315](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=211). BKat 52.2, 52.2.1. |
| G03-R05 | im Haltverbot. → im eingeschränkten Haltverbot für eine Zone (Zeichen 290). → Parken | Personal Ja/Nein; Ja → description | Start + end | 25 / 40 | Länger als 1 Stunde, ohne zusätzliche Behinderung: 40 EUR. Länger als 1 Stunde, mit nachgewiesener Behinderung: 50 EUR. KBA TBNR [141118](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=225); [141119](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=225); [141121](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=225); [141122](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=225). BKat 52, 52.1, 52.2, 52.2.1. |
| G03-R06 | im Haltverbot. → im eingeschränkten Haltverbot für eine Zone (Zeichen 290). → Parken länger als 1 Stunde | Personal Ja/Nein; Ja → description | Start + end | 40 / 50 | Route already requires >1 h. KBA TBNR [141121](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=225); [141122](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=225). BKat 52.2, 52.2.1. |
| G03-R07 | in einem gesperrten Verkehrsbereich. → der durch Zeichen 250 gesperrt war. | No obstruction input observed | Start + end | 55 / 70 | Länger als 3 Stunden: 70 EUR. Zeichen und Fahrzeugklasse müssen zusammenpassen; insbesondere ist Zeichen 253 kein allgemeines PKW-Verbot und Zeichen 255 betrifft nicht einfach jeden PKW. Ausnahmen/Berechtigungen prüfen. Die 55-EUR-Parkvariante nicht durch den 50/55/100-EUR-Tarif für Befahren/Halten ersetzen. KBA TBNR [141164](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=225); [141865](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=225); [141866](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=225). BKat 144, 144.1, 144.2. |
| G03-R08 | in einem gesperrten Verkehrsbereich. → der durch Zeichen 251 gesperrt war. | No obstruction input observed | Start + end | 55 / 70 | Länger als 3 Stunden: 70 EUR. Zeichen und Fahrzeugklasse müssen zusammenpassen; insbesondere ist Zeichen 253 kein allgemeines PKW-Verbot und Zeichen 255 betrifft nicht einfach jeden PKW. Ausnahmen/Berechtigungen prüfen. Die 55-EUR-Parkvariante nicht durch den 50/55/100-EUR-Tarif für Befahren/Halten ersetzen. KBA TBNR [141164](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=225); [141865](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=225); [141866](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=225). BKat 144, 144.1, 144.2. |
| G03-R09 | in einem gesperrten Verkehrsbereich. → der durch Zeichen 253 gesperrt war. | No obstruction input observed | Start + end | 55 / 70 | Länger als 3 Stunden: 70 EUR. Zeichen und Fahrzeugklasse müssen zusammenpassen; insbesondere ist Zeichen 253 kein allgemeines PKW-Verbot und Zeichen 255 betrifft nicht einfach jeden PKW. Ausnahmen/Berechtigungen prüfen. Die 55-EUR-Parkvariante nicht durch den 50/55/100-EUR-Tarif für Befahren/Halten ersetzen. KBA TBNR [141164](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=225); [141865](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=225); [141866](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=225). BKat 144, 144.1, 144.2. |
| G03-R10 | in einem gesperrten Verkehrsbereich. → der durch Zeichen 255 gesperrt war. | No obstruction input observed | Start + end | 55 / 70 | Länger als 3 Stunden: 70 EUR. Zeichen und Fahrzeugklasse müssen zusammenpassen; insbesondere ist Zeichen 253 kein allgemeines PKW-Verbot und Zeichen 255 betrifft nicht einfach jeden PKW. Ausnahmen/Berechtigungen prüfen. Die 55-EUR-Parkvariante nicht durch den 50/55/100-EUR-Tarif für Befahren/Halten ersetzen. KBA TBNR [141164](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=225); [141865](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=225); [141866](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=225). BKat 144, 144.1, 144.2. |
| G03-R11 | in einem gesperrten Verkehrsbereich. → der durch Zeichen 260 gesperrt war. | No obstruction input observed | Start + end | 55 / 70 | Länger als 3 Stunden: 70 EUR. Zeichen und Fahrzeugklasse müssen zusammenpassen; insbesondere ist Zeichen 253 kein allgemeines PKW-Verbot und Zeichen 255 betrifft nicht einfach jeden PKW. Ausnahmen/Berechtigungen prüfen. Die 55-EUR-Parkvariante nicht durch den 50/55/100-EUR-Tarif für Befahren/Halten ersetzen. KBA TBNR [141164](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=225); [141865](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=225); [141866](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=225). BKat 144, 144.1, 144.2. |
| G03-R12 | auf einem Sonderparkplatz für Bewohner. → bei Zeichen 314 mit Zusatzzeichen. Ein besonderer Parkausweis lag nicht gut lesbar aus. | Personal Ja/Nein; Ja → description | Start + end | 10 / 15 | Länger als 3 Stunden, ohne zusätzliche Behinderung: 20 EUR. Länger als 3 Stunden, mit nachgewiesener Behinderung: 30 EUR. KBA TBNR [142252](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=275); [142253](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=275); [142254](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=275); [142255](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=275). BKat 54, 54.1, 54.2, 54.2.1. |
| G03-R13 | auf einem Sonderparkplatz für Bewohner. → bei Zeichen 315 mit Zusatzzeichen. Ein besonderer Parkausweis lag nicht gut lesbar aus. | Personal Ja/Nein; Ja → description | Start + end | 10 / 15 | Länger als 3 Stunden, ohne zusätzliche Behinderung: 20 EUR. Länger als 3 Stunden, mit nachgewiesener Behinderung: 30 EUR. KBA TBNR [142252](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=275); [142253](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=275); [142254](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=275); [142255](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=275). BKat 54, 54.1, 54.2, 54.2.1. |
| G03-R14 | auf einem Sonderparkplatz für Bewohner. → (Zeichen 286) mit Zusatzzeichen für "Bewohner mit besonderem Parkausweis". Ein besonderer Parkausweis lag nicht gut lesbar aus. | Personal Ja/Nein; Ja → description | Start + end | 25 / 40 | Länger als 1 Stunde, ohne zusätzliche Behinderung: 40 EUR. Länger als 1 Stunde, mit nachgewiesener Behinderung: 50 EUR. KBA TBNR [141392](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=216); [141393](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=216); [141394](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=216); [141395](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=216). BKat 52, 52.1, 52.2, 52.2.1. |
| G03-R15 | auf einem Sonderparkplatz für Bewohner. → (Zeichen 290) mit Zusatzzeichen für "Bewohner mit besonderem Parkausweis". Ein besonderer Parkausweis lag nicht gut lesbar aus. | Personal Ja/Nein; Ja → description | Start + end | 25 / 40 | Länger als 1 Stunde, ohne zusätzliche Behinderung: 40 EUR. Länger als 1 Stunde, mit nachgewiesener Behinderung: 50 EUR. KBA TBNR [141392](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=216); [141393](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=216); [141394](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=216); [141395](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=216). BKat 52, 52.1, 52.2, 52.2.1. |
| G03-R16 | auf einem Sonderparkplatz für Carsharing. → unberechtigt auf einem Parkplatz bei Zeichen 314 mit Zusatzzeichen. | No obstruction input observed | Start + end | 55 | Berechtigung und Zusatzzeichen prüfen; kein pauschaler weiterer Dauer-/Behinderungsaufschlag aus der UI ableitbar. KBA TBNR [142290](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=277). BKat 55b. |
| G03-R17 | auf einem Sonderparkplatz für Carsharing. → unberechtigt auf einem Parkplatz bei Zeichen 315 mit Zusatzzeichen. | No obstruction input observed | Start + end | 55 | Berechtigung und Zusatzzeichen prüfen; kein pauschaler weiterer Dauer-/Behinderungsaufschlag aus der UI ableitbar. KBA TBNR [142290](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=277). BKat 55b. |
| G03-R18 | auf einem Sonderparkplatz für Elektrofahrzeuge. → unberechtigt auf einem Parkplatz bei Zeichen 314 mit Zusatzzeichen. | No obstruction input observed | Start + end | 55 | Beschilderung, zeitliche Einschränkungen und konkrete Nutzungsberechtigung prüfen; nicht nur anhand der Marke oder Farbe beurteilen. KBA TBNR [142284](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=277). BKat 55a. |
| G03-R19 | auf einem Sonderparkplatz für Elektrofahrzeuge. → unberechtigt auf einem Parkplatz bei Zeichen 315 mit Zusatzzeichen. | No obstruction input observed | Start + end | 55 | Beschilderung, zeitliche Einschränkungen und konkrete Nutzungsberechtigung prüfen; nicht nur anhand der Marke oder Farbe beurteilen. KBA TBNR [142284](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=277). BKat 55a. |
| G03-R20 | auf einem Sonderparkplatz für Schwerbehinderte. → unberechtigt auf einem Parkplatz bei Zeichen 314 mit Zusatzzeichen. | No obstruction input observed | Start + end | 55 | Berechtigung/Parkausweis und konkrete Beschilderung prüfen; keine persönlichen Gesundheitsmerkmale aus Bildern ableiten. KBA TBNR [142278](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=277). BKat 55. |
| G03-R21 | auf einem Sonderparkplatz für Schwerbehinderte. → unberechtigt auf einem Parkplatz bei Zeichen 315 mit Zusatzzeichen. | No obstruction input observed | Start + end | 55 | Berechtigung/Parkausweis und konkrete Beschilderung prüfen; keine persönlichen Gesundheitsmerkmale aus Bildern ableiten. KBA TBNR [142278](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=277). BKat 55. |
| G03-R22 | auf einem Parkplatz (Zeichen 314), obwohl dies durch folgenden Zusatzzeichen für Sie verboten war. → nur PKW | Personal Ja/Nein; Ja → description | Start + end | 10 / 15 | Länger als 3 Stunden, ohne zusätzliche Behinderung: 20 EUR. Länger als 3 Stunden, mit nachgewiesener Behinderung: 30 EUR. Nur wenn das tatsächliche Fahrzeug gerade nicht von der durch Zusatzzeichen erlaubten Fahrzeugart erfasst ist. Beispiel: Ein PKW auf einem nur für PKW zugelassenen Parkplatz verwirklicht diese Route nicht allein dadurch. KBA TBNR [142262](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=276); [142263](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=276); [142264](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=276); [142265](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=276). BKat 54, 54.1, 54.2, 54.2.1. |
| G03-R23 | auf einem Parkplatz (Zeichen 314), obwohl dies durch folgenden Zusatzzeichen für Sie verboten war. → nur Wohmobile | Personal Ja/Nein; Ja → description | Start + end | 10 / 15 | Länger als 3 Stunden, ohne zusätzliche Behinderung: 20 EUR. Länger als 3 Stunden, mit nachgewiesener Behinderung: 30 EUR. Nur wenn das tatsächliche Fahrzeug gerade nicht von der durch Zusatzzeichen erlaubten Fahrzeugart erfasst ist. Beispiel: Ein PKW auf einem nur für PKW zugelassenen Parkplatz verwirklicht diese Route nicht allein dadurch. KBA TBNR [142262](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=276); [142263](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=276); [142264](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=276); [142265](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=276). BKat 54, 54.1, 54.2, 54.2.1. |
| G03-R24 | auf einem Parkplatz (Zeichen 314), obwohl dies durch folgenden Zusatzzeichen für Sie verboten war. → nur LKW | Personal Ja/Nein; Ja → description | Start + end | 10 / 15 | Länger als 3 Stunden, ohne zusätzliche Behinderung: 20 EUR. Länger als 3 Stunden, mit nachgewiesener Behinderung: 30 EUR. Nur wenn das tatsächliche Fahrzeug gerade nicht von der durch Zusatzzeichen erlaubten Fahrzeugart erfasst ist. Beispiel: Ein PKW auf einem nur für PKW zugelassenen Parkplatz verwirklicht diese Route nicht allein dadurch. KBA TBNR [142262](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=276); [142263](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=276); [142264](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=276); [142265](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=276). BKat 54, 54.1, 54.2, 54.2.1. |

Exact conditional field prompts:

- Das Fahrzeug parkte*
- Ihre Auswahl:*
- Bitte wählen Sie aus:*
- Wurden Sie behindert?*
- in einem gesperrten Verkehrsbereich*
- Ihre Auswah:*

## 4. Einbahnstraße/linke Fahrbahnseite/linker Seitenstreifen

Selection order and labels follow the portal. The route IDs below are local catalog references, not Tatbestandsnummern.

| Route | Exact choice sequence | Obstruction controls | Incident times | Likely EUR (basic / obstruction) | Fine conditions / official reference |
|---|---|---|---|---|---|
| G04-R01 | in der Einbahnstraße entgegen der Fahrtrichtung | No obstruction input observed | Start + end | 15 | Nicht mit dem Befahren einer Einbahnstraße entgegen der Fahrtrichtung gleichsetzen oder dessen Tarif hinzufügen. KBA TBNR [112076](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=111); no dedicated BKat number. |
| G04-R02 | verbotswidrig auf der linken Fahrbahnseite | Personal Ja/Nein; Ja → description | Start + end | 15 / 25 | Länger als 1 Stunde, ohne zusätzliche Behinderung: 25 EUR. Länger als 1 Stunde, mit nachgewiesener Behinderung: 35 EUR. Ausnahmen, insbesondere zulässiges Linksparken in Einbahnstraßen oder bei rechts liegenden Schienen, prüfen. KBA TBNR [112042](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=109); [112043](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=109); [112044](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=109); [112045](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=109); no dedicated BKat number. |
| G04-R03 | verbotswidrig auf dem linken Seitenstreifen | Personal Ja/Nein; Ja → description | Start + end | 15 / 25 | Länger als 1 Stunde, ohne zusätzliche Behinderung: 25 EUR. Länger als 1 Stunde, mit nachgewiesener Behinderung: 35 EUR. Ausnahmen, insbesondere zulässiges Linksparken in Einbahnstraßen oder bei rechts liegenden Schienen, prüfen. KBA TBNR [112042](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=109); [112043](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=109); [112044](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=109); [112045](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=109); no dedicated BKat number. |

Exact conditional field prompts:

- Das Fahrzeug parkte:*
- Wurden Sie behindert?*

## 5. Grünstreifen/Verkehrsinsel/Sperrfläche/Grenzmarkierung/verkehrsberuhigter Bereich

Selection order and labels follow the portal. The route IDs below are local catalog references, not Tatbestandsnummern.

| Route | Exact choice sequence | Obstruction controls | Incident times | Likely EUR (basic / obstruction) | Fine conditions / official reference |
|---|---|---|---|---|---|
| G05-R01 | dem Grünstreifen. | No obstruction input observed | Start + end | 55 | Parkbezogene KBA-Zuordnung nach § 12 Absatz 4 StVO. Eine gesonderte Einordnung als verbotswidrige Benutzung nach BKat 2 kann andere Varianten ergeben (z. B. mit Behinderung 70 EUR: 102724/102730); nicht automatisch auf den Parktarif aufschlagen. Örtliche Grünanlagensatzungen können zusätzlich oder abweichend relevant sein. KBA TBNR [112030](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=109); no dedicated BKat number. |
| G05-R02 | einer Verkehrsinsel. | No obstruction input observed | Start + end | 55 | Parkbezogene KBA-Zuordnung nach § 12 Absatz 4 StVO. Eine gesonderte Einordnung als verbotswidrige Benutzung nach BKat 2 kann andere Varianten ergeben (z. B. mit Behinderung 70 EUR: 102724/102730); nicht automatisch auf den Parktarif aufschlagen. Örtliche Grünanlagensatzungen können zusätzlich oder abweichend relevant sein. KBA TBNR [112030](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=109); no dedicated BKat number. |
| G05-R03 | benutzten die Sperrfläche (Zeichen 298) zum Parken. | No obstruction input observed | Start + end | 25 | BKat 156; nicht mit bloßem Befahren der Sperrfläche oder Überholen auf ihr verwechseln. KBA TBNR [141245](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=220). BKat 156. |
| G05-R04 | innerhalb einer Grenzmarkierung (Zeichen 299) für ein Haltverbot. | No obstruction input observed | Start + end | 25 / 40 | Länger als 1 Stunde, ohne zusätzliche Behinderung: 40 EUR. Länger als 1 Stunde, mit nachgewiesener Behinderung: 50 EUR. Diese Route sagt Haltverbot. Grenzmarkierung für Parkverbot hat eine andere Familie; bei Haltestelle/Bussonderfahrstreifen sind ebenfalls spezielle Tarife zu prüfen. KBA TBNR [141352](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=213); [141353](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=213); [141354](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=213); [141355](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=213). BKat 52, 52.1, 52.2, 52.2.1. |
| G05-R05 | in einem verkehrsberuhigten Bereich (Zeichen 325) verbotswidrig außerhalb der zum Parken gekennzeichneten Flächen. | No obstruction input observed | Start + end | 10 / 15 | Länger als 3 Stunden, ohne zusätzliche Behinderung: 20 EUR. Länger als 3 Stunden, mit nachgewiesener Behinderung: 30 EUR. KBA TBNR [142103](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=278); [142104](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=278); [142106](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=278); [142107](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=278). BKat 159, 159.1, 159.2, 159.2.1. |

Exact conditional field prompts:

- Das Fahrzeug parkte verbotswidrig auf:*

## 6. Feuerwehrzufahrt

Selection order and labels follow the portal. The route IDs below are local catalog references, not Tatbestandsnummern.

| Route | Exact choice sequence | Obstruction controls | Incident times | Likely EUR (basic / obstruction) | Fine conditions / official reference |
|---|---|---|---|---|---|
| G06-R01 | Das Fahrzeug parkte vor oder in einer amtlich gekennzeichneten Feuerwehrzufahrt. | Rescue Ja/Nein; Ja → description | Start + end | 55 / 100 (rescue vehicle in action) | Der 100-EUR-Tatbestand verlangt ein Rettungsfahrzeug im Einsatz, nicht nur eine abstrakt versperrte Zufahrt. KBA TBNR [112216](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=102); [112612](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=102). BKat 53, 53.1. |

Exact conditional field prompts:

- Bitte wählen Sie aus:*
- Wurde ein Rettungsfahrzeug im Einsatz behindert?*

## 7. Taxi/Haltestellen/zweite Reihe

Selection order and labels follow the portal. The route IDs below are local catalog references, not Tatbestandsnummern.

| Route | Exact choice sequence | Obstruction controls | Incident times | Likely EUR (basic / obstruction) | Fine conditions / official reference |
|---|---|---|---|---|---|
| G07-R01 | Halten → auf einem Sonderparkplatz für Taxen. | Personal Ja/Nein; Ja → description | Single time | 20 / 35 | Die erhöhte Variante bezieht sich auf tatsächlich behinderten Taxenverkehr, nicht automatisch auf jede beliebige Behinderungsbeschreibung. KBA TBNR [141380](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=215); [141381](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=215). BKat 51, 51.1. |
| G07-R02 | Halten → auf einem Busfahrstreifen. | No obstruction input observed | Single time | 55 / 70 | KBA TBNR [141120](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=217); [141825](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=217). BKat 54.3, 54.3.1. |
| G07-R03 | Halten → in der zweiten Reihe. | No obstruction input observed | Single time | 55 / 70 | KBA TBNR [112460](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=111); [112661](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=111). BKat 51a, 51a.1. |
| G07-R04 | Parken → auf einem Sonderparkplatz für Taxen. | Personal Ja/Nein; Ja → description | Start + end | 25 / 40 | Länger als 1 Stunde, ohne zusätzliche Behinderung: 40 EUR. Länger als 1 Stunde, mit nachgewiesener Behinderung: 50 EUR. Erhöhte Variante: tatsächlich behinderter Taxenverkehr. KBA TBNR [141382](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=215); [141383](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=216); [141384](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=216); [141385](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=216). BKat 52, 52.1, 52.2, 52.2.1. |
| G07-R05 | Parken → im Bereich einer Haltestelle. | Personal Ja/Nein; Ja → description | Start + end | 55 / 70 | Länger als 3 Stunden, ohne zusätzliche Behinderung: 70 EUR. Länger als 3 Stunden, mit nachgewiesener Behinderung: 80 EUR. KBA TBNR [141402](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=217); [141818](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=217); [141821](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=217); [141822](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=217). BKat 54.4, 54.4.1, 54.4.4, 54.4.4.1. |
| G07-R06 | Parken → auf einem Busfahrstreifen. | Personal Ja/Nein; Ja → description | Start + end | 55 / 70 | Länger als 3 Stunden, ohne zusätzliche Behinderung: 70 EUR. Länger als 3 Stunden, mit nachgewiesener Behinderung: 80 EUR. KBA TBNR [141125](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=218); [141828](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=218); [141831](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=219); [141832](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=219). BKat 54.4, 54.4.1, 54.4.4, 54.4.4.1. |
| G07-R07 | Parken → in der zweiten Reihe. | Personal Ja/Nein; Ja → description | Start + end | 55 / 80 | Länger als 15 Minuten, ohne zusätzliche Behinderung: 85 EUR. Länger als 15 Minuten, mit nachgewiesener Behinderung: 90 EUR. KBA TBNR [112464](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=111); [112665](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=111); [112666](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=111); [112667](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=111). BKat 58, 58.1, 58.2, 58.2.1. |

Exact conditional field prompts:

- Es handelt es sich um:*
- Bitte wählen Sie aus:*
- Wurden Sie behindert?*

## 8. Bordsteinabsenkung/Grundstückszufahrten/Kreuzungen und Einmündungen

Selection order and labels follow the portal. The route IDs below are local catalog references, not Tatbestandsnummern.

| Route | Exact choice sequence | Obstruction controls | Incident times | Likely EUR (basic / obstruction) | Fine conditions / official reference |
|---|---|---|---|---|---|
| G08-R01 | im Bereich einer Bordsteinabsenkung. | Personal Ja/Nein; Ja → description | Start + end | 10 / 15 | Länger als 3 Stunden, ohne zusätzliche Behinderung: 20 EUR. Länger als 3 Stunden, mit nachgewiesener Behinderung: 30 EUR. KBA TBNR [112372](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=107); [112373](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=107); [112374](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=107); [112375](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=107). BKat 54, 54.1, 54.2, 54.2.1. |
| G08-R02 | im Bereich einer Grundstückszufahrt. | Personal Ja/Nein; Ja → description | Start + end | 10 / 15 | Länger als 3 Stunden, ohne zusätzliche Behinderung: 20 EUR. Länger als 3 Stunden, mit nachgewiesener Behinderung: 30 EUR. KBA TBNR [112292](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=105); [112293](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=105); [112294](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=105); [112295](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=105). BKat 54, 54.1, 54.2, 54.2.1. |
| G08-R03 | gegenüber der Grundstückszufahrt auf Straßen unter 5 Meter Breite. | Personal Ja/Nein; Ja → description | Start + end | 10 / 15 | Länger als 3 Stunden, ohne zusätzliche Behinderung: 20 EUR. Länger als 3 Stunden, mit nachgewiesener Behinderung: 30 EUR. § 12 Absatz 3 verlangt eine schmale Fahrbahn; die UI-Vorgabe „unter 5 Meter“ ersetzt keine Feststellung der örtlichen Verhältnisse. KBA TBNR [112302](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=105); [112303](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=105); [112304](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=105); [112305](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=105). BKat 54, 54.1, 54.2, 54.2.1. |
| G08-R04 | weniger als 5 Meter VOR der Kreuzung. | Personal Ja/Nein; Ja → description | Start + end | 10 / 15 | Länger als 3 Stunden, ohne zusätzliche Behinderung: 20 EUR. Länger als 3 Stunden, mit nachgewiesener Behinderung: 30 EUR. KBA TBNR [112262](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=103); [112263](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=103); [112264](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=103); [112265](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=103). BKat 54, 54.1, 54.2, 54.2.1. |
| G08-R05 | weniger als 5 Meter VOR einer Einmündung. | Personal Ja/Nein; Ja → description | Start + end | 10 / 15 | Länger als 3 Stunden, ohne zusätzliche Behinderung: 20 EUR. Länger als 3 Stunden, mit nachgewiesener Behinderung: 30 EUR. KBA TBNR [112262](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=103); [112263](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=103); [112264](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=103); [112265](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=103). BKat 54, 54.1, 54.2, 54.2.1. |
| G08-R06 | weniger als 5 Meter HINTER der Kreuzung. | Personal Ja/Nein; Ja → description | Start + end | 10 / 15 | Länger als 3 Stunden, ohne zusätzliche Behinderung: 20 EUR. Länger als 3 Stunden, mit nachgewiesener Behinderung: 30 EUR. KBA TBNR [112272](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=103); [112273](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=103); [112274](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=104); [112275](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=104). BKat 54, 54.1, 54.2, 54.2.1. |
| G08-R07 | weniger als 5 Meter HINTER der Einmündung. | Personal Ja/Nein; Ja → description | Start + end | 10 / 15 | Länger als 3 Stunden, ohne zusätzliche Behinderung: 20 EUR. Länger als 3 Stunden, mit nachgewiesener Behinderung: 30 EUR. KBA TBNR [112272](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=103); [112273](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=103); [112274](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=104); [112275](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=104). BKat 54, 54.1, 54.2, 54.2.1. |

Exact conditional field prompts:

- Das Fahrzeugt parkte:*
- Wurden Sie behindert?*

## Portal requirements and UI limitations

Scope and reporting requirements: [Frankfurt service page](https://frankfurt.de/service-und-rathaus/verwaltung/aemter-und-institutionen/ordnungsamt/bussgeldstelle/verkehrsordnungswidrigkeiten-im-ruhenden-verkehr) and [official guidance leaflet](https://frankfurt.de/-/media/frankfurtde/service-und-rathaus/verwaltung/aemter-und-institutionen/ordnungsamt/bussgeldstelle/pdf/anzeige-verkehrsordnungswidrigkeiten.ashx). Recheck the live form when its behaviour differs.

- **Scope:** stationary traffic offences in Frankfurt am Main. Use a separate report per plate and one accusation per report. Moving traffic offences are excluded.
- **Reporter:** named witness with a serviceable address; manual entry or BundID. Voluntary email/phone enter the file and may be disclosed on file inspection. Prosecution is discretionary; routine case-progress information is not supplied.
- **Evidence:** both plate and alleged violation must be shown. Apply the skill's default black-bar pedestrian redaction and conceal unrelated readable plates. Upload requirements and time schemas are listed under “Incident schemas and shared requirements” above. Convert HEIC copies to an accepted format while preserving originals.
- **Dates:** no earliest permitted incident date is established. The phrase “tagesaktuelles Beweisfoto” does not establish a filing deadline. Check applicable statutory limitation for older cases as directed in SKILL.md. If date entry looks filled but fails validation, use keyboard input, press Tab and verify the committed value.
- **Schutzstreifen (Zeichen 340):** offered under Radweg/Radfahrstreifen → Halten only. Use that exact route for a supported Schutzstreifen case, including a longer stay, and preserve the actual full observed span in the chat review and any genuine comments field. Do not invent another allegation to obtain an interval field.
- **Fußgängerfurt:** its obstruction description is mandatory without a separate Ja/Nein radio. The final review can display “Wurden Sie behindert? Ja” automatically. Inspect and disclose the actual consequential answer; entering a description is not evidence of personal obstruction.
- **Comments:** no general comments field is available in the catalogued incident schemas. Do not invent one or place unrelated narrative in another field.
- **Validation:** obstruction descriptions are limited to 1000 characters. Use a plain hyphen instead of an en dash if validation rejects it, and resolve the actual message before advancing.
- **Session:** the portal displays a 60-minute inactivity countdown. Check what remains after a timeout.
- **Submission and receipt:** Absenden transmits the report. Save the downloadable summary PDF and a receipt screenshot before restarting; the portal does not email the summary. A submission receipt does not guarantee a sanction.
- **Alternative channels:** the city offers a paper form by post. Verify the current official guidance before recommending email or another service; do not promise acceptance of arbitrary email, weg.li or bulk exports.

## Additional severity variants and vehicle-dependent checks

These are additional official variants, not automatic consequences of a portal selection. Use them only when their own facts are supported. Do not apply several alternatives cumulatively.

| Tariff family (route references) | Additional facts | Likely EUR | Official reference |
|---|---|---|---|
| cycle-halt (G01-R01) | Mit nachgewiesener konkreter Gefährdung | 80 | [TBNR 141572](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=222) |
| cycle-halt (G01-R01) | Mit Unfall/Sachbeschädigung gemäß konkretem Tatbestand | 100 | [TBNR 141573](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=222) |
| shared-halt (G01-R02, G01-R03) | Mit nachgewiesener konkreter Gefährdung | 70 | [TBNR 141592](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=223) |
| shared-halt (G01-R02, G01-R03) | Mit Unfall/Sachbeschädigung gemäß konkretem Tatbestand | 90 | [TBNR 141593](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=223) |
| cycle-street-halt (G01-R04) | Mit nachgewiesener konkreter Gefährdung | 80 | [TBNR 141522](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=226) |
| cycle-street-halt (G01-R04) | Mit Unfall/Sachbeschädigung gemäß konkretem Tatbestand | 100 | [TBNR 141523](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=226) |
| cycle-park (G01-R06, G01-R10) | Mit nachgewiesener konkreter Gefährdung | 80 | [TBNR 141778](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=222) |
| cycle-park (G01-R06, G01-R10) | Mit Unfall/Sachbeschädigung gemäß konkretem Tatbestand | 100 | [TBNR 141779](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=222) |
| shared-park (G01-R07, G01-R08, G01-R11, G01-R12, G02-R06, G02-R07) | Mit nachgewiesener konkreter Gefährdung | 80 | [TBNR 141798](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=224) |
| shared-park (G01-R07, G01-R08, G01-R11, G01-R12, G02-R06, G02-R07) | Mit Unfall/Sachbeschädigung gemäß konkretem Tatbestand | 100 | [TBNR 141799](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=224) |
| cycle-street-park (G01-R09, G01-R13) | Mit nachgewiesener konkreter Gefährdung | 80 | [TBNR 141528](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=226) |
| cycle-street-park (G01-R09, G01-R13) | Mit Unfall/Sachbeschädigung gemäß konkretem Tatbestand | 100 | [TBNR 141529](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=227) |
| pavement-park (G02-R03, G02-R12) | Mit nachgewiesener konkreter Gefährdung | 80 | [TBNR 112658](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=110) |
| pavement-park (G02-R03, G02-R12) | Mit Unfall/Sachbeschädigung gemäß konkretem Tatbestand | 100 | [TBNR 112659](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=110) |
| pavement-halt (G02-R01) | Mit nachgewiesener konkreter Gefährdung | 70 | [TBNR 112552](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=109) |
| pavement-halt (G02-R01) | Mit Unfall/Sachbeschädigung gemäß konkretem Tatbestand | 90 | [TBNR 112553](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=109) |
| bus-halt (G07-R02) | Mit nachgewiesener konkreter Gefährdung | 80 | [TBNR 141826](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=218) |
| bus-halt (G07-R02) | Mit Unfall/Sachbeschädigung gemäß konkretem Tatbestand | 100 | [TBNR 141827](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=218) |
| stop-park (G07-R05) | Mit nachgewiesener konkreter Gefährdung | 80 | [TBNR 141819](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=217) |
| stop-park (G07-R05) | Mit Unfall/Sachbeschädigung gemäß konkretem Tatbestand | 100 | [TBNR 141820](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=217) |
| bus-park (G07-R06) | Mit nachgewiesener konkreter Gefährdung | 80 | [TBNR 141829](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=218) |
| bus-park (G07-R06) | Mit Unfall/Sachbeschädigung gemäß konkretem Tatbestand | 100 | [TBNR 141830](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=218) |
| second-halt (G07-R03) | Mit nachgewiesener konkreter Gefährdung | 80 | [TBNR 112662](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=111) |
| second-halt (G07-R03) | Mit Unfall/Sachbeschädigung gemäß konkretem Tatbestand | 100 | [TBNR 112663](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=111) |
| second-park (G07-R07) | Mit nachgewiesener konkreter Gefährdung | 90 | [TBNR 112668](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=111) |
| second-park (G07-R07) | Mit Unfall/Sachbeschädigung gemäß konkretem Tatbestand | 110 | [TBNR 112669](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=112) |
| schutz (G01-R05) | Mit nachgewiesener konkreter Gefährdung | 80 | [TBNR 142672](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=276) |
| schutz (G01-R05) | Mit Unfall gemäß konkretem Tatbestand | 100 | [TBNR 142673](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=276) |

For a signed closed pedestrian/shared area interpreted as an unauthorised driving/stopping offence, check these vehicle categories separately. They are **not** replacements for the 55-EUR parking family merely because the vehicle is larger.

| Case | Likely EUR | Official reference |
|---|---|---|
| Sonstiges Kfz/PKW: unzulässiges Befahren/Halten im gesperrten Bereich | 50 | [TBNR 141166](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=224) |
| Kfz bis 3,5 t mit Anhänger oder Kraftomnibus: unzulässiges Befahren/Halten | 55 | [TBNR 141159](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=224) |
| Kfz über 3,5 t, ausgenommen PKW/KOM: unzulässiges Befahren/Halten | 100 | [TBNR 141737](https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/bkat_owi_22_08_2024.pdf?__blob=publicationFile&v=2#page=224) |
