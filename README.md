# ESK – promo web

Prezentační web služby **Elektronická servisní kniha (ESK)**. Jedna statická stránka bez build kroku, hostovaná na GitHub Pages na doméně <https://eservisnikniha.cz> (soubor `CNAME`). DNS u Forpsi: A záznamy domény na 185.199.108.153, .109.153, .110.153, .111.153 a `www` jako CNAME na `romanzdk.github.io`.

- `index.html` – celý obsah stránky
- `assets/style.css` – vzhled
- `assets/fonts/` – Barlow a Barlow Condensed (stejné jako v aplikaci) hostované lokálně, takže se nic nenačítá od Googlu a web nepotřebuje cookie lištu
- `assets/og.png` – náhled pro sdílení na sociálních sítích

Lokálně: otevřete `index.html` v prohlížeči.

Před spuštěním doplňte skutečný kontaktní e-mail místo `esk@example.com` v `index.html`.

## Licence

Všechna práva vyhrazena, žádné další použití bez písemného souhlasu. Podrobnosti v [LICENSE](LICENSE). Repozitář je veřejný jen kvůli GitHub Pages.

## Seznam servisů

Sekce „Najít servis“ načítá `assets/autoservisy.json` (teď prázdný seznam). Až aplikace ESK poběží na veřejné adrese, změňte v `index.html` konstantu `DIR_URL` na `https://<adresa aplikace>/autoservisy.json` – aplikace vrací stejný formát a povoluje načtení z jiné domény.

## Podmínky a ochrana údajů

`podminky.html` je vygenerovaná kopie návrhů z repa aplikace (`docs/pravni/*.md`, bez poznámek pro advokáta). Po změně podmínek ji vygenerujte znovu stejným postupem (Markdown → HTML) a commitněte. `ochrana-udaju.html` se píše ručně a má odpovídat stránce Ochrana osobních údajů v aplikaci.

## Kontaktní formulář

Formulář v sekci Kontakt odesílá zprávy do aplikace ESK (`/api/kontakt/`, zprávy uvidíte v administraci). Dokud aplikace neběží veřejně, je skrytý a zobrazuje se tlačítko „Napsat e-mail“. Po nasazení nastavte v `index.html` u `<form id="contact-form">` atribut `data-endpoint="https://<adresa aplikace>/api/kontakt/"`.

