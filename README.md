# torsten-frenzel.de – Publii-Projekt

Neuaufbau von [torsten-frenzel.de](https://torsten-frenzel.de) mit dem Static-CMS [Publii](https://getpublii.com) und einem Theme auf Basis von [KERN-UX](https://www.kern-ux.de), dem Design-System der deutschen Verwaltung.

## Inhalt des Repositorys

- `themes/frenzel-kern/` – Publii-Theme „Frenzel KERN“ (KERN-UX `kern.min.css`, Fira Sans lokal eingebunden, keine externen Skripte, keine Cookies)
- `content/` – Ausgangstexte (Markdown) für die Seiten Öffentliches, Impressum und Datenschutz
- `media/pixabay/CREDITS.md` – Nachweise für optionale Pixabay-Bilder (die Bilddateien selbst sind nicht im Repo)
- `LICENSE` – EUPL-1.2

## Einrichtung

1. Publii öffnen, neue Website anlegen (Sprache `de`, Name „Torsten Frenzel“).
2. Ordner `themes/frenzel-kern` nach `~/Documents/Publii/themes/frenzel-kern` kopieren (oder zippen und in Publii unter *Themes* installieren). Der Ordnername muss `frenzel-kern` heißen. Publii danach neu starten, weil es Theme-Einstellungen nur beim Start einliest.
3. In der Website unter *Theme* das Theme „Frenzel KERN“ auswählen.
4. Unter *Pages* drei Seiten anlegen: „Öffentliches“ (Slug `oeffentliches`), „Impressum“ (`impressum`), „Datenschutz“ (`datenschutz`). Die Texte stehen in `content/`.
5. Unter *Menus* anlegen und zuordnen:
   - **Hauptmenü** (Position „Hauptmenü“): „Öffentliches“. Die Links „Podcasts“ und „Kontakt“ setzt das Theme selbst.
   - **Startseite: Link Öffentliches**: ein Eintrag „Öffentliches“.
   - **Fußmenü**: „Impressum“ und „Datenschutz“.
6. Unter *Theme* → Custom settings Texte, Podcast-Karten, Links und Kontaktdaten prüfen.

## Inhalte in Publii ändern

- **Startseite** (Einleitung, Portrait, Podcast-Karten, Öffentliches, Kontakt, Fußzeile): *Theme* → Custom settings, gegliedert in „Startseite: …“, „Links & Kontakt“ und „Fußzeile“. Die Podcast-Cover sind URL-Felder (quadratische Bilder).
- **Öffentliches, Impressum, Datenschutz**: *Pages*.
- **Menüs**: *Menus*.

## Hinweise zum Theme

- Publii nutzt eine eigene Theme-API: `config.json` mit `customConfig` und `menus`, Platzhalter wie `{{@website.*}}`, `{{{publiiHead}}}` und `{{css "style.css"}}`. Das Haupt-Stylesheet liegt in `assets/css/main.css` und `style.css` (beide identisch, Publii braucht beide).
- Das Portrait gibt es zweimal: im hellen Modus freigestellt (`portrait-schwarz-freigestellt.webp`), im dunklen Modus als Originalfoto.
- Der Link zu „Öffentliches“ auf der Startseite und die Anker-Links im Hauptmenü entstehen aus Publii-Menüs bzw. `{{@website.url}}`, damit sie in Vorschau und Live-Betrieb funktionieren.

## Lizenz

Der Code und die Texte dieses Repositorys stehen unter der **EUPL-1.2** (siehe `LICENSE`). Drittkomponenten: KERN-UX (EUPL-1.2) und Fira Sans (SIL OFL 1.1), beide kompatibel.

**Bilder:** Die Portraitfotos in `themes/frenzel-kern/assets/images/` sind © Torsten Frenzel, alle Rechte vorbehalten. Sie stehen **nicht** unter der EUPL-1.2 (siehe `themes/frenzel-kern/assets/images/LICENSE-IMAGES.md`). Pixabay-Bilder (Pixabay Content License) liegen nicht im Repository. Die Podcast-Cover werden von podcastfunkhaus.de eingebunden.

## Status

Impressum und Datenschutz sind aus der Webseite des eGovernment Podcasts übernommen und gekürzt. Sie sollten vor der Veröffentlichung rechtlich geprüft werden.
