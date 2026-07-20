# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-20T01:35:21+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **668814** (666728 priced in exalted)
- Distinct bases: 996 · distinct mods: 3292 · mod rows: 3166867
- Sold signals: **24481** sold · 381011 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-20T01:22:04+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×25.31** (median |log error| 3.2313)
- Within ±30% of asking price: **19%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.13** · typical error ×78.05 · ±30% 4% · n=97713
- Premium segment (60ex+): skill **+0.13** · typical error ×349.36 · ±30% 0% · n=65755

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 14105 | ×55.76 | 21% | +0.03 | +0.06 |
| jewel | 13458 | ×57.49 | 22% | +0.03 | +0.03 |
| accessory.amulet | 12806 | ×30.40 | 18% | +0.04 | +0.04 |
| accessory.belt | 9260 | ×19.60 | 8% | +0.09 | +0.12 |
| armour.chest | 8931 | ×16.83 | 24% | +0.07 | +0.09 |
| armour.helmet | 8734 | ×26.77 | 21% | +0.07 | +0.10 |
| armour.boots | 8098 | ×27.14 | 20% | +0.09 | +0.12 |
| armour.gloves | 7930 | ×35.39 | 17% | +0.07 | +0.10 |
| other | 7893 | ×1.84 | 44% | +0.11 | +0.18 |
| weapon.wand | 4760 | ×42.57 | 16% | +0.09 | +0.10 |
| weapon.bow | 3732 | ×29.64 | 13% | +0.14 | +0.15 |
| weapon.crossbow | 3512 | ×30.11 | 17% | +0.10 | +0.14 |
| weapon.warstaff | 2407 | ×17.35 | 7% | +0.20 | +0.20 |
| weapon.staff | 2285 | ×19.82 | 6% | +0.18 | +0.16 |
| weapon.sceptre | 2229 | ×20.25 | 5% | +0.10 | +0.10 |
| weapon.spear | 1774 | ×19.03 | 7% | +0.12 | +0.14 |
| armour.focus | 1488 | ×18.93 | 7% | +0.11 | +0.12 |
| armour.quiver | 1389 | ×21.93 | 7% | +0.17 | +0.18 |
| flask.charm | 1161 | ×14.43 | 29% | -0.01 | +0.02 |
| armour.shield | 1144 | ×18.58 | 7% | +0.09 | +0.11 |
| weapon.twomace | 1062 | ×9.23 | 8% | +0.12 | +0.12 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=73269, R²=-1.8978

intercept: `-0.0525`  ·  log_price: True  ·  ilvl: `0.00065`  ·  n_mods: `1.02334`  ·  n_top_tier: `-0.84446`  ·  corrupted: `1.36492`  ·  quality: `0.31220`

| stat_id | coef |
|---|---|
| `explicit.stat_3485067555@T1` | 3.82282 |
| `explicit.stat_3714003708@T1` | 3.16922 |
| `explicit.stat_3473929743@T1` | -2.76907 |
| `explicit.stat_1604736568@T1` | -2.70974 |
| `explicit.stat_1604736568` | 2.54104 |
| `explicit.stat_3556824919@T1` | 1.06560 |
| `explicit.stat_587431675@T1` | -0.94217 |
| `explicit.stat_274716455@T1` | -0.88646 |
| `explicit.stat_1854213750@T1` | 0.86839 |
| `explicit.stat_1697447343@T1` | -0.81832 |
| `explicit.stat_2194114101@T1` | -0.62021 |
| `explicit.stat_3174700878@T1` | 0.59060 |

### accessory.ring — n=64455, R²=-2.0411

intercept: `3.4552`  ·  log_price: True  ·  ilvl: `-0.04286`  ·  n_mods: `0.00148`  ·  n_top_tier: `1.10346`  ·  corrupted: `0.01203`  ·  n_sockets: `1.67370`  ·  quality: `0.02503`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.13170 |
| `explicit.stat_4220027924@T2` | -1.13034 |
| `explicit.stat_803737631@T1` | -1.12932 |
| `explicit.stat_2231156303@T1` | -1.12683 |
| `explicit.stat_1573130764@T2` | -1.12627 |
| `explicit.stat_4080418644@T1` | -1.11965 |
| `explicit.stat_736967255@T2` | -1.11695 |
| `explicit.stat_789117908@T2` | -1.11617 |
| `explicit.stat_789117908@T1` | -1.11555 |
| `explicit.stat_2923486259@T2` | -1.11296 |
| `explicit.stat_2891184298@T1` | -1.11270 |
| `explicit.stat_3261801346@T1` | -1.11250 |

