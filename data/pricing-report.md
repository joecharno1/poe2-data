# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-13T10:52:22+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **419674** (418899 priced in exalted)
- Distinct bases: 970 · distinct mods: 2977 · mod rows: 1994852
- Sold signals: **27742** sold · 226658 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-13T10:41:38+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×23.32** (median |log error| 3.1494)
- Within ±30% of asking price: **18%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.09** · typical error ×64.33 · ±30% 5% · n=60860
- Premium segment (60ex+): skill **+0.10** · typical error ×330.00 · ±30% 0% · n=39505

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 8153 | ×51.37 | 21% | +0.03 | +0.04 |
| accessory.amulet | 7651 | ×36.84 | 20% | +0.02 | +0.03 |
| jewel | 7471 | ×8.28 | 7% | +0.02 | +0.05 |
| accessory.belt | 6039 | ×21.37 | 5% | +0.04 | +0.06 |
| armour.chest | 5866 | ×19.30 | 19% | +0.06 | +0.08 |
| armour.helmet | 5758 | ×25.77 | 12% | +0.08 | +0.10 |
| armour.boots | 5373 | ×24.30 | 22% | +0.05 | +0.07 |
| armour.gloves | 5251 | ×38.65 | 16% | +0.05 | +0.08 |
| other | 4777 | ×2.10 | 42% | +0.09 | +0.16 |
| weapon.wand | 3450 | ×38.65 | 20% | +0.06 | +0.07 |
| weapon.bow | 2792 | ×30.65 | 17% | +0.08 | +0.11 |
| weapon.crossbow | 2613 | ×22.29 | 21% | +0.10 | +0.13 |
| weapon.warstaff | 1455 | ×77.99 | 17% | +0.08 | +0.08 |
| weapon.staff | 1366 | ×60.00 | 17% | +0.06 | +0.07 |
| weapon.sceptre | 1360 | ×76.26 | 14% | +0.08 | +0.08 |
| weapon.spear | 1161 | ×49.99 | 18% | +0.07 | +0.07 |
| armour.focus | 959 | ×32.67 | 14% | +0.13 | +0.13 |
| armour.quiver | 890 | ×28.69 | 16% | +0.04 | +0.10 |
| armour.shield | 776 | ×15.03 | 16% | +0.04 | +0.06 |
| weapon.twomace | 681 | ×21.00 | 14% | +0.06 | +0.08 |
| flask.charm | 639 | ×10.00 | 36% | +0.01 | +0.01 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=41502, R²=-0.6306

intercept: `1.6068`  ·  log_price: True  ·  ilvl: `0.00003`  ·  n_mods: `0.01432`  ·  n_top_tier: `0.33250`  ·  corrupted: `0.34921`  ·  n_sockets: `-0.00005`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.54230 |
| `explicit.stat_2974417149@T1` | 0.46761 |
| `explicit.stat_789117908@T1` | -0.31977 |
| `explicit.stat_3917489142@T1` | 0.26778 |
| `explicit.stat_1050105434@T1` | -0.25872 |
| `explicit.stat_3299347043@T1` | -0.24549 |
| `explicit.stat_2891184298@T1` | 0.23738 |
| `explicit.stat_2106365538@T1` | 0.23371 |
| `implicit.stat_4041853756` | 0.22883 |
| `implicit.stat_3879011313` | 0.22882 |
| `implicit.stat_1379411836` | -0.18602 |
| `explicit.stat_101878827@T1` | -0.10515 |

### jewel — n=39910, R²=-0.7305

intercept: `-1.3179`  ·  log_price: True  ·  ilvl: `0.03403`  ·  n_mods: `0.38382`  ·  n_top_tier: `-0.15935`  ·  corrupted: `0.10769`  ·  quality: `0.23474`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.74190 |
| `explicit.stat_3780644166@T1` | -3.56832 |
| `explicit.stat_3741323227@T1` | -2.59257 |
| `explicit.stat_234296660@T1` | -2.56260 |
| `explicit.stat_3174700878@T1` | 2.45991 |
| `explicit.stat_1315743832@T1` | 2.09863 |
| `explicit.stat_2527686725@T1` | 2.07091 |
| `explicit.stat_3714003708@T1` | -1.95409 |
| `explicit.stat_21071013@T1` | 1.93367 |
| `explicit.stat_627767961@T1` | -1.90065 |
| `explicit.stat_1569101201@T1` | 1.89580 |
| `explicit.stat_3485067555@T1` | 1.89311 |

