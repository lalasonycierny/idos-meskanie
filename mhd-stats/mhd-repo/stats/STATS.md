# Štatistiky MHD Bratislava

Automaticky generované 2026-10-26 07:14. Zdroj: kdejemhd.sk, zber každú minútu.

- Dní v štatistike: **1** (2026-10-26 až 2026-10-26)
- Priemerné pokrytie zberom: **0 %** (100 % = zber každú minútu celý deň)
- Posledných 7 dní: načas 50.2 %, meškanie 5 min a viac 13.5 %, v službe priemerne 556 vozidiel (556 meraní).

## Kedy meškajú najviac

![heatmapa](charts/heatmap_delay_weekday_hour.png)

![vozidlá podľa hodiny](charts/vehicles_by_hour.png)

## Podľa typu vozidla (30 dní)

| Typ | Meraní | Načas % | 5 min+ % |
|---|---|---|---|
| Autobusy | 342 | 48.5 | 15.5 |
| Tramvaje | 110 | 52.7 | 10.9 |
| Trolejbusy | 104 | 52.9 | 9.6 |

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