### other — n=63649, R²=-0.6256

intercept: `1.6092`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.01313`  ·  n_top_tier: `0.33346`  ·  corrupted: `0.20820`  ·  n_sockets: `-0.00003`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.37132 |
| `explicit.stat_3299347043@T1` | -0.28039 |
| `implicit.stat_2219129443` | 0.22894 |
| `implicit.stat_3879011313` | 0.22894 |
| `implicit.stat_4041853756` | 0.22894 |
| `explicit.stat_2974417149@T1` | 0.13262 |
| `explicit.stat_3917489142@T1` | -0.09080 |
| `explicit.stat_736967255@T1` | -0.08627 |
| `explicit.stat_789117908@T1` | -0.06947 |
| `explicit.stat_2106365538@T1` | -0.05429 |
| `explicit.stat_3291658075@T1` | -0.05161 |
| `pseudo.total_ele_res>=40` | -0.04850 |

### accessory.amulet — n=58221, R²=-2.1426

intercept: `3.4663`  ·  log_price: True  ·  ilvl: `-0.04312`  ·  n_mods: `-0.02089`  ·  n_top_tier: `1.39018`  ·  corrupted: `0.08707`  ·  n_sockets: `-0.13581`  ·  quality: `0.03258`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.95894 |
| `explicit.stat_3299347043@T2` | -1.90230 |
| `explicit.stat_587431675@T2` | -1.59866 |
| `explicit.stat_803737631@T1` | -1.50641 |
| `explicit.stat_2974417149@T1` | -1.48699 |
| `explicit.stat_2866361420@T2` | -1.46771 |
| `explicit.stat_1050105434@T2` | -1.45592 |
| `explicit.stat_803737631@T2` | -1.44533 |
| `explicit.stat_2866361420@T1` | -1.44270 |
| `explicit.stat_2748665614@T1` | -1.44093 |
| `explicit.stat_1671376347@T2` | -1.42522 |
| `explicit.stat_3261801346@T1` | -1.42309 |

### accessory.belt — n=42334, R²=-1.2367

intercept: `6.1715`  ·  log_price: True  ·  ilvl: `-0.06504`  ·  n_mods: `-0.15870`  ·  n_top_tier: `0.60429`  ·  corrupted: `1.04289`  ·  n_sockets: `0.76340`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.42907 |
| `implicit.stat_731781020` | -1.15138 |
| `explicit.stat_3299347043@T2` | -0.93241 |
| `explicit.stat_2923486259@T1` | 0.82199 |
| `explicit.stat_2881298780@T1` | -0.77277 |
| `explicit.stat_51994685@T1` | -0.72905 |
| `explicit.stat_4220027924@T2` | -0.68588 |
| `explicit.stat_3372524247@T2` | -0.66225 |
| `explicit.stat_1570770415@T2` | -0.64929 |
| `explicit.stat_1389754388@T1` | -0.61018 |
| `explicit.stat_4080418644@T1` | -0.60865 |
| `explicit.stat_644456512@T1` | -0.60062 |

### armour.chest — n=41955, R²=-1.8086

intercept: `3.1187`  ·  log_price: True  ·  ilvl: `-0.03857`  ·  n_mods: `-0.01067`  ·  n_top_tier: `0.30618`  ·  corrupted: `0.05339`  ·  n_sockets: `0.01558`  ·  quality: `0.07214`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.65173 |
| `explicit.stat_3981240776@T1` | 0.74768 |
| `explicit.stat_986397080@T2` | -0.37983 |
| `explicit.stat_986397080@T1` | -0.36645 |
| `explicit.stat_1692879867@T2` | -0.34181 |
| `explicit.stat_4080418644@T1` | -0.32840 |
| `explicit.stat_915769802@T2` | -0.32756 |
| `explicit.stat_3484657501@T1` | -0.32546 |
| `explicit.stat_4080418644@T2` | -0.32364 |
| `explicit.stat_1692879867@T1` | -0.32298 |
| `explicit.stat_915769802@T1` | -0.31972 |
| `explicit.stat_3299347043@T2` | -0.31745 |

### armour.helmet — n=40811, R²=-1.8097

intercept: `3.1494`  ·  log_price: True  ·  ilvl: `-0.03960`  ·  n_mods: `-0.01461`  ·  n_top_tier: `0.43102`  ·  corrupted: `0.68916`  ·  n_sockets: `0.02925`  ·  quality: `0.07053`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.71319 |
| `explicit.stat_1263695895@T1` | -0.65270 |
| `explicit.stat_2162097452@T2` | -0.61369 |
| `explicit.stat_3917489142@T2` | -0.58971 |
| `explicit.stat_1263695895@T2` | -0.53563 |
| `explicit.stat_3917489142@T1` | -0.51973 |
| `explicit.stat_2162097452@T1` | 0.47311 |
| `explicit.stat_4052037485@T2` | -0.46353 |
| `explicit.stat_1999113824@T1` | -0.46067 |
| `explicit.stat_803737631@T1` | -0.46000 |
| `explicit.stat_53045048@T1` | -0.45638 |
| `explicit.stat_803737631@T2` | -0.45358 |

### armour.boots — n=37942, R²=-1.7593

intercept: `3.3313`  ·  log_price: True  ·  ilvl: `-0.04113`  ·  n_mods: `-0.01566`  ·  n_top_tier: `0.48822`  ·  corrupted: `0.04103`  ·  n_sockets: `0.03603`  ·  quality: `0.06707`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.73876 |
| `crafted.stat_3917489142@T1` | 1.57625 |
| `explicit.stat_2339757871@T1` | -1.19494 |
| `explicit.stat_2923486259@T1` | 0.78440 |
| `explicit.stat_3917489142@T2` | -0.57918 |
| `explicit.stat_3299347043@T1` | -0.56742 |
| `explicit.stat_2923486259@T2` | -0.54625 |
| `explicit.stat_1874553720@T1` | -0.53251 |
| `explicit.stat_2160282525@T1` | -0.53139 |
| `explicit.stat_1671376347@T2` | -0.51795 |
| `explicit.stat_1062208444@T2` | -0.51652 |
| `explicit.stat_124859000@T1` | -0.51504 |

### armour.gloves — n=36871, R²=-1.7401

intercept: `3.8070`  ·  log_price: True  ·  ilvl: `-0.04932`  ·  n_mods: `-0.01680`  ·  n_top_tier: `0.75082`  ·  corrupted: `0.00398`  ·  n_sockets: `0.09820`  ·  quality: `0.05873`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 5.45905 |
| `explicit.stat_2923486259@T1` | -1.25172 |
| `explicit.stat_3484657501@T2` | -0.97349 |
| `explicit.stat_3321629045@T2` | -0.96516 |
| `explicit.stat_4015621042@T2` | -0.93718 |
| `explicit.stat_4052037485@T2` | -0.91354 |
| `explicit.stat_803737631@T2` | -0.90980 |
| `explicit.stat_4052037485@T1` | -0.89931 |
| `rune.stat_201332984` | 0.88749 |
| `explicit.stat_3484657501@T1` | -0.88449 |
| `explicit.stat_803737631@T1` | -0.88420 |
| `explicit.stat_9187492@T2` | -0.88000 |

### weapon.wand — n=22182, R²=-1.9891

intercept: `4.0849`  ·  log_price: True  ·  ilvl: `-0.05079`  ·  n_mods: `-0.04978`  ·  n_top_tier: `0.23201`  ·  corrupted: `-0.04636`  ·  n_sockets: `0.03840`  ·  quality: `0.03600`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.14769 |
| `rune.stat_124131830` | -2.73357 |
| `explicit.stat_2254480358@T1` | 2.65524 |
| `explicit.stat_124131830@T1` | 2.45874 |
| `explicit.stat_4226189338@T1` | 2.19490 |
| `explicit.stat_591105508@T1` | 2.12614 |
| `explicit.stat_736967255@T2` | 2.02816 |
| `explicit.stat_1600707273@T1` | 1.38548 |
| `explicit.stat_2254480358@T2` | 1.37268 |
| `crafted.stat_124131830` | 1.25595 |
| `explicit.stat_4226189338@T2` | 1.18811 |
| `explicit.stat_1545858329@T2` | 0.70160 |

### flask.charm — n=18497, R²=-0.6343

intercept: `0.1048`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.47668`  ·  corrupted: `1.59144`  ·  quality: `0.00399`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.63537 |
| `explicit.stat_1056492907` | 2.72128 |
| `explicit.stat_3246948616` | 1.59566 |
| `explicit.stat_828533480@T2` | -1.47671 |
| `explicit.stat_1120862500@T2` | -1.47670 |
| `explicit.stat_1873752457@T2` | -1.47667 |
| `explicit.stat_388617051@T2` | -1.47666 |
| `explicit.stat_3196823591@T2` | -1.47664 |
| `explicit.stat_2365392475@T2` | -1.47663 |
| `explicit.stat_2676834156@T2` | -1.47486 |
| `explicit.stat_1873752457@T1` | -1.47319 |
| `explicit.stat_828533480@T1` | -1.47256 |

