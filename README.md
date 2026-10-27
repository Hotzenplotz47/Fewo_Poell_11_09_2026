# Ferienwohnung Pöll · Landhaus Wackerl

Zwei Ferienunterkünfte in Mittenwald, Oberbayern.
Reines HTML und CSS. Keine Datenbank, kein Framework, kein JavaScript.

## Dateien

Zwei Domains, zwei Ordner. Jeder Ordner ist vollständig und wird so, wie
er ist, in das Verzeichnis seiner Domain bei All-inkl hochgeladen.

    poell/      -> www.ferienwohnung-poell.de
    wackerl/    -> www.landhaus-wackerl.de
    index.html  nur Testübersicht für GitHub Pages, nicht hochladen

Inhalt jedes Ordners:

    index.html          Startseite
    impressum.html      Impressum
    datenschutz.html    Datenschutzerklärung
    404.html            Fehlerseite
    .htaccess           Fehlerseite, Weiterleitungen, Zwischenspeicher
    style.css           Stylesheet (in beiden Ordnern identisch)
    robots.txt          Steuerung für Suchmaschinen
    sitemap.xml         Seitenverzeichnis
    favicon.svg         Signet
    apple-touch-icon.png  Symbol für den iOS-Startbildschirm
    vorschau-*.jpg      Vorschaubild beim Teilen von Links
    bilder/             nur die Fotos, die dieses Haus verwendet
    schriften/          5 Schriftdateien, lokal eingebunden

`style.css` und `schriften/` liegen absichtlich doppelt vor. Wer das
Stylesheet ändert, kopiert es danach in den anderen Ordner und zählt die
Versionsnummer `?v=` in allen HTML-Dateien beider Ordner hoch.

Die Knöpfe zum jeweils anderen Haus verweisen auf die volle Domain.

## Gestaltung ändern

Alle Farben, Schriften und Abstände stehen als benannte Werte im
`:root`-Block ganz oben in `style.css` – 28 Stück. Nur dort werden Werte
geändert. Im übrigen Stylesheet steht kein einziger Farbwert, geprüft.

Beide Häuser teilen eine Gestaltung und unterscheiden sich nur in der
Akzentfarbe. Gesteuert über `data-haus` im `<html>`-Tag: `poell` ergibt
Tannengrün, `wackerl` Lüftlmalerei-Rot.

## Vor dem Livegang abarbeiten

1. ~~Impressum und Datenschutzerklärung ausfüllen~~ – erledigt, auf Basis
   der alten TYPO3-Texte, an den heutigen Stand angepasst. Keine
   USt-IdNr. eingetragen (die alte Seite hatte keine) – falls doch eine
   existiert, im Impressum ergänzen.
2. Prüfen, ob der Tarif "all-inkl Privat" für gewerbliche Vermietung
   zulässig ist, und den Vertrag zur Auftragsverarbeitung im KAS
   abschließen. Die Datenschutzerklärung setzt ihn bereits voraus.
3. ~~Altes TYPO3 sichern~~ – Datenbank exportiert, Dateien per FTP noch
   offen. Die Sicherung gehört nicht in dieses Repository.
4. Im KAS jeder Domain ihr eigenes Verzeichnis zuweisen und das
   SSL-Zertifikat (Let's Encrypt) für beide Domains einschalten.
5. In jeder `.htaccess` die drei auskommentierten Zeilen der
   https-Weiterleitung aktivieren (# entfernen).
6. ~~Suchmaschinen-Sperre aufheben~~ – erledigt: `robots.txt` freigegeben,
   `noindex` entfernt (bleibt nur auf den Fehlerseiten).
7. Ordnerinhalt per FTP hochladen, auch die versteckte Datei `.htaccess`.
   Danach prüfen: http leitet auf https um, ohne www leitet auf www um,
   eine unbekannte Adresse zeigt die Fehlerseite, alle Links im
   Fußbereich funktionieren.
8. Beide Domains in der Google Search Console anmelden und die Sitemap
   einreichen.

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

Am 27.10.2026 erneut mit der laufenden alten Seite abgeglichen. Sätze, die
dort nicht stehen (Preisnachlass/Kinderermäßigung, Hunde- und Gartentext,
Buckelwiesen/5 km), wurden entfernt bzw. durch den Originalwortlaut ersetzt.
Kontakt Landhaus Wackerl: Steffi Pöll, wie auf der alten Kontaktseite.

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
