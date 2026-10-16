# Sekáče Bratislava

Mapa second handov v Bratislave. Zelený pin = práve otvorené, červený = zatvorené, sivý = Google Mapy neuvádzajú hodiny.

## Ako to spustiť
Celá stránka je jeden súbor **`index.html`** (mapa, dáta aj knižnica sú v ňom). Stačí ho otvoriť v prehliadači.
Internet treba len na mapové podklady a fotky.

**Mobil s polohou (modrá gulička):** prehliadač dá polohu len stránke na https adrese.
Nahraj `index.html` napr. na GitHub Pages alebo Netlify Drop (app.netlify.com/drop – stačí potiahnuť priečinok)
a otvor tú adresu v mobile. Cez „Pridať na plochu“ ju máš ako appku.

## Ovládanie na mobile
- ťukni na pin → dole sa vysunie panel s fotkou, stavom a tlačidlami
- potiahni panel hore → celé otváracie hodiny a veľká fotka; potiahni dole → zavrie sa
- tlačidlo so zameriavačom → tvoja poloha; potom sa dole ukáže najbližší otvorený sekáč
- tlačidlo s čiarami → zoznam podľa vzdialenosti

## Úprava dát
Zdrojové súbory sú v `zdroj/`. Obchody sú v `zdroj/data.js` (hodiny v minútach od polnoci,
0 = nedeľa … 6 = sobota, `[[540, 1140]]` = 9:00–19:00, `[]` = zatvorené, `null` = neznáme).
Po úprave spusti `python zostav.py` v priečinku `zdroj` (potrebuje leaflet.js a leaflet.css v `zdroj/leaflet/`).
