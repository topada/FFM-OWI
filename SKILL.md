---
name: frankfurt-owi-anzeige
description: Extract incident times and location from user-supplied traffic violation photos, assess the likely German stationary traffic offence, and use Computer Use to fill Frankfurt's ekom21 Anzeige einer Verkehrsordnungswidrigkeit form with the user's reporter details.
metadata:
  author: "info@topada.de"
---

# Frankfurt OWi Anzeige

Author contact: info@topada.de. This is attribution only; never use it as a reporter's email unless supplied in their own profile.

Turn photos of a suspected stationary traffic violation into an evidence-based German report and fill the Frankfurt portal using **Computer Use**:
https://portal-civ.ekom21.de/civ.public/start.html?oe=00.00.PA.FFOrdA&mode=cc&cc_key=AnzeigeOwi

The requested outcome is a completed form ready for user review. Submitting an accusation is a separate action; do not infer submission authorization from a request to fill the form.

## User language and German legal authority

Run the conversation in the user's preferred language. Follow an explicit language preference; otherwise use the language the user is using (German stays German, English stays English), and follow later requests to switch. Do not infer a language from their name, address, photo location or the German portal. Apply this to progress updates, profile onboarding, questions, offence choices, fine explanations, reviews, confirmation buttons and completion messages. German wording elsewhere in this skill is a portal label or example, not a requirement to speak German to an English-speaking user.

German law remains authoritative regardless of conversation language. Cite the applicable German statute with its exact title/abbreviation and precise provision (paragraph, subsection and relevant sentence/number or sign where material), and link the official German text applicable to the incident. Keep original legal terms and exact German portal choices alongside a plain-language explanation in the user's language when needed to identify the selected allegation. Translations are explanatory; do not present them as legally binding texts or replace the German source with another country's law. Distinguish binding legislation from the KBA catalogue and secondary explanations.

Enter factual narratives and other free-text submissions to the German authority in German. Show the exact German text being submitted and, when the conversation is in another language, explain its meaning in that language. Preserve exact German declarations and consequential form answers in the review, accompanied by a translation as needed. Localize selectable action labels (for example, English “Confirm — submit report” or German “Bestätigen — Anzeige absenden”) without changing what confirmation authorizes. Language preference does not change the evidence requirements or submission-approval workflow.

## Inputs and evidence

Accept incident images and, where available, their original files. Request original files only if missing metadata matters. Do not infer reporter identity from the incident or search unrelated accounts for personal details. Load the local reporter profile described below and reuse supplied details from the current conversation; current user corrections take precedence. Ask for material missing reporter information in one concise request.

## Local reporter profile and sharing

Read the reporter profile from `$CODEX_HOME/profiles/frankfurt-owi-anzeige.json`, falling back to `~/.codex/profiles/frankfurt-owi-anzeige.json` when CODEX_HOME is unset. Resolve this on the current user's machine; never hard-code the creator's home directory. The profile lives **outside the skill folder**, so sharing the skill does not include its owner's details.

If the profile is missing, ask **once for all reporter data together in one form**. Do not ask field by field or require the user to edit JSON manually. Use a supported multi-field form if available; otherwise present the following single copy-and-fill form in one chat message or one free-text input request. Prefill only values already supplied by this user. Explain that completing it saves a reusable local profile outside the shareable skill and that optional fields may be left blank. Mention once that the reporter is a named witness and voluntary contact details may be disclosed on file inspection.

```text
Lokales Anzeigeprofil (mit * markierte Felder sind Pflichtfelder)
Anrede*:
Nachname*:
Vorname*:
Postleitzahl*:
Ort*:
Straße*:
Hausnummer*:
Adresszusatz (optional):
Akademischer Grad (optional):
Namenszusatz (optional):
E-Mail (optional):
Telefon (optional):
```

Wait for the user's completed form before saving or transmitting reporter data. Use [assets/local-profile.example.json](assets/local-profile.example.json) as the schema, map the supplied answers, create the external parent directory if needed, and save the profile. Use UTF-8 and owner-only file permissions (0600), with a private parent directory (0700) where supported. Do not save a blank template as a completed profile. If required answers are missing or ambiguous, request only those corrections together; do not repeat the full onboarding form. Optional empty strings are deliberately unspecified and must not trigger repeat questions. On future runs load the saved profile without asking the onboarding questions again. Never overwrite an existing profile without the user's instruction. Saving a profile does not itself authorize submitting a report or transmitting its data to a website.

