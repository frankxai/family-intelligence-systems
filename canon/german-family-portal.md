# Deutsches Familienportal

## Produktname

**Lebendiges Familienarchiv Riemer-Gorte**

Unterzeile: *Erinnerungen bewahren. Aussagen belegen. Zugänge verantwortungsvoll weitergeben.*

## Informationsarchitektur

| Bereich | Aufgabe |
|---|---|
| Heute | Ein ruhiger Überblick über Einladungen, offene Freigaben, Erinnerungen und nächste Gespräche |
| Mein Bereich | Private Notizen, Geschichten, Dokumente, Wünsche und Freigabeentwürfe |
| Engster Kreis | Geteilte Informationen für ausdrücklich eingeladene Vertrauenspersonen |
| Familienarchiv | Belegte Geschichten, Fotos, Quellen, Zeitstrahl und Familienbaum |
| Offene Aussagen | Neue Hinweise, Widersprüche, mögliche Duplikate und ungeklärte Verbindungen |
| Gespräche | Zeitzeugen-Interviews, Transkripte, Einwilligung und Quellenbezug |
| Nachkommen & Patenschaften | Guardian-verwaltete, altersgerechte Übergabe von Wissen und Erinnerungen |
| Notfall & Vorsorge | Minimaler Notfallzugang, Handlungsanweisungen, Vertrauenspersonen und Übungen |
| Freigaben | Wer darf was zu welchem Zweck sehen, teilen oder veröffentlichen? |
| Einstellungen & Export | Datenschutz, Berichtigung, Löschung, Widerruf, vollständiger Export und Wiederherstellung |

## Sprache

- `claim` -> Aussage / Familienaussage
- `evidence` -> Beleg / Quelle
- `steward` -> Familienverwalter:in or Archivverantwortliche:r
- `guardian` -> Schutzverantwortliche:r; `Patenonkel` remains the relationship term
- `consent` -> Einwilligung / Freigabe
- `provenance` -> Herkunftsnachweis
- `dispute` -> Widerspruch
- `succession` -> Nachfolge / Zugangsübergabe
- `family tree` -> Familienbaum or Stammbaum; prefer Familienbaum in inclusive UI

## UX rules

- Never label an uncertain connection as established.
- Show source, confidence, review state, and privacy scope beside every relationship.
- Use plain German; legal notices can link to detailed language.
- No child profile appears in public search, analytics, screenshots, or sample data.
- Every publish action previews exactly what will become public.
- The most important action is usually `Prüfen`, `Freigeben`, `Widersprechen`, or `Privat behalten`, not `Teilen`.
