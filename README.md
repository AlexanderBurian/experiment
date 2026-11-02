# kept.cz

Oficiální ping pong. Obličej se odráží po obrazovce jako DVD logo a nikdy netrefí roh.
Ťukni / klikni = další obličej. Funguje na mobilu i na počítači.

## Soubory
- `index.html` — celá stránka (žádné závislosti)
- `face.webp` — hlavní odrážející se obličej
- `rare.webp`, `rare2.webp` — rare "PTAK drip" spawny (každý 3. spawn, náhodně z poolu)
- `CNAME` — vlastní doména `kept.cz`

### Přidání dalšího rare obrázku
Hoď `*.webp` do složky a dopiš ho do `RARE_SRCS` v `index.html` (+ volitelně do `ratioCache`). Chybějící rare obrázek se bezpečně nahradí existujícím.

## Nasazení přes GitHub Pages
1. Vytvoř nový, prázdný repozitář (ať se to nemíchá s jinými projekty).
2. Nahraj sem obsah téhle složky (`index.html`, `face.webp`, `CNAME`, `README.md`) do větve `main`.
3. V repu: **Settings → Pages → Source: Deploy from a branch → `main` / `/ (root)`**.
4. Custom domain: `kept.cz` (CNAME soubor to nastaví automaticky), zapni **Enforce HTTPS**.

## DNS pro kept.cz (u registrátora domény)
Apex doména `kept.cz` → A záznamy na GitHub Pages:
```
A  @  185.199.108.153
A  @  185.199.109.153
A  @  185.199.110.153
A  @  185.199.111.153
```
Volitelně `www` → CNAME na `<tvuj-github-username>.github.io`.
Po propagaci DNS (klidně pár hodin) bude web na https://kept.cz.