Optional local `reporting_preferences.assume_continuous_presence` is a boolean witness-reporting preference, not personal identity data. Set it true only when the profile owner explicitly says their same-vehicle/same-location photo sequences represent a continuous stay. Keep the shared template false so another user does not inherit that factual assertion.

JSON field mapping: `anrede` → Anrede, `name` → surname/Name, `vorname` → Vorname, `postleitzahl` → Postleitzahl, `ort` → Ort, `strasse` → Straße/Postfach, `hausnummer` → Nr.; optional `adresszusatz`, `akademischer_grad`, `namenszusatz`, `email`, `telefon` map to corresponding live fields. Store postcodes and house numbers as strings, retaining leading zeroes, suffixes and German characters. Empty values must never be inserted as invented data.

Keep actual reporter values solely in the external local profile. Do not copy them into SKILL.md, templates, screenshots for distribution, or a shared archive. To share this skill, package SKILL.md, agents/openai.yaml, the blank assets/local-profile.example.json, references/form-catalog.md, and references/form-catalog.json. Exclude private profiles, raw browser captures, incident evidence and case outputs. The recipient installs the skill and completes the one-time profile form; the skill saves their own external profile without changes to skill instructions. Do not include the profiles directory in any export.

## Image evidence

Inspect every relevant image. Group by vehicle, location and incident before extracting first/last times; do not merge separate offences. For each incident establish:

- Earliest and latest supported capture date/time, source image, source type (original EXIF, visible timestamp, user statement) and any uncertainty. If original files are available, read metadata with an available read-only metadata tool. File creation/modification times and filenames alone are not reliable capture times. Preserve source time zones; convert to Europe/Berlin only when the source offset is known. Flag conflicts instead of silently picking one.
- Location: city, street, nearest number/intersection, side and any visible signs or markings. Distinguish GPS metadata and readable signage from visual inference; ask for the missing address rather than guess it. Do not upload incident images to external image-search services without authorization.
- Registration plate (retain uncertain characters as uncertain), observable vehicle details, position, signs/markings, and what the photos show about obstruction. Do not identify people in the photos or assume the keeper was the driver.

A single photo supports one observation time, not an invented interval. Multiple photos support the span between observations. Read `reporting_preferences.assume_continuous_presence` from the local profile: when true, the user has expressly stated that their photos of the same vehicle at the same location represent one continuous stay from the first capture time to the last. Use that interval without asking them to confirm continuity again, unless the photos or current account conflict with it. Attribute continuity to this standing user statement; timestamps establish the endpoints. When the preference is absent or false and continuity materially affects the allegation, ask once. A continuous stop over three minutes supports Parken under current § 12(2) StVO; still verify the applicable provision. Keep precise extracted times even if the form accepts only minutes. Do not claim the driver left, that a permit was absent, measured distances, actual obstruction or danger unless supported by the images or the user's observations. Treat the observer's account separately from image evidence.

Present a compact incident table and list only material missing facts. A draft may proceed while uncertainties are labelled; do not enter uncertain mandatory facts as established facts.

### Default pedestrian redaction

Before uploading evidence, redact unrelated pedestrians by default with solid, fully opaque black bars or rectangles in local copies. This is the requested default preparation step; do not ask the user to choose between cropping and blacking out each time. Use a deterministic, non-generative local image tool to overlay the bars; do not reconstruct, retouch or generate incident evidence. Cover enough of each pedestrian to prevent recognition, rather than only placing a narrow bar across the eyes. Preserve the originals unchanged and extract capture timestamps/GPS from those originals before conversion or redaction.

Keep the reported vehicle, its registration plate, its position, relevant signs/markings and location evidence visible. Also conceal unrelated readable registration plates as required by the portal. Inspect every final upload copy to confirm that the black bars fully cover the intended people and do not hide material evidence. Use clearly named redacted copies in an accepted portal format and disclose the redaction in the final attachment review. If a person overlaps decisive evidence so that blacking them out would obscure the allegation, use another adequate photo or ask for the minimum needed correction. Keep original metadata and any conversion/redaction record locally; do not invent capture metadata in the edited image.

## Tentative legal classification

Browse current official German sources for the specific proposed offence. Start with the relevant StVO provision and use the official KBA Bundeseinheitlicher Tatbestandskatalog when a catalogue description or number is needed:

