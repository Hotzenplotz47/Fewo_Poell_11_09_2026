# Ferienwohnung Pöll · Landhaus Wackerl

Zwei Ferienunterkünfte in Mittenwald, Oberbayern.
Reines HTML und CSS. Keine Datenbank, kein Framework, kein JavaScript.

## Dateien

    index.html                 Startseite Ferienwohnung Pöll
    landhaus-wackerl.html      Startseite Landhaus Wackerl
    impressum.html             Impressum Pöll
    datenschutz.html           Datenschutz Pöll
    impressum-wackerl.html     Impressum Wackerl
    datenschutz-wackerl.html   Datenschutz Wackerl
    404.html                   Fehlerseite
    style.css                  gemeinsames Stylesheet
    robots.txt                 Steuerung für Suchmaschinen
    sitemap.xml                Seitenverzeichnis
    favicon.svg                Signet Pöll
    favicon-wackerl.svg        Signet Wackerl
    apple-touch-icon*.png      Symbol für den iOS-Startbildschirm
    vorschau-*.jpg             Vorschaubild beim Teilen von Links
    bilder/                    33 Fotos
    schriften/                 5 Schriftdateien, lokal eingebunden

## Gestaltung ändern

Alle Farben, Schriften und Abstände stehen als benannte Werte im
`:root`-Block ganz oben in `style.css` – 28 Stück. Nur dort werden Werte
geändert. Im übrigen Stylesheet steht kein einziger Farbwert, geprüft.

Beide Häuser teilen eine Gestaltung und unterscheiden sich nur in der
Akzentfarbe. Gesteuert über `data-haus` im `<html>`-Tag: `poell` ergibt
Tannengrün, `wackerl` Lüftlmalerei-Rot.

## Vor dem Livegang abarbeiten

1. Impressum und Datenschutzerklärung ausfüllen. Beide Seiten enthalten
   gelb markierte Lücken und einen Hinweiskasten, der danach gelöscht wird.
   Die bestehenden Texte liegen im alten TYPO3 auf dem All-inkl-Server.
2. In allen sieben HTML-Dateien die Zeile
   `<meta name="robots" content="noindex, nofollow">` entfernen.
3. In `robots.txt` die Sperre aufheben (Anleitung steht in der Datei).
4. Auf der echten Domain heißen die Rechtstexte `impressum.html` und
   `datenschutz.html`. Die Wackerl-Dateien entsprechend umbenennen und die
   Verweise im Fußbereich anpassen.
5. HTTPS im KAS aktivieren und Weiterleitung von http auf https einrichten.
6. Prüfen, ob der Tarif "all-inkl Privat" für gewerbliche Vermietung
   zulässig ist, und den Vertrag zur Auftragsverarbeitung anfordern.

## Herkunft der Texte

Sämtliche Texte stammen wörtlich von der alten Website und aus den
Gastgeberprofilen auf alpenwelt-karwendel.de. Korrigiert wurden ausschließlich
Rechtschreib- und Grammatikfehler:

- "straßenabgewande" → "straßenabgewandte"
- "Ferienwohung" → "Ferienwohnung"
- "Privatssphäre" → "Privatsphäre"
- "Gesseligkeit" → "Geselligkeit"
- "Paterre" → "Parterre"
- "mit 47m² ist und separates Schlafzimmer" → "mit 47 m² hat ein separates Schlafzimmer"

## Was bereits erledigt ist

- Schriften liegen lokal, keine Verbindung zu Google Fonts
- keine Cookies, kein Tracking, kein JavaScript, keine externen Aufrufe
- alle Farbkontraste erfüllen WCAG AA
- alle Bilder mit Alternativtext, Sprunglink zum Inhalt vorhanden
- Vorschaubilder und Beschreibungen für geteilte Links
- strukturierte Daten für Suchmaschinen
- Fehlerseite, Signet, Symbol für den Startbildschirm

## Hosting

Test: GitHub Pages.
Livebetrieb: All-inkl, Vertrag läuft auf die Inhaberin.
GitHub Pages eignet sich nicht für den Dauerbetrieb, weil kein Vertrag zur
Auftragsverarbeitung besteht und IP-Adressen in die USA übertragen werden.
