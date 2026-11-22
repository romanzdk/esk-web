# ESK – promo web

Prezentační web služby **Elektronická servisní kniha (ESK)**. Jedna statická stránka bez build kroku, hostovaná na GitHub Pages.

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