- StVO: https://www.gesetze-im-internet.de/stvo_2013/
- Halten/Parken: https://www.gesetze-im-internet.de/stvo_2013/__12.html
- KBA catalogue: https://www.kba.de/DE/Themen/ZentraleRegister/FAER/BT_KAT_OWI/btkat_node.html

Check the applicable signs, markings and exceptions as needed. Explain the likely offence briefly in the user's preferred language, retaining the relevant German legal term and exact applicable provision, with a direct official-source link and which visible facts support it. Mark the classification as tentative; the authority decides. Do not invent a Tatbestandsnummer or fine, assume a duration threshold, or add aggravating elements without evidence. If several offences plausibly fit, use the selectable-offence workflow below and ask only for a decisive fact that the available evidence cannot establish. A photo may be insufficient to establish any offence.

### Photo assessment and selectable offences

Try to identify the offence from all supplied photos, their timestamps, signs, markings and vehicle placement, incorporating the user's account. If the user already suggests an offence, take that as the starting lead: check that route first, include it when plausible and mark it “Von Ihnen vorgeschlagen”. Do not silently substitute a different allegation. If that suggestion conflicts with the visible evidence, legal elements or actual portal choices, explain the specific conflict and offer the nearest supported alternative.

Before selecting the offence in the portal, present a **selectable shortlist of plausible offences**, using the available clickable user-input tool when possible. Sort the options by **highest to lowest likely EUR fine** for the facts actually supported by this case. This is presentation order, not a recommendation to choose the largest fine. Do not show the entire 72-route catalog, duplicate the same conduct as separate duration variants, or manufacture obstruction/danger to increase an option's amount.

Each option should identify the offence plainly in the user's preferred language, with the corresponding exact German portal offence label where needed, the likely amount, a brief evidence/confidence cue, and its catalog route. Clearly mark the **most obvious / best-supported match** regardless of its position in the price-sorted list; it can be lower in the list. If confidence is low, always include and explain the most obvious plausible offence as a tentative choice with the decisive uncertainty, instead of only asking the user to classify the photos. If the photos establish no plausible offence at all, state that and request the minimal missing evidence rather than invent one to populate a list.

Use only aggravating variants supported by photos or the user's observations. For an unresolved fine range, display the range and sort by its supported lower bound (then upper bound, then evidence strength), so a hypothetical high maximum cannot push a weak allegation to the top. Place genuinely unpriced/uncertain candidates after priced ones and explain what is missing. Add a final “Keine davon / Sachverhalt korrigieren” choice where the input tool permits it. The user's prior proposed offence and the most obvious match remain explicitly labelled even when they differ.

Wait for an explicit submitted selection before populating the offence controls. A preselected option is not confirmation. If the user has already explicitly chosen an offence for this case, preserve that choice: show it as selected in the summary/list and do not require the same choice again. Continue independent metadata/profile preparation while waiting when useful. Selecting an offence does not authorize submission; retain the separate full-form review and confirm-to-submit step.

### Likely fine information

For every case, use the selected route's fine estimates in [references/form-catalog.md](references/form-catalog.md), backed by `fine_estimate` and `fine_sources` in [references/form-catalog.json](references/form-catalog.json). The catalog provides KBA TBNRs, applicable BKat references, source links and verification dates. A portal-label-to-TBNR match is an assessment: the portal does not expose its internal TBNR.

Present the likely standard monetary amount separately from the actual form fields, with the decisive facts, direct official source, and verification date. Example format: “Voraussichtliches Verwarnungs-/Bußgeld: … EUR bei …, ohne mögliche Gebühren/Auslagen; amtlicher Regelsatz …, Entscheidung durch die Behörde.” Recheck current official sources and the law applicable on the incident date before presenting it as current. If a fact or mapping remains uncertain, give conditional amounts or explain the uncertainty rather than a false single figure.

Apply duration thresholds to the actual interval, including 15-minute or 3-hour increases not separately offered by the UI. A route labelled over one hour already requires that duration variant. Obstruction, concrete danger, accident and an emergency vehicle actually in action are distinct conditions; a saved phrase or a selected radio is not proof. The Fußgängerfurt entry 101048 requires actual obstruction. Vehicle class, weight, applicable supplementary signs, permission and exceptions can change whether the offence applies at all. Do not add alternatives together, imply a guaranteed sanction or choose an allegation to maximize the fine. Do not enter the estimate into an unrelated portal field.

