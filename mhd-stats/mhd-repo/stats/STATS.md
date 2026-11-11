# Štatistiky MHD Bratislava

Automaticky generované 2026-11-11 13:10. Zdroj: kdejemhd.sk, zber každú minútu.

- Dní v štatistike: **2** (2026-10-26 až 2026-11-11)
- Priemerné pokrytie zberom: **3 %** (100 % = zber každú minútu celý deň)
- Posledných 7 dní: načas 44.5 %, meškanie 5 min a viac 28.5 %, v službe priemerne 462 vozidiel (10 637 meraní).

## Kedy meškajú najviac

![heatmapa](charts/heatmap_delay_weekday_hour.png)

![vozidlá podľa hodiny](charts/vehicles_by_hour.png)

## Linky s najväčším podielom meškaní (30 dní)

| Linka | Meraní | Načas % | 5 min+ % | Priem. meškanie (min) |
|---|---|---|---|---|
| 75 | 563 | 18.7 | 64.1 | 7.3 |
| 50 | 983 | 35.6 | 36.9 | 5.2 |
| 21 | 1417 | 38.0 | 34.9 | 4.6 |
| 98 | 1176 | 36.0 | 32.7 | 4.5 |
| 65 | 1228 | 25.0 | 31.5 | 4.6 |
| 80 | 605 | 45.6 | 31.1 | 4.9 |
| 96 | 1036 | 35.3 | 29.7 | 3.3 |
| 47 | 813 | 40.6 | 26.7 | 3.5 |
| 84 | 1302 | 33.0 | 26.7 | 4.3 |
| 39 | 749 | 48.5 | 26.2 | 3.7 |

![linky](charts/worst_routes.png)

## Podľa typu vozidla (30 dní)

| Typ | Meraní | Načas % | 5 min+ % |
|---|---|---|---|
| Autobusy | 25648 | 40.3 | 25.3 |
| Tramvaje | 8418 | 48.3 | 14.5 |
| Trolejbusy | 8011 | 44.3 | 22.7 |

## Miesta, kde vozidlá stoja

![miesta](charts/hotspots.png)

Zahŕňa aj konečné a zastávky, kde vozidlá stoja prirodzene.

## Dáta na stiahnutie

Denné agregáty vo formáte CSV (zostávajú v repozitári natrvalo):

- [daily.csv](data/daily.csv) celkové údaje po dňoch
- [daily_route.csv](data/daily_route.csv) po linkách
- [daily_hour.csv](data/daily_hour.csv) po hodinách
- [daily_type.csv](data/daily_type.csv) po type vozidla
- [daily_hotspots.csv](data/daily_hotspots.csv) miesta, kde vozidlá stoja

## Poznámky k metodike

- Meškanie zdroj udáva v celých minútach. Hodnota 15:00 vyzerá ako strop, takže priemerné meškanie je orezané a presnejšie sú podiely. Stĺpec `pct_cap15` v CSV ukazuje podiel hodnôt na strope.
- „Načas“ je meškanie pod 1 minútu, „5 min a viac“ zodpovedá kategórii „nad 5 min“ na webe.
- Do štatistík meškaní sa počítajú len vozidlá, ktoré majú údaj o meškaní (sú na spoji).
- Dni sa počítajú v čase Europe/Bratislava. Pokrytie pod 100 % znamená výpadky zberu.
- Nezávislý projekt, nie je súčasťou Dopravného podniku Bratislava.
