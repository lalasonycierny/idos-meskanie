# Štatistiky MHD Bratislava

Automaticky generované 2026-11-11 15:10. Zdroj: kdejemhd.sk, zber každú minútu.

- Dní v štatistike: **2** (2026-10-26 až 2026-11-11)
- Priemerné pokrytie zberom: **7 %** (100 % = zber každú minútu celý deň)
- Posledných 7 dní: načas 42.5 %, meškanie 5 min a viac 25.2 %, v službe priemerne 502 vozidiel (71 855 meraní).

## Kedy meškajú najviac

![heatmapa](charts/heatmap_delay_weekday_hour.png)

![vozidlá podľa hodiny](charts/vehicles_by_hour.png)

## Linky s najväčším podielom meškaní (30 dní)

| Linka | Meraní | Načas % | 5 min+ % | Priem. meškanie (min) |
|---|---|---|---|---|
| 45 | 667 | 19.2 | 73.9 | 10.9 |
| 32 | 1129 | 31.4 | 57.0 | 7.8 |
| 75 | 1438 | 20.6 | 47.6 | 6.6 |
| 53 | 1168 | 33.1 | 41.6 | 5.8 |
| 23 | 1096 | 34.0 | 41.4 | 6.5 |
| 52 | 512 | 24.0 | 39.1 | 5.7 |
| 60 | 1697 | 38.6 | 37.4 | 5.8 |
| 65 | 2608 | 19.1 | 35.5 | 5.2 |
| 47 | 2133 | 36.6 | 32.9 | 4.7 |
| 3 | 8355 | 36.2 | 31.7 | 5.1 |

![linky](charts/worst_routes.png)

## Podľa typu vozidla (30 dní)

| Typ | Meraní | Načas % | 5 min+ % |
|---|---|---|---|
| Autobusy | 62938 | 42.0 | 23.5 |
| Tramvaje | 20671 | 43.7 | 22.4 |
| Trolejbusy | 19686 | 42.0 | 26.5 |

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