### accessory.ring — n=37495, R²=-1.9434

intercept: `3.6757`  ·  log_price: True  ·  ilvl: `-0.04514`  ·  n_mods: `0.00402`  ·  n_top_tier: `0.30628`  ·  corrupted: `0.37345`  ·  n_sockets: `-0.15299`  ·  quality: `0.03086`

| stat_id | coef |
|---|---|
| `explicit.stat_1671376347@T1` | 1.20339 |
| `explicit.stat_1263695895@T1` | -0.36813 |
| `explicit.stat_2231156303@T1` | -0.35452 |
| `explicit.stat_3291658075@T2` | -0.35187 |
| `explicit.stat_1368271171@T1` | -0.34349 |
| `explicit.stat_1368271171@T2` | -0.34140 |
| `explicit.stat_3032590688@T2` | -0.33748 |
| `explicit.stat_4220027924@T2` | -0.33697 |
| `explicit.stat_3325883026@T1` | -0.33442 |
| `explicit.stat_4067062424@T1` | -0.33323 |
| `explicit.stat_1263695895@T2` | -0.33045 |
| `explicit.stat_2231156303@T2` | -0.32953 |

### accessory.amulet — n=35014, R²=-2.0964

intercept: `3.9506`  ·  log_price: True  ·  ilvl: `-0.04749`  ·  n_mods: `-0.02511`  ·  n_top_tier: `0.77895`  ·  corrupted: `0.04749`  ·  n_sockets: `-0.17584`  ·  quality: `0.00073`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -1.64401 |
| `explicit.stat_983749596@T2` | -1.38537 |
| `explicit.stat_124131830@T2` | -1.22142 |
| `explicit.stat_124131830` | 0.97098 |
| `explicit.stat_2748665614@T1` | -0.90665 |
| `explicit.stat_2748665614@T2` | -0.89217 |
| `explicit.stat_2901986750@T1` | -0.86200 |
| `explicit.stat_3917489142@T2` | -0.84894 |
| `explicit.stat_3917489142@T1` | -0.84863 |
| `explicit.stat_472520716@T1` | -0.83543 |
| `explicit.stat_1050105434@T2` | -0.83340 |
| `explicit.stat_3299347043@T2` | -0.82872 |

### accessory.belt — n=27538, R²=-0.8508

intercept: `6.2270`  ·  log_price: True  ·  ilvl: `-0.05788`  ·  n_mods: `-0.30982`  ·  n_top_tier: `0.80222`  ·  corrupted: `1.19232`  ·  n_sockets: `0.28013`

| stat_id | coef |
|---|---|
| `explicit.stat_1389754388@T1` | -1.34285 |
| `explicit.stat_51994685@T1` | -1.19686 |
| `explicit.stat_809229260@T2` | -1.16558 |
| `explicit.stat_2881298780@T1` | -1.03156 |
| `explicit.stat_1389754388@T2` | -1.01827 |
| `explicit.stat_1671376347@T2` | -0.96047 |
| `explicit.stat_644456512@T1` | -0.92037 |
| `explicit.stat_3299347043@T2` | -0.91492 |
| `explicit.stat_4220027924@T2` | -0.91122 |
| `explicit.stat_3325883026@T1` | -0.89858 |
| `explicit.stat_3299347043@T1` | -0.87753 |
| `explicit.stat_1050105434@T1` | -0.82419 |

### armour.chest — n=27278, R²=-1.5884

intercept: `3.8318`  ·  log_price: True  ·  ilvl: `-0.04727`  ·  n_mods: `-0.02034`  ·  n_top_tier: `0.34516`  ·  corrupted: `0.10214`  ·  n_sockets: `0.02366`  ·  quality: `0.03489`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.29782 |
| `explicit.stat_3981240776@T1` | 1.30400 |
| `explicit.stat_4015621042@T1` | -0.41746 |
| `explicit.stat_4080418644@T2` | -0.40062 |
| `explicit.stat_915769802@T1` | -0.38779 |
| `explicit.stat_3261801346@T2` | -0.37900 |
| `explicit.stat_124859000@T2` | -0.37826 |
| `explicit.stat_3484657501@T1` | -0.37513 |
| `explicit.stat_1999113824@T1` | -0.37308 |
| `explicit.stat_915769802@T2` | -0.37199 |
| `explicit.stat_1692879867@T1` | -0.36913 |
| `explicit.stat_3325883026@T2` | -0.36759 |