### weapon.bow — n=17670, R²=-1.857

intercept: `3.9759`  ·  log_price: True  ·  ilvl: `-0.04708`  ·  n_mods: `-0.08011`  ·  n_top_tier: `0.71231`  ·  corrupted: `0.50718`  ·  n_sockets: `0.06662`  ·  quality: `0.03493`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.87349 |
| `crafted.stat_3035140377` | 1.35610 |
| `explicit.stat_3336890334@T1` | 1.28436 |
| `explicit.stat_709508406@T1` | 1.02947 |
| `explicit.stat_1263695895@T1` | -0.97235 |
| `explicit.stat_1263695895@T2` | -0.95625 |
| `explicit.stat_2463230181@T2` | -0.82522 |
| `explicit.stat_1509134228@T1` | -0.82339 |
| `explicit.stat_210067635@T2` | -0.80559 |
| `explicit.stat_3695891184@T2` | -0.80246 |
| `explicit.stat_3639275092@T1` | -0.79217 |
| `explicit.stat_1368271171@T2` | -0.78826 |

### weapon.crossbow — n=16583, R²=-1.8721

intercept: `4.0310`  ·  log_price: True  ·  ilvl: `-0.04960`  ·  n_mods: `-0.04217`  ·  n_top_tier: `0.34279`  ·  corrupted: `0.07839`  ·  n_sockets: `0.05807`  ·  quality: `0.02945`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 1.75974 |
| `explicit.stat_1980802737@T2` | -1.61092 |
| `explicit.stat_2250681686@T2` | -1.61031 |
| `explicit.stat_2250681686` | 1.40772 |
| `explicit.stat_1980802737` | 1.35973 |
| `explicit.stat_1509134228@T1` | 0.90386 |
| `explicit.stat_709508406@T1` | 0.83842 |
| `crafted.stat_3035140377` | 0.74984 |
| `explicit.stat_1263695895@T2` | -0.56560 |
| `explicit.stat_387439868@T1` | 0.53079 |
| `explicit.stat_1263695895@T1` | -0.51293 |
| `explicit.stat_3336890334@T2` | -0.46677 |