Draft a neutral German Sachverhalt: precise location, observed times, vehicle/plate, observable positioning, applicable signs and any directly observed impact. Separate observation from inference. Avoid speculation about intent or the driver's identity. Give the user a reviewable draft before consequential entry where authorization is still needed.

## Older cases

For older incidents, check the limitation period and the law applicable on the incident date using [§ 26 StVG](https://www.gesetze-im-internet.de/stvg/__26.html), [§ 31 OWiG](https://www.gesetze-im-internet.de/owig_1968/__31.html) and [§ 33 OWiG](https://www.gesetze-im-internet.de/owig_1968/__33.html), including any relevant amendments or interruptions. Do not invent a three-month portal cutoff, auto-reject by photo age alone, assume a private report interrupts limitation, or alter the incident date to pass validation. Explain any actual portal rejection accurately.

## Computer Use form completion

Before choosing a vehicle value or offence route, read the relevant section of [references/form-catalog.md](references/form-catalog.md). It lists every observed vehicle type, registration country, brand and all 72 offence routes across eight groups, including conditional obstruction controls and the next incident page's time schema. For precise programmatic lookup, use [references/form-catalog.json](references/form-catalog.json); its Gxx-Rxx IDs are local references, not official Tatbestandsnummern. Search or read only the relevant group instead of loading the full JSON unnecessarily. The catalog also contains portal requirements and UI limitations; recheck live controls when the form differs. A catalog entry does not by itself establish the facts or legal elements of an offence.

Use the available Computer Use surface (cua_repl) for portal interaction, as requested. Read its tool documentation at first use. Discover current controls from live accessibility/DOM state and use labels; numeric indices, generated widget IDs and coordinates are not stable. Refresh state after actions before deciding the next action. Do not substitute direct HTTP submissions or hidden form APIs.

Use the following workflow, checking the live form each run:

- The portal belongs to Frankfurt am Main and accepts stationary traffic violations, not moving traffic offences. Confirm the incident falls in its jurisdiction; do not force another municipality or category into this form.
- Start page → Weiter → Datenerfassung – anzeigende Person. Choose **Daten manuell eingeben** for manual completion, then Weiter. Use BundID only if the user chooses that route; hand over authentication when necessary.
- Manual reporter fields include required **Anrede**, **Name** (surname), **Vorname**, **Postleitzahl**, **Ort**, **Straße/Postfach**, **Nr.**; optional fields observed include academic title, name/address suffix and telephone. Read later screens for additional fields such as email. Do not invent values or treat these observations as an exhaustive field list.
- The portal states the reporter is a named witness and voluntary contact details enter the file and may be disclosed on file inspection. Explain this once before supplying those voluntary details, and let the user choose whether to include them.
- The portal requires evidentiary photos showing the registration plate and violation. It instructs that unrelated people and other plates must not be recognizable. Apply **Default pedestrian redaction** above: prepare and inspect local copies with opaque black bars before upload, preserving the originals and material evidence; do not upload an unsuitable original.

Reuse details already authorized for this specific portal without repeat questions. Before typing private reporter data, precise incident location or uploading personal evidence, ensure authorization covers those specific data/files and this destination. If it does not, show the prepared data/draft and ask one specific bundled confirmation immediately before entry/upload. Typing can itself transmit data. Follow the active Computer Use confirmation rules for declarations or other consequential controls.

### Vehicle details

Complete the vehicle fields through Computer Use using the incident photos and the live form options:

- **Fahrzeugart (PKW/LKW/…):** use PKW by default, as the user requested. Choose another available type only when the image strongly suggests it (for example, an unmistakable heavy goods vehicle, motorcycle or bus), or when the user provides a correction. Do not ask for the formal registration class merely because a photographed van could have different registrations. Do not infer a specific weight threshold from appearance alone.
- **Kennzeichen Land:** check for a readable country identifier or other clear registration evidence. Deutschland is the user's expected usual case, not an unconditional default. Select Deutschland when supported; do not infer the country just from the incident being in Germany. If the country is required and unclear, ask.
- **Kennzeichen:** transcribe only the actual readable plate characters. For an ordinary German plate, use the user's requested presentation `ABC-DD 9999`: a hyphen between the registration-area code and following letters, then a space before the digits. This is a formatting example, not fixed segment lengths or a value to enter. Preserve the actual letters, number of digits and any visible suffix; do not pad digits or invent characters. Retain special/foreign plate formats where applicable and follow the live form's accepted format. Resolve ambiguous characters before entering the plate as certain.
- **Fahrzeugmarke, Modell, Farbe:** populate each field only when that individual detail can really be extracted from the photos. A readable badge may support a brand while leaving the model unknown. Do not infer a model from a vague resemblance or a colour from lighting that makes it unreliable. Leave unsupported optional fields blank (or choose an explicit unknown option); ask only if the portal requires a value. Never substitute a guessed model, brand or colour to get past validation.

Verify the selected vehicle type and registration country, entered plate and any supported descriptive details on the review screen.

### Selecting the offence group

Use the catalogue to map the user's selected, evidence-supported offence to the live group and exact route. Read the resulting conditional controls and verify duration, obstruction and danger qualifiers. If categories overlap, choose one supported allegation rather than duplicate reports. Ask only for a decisive missing fact; an option-list screenshot is not incident evidence.

Schutzstreifen routing: the portal offers **Radweg/Radfahrstreifen → Halten → verbotswidrig auf einem Schutzstreifen für den Radverkehr (Zeichen 340)** but omits Schutzstreifen from Parken. Use that exact offered route for a supported Schutzstreifen case, including a longer continuous stay. Preserve its actual full first/last timestamp span in a genuine comments field if one is available, and in the chat review. Do not claim that a longer stay was under three minutes or invent an alternative offence. This route provides only a single time and no general comments field; disclose that limitation. Do not assume a rationale about fine amounts without checking an official source.

Distinguish a signal-controlled **Fußgängerfurt** from a zebra **Fußgängerüberweg**. When the user's observations or photos establish parking on the marked pedestrian crossing at traffic lights, use **Gehweg/Fußgängerüberweg/Fußgängerfurt → Parken → auf einer Fußgängerfurt**. Merely being near traffic lights is insufficient. Do not use this category as a generic substitute for an unavailable Schutzstreifen offence; its own facts must be supported.

When an obstruction description is requested, read `reporting_preferences.obstruction_text` from the local profile, if present. Use that wording when consistent with the reported effect. The profile owner's preferred default can be “Fahrzeug muss umfahren werden”. A saved phrase is not evidence that a person was actually obstructed: do not automatically select Ja to a personal-obstruction question or add danger solely to reveal the text field. Preserve user-supplied factual wording and ask only if an essential assertion is unclear.

Verify the selected group and precise offence in the final review.

Continue through available incident, vehicle, offence and attachment fields using the live UI. Choose only options supported by the evidence and current official sources; if the correct offence is missing, explain the portal limitation instead of selecting a misleading substitute. Populate all applicable supplied reporter details, leaving genuinely optional unknown values blank. Resolve required unknowns with the user rather than fabricate data. Do not tick witness statements or attestations about facts the user has not supplied.

Verify entered values, accepted address autocomplete choices, dates/times, plate, offence, narrative, attachment names/count and validation errors. Stop at a reviewable completed form before final submission. Save and display a review screenshot using the Computer Use documentation; keep the tab available when handing control to the user. State clearly what is complete and anything still missing. Never claim completion from attempted clicks alone.

At the final review page, gather the complete actual form data (expand any collapsed sections). Present it directly in chat for confirmation: reporter identity/address/contact details, offence group and precise selection, vehicle fields, all obstruction answers and descriptions, location, date, start/end times, every uploaded filename and category, further witnesses or other populated fields, and the declaration status and its substantive witness obligations. Preserve the wording of consequential answers such as “Wurden Sie behindert? Ja”; do not silently turn them into generic obstruction claims. Flag any discrepancy before asking to submit. Include a current review screenshot and keep the live tab available.

Offer a clickable confirmation in chat using the available user-input tool: “Confirm — submit report” and “Keep as draft”. Its question must identify submission of the displayed report, reporter details, allegations, declaration and attached photos to Frankfurt's Ordnungsamt. If clickable input is unavailable, ask the user to reply **confirm**. Wait for an explicit submitted confirmation (the preselected choice is not approval); an instruction explaining this workflow, approval of a declaration alone, or a prior confirmation for a different draft does not authorize submission. Once the user confirms the displayed report, recheck the live review for material changes, apply any still-required action-time confirmation for declarations, then click Absenden once and verify the receipt/reference. Do not ask for the same submission approval again if the displayed data are unchanged. If the result is ambiguous, check for a receipt before retrying to avoid duplicate reports. A session timeout requires checking which data remain rather than assuming a saved draft. If the report materially changes after confirmation, present the updated data for renewed confirmation.