### armour.helmet — n=26611, R²=-1.3716

intercept: `4.2789`  ·  log_price: True  ·  ilvl: `-0.05416`  ·  n_mods: `-0.03597`  ·  n_top_tier: `0.46130`  ·  corrupted: `0.77641`  ·  n_sockets: `0.04684`  ·  quality: `0.05006`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.95372 |
| `crafted.stat_3917489142@T1` | 2.82733 |
| `explicit.stat_53045048@T1` | -0.77801 |
| `explicit.stat_1263695895@T1` | -0.72157 |
| `explicit.stat_53045048@T2` | -0.63565 |
| `explicit.stat_587431675@T2` | -0.63252 |
| `explicit.stat_1263695895@T2` | -0.62248 |
| `explicit.stat_2162097452@T2` | -0.60318 |
| `explicit.stat_3917489142@T2` | -0.59072 |
| `explicit.stat_1999113824@T1` | -0.59069 |
| `explicit.stat_4220027924@T1` | 0.56542 |
| `explicit.stat_3261801346@T2` | -0.54131 |

### armour.boots — n=24934, R²=-1.6399

intercept: `3.6733`  ·  log_price: True  ·  ilvl: `-0.04518`  ·  n_mods: `-0.00915`  ·  n_top_tier: `0.63293`  ·  corrupted: `0.02243`  ·  n_sockets: `0.00368`  ·  quality: `0.01813`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.61270 |
| `desecrated.stat_2250533757@T2` | -0.96495 |
| `explicit.stat_3917489142@T2` | -0.76811 |
| `explicit.stat_3917489142@T1` | -0.72159 |
| `explicit.stat_3362812763@T1` | -0.68596 |
| `explicit.stat_2923486259@T2` | -0.66966 |
| `explicit.stat_3362812763@T2` | -0.66718 |
| `explicit.stat_1062208444@T2` | -0.66111 |
| `explicit.stat_2160282525@T1` | -0.65908 |
| `explicit.stat_53045048@T1` | -0.65029 |
| `explicit.stat_1671376347@T2` | -0.64960 |
| `explicit.stat_2160282525@T2` | -0.64779 |

### armour.gloves — n=24301, R²=-1.594

intercept: `4.1432`  ·  log_price: True  ·  ilvl: `-0.05369`  ·  n_mods: `-0.02056`  ·  n_top_tier: `0.36289`  ·  corrupted: `0.00437`  ·  n_sockets: `0.10826`  ·  quality: `0.03496`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 2.26936 |
| `explicit.stat_1671376347@T1` | 0.87748 |
| `explicit.stat_9187492@T1` | 0.83585 |
| `explicit.stat_3484657501@T2` | -0.79769 |
| `rune.stat_201332984` | 0.72552 |
| `explicit.stat_9187492@T2` | -0.66963 |
| `explicit.stat_1999113824@T1` | 0.61808 |
| `explicit.stat_3917489142@T2` | -0.61448 |
| `explicit.stat_803737631@T2` | -0.59512 |
| `explicit.stat_3321629045@T1` | -0.53822 |
| `explicit.stat_681332047@T2` | -0.51707 |
| `explicit.stat_3484657501@T1` | -0.51329 |

### weapon.wand — n=16036, R²=-2.17

intercept: `4.0749`  ·  log_price: True  ·  ilvl: `-0.05061`  ·  n_mods: `-0.01374`  ·  n_top_tier: `0.35676`  ·  corrupted: `-0.03685`  ·  n_sockets: `0.04372`  ·  quality: `0.00696`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 3.12128 |
| `explicit.stat_1545858329@T1` | 3.08721 |
| `rune.stat_124131830` | -2.96535 |
| `explicit.stat_591105508@T1` | 2.04621 |
| `explicit.stat_4226189338@T1` | 1.99516 |
| `explicit.stat_736967255@T2` | 1.71581 |
| `explicit.stat_124131830@T1` | 1.33366 |
| `explicit.stat_1600707273@T1` | 1.25676 |
| `crafted.stat_124131830` | 1.22309 |
| `explicit.stat_2768835289@T2` | 0.84956 |
| `explicit.stat_1600707273@T2` | 0.47044 |
| `explicit.stat_737908626@T1` | -0.39655 |

### weapon.bow — n=13060, R²=-1.9792