### weapon.warstaff — n=11400, R²=-0.3435

intercept: `-10.9556`  ·  log_price: True  ·  ilvl: `0.14671`  ·  n_mods: `-0.19595`  ·  n_top_tier: `0.36668`  ·  corrupted: `0.40305`  ·  n_sockets: `0.15597`  ·  quality: `0.05818`

| stat_id | coef |
|---|---|
| `desecrated.stat_2231156303@T1` | 1.78891 |
| `desecrated.stat_2527686725@T1` | 1.78891 |
| `crafted.stat_210067635@T2` | 1.26419 |
| `desecrated.stat_3291658075@T1` | -1.15588 |
| `desecrated.stat_473429811@T1` | -1.15588 |
| `explicit.stat_1368271171@T1` | -0.77802 |
| `explicit.stat_328541901@T1` | -0.76398 |
| `desecrated.stat_9187492` | 0.74749 |
| `explicit.stat_1037193709@T1` | 0.70451 |
| `explicit.stat_328541901@T2` | -0.67674 |
| `explicit.stat_691932474@T2` | -0.66663 |
| `explicit.stat_1509134228@T1` | 0.63349 |

### weapon.staff — n=10776, R²=-0.3654

intercept: `-15.4237`  ·  log_price: True  ·  ilvl: `0.19784`  ·  n_mods: `-0.07005`  ·  n_top_tier: `0.45714`  ·  corrupted: `0.79827`  ·  n_sockets: `0.18986`  ·  quality: `0.03831`

