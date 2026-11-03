# Tanári megoldókulcs — `hibas.html` (25 hiba)

> Ezt a fájlt ne add ki a hallgatóknak. A javított változat: `megoldas.html`.
> A sorszámok a `hibas.html`-re vonatkoznak.

## HTML (10 hiba)

| # | Sor | Hibás | Helyes | Mit okoz |
|---|-----|-------|--------|----------|
| 1 | 1 | `<!DOCTYP html>` | `<!DOCTYPE html>` | Quirks (kompatibilitási) mód, a validator is jelzi. |
| 2 | 4 | `<meta chrset="UTF-8">` | `<meta charset="UTF-8">` | Az ékezetek elromolhatnak (pl. `Ã©` jelenik meg). |
| 3 | 6 | `</titel>` | `</title>` | **A legnagyobb hiba:** a böngésző a lezárásig mindent címnek vesz → üres oldal, a fül címe a teljes forráskód. Ezt kell elsőként megtalálni. |
| 4 | 77 | `<a hre="#">` | `<a href="#">` | A „Hallgatók” nem kattintható link. |
| 5 | 84 | `<h2>Oktatóink<h2>` | `<h2>Oktatóink</h2>` | A lezárás hiányzik → az alatta lévő bekezdés is óriási, félkövér címsor lesz. |
| 6 | 104 | `<tb ...>...</tb>` | `<td ...>...</td>` | Nem létező tag → a „Webfejlesztés” szöveg kiesik a táblázat fölé, a sor csonka. |
| 7 | 120 | `scr="..."` | `src="..."` | A kép nem jelenik meg. |
| 8 | 123 | `<audio>` | `<audio controls>` | A hanglejátszó láthatatlan. |
| 9 | 128, 130 | `<vidoe>` … `</vidoe>` | `<video>` … `</video>` | Nincs videólejátszó. |
| 10 | 134 | `youtube.com/watch?v=...` | `youtube.com/embed/...` | A YouTube megtagadja a beágyazást („refused to connect”). |
| 11 | 143 | `<scirpt>` | `<script>` | A JavaScript-kód sima szövegként jelenik meg az oldal alján, nem fut le. |

## CSS (8 hiba)

| # | Sor | Hibás | Helyes | Mit okoz |
|---|-----|-------|--------|----------|
| 12 | 16 | `backgroud-color` | `background-color` | A fejléc nem fekete (fehér szöveg fehér alapon → „eltűnik” a cím). |
| 13 | 22 | `// Menü linkek` | `/* Menü linkek */` | A CSS-ben nincs `//` komment → a következő szabály (`.menu a`) teljesen elveszik, a linkek kékek és aláhúzottak. |
| 14 | 29 | `tartalom {` | `.tartalom {` | Hiányzik a pont → nem az osztályra vonatkozik, a tartalom nincs középre igazítva. |
| 15 | 41 | `colapse` | `collapse` | Dupla vonalas cellakeretek. |
| 16 | 52 | `color: wihte;` | `color: white;` (vagy `#fff`) | A táblázat fejlécének szövege fekete a sötét háttéren. |
| 17 | 58 | `width: 300 px;` | `width: 300px;` | Szóköz a szám és a mértékegység között → érvénytelen, a kép eredeti méretű. |
| 18 | 64 | `color: #aaa` (nincs `;`) | `color: #aaa;` | A `color` és a `text-align` is érvénytelen lesz → a lábléc szövege nem szürke és nem középen van. |
| 19 | 86 | `class="kiemlet"` | `class="kiemelt"` | A HTML és a CSS osztálynév nem egyezik → a „Médiadesign” nem rózsaszín. |

## JavaScript (6 hiba)

| # | Sor | Hibás | Helyes | Mit okoz |
|---|-----|-------|--------|----------|
| 20 | 144 | `"Az oldal betöltődött.);` | `"Az oldal betöltődött.");` | Lezáratlan string → SyntaxError, **egyetlen sor sem fut le**. |
| 21 | 146 | `Alert(...)` | `alert(...)` | `Alert is not defined` — a JS kis-/nagybetű-érzékeny. |
| 22 | 149 | `+ Nev` | `+ nev` | `Nev is not defined` — a változó `nev` néven lett létrehozva. |
| 23 | 151 | `"Szia, " nev + ...` | `"Szia, " + nev + ...` | Hiányzó `+` → SyntaxError. |
| 24 | 153 | `confrim(...)` | `confirm(...)` | `confrim is not defined`. |
| 25 | 154 | `+ valasz;` | `+ valasz);` | Hiányzó zárójel → SyntaxError. |

## Javasolt sorrend / didaktikai megjegyzés

1. Először a `</titel>`-t kell megtalálni — amíg ez hibás, semmi más nem látszik. Jó belépő a „nézd meg a forráskódot / a fül címét” gondolkodáshoz.
2. Utána a `<scirpt>` — a kód szövegként jelenik meg az oldal alján, ez látványos.
3. A JS-hibákat a konzol egyenként mutatja: a **szintaktikai** hibák (20, 23, 25) az egész scriptet leállítják, ezért először ezek jönnek elő; a **futásidejű** hibák (21, 22, 24) csak utánuk.
4. A CSS-hibák csendesek — a böngésző nem szól, csak „nem csinálja”. Itt az F12 → Elements panel áthúzott sorai a legjobb nyom.
