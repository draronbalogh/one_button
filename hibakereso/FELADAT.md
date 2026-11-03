# Hibakereső feladat — METU Médiadesign „Oktatóink” oldal

A `hibas.html` a metumediadesign.hu oldal egy nagyon leegyszerűsített „Oktatóink” aloldala.
Valaki nagyon sietett, amikor megírta: **legalább 20 hiba** van benne, és mindhárom nyelvben akad belőlük:

- **HTML** (elírt tagek, rossz attribútumok, rossz beágyazás)
- **CSS** (elírt tulajdonságok, hiányzó jelek, rossz szelektorok)
- **JavaScript** (`alert`, `prompt`, `confirm`, `console.log`)

## A feladat

1. Nyisd meg a `hibas.html`-t böngészőben. Mit látsz? (Spoiler: nem sokat.)
2. Nyomozd ki a hibákat, és javítsd ki őket egyesével.
3. Minden javítás után mentsd el a fájlt, és frissítsd a böngészőt (F5).
4. Írd fel egy listába: **hányadik sor, mi volt a hiba, mire javítottad.**

## Ha kész, ilyennek kell lennie az oldalnak

- Fekete fejléc fehér címmel, alatta 4 fehér menüpont (mind kattintható link).
- Középre igazított tartalom, egy rózsaszín, félkövér „Médiadesign” szó.
- Táblázat keretekkel, sötét fejléccel, fehér fejléc-szöveggel, minden cella a helyén.
- Egy lekerekített sarkú kép, egy lejátszható hang, egy lejátszható videó, egy működő YouTube-videó.
- Fekete lábléc szürke, középre igazított szöveggel.
- Betöltéskor: üdvözlő **alert** → **prompt** a nevedre → személyes **alert** → **confirm** a jelentkezésről → **alert** a válasszal.
- A konzolban (F12 → Console) **3 üzenet** jelenik meg, és **egyetlen piros hiba sem**.

## Nyomozó eszközök

- **F12 → Console**: a JavaScript-hibákat pirossal mutatja, sorszámmal együtt.
- **F12 → Elements**: itt látod, hogyan értette meg a böngésző a HTML-edet. Áthúzott CSS-sor = a böngésző nem fogadta el.
- **Ctrl+U**: az oldal forráskódja.
- **https://validator.w3.org/#validate_by_input**: másold be a kódot, és megmutatja a HTML-hibákat.

## Tippek

- Ha egy JavaScript-hibát kijavítasz, utána jöhet a következő — a böngésző mindig csak az elsőt mutatja.
- Figyelj a kis- és nagybetűkre, az idézőjelekre, a pontosvesszőkre és a zárójelekre.
- A CSS-ben egy osztályt `.` (pont) jelöl.
- A YouTube-videó oldalának linkje nem ugyanaz, mint a beágyazási link.
