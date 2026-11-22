# Vozopis – promo web

Prezentační web služby **Vozopis – elektronická servisní kniha**. Jedna statická stránka bez build kroku, hostovaná na GitHub Pages na doméně <https://vozopis.cz> (soubor `CNAME`). DNS u Forpsi: A záznamy domény na 185.199.108.153, .109.153, .110.153, .111.153 a `www` jako CNAME na `romanzdk.github.io`. Stará doména eservisnikniha.cz přesměrovává na vozopis.cz přes repozitář `romanzdk/eservisnikniha-redirect`.

- `index.html` – celý obsah stránky
- `assets/style.css` – vzhled
- `assets/fonts/` – Barlow a Barlow Condensed (stejné jako v aplikaci) hostované lokálně, takže se nic nenačítá od Googlu a web nepotřebuje cookie lištu
- `assets/og.png` – náhled pro sdílení na sociálních sítích
- `robots.txt` a `sitemap.xml` – pro vyhledávače. Když přidáte novou stránku, doplňte ji do mapy a upravte `lastmod`

Lokálně: otevřete `index.html` v prohlížeči.

Před spuštěním doplňte skutečný kontaktní e-mail místo `esk@example.com` v `index.html`.

## Licence

Všechna práva vyhrazena, žádné další použití bez písemného souhlasu. Podrobnosti v [LICENSE](LICENSE). Repozitář je veřejný jen kvůli GitHub Pages.

## Seznam servisů

Sekce „Najít servis“ načítá živý seznam z ostré aplikace: `https://app.vozopis.cz/autoservisy.json` (konstanta `DIR_URL` v `index.html`). Dokud je seznam prázdný, sekce i odkazy na ni jsou skryté. Objeví se samy s prvním servisem, který souhlasí se zveřejněním.

## Podmínky a ochrana údajů

`podminky.html` je vygenerovaná kopie návrhů z repa aplikace (`docs/pravni/*.md`, bez poznámek pro advokáta). Po změně podmínek ji vygenerujte znovu stejným postupem (Markdown → HTML) a commitněte. `ochrana-udaju.html` se píše ručně a má odpovídat stránce Ochrana osobních údajů v aplikaci.

## Kontaktní formulář

Formulář v sekci Kontakt odesílá zprávy do ostré aplikace (`https://app.vozopis.cz/api/kontakt/`, atribut `data-endpoint`). Zprávy jsou v administraci aplikace, provozovatel dostane e-mail s odkazem (bez obsahu zprávy). Když odeslání selže, formulář nabídne e-mail.