| stat_id | coef |
|---|---|
| `explicit.stat_591105508@T1` | 2.29559 |
| `explicit.stat_4226189338@T1` | 2.15317 |
| `explicit.stat_1545858329@T1` | 2.06417 |
| `explicit.stat_124131830@T1` | 1.35907 |
| `explicit.stat_2254480358@T1` | 1.25140 |
| `explicit.stat_293638271@T2` | -1.19763 |
| `explicit.stat_1600707273@T1` | 1.10893 |
| `explicit.stat_2254480358@T2` | 0.89089 |
| `explicit.stat_3962278098@T2` | 0.75458 |
| `explicit.stat_591105508@T2` | 0.63458 |
| `explicit.stat_1263695895@T1` | 0.63054 |
| `explicit.stat_473429811@T2` | -0.62058 |

### weapon.sceptre — n=10601, R²=-0.3397

intercept: `-21.3497`  ·  log_price: True  ·  ilvl: `0.27254`  ·  n_mods: `0.02319`  ·  n_top_tier: `0.22835`  ·  corrupted: `0.09770`  ·  n_sockets: `0.19778`  ·  quality: `0.02720`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.35608 |
| `explicit.stat_3057012405@T1` | 1.42917 |
| `explicit.stat_1263695895@T2` | -1.12029 |
| `explicit.stat_2162097452@T2` | 1.08814 |
| `explicit.stat_1263695895@T1` | -0.91461 |
| `explicit.stat_1798257884@T2` | 0.89271 |
| `explicit.stat_101878827@T1` | 0.83088 |
| `explicit.stat_2854751904@T2` | -0.76703 |
| `explicit.stat_101878827@T2` | 0.76416 |
| `explicit.stat_1250712710@T2` | 0.64438 |
| `explicit.stat_849987426@T1` | 0.62976 |
| `explicit.stat_770672621@T1` | -0.53718 |

### weapon.spear — n=8546, R²=-0.371

intercept: `-13.9161`  ·  log_price: True  ·  ilvl: `0.19110`  ·  n_mods: `-0.15545`  ·  n_top_tier: `0.71615`  ·  corrupted: `-0.40585`  ·  n_sockets: `0.23268`  ·  quality: `0.07460`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.73044 |
| `explicit.stat_1202301673@T1` | 1.35164 |
| `explicit.stat_1509134228@T1` | 1.30877 |
| `explicit.stat_1940865751@T2` | -1.18777 |
| `explicit.stat_4080418644@T2` | -1.07999 |
| `explicit.stat_9187492@T1` | 1.03611 |
| `explicit.stat_691932474@T1` | -0.95354 |
| `explicit.stat_3336890334@T2` | -0.91298 |
| `explicit.stat_691932474@T2` | -0.90125 |
| `explicit.stat_748522257@T2` | -0.85133 |
| `desecrated.stat_210067635@T1` | -0.81722 |
| `explicit.stat_9187492@T2` | -0.78300 |

### armour.focus — n=6985, R²=-0.3394

intercept: `-15.6029`  ·  log_price: True  ·  ilvl: `0.19954`  ·  n_mods: `-0.16209`  ·  n_top_tier: `0.96359`  ·  corrupted: `0.12601`  ·  n_sockets: `0.23216`  ·  quality: `0.05263`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 3.95578 |
| `explicit.stat_2923486259@T1` | -1.67608 |
| `explicit.stat_4220027924@T1` | -1.53885 |
| `explicit.stat_4220027924@T2` | -1.33623 |
| `explicit.stat_2339757871@T2` | -1.12373 |
| `explicit.stat_274716455@T1` | -1.07187 |
| `explicit.stat_2923486259@T2` | -1.06693 |
| `explicit.stat_2231156303@T1` | -1.06192 |
| `explicit.stat_274716455@T2` | -1.05967 |
| `explicit.stat_4015621042@T1` | -1.05072 |
| `explicit.stat_1050105434@T2` | -0.99387 |
| `explicit.stat_1050105434@T1` | -0.96676 |

### armour.quiver — n=6540, R²=-0.291

