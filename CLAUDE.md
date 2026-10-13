# INCH_ website

Statische one-pager voor INCH_ (communicatie voor cyber), gehost op GitHub Pages.
Eigenaar: Marieke Rijken. **Dit project staat helemaal los van AdversIQ.**

## Geldt hier NIET

De globale regels in `~/.claude/CLAUDE.md` over AdversIQ gelden niet in deze repo:
geen Forgejo, geen `as-agent`, geen galaxy, geen AdversIQ-skills of -context.

## Repo en account

- GitHub: `Piiindakaas/inch-website`, via `gh` met account **Piiindakaas**.
  Check vóór elke push of PR: `gh auth status` moet Piiindakaas als actief tonen,
  anders eerst `gh auth switch -u Piiindakaas`.
- Git-identiteit staat lokaal in deze repo (`git config user.*`); niet aanpassen.

## Structuur

- `index.html` — alle content (Nederlands). Elke sectie heeft een commentaar `<!-- 0X Naam -->`.
- `assets/css/style.css` — opmaak; kleuren en fonts als tokens bovenaan `:root`.
- `assets/img/` — logo's (SVG), favicon, portret.
- `.github/workflows/pages.yml` — elke push naar `main` gaat automatisch live.
- Design-bron: Figma `INCH_` (fileKey `2M6f6OQY3feX0vK7lNw3pq`), Page 1 = website, Page 2 = logo's.

Geen build-stap, geen framework, geen npm. Houd het zo.

## Werkwijze bij een wijzigingsverzoek

Marieke zegt bijvoorbeeld "pas de tekst bij Crisis aan" of "voeg een sectie toe". Dan:

1. `git switch main && git pull`, daarna een branch: `wijziging/<korte-omschrijving>`.
2. Pas alleen aan wat gevraagd is. Content-wijzigingen raken alleen `index.html`;
   het design (kleuren, fonts, maten) alleen als daar expliciet om gevraagd wordt.
3. Preview: start de server `inch-site` uit `.claude/launch.json` en laat het resultaat
   zien in het browserpaneel, op desktop én mobiel (375px).
4. Commit, push, en open een PR met `gh pr create` met een korte Nederlandse omschrijving
   van wat er zichtbaar verandert.
5. Geef Marieke de PR-link. Zij merget; ~1 minuut later staat het live.

Merge nooit zelf naar `main` tenzij Marieke dat in de sessie expliciet vraagt.

## Schrijfstijl

Teksten zijn in Mariekes eigen stem: direct, informeel, ik-vorm, geen marketingjargon.
Placeholders staan tussen `[HAKEN]`; verzin nooit feiten, cijfers of klantnamen.

## Nog open

- Placeholders invullen (statement, telefoon, mail, eerder-gedaan-regels).
- `<meta name="robots" content="noindex">` weghalen bij livegang.
- Eigen domein `insertcompanynamehere.nl` (DNS bij Mijndomein) koppelen.