intercept: `3.4964`  ·  log_price: True  ·  ilvl: `-0.04268`  ·  n_mods: `-0.02457`  ·  n_top_tier: `0.65543`  ·  corrupted: `-0.05969`  ·  n_sockets: `-0.00704`  ·  quality: `0.03363`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.22660 |
| `explicit.stat_1202301673@T1` | 1.51691 |
| `crafted.stat_3035140377` | 1.32222 |
| `desecrated.stat_666077204@T1` | 1.19725 |
| `explicit.stat_2463230181@T1` | 0.95283 |
| `explicit.stat_55876295@T1` | -0.71876 |
| `explicit.stat_1263695895@T1` | -0.71670 |
| `explicit.stat_669069897@T1` | -0.70852 |
| `explicit.stat_3336890334@T2` | -0.69749 |
| `explicit.stat_3695891184@T1` | -0.69596 |
| `explicit.stat_2694482655@T1` | -0.69269 |
| `explicit.stat_1037193709@T1` | -0.69019 |

### weapon.crossbow — n=12343, R²=-1.8995

intercept: `3.8020`  ·  log_price: True  ·  ilvl: `-0.04683`  ·  n_mods: `-0.01501`  ·  n_top_tier: `0.70514`  ·  corrupted: `-0.04172`  ·  n_sockets: `0.03018`  ·  quality: `0.00143`

| stat_id | coef |
|---|---|
| `explicit.stat_2250681686@T2` | -2.06492 |
| `explicit.stat_1980802737@T2` | -1.92041 |
| `explicit.stat_709508406@T1` | 1.44422 |
| `explicit.stat_1202301673@T1` | 1.42007 |
| `explicit.stat_2250681686` | 1.39884 |
| `explicit.stat_1980802737` | 1.16571 |
| `explicit.stat_1263695895@T2` | -0.88256 |
| `explicit.stat_1202301673@T2` | -0.84336 |
| `crafted.stat_3035140377` | 0.84049 |
| `explicit.stat_1509134228@T1` | 0.83166 |
| `explicit.stat_1509134228@T2` | -0.79124 |
| `explicit.stat_1263695895@T1` | -0.77843 |

