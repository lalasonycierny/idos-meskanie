# Štatistiky MHD Bratislava

Automaticky generované 2026-11-11 14:10. Zdroj: kdejemhd.sk, zber každú minútu.

- Dní v štatistike: **2** (2026-10-26 až 2026-11-11)
- Priemerné pokrytie zberom: **5 %** (100 % = zber každú minútu celý deň)
- Posledných 7 dní: načas 44.6 %, meškanie 5 min a viac 26.6 %, v službe priemerne 476 vozidiel (39 469 meraní).

## Kedy meškajú najviac

![heatmapa](charts/heatmap_delay_weekday_hour.png)

![vozidlá podľa hodiny](charts/vehicles_by_hour.png)

## Linky s najväčším podielom meškaní (30 dní)

| Linka | Meraní | Načas % | 5 min+ % | Priem. meškanie (min) |
|---|---|---|---|---|
| 75 | 958 | 18.7 | 57.6 | 7.6 |
| 32 | 812 | 29.8 | 57.5 | 7.9 |
| 53 | 749 | 33.5 | 43.1 | 6.0 |
| 23 | 693 | 34.9 | 38.1 | 6.0 |
| 65 | 1910 | 20.3 | 34.9 | 5.1 |
| 60 | 1140 | 41.8 | 33.6 | 5.2 |
| 47 | 1473 | 36.1 | 33.1 | 4.5 |
| 67 | 705 | 52.3 | 31.2 | 4.3 |
| 21 | 2184 | 40.6 | 31.0 | 4.4 |
| 50 | 1835 | 41.2 | 30.6 | 4.3 |

![linky](charts/worst_routes.png)

## Podľa typu vozidla (30 dní)

| Typ | Meraní | Načas % | 5 min+ % |
|---|---|---|---|
| Autobusy | 42731 | 42.3 | 24.8 |
| Tramvaje | 14437 | 46.9 | 20.1 |
| Trolejbusy | 13741 | 43.7 | 25.2 |

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