intercept: `-16.7152`  ·  log_price: True  ·  ilvl: `0.20731`  ·  n_mods: `-0.13009`  ·  n_top_tier: `0.80357`  ·  corrupted: `0.83361`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.17000 |
| `explicit.stat_2463230181@T1` | 1.71127 |
| `explicit.stat_681332047@T2` | -1.41380 |
| `explicit.stat_1573130764@T1` | -1.39005 |
| `explicit.stat_1573130764@T2` | -1.15602 |
| `explicit.stat_681332047@T1` | -1.10887 |
| `explicit.stat_4067062424@T1` | -1.00455 |
| `explicit.stat_2463230181@T2` | 0.99749 |
| `explicit.stat_803737631@T1` | -0.93210 |
| `explicit.stat_803737631@T2` | -0.89639 |
| `explicit.stat_2321178454@T2` | -0.85842 |
| `explicit.stat_4067062424@T2` | -0.77703 |

### armour.shield — n=5615, R²=-0.4242

intercept: `-13.6866`  ·  log_price: True  ·  ilvl: `0.18073`  ·  n_mods: `-0.12376`  ·  n_top_tier: `0.73682`  ·  corrupted: `-0.33904`  ·  n_sockets: `0.36925`  ·  quality: `0.06038`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.03438 |
| `explicit.stat_2339757871@T2` | -1.28446 |
| `explicit.stat_3321629045@T2` | -1.21801 |
| `explicit.stat_3484657501@T1` | -1.13535 |
| `explicit.stat_3855016469@T1` | -1.07420 |
| `explicit.stat_2451402625@T1` | -1.06186 |
| `explicit.stat_4095671657@T2` | -1.05489 |
| `explicit.stat_328541901@T1` | -1.01184 |
| `explicit.stat_2901986750@T1` | -0.98286 |
| `explicit.stat_3484657501@T2` | -0.96112 |
| `explicit.stat_4220027924@T1` | -0.89565 |
| `explicit.stat_3033371881@T2` | -0.88633 |

### weapon.twomace — n=5178, R²=-0.4445

intercept: `-10.5831`  ·  log_price: True  ·  ilvl: `0.14390`  ·  n_mods: `-0.21070`  ·  n_top_tier: `0.37355`  ·  corrupted: `0.55784`  ·  n_sockets: `0.13633`  ·  quality: `0.06275`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.27717 |
| `explicit.stat_1037193709@T1` | -1.57764 |
| `explicit.stat_3336890334@T1` | -1.12083 |
| `explicit.stat_1263695895@T2` | -1.10908 |
| `explicit.stat_2694482655@T1` | 0.93608 |
| `explicit.stat_9187492@T1` | -0.81488 |
| `explicit.stat_518292764@T1` | 0.77269 |
| `explicit.stat_387439868@T2` | -0.73246 |
| `explicit.stat_691932474@T1` | -0.70350 |
| `explicit.stat_3695891184@T1` | -0.69619 |
| `explicit.stat_3695891184@T2` | -0.67635 |
| `explicit.stat_387439868@T1` | -0.58105 |

## Coverage (listings per base)

- … **Sapphire** — 33791 listings (33735 priced) [0.3–3985176410.3 ex]
- … **Emerald** — 32917 listings (32875 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 25283 listings (25253 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 12086 listings (12068 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 10875 listings (10851 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 10524 listings (10500 priced) [1.0–3985176410.3 ex]
- … **Amethyst Ring** — 10434 listings (10423 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 9816 listings (9794 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 9750 listings (9728 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 9332 listings (9319 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 8080 listings (8065 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 7785 listings (7776 priced) [0.3–3985176410.3 ex]
- … **Ruby Ring** — 7681 listings (7672 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7129 listings (7107 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6722 listings (6715 priced) [0.3–19945827.9 ex]
- … **Unset Ring** — 6651 listings (6632 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 6644 listings (6630 priced) [0.3–4547453.5 ex]
- … **Plate Belt** — 6613 listings (6585 priced) [0.3–398912568423.8 ex]
- … **Amber Amulet** — 6610 listings (6603 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 6496 listings (6467 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 6405 listings (6395 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 6401 listings (6392 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 6079 listings (6076 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 5982 listings (5968 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5854 listings (5844 priced) [0.3–398912568423.8 ex]