### flask.charm — n=10049, R²=-0.4557

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.07452`  ·  corrupted: `1.55615`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.72080 |
| `explicit.stat_1056492907` | 3.21881 |
| `explicit.stat_2676834156@T1` | 1.53833 |
| `explicit.stat_2541588185@T1` | 0.40784 |
| `explicit.stat_828533480@T2` | -0.07453 |
| `explicit.stat_1120862500@T2` | -0.07452 |
| `explicit.stat_1873752457@T2` | -0.07451 |
| `explicit.stat_1366840608@T2` | -0.07451 |
| `explicit.stat_1873752457@T1` | -0.07451 |
| `explicit.stat_3196823591@T2` | -0.07451 |
| `explicit.stat_388617051@T2` | -0.07451 |
| `explicit.stat_2676834156@T2` | -0.07451 |

### weapon.warstaff — n=6926, R²=-0.613

intercept: `-0.9234`  ·  log_price: True  ·  ilvl: `0.01250`  ·  n_mods: `-0.03411`  ·  n_top_tier: `0.37481`  ·  corrupted: `0.11714`  ·  n_sockets: `0.02321`  ·  quality: `0.05393`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.54213 |
| `explicit.stat_9187492@T1` | 0.79592 |
| `rune.stat_731403740` | 0.77596 |
| `desecrated.stat_9187492` | 0.52650 |
| `crafted.stat_3035140377` | 0.51407 |
| `explicit.stat_328541901@T1` | -0.44131 |
| `explicit.stat_328541901@T2` | -0.43573 |
| `explicit.stat_3336890334@T2` | -0.40723 |
| `explicit.stat_1368271171@T1` | -0.40504 |
| `explicit.stat_821021828@T1` | -0.40338 |
| `explicit.stat_1037193709@T1` | 0.40020 |
| `explicit.stat_691932474@T2` | -0.39238 |

### weapon.sceptre — n=6444, R²=-0.5367

intercept: `-8.2925`  ·  log_price: True  ·  ilvl: `0.10366`  ·  n_mods: `-0.01380`  ·  n_top_tier: `0.11838`  ·  corrupted: `0.61863`  ·  n_sockets: `0.14477`  ·  quality: `0.08556`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.78391 |
| `explicit.stat_2162097452@T2` | 1.58077 |
| `explicit.stat_1798257884@T2` | 0.83452 |
| `explicit.stat_4080418644@T1` | -0.54090 |
| `explicit.stat_3984865854@T2` | 0.53650 |
| `explicit.stat_3984865854@T1` | 0.51332 |
| `explicit.stat_1263695895@T2` | -0.43829 |
| `explicit.stat_328541901@T2` | 0.37591 |
| `explicit.stat_1263695895@T1` | -0.35784 |
| `explicit.stat_4080418644@T2` | -0.35532 |
| `explicit.stat_2347036682@T1` | 0.34575 |
| `explicit.stat_101878827@T2` | 0.34532 |

### weapon.staff — n=6409, R²=-0.6564

intercept: `-1.2036`  ·  log_price: True  ·  ilvl: `0.01508`  ·  n_mods: `-0.00644`  ·  n_top_tier: `0.50940`  ·  corrupted: `0.04213`  ·  n_sockets: `0.04908`  ·  quality: `0.06856`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 2.30042 |
| `explicit.stat_4226189338@T1` | 1.79832 |
| `explicit.stat_1600707273@T1` | 1.66249 |
| `explicit.stat_1545858329@T1` | 1.57578 |
| `explicit.stat_2254480358@T1` | 1.51309 |
| `explicit.stat_124131830@T1` | 1.06715 |
| `explicit.stat_2768835289@T2` | 1.01389 |
| `explicit.stat_2254480358@T2` | 0.79621 |
| `explicit.stat_3291658075@T2` | 0.64558 |
| `explicit.stat_2974417149@T1` | -0.55716 |
| `explicit.stat_591105508@T1` | -0.54562 |
| `crafted.stat_124131830` | 0.54546 |

### weapon.spear — n=5473, R²=-0.6827

intercept: `-0.4727`  ·  log_price: True  ·  ilvl: `0.00616`  ·  n_mods: `-0.00283`  ·  n_top_tier: `0.38395`  ·  corrupted: `-0.01957`  ·  n_sockets: `0.00980`  ·  quality: `0.10619`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 2.31991 |
| `explicit.stat_9187492@T1` | 2.10757 |
| `crafted.stat_210067635@T2` | -1.94164 |
| `crafted.stat_3035140377` | 1.26627 |
| `explicit.stat_210067635@T1` | 0.69472 |
| `crafted.stat_518292764` | 0.63300 |
| `explicit.stat_1509134228@T1` | 0.56993 |
| `explicit.stat_55876295@T1` | -0.40066 |
| `explicit.stat_691932474@T1` | -0.39727 |
| `explicit.stat_4080418644@T2` | -0.39284 |
| `explicit.stat_1263695895@T2` | -0.39201 |
| `explicit.stat_9187492@T2` | -0.39066 |

### armour.focus — n=4501, R²=-0.519

intercept: `-6.9387`  ·  log_price: True  ·  ilvl: `0.08570`  ·  n_mods: `-0.01359`  ·  n_top_tier: `0.93170`  ·  corrupted: `0.72999`  ·  n_sockets: `0.28766`  ·  quality: `0.06899`

| stat_id | coef |
|---|---|
| `desecrated.stat_378817135@T1` | 6.12695 |
| `explicit.stat_4220027924@T1` | -1.23685 |
| `explicit.stat_4220027924@T2` | -1.15288 |
| `explicit.stat_2923486259@T1` | -1.15149 |
| `crafted.stat_2974417149@T1` | 1.14419 |
| `explicit.stat_2891184298@T2` | -1.05752 |
| `explicit.stat_2891184298@T1` | -1.05151 |
| `explicit.stat_736967255@T2` | -1.04169 |
| `explicit.stat_2974417149@T1` | -0.96976 |
| `explicit.stat_3962278098@T2` | -0.96393 |
| `explicit.stat_737908626@T2` | -0.93923 |
| `explicit.stat_3962278098@T1` | -0.90234 |

### armour.quiver — n=4195, R²=-0.5484

intercept: `-5.5434`  ·  log_price: True  ·  ilvl: `0.06578`  ·  n_mods: `0.00643`  ·  n_top_tier: `0.70981`  ·  corrupted: `0.27696`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 7.83900 |
| `explicit.stat_2463230181@T1` | 1.50623 |
| `explicit.stat_2321178454@T2` | -0.96273 |
| `explicit.stat_2194114101@T2` | -0.92219 |
| `explicit.stat_681332047@T2` | -0.92079 |
| `explicit.stat_1573130764@T1` | -0.89909 |
| `explicit.stat_1368271171@T2` | -0.84814 |
| `explicit.stat_1573130764@T2` | -0.78491 |
| `explicit.stat_2463230181@T2` | 0.77064 |
| `explicit.stat_3261801346@T1` | -0.74800 |
| `explicit.stat_4067062424@T1` | -0.74431 |
| `explicit.stat_2321178454@T1` | -0.67950 |

### armour.shield — n=3685, R²=-0.5901

intercept: `-5.5061`  ·  log_price: True  ·  ilvl: `0.06889`  ·  n_mods: `0.00263`  ·  n_top_tier: `0.47292`  ·  corrupted: `0.31729`  ·  n_sockets: `0.00917`  ·  quality: `0.05291`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -0.92919 |
| `explicit.stat_1011760251@T1` | -0.87926 |
| `explicit.stat_328541901@T1` | -0.86884 |
| `explicit.stat_1978899297@T1` | 0.83666 |
| `explicit.stat_1011760251@T2` | -0.82658 |
| `explicit.stat_2481353198@T2` | -0.74118 |
| `explicit.stat_1978899297@T2` | -0.72616 |
| `explicit.stat_2481353198@T1` | -0.71758 |
| `explicit.stat_3362812763@T1` | -0.69566 |
| `explicit.stat_1301765461@T1` | 0.68428 |
| `explicit.stat_328541901@T2` | -0.67299 |
| `explicit.stat_2901986750@T1` | -0.64317 |

### weapon.twomace — n=3323, R²=-0.4999

intercept: `-7.4510`  ·  log_price: True  ·  ilvl: `0.09620`  ·  n_mods: `-0.08135`  ·  n_top_tier: `0.46028`  ·  corrupted: `0.82917`  ·  n_sockets: `0.10393`  ·  quality: `0.04553`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.47962 |
| `desecrated.stat_1509134228@T1` | 2.08056 |
| `explicit.stat_1037193709@T1` | -1.23564 |
| `crafted.stat_3035140377` | 1.06932 |
| `explicit.stat_1509134228@T1` | 0.94538 |
| `explicit.stat_3336890334@T1` | -0.93611 |
| `explicit.stat_1263695895@T1` | -0.84407 |
| `explicit.stat_1263695895@T2` | -0.83654 |
| `explicit.stat_1037193709@T2` | -0.77449 |
| `explicit.stat_387439868@T2` | -0.74713 |
| `explicit.stat_709508406@T1` | -0.74610 |
| `explicit.stat_210067635@T1` | 0.71020 |

## Coverage (listings per base)

- … **Sapphire** — 18754 listings (18729 priced) [0.3–7553463.8 ex]
- … **Emerald** — 18511 listings (18491 priced) [0.3–7553463.8 ex]
- … **Ruby** — 14272 listings (14260 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 8146 listings (8137 priced) [0.2–3985176410.3 ex]
- … **Prismatic Ring** — 6471 listings (6464 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 6293 listings (6281 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 6208 listings (6204 priced) [0.2–19945827.9 ex]
- … **Stellar Amulet** — 5992 listings (5989 priced) [0.3–35690283.3 ex]
- … **Gold Amulet** — 5943 listings (5933 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 5800 listings (5794 priced) [0.2–24532814.5 ex]
- … **Dueling Wand** — 5080 listings (5068 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 4816 listings (4811 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 4675 listings (4672 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 4664 listings (4662 priced) [0.2–37474957.5 ex]
- … **Plate Belt** — 4254 listings (4248 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 4189 listings (4185 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 4127 listings (4120 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 4070 listings (4068 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 4053 listings (4049 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 3988 listings (3986 priced) [0.2–24532814.5 ex]
- … **Obliterator Bow** — 3906 listings (3895 priced) [0.3–42622633798.0 ex]
- … **Bloodstone Amulet** — 3895 listings (3891 priced) [0.3–4275054.0 ex]
- … **Heavy Belt** — 3843 listings (3841 priced) [0.3–2608914286.6 ex]
- … **Pearl Ring** — 3741 listings (3738 priced) [0.2–275252424.7 ex]
- … **Lunar Amulet** — 3678 listings (3674 priced) [0.3–4877938.3 ex]
