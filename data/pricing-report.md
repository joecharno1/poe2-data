# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-13T04:49:01+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **407813** (407068 priced in exalted)
- Distinct bases: 969 · distinct mods: 2960 · mod rows: 1937931
- Sold signals: **28012** sold · 219309 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-13T04:40:18+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×24.94** (median |log error| 3.2163)
- Within ±30% of asking price: **18%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.09** · typical error ×64.46 · ±30% 5% · n=59155
- Premium segment (60ex+): skill **+0.09** · typical error ×304.66 · ±30% 0% · n=38089

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 7915 | ×54.41 | 21% | +0.03 | +0.06 |
| accessory.amulet | 7396 | ×48.31 | 20% | +0.02 | +0.03 |
| jewel | 7181 | ×8.06 | 7% | +0.02 | +0.04 |
| accessory.belt | 5857 | ×21.59 | 5% | +0.03 | +0.05 |
| armour.chest | 5684 | ×19.97 | 19% | +0.06 | +0.08 |
| armour.helmet | 5531 | ×21.97 | 11% | +0.09 | +0.11 |
| armour.boots | 5210 | ×22.46 | 21% | +0.06 | +0.08 |
| armour.gloves | 5117 | ×40.74 | 19% | +0.04 | +0.07 |
| other | 4798 | ×3.66 | 41% | +0.08 | +0.16 |
| weapon.wand | 3309 | ×44.39 | 21% | +0.06 | +0.05 |
| weapon.bow | 2681 | ×29.61 | 18% | +0.08 | +0.10 |
| weapon.crossbow | 2540 | ×22.80 | 22% | +0.09 | +0.11 |
| weapon.warstaff | 1455 | ×78.14 | 17% | +0.08 | +0.08 |
| weapon.sceptre | 1308 | ×79.46 | 13% | +0.08 | +0.09 |
| weapon.staff | 1307 | ×64.72 | 15% | +0.06 | +0.08 |
| weapon.spear | 1111 | ×48.62 | 19% | +0.06 | +0.07 |
| armour.focus | 928 | ×44.71 | 15% | +0.12 | +0.14 |
| armour.quiver | 833 | ×34.58 | 15% | +0.04 | +0.09 |
| armour.shield | 711 | ×22.98 | 17% | +0.03 | +0.07 |
| weapon.twomace | 651 | ×22.98 | 14% | +0.06 | +0.09 |
| flask.charm | 572 | ×5.00 | 40% | +0.01 | -0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=40401, R²=-0.6281

intercept: `1.6078`  ·  log_price: True  ·  ilvl: `0.00002`  ·  n_mods: `0.00593`  ·  n_top_tier: `0.34237`  ·  corrupted: `0.39830`  ·  n_sockets: `-0.00004`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.61933 |
| `explicit.stat_2974417149@T1` | 0.52922 |
| `explicit.stat_2106365538@T1` | 0.34803 |
| `explicit.stat_2891184298@T1` | 0.34516 |
| `explicit.stat_789117908@T1` | -0.34375 |
| `explicit.stat_1050105434@T1` | -0.31147 |
| `explicit.stat_3299347043@T1` | -0.28044 |
| `explicit.stat_3917489142@T1` | 0.26075 |
| `implicit.stat_1379411836` | -0.23071 |
| `implicit.stat_4041853756` | 0.22967 |
| `implicit.stat_3879011313` | 0.22966 |
| `explicit.stat_101878827@T1` | -0.19472 |

### jewel — n=38522, R²=-0.7145

intercept: `-1.3298`  ·  log_price: True  ·  ilvl: `0.03438`  ·  n_mods: `0.30142`  ·  n_top_tier: `-0.08090`  ·  corrupted: `0.12078`  ·  quality: `0.23741`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -4.92767 |
| `explicit.stat_3780644166@T1` | -3.16938 |
| `explicit.stat_3741323227@T1` | -2.85481 |
| `explicit.stat_1569101201@T1` | 2.41153 |
| `explicit.stat_3485067555@T1` | 2.29986 |
| `explicit.stat_627767961@T1` | -2.18362 |
| `explicit.stat_234296660@T1` | -2.06732 |
| `explicit.stat_795138349@T1` | -2.01087 |
| `explicit.stat_1423639565@T1` | -2.00132 |
| `explicit.stat_1315743832@T1` | 1.97120 |
| `explicit.stat_1697951953@T1` | -1.85920 |
| `explicit.stat_3174700878@T1` | 1.82518 |

### accessory.ring — n=36347, R²=-1.9177

intercept: `4.5021`  ·  log_price: True  ·  ilvl: `-0.05509`  ·  n_mods: `0.00392`  ·  n_top_tier: `0.11741`  ·  corrupted: `0.57183`  ·  n_sockets: `-0.51440`  ·  quality: `0.01121`

| stat_id | coef |
|---|---|
| `explicit.stat_1671376347@T1` | 1.22016 |
| `explicit.stat_3032590688@T1` | 0.21370 |
| `explicit.stat_1263695895@T1` | -0.18870 |
| `implicit.stat_2748665614` | -0.18331 |
| `explicit.stat_3325883026@T1` | -0.17831 |
| `explicit.stat_1967040409` | 0.16792 |
| `explicit.stat_3291658075@T2` | -0.16197 |
| `explicit.stat_1368271171@T2` | -0.15832 |
| `explicit.stat_1368271171@T1` | -0.15611 |
| `explicit.stat_2231156303@T1` | -0.15489 |
| `explicit.stat_1050105434@T2` | -0.14786 |
| `explicit.stat_1573130764@T1` | -0.14447 |

### accessory.amulet — n=33970, R²=-2.1088

intercept: `4.1148`  ·  log_price: True  ·  ilvl: `-0.04960`  ·  n_mods: `-0.02852`  ·  n_top_tier: `0.69254`  ·  corrupted: `0.07532`  ·  n_sockets: `0.15380`  ·  quality: `-0.00002`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T2` | -1.06052 |
| `explicit.stat_124131830` | 1.04520 |
| `explicit.stat_983749596@T1` | -0.95395 |
| `explicit.stat_3981240776@T2` | 0.90572 |
| `explicit.stat_983749596@T2` | -0.87622 |
| `explicit.stat_3556824919@T1` | 0.85965 |
| `explicit.stat_2748665614@T2` | -0.78079 |
| `explicit.stat_2748665614@T1` | -0.77822 |
| `explicit.stat_3981240776@T1` | 0.75932 |
| `explicit.stat_2106365538@T1` | -0.75840 |
| `explicit.stat_3917489142@T2` | -0.75587 |
| `explicit.stat_3917489142@T1` | -0.75472 |

### accessory.belt — n=26806, R²=-0.8634

intercept: `6.5943`  ·  log_price: True  ·  ilvl: `-0.06029`  ·  n_mods: `-0.31292`  ·  n_top_tier: `0.67217`  ·  corrupted: `1.09121`  ·  n_sockets: `0.20226`

| stat_id | coef |
|---|---|
| `implicit.stat_731781020` | -1.21604 |
| `explicit.stat_1389754388@T1` | -1.16197 |
| `explicit.stat_51994685@T1` | -1.11536 |
| `explicit.stat_2881298780@T1` | -1.08042 |
| `explicit.stat_809229260@T2` | -0.96760 |
| `explicit.stat_3325883026@T1` | -0.80160 |
| `explicit.stat_1671376347@T2` | -0.78530 |
| `explicit.stat_3299347043@T2` | -0.77682 |
| `explicit.stat_1389754388@T2` | -0.72699 |
| `explicit.stat_2881298780@T2` | -0.72371 |
| `explicit.stat_4220027924@T2` | -0.70639 |
| `explicit.stat_3299347043@T1` | -0.69703 |

### armour.chest — n=26501, R²=-1.5451

intercept: `3.9444`  ·  log_price: True  ·  ilvl: `-0.04861`  ·  n_mods: `-0.02263`  ·  n_top_tier: `0.40746`  ·  corrupted: `0.06791`  ·  n_sockets: `0.02442`  ·  quality: `0.03415`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.30433 |
| `explicit.stat_3981240776@T1` | 1.25387 |
| `explicit.stat_4015621042@T1` | -0.53410 |
| `explicit.stat_4080418644@T2` | -0.48318 |
| `explicit.stat_915769802@T1` | -0.47526 |
| `explicit.stat_4080418644@T1` | -0.47328 |
| `explicit.stat_4015621042@T2` | -0.47175 |
| `explicit.stat_3261801346@T2` | -0.44665 |
| `explicit.stat_915769802@T2` | -0.44590 |
| `explicit.stat_3325883026@T2` | -0.43906 |
| `explicit.stat_986397080@T2` | -0.43763 |
| `explicit.stat_1692879867@T1` | -0.43363 |

### armour.helmet — n=25869, R²=-1.3016

intercept: `4.2511`  ·  log_price: True  ·  ilvl: `-0.05354`  ·  n_mods: `-0.04168`  ·  n_top_tier: `0.46045`  ·  corrupted: `0.65894`  ·  n_sockets: `0.05074`  ·  quality: `0.04993`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 5.48266 |
| `explicit.stat_2339757871@T1` | -4.06081 |
| `explicit.stat_53045048@T1` | -0.89781 |
| `explicit.stat_53045048@T2` | -0.76182 |
| `explicit.stat_587431675@T2` | -0.65309 |
| `explicit.stat_1263695895@T1` | -0.64866 |
| `explicit.stat_2162097452@T2` | -0.64649 |
| `explicit.stat_1999113824@T1` | -0.56429 |
| `explicit.stat_1263695895@T2` | -0.55571 |
| `explicit.stat_1062208444@T2` | -0.55384 |
| `explicit.stat_3917489142@T2` | -0.55206 |
| `explicit.stat_803737631@T2` | -0.55138 |

### armour.boots — n=24330, R²=-1.622

intercept: `3.6553`  ·  log_price: True  ·  ilvl: `-0.04494`  ·  n_mods: `-0.01162`  ·  n_top_tier: `0.48195`  ·  corrupted: `-0.01062`  ·  n_sockets: `0.00368`  ·  quality: `0.02042`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.72874 |
| `desecrated.stat_2250533757@T2` | -1.02893 |
| `crafted.stat_3917489142@T1` | -0.72967 |
| `explicit.stat_3917489142@T2` | -0.56933 |
| `explicit.stat_4220027924@T1` | 0.56588 |
| `explicit.stat_2923486259@T2` | -0.54595 |
| `explicit.stat_3362812763@T1` | -0.53090 |
| `explicit.stat_1062208444@T2` | -0.53078 |
| `explicit.stat_53045048@T1` | -0.52783 |
| `explicit.stat_2339757871@T1` | -0.52642 |
| `explicit.stat_2160282525@T2` | -0.51552 |
| `explicit.stat_2160282525@T1` | -0.51346 |

### armour.gloves — n=23678, R²=-1.7502

intercept: `4.0926`  ·  log_price: True  ·  ilvl: `-0.05193`  ·  n_mods: `-0.01789`  ·  n_top_tier: `0.41010`  ·  corrupted: `0.05070`  ·  n_sockets: `0.05243`  ·  quality: `0.03966`

| stat_id | coef |
|---|---|
| `explicit.stat_9187492@T1` | 0.84049 |
| `explicit.stat_9187492@T2` | -0.72667 |
| `rune.stat_201332984` | 0.71407 |
| `explicit.stat_3484657501@T2` | -0.64152 |
| `explicit.stat_1671376347@T1` | 0.63023 |
| `explicit.stat_3917489142@T2` | -0.53162 |
| `explicit.stat_803737631@T2` | -0.52877 |
| `explicit.stat_3484657501@T1` | -0.52477 |
| `explicit.stat_681332047@T2` | -0.49140 |
| `explicit.stat_3321629045@T1` | -0.48789 |
| `explicit.stat_3032590688@T1` | -0.48672 |
| `explicit.stat_3299347043@T2` | -0.45780 |

### weapon.wand — n=15689, R²=-2.2007

intercept: `4.0373`  ·  log_price: True  ·  ilvl: `-0.05004`  ·  n_mods: `-0.01273`  ·  n_top_tier: `0.28009`  ·  corrupted: `-0.03144`  ·  n_sockets: `0.04114`  ·  quality: `0.00731`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 3.56988 |
| `rune.stat_124131830` | -3.27237 |
| `explicit.stat_4226189338@T1` | 2.99376 |
| `explicit.stat_1545858329@T1` | 2.43313 |
| `explicit.stat_591105508@T1` | 2.10135 |
| `explicit.stat_1600707273@T1` | 1.80422 |
| `explicit.stat_736967255@T2` | 1.70408 |
| `explicit.stat_124131830@T1` | 1.26324 |
| `crafted.stat_124131830` | 1.10260 |
| `explicit.stat_1600707273@T2` | 0.45601 |
| `explicit.stat_2974417149@T1` | 0.40482 |
| `explicit.stat_3962278098@T2` | -0.32302 |

### weapon.bow — n=12816, R²=-1.9895

intercept: `3.4508`  ·  log_price: True  ·  ilvl: `-0.04222`  ·  n_mods: `-0.02586`  ·  n_top_tier: `0.75037`  ·  corrupted: `-0.05022`  ·  n_sockets: `-0.00467`  ·  quality: `0.03515`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.03471 |
| `crafted.stat_3035140377` | 1.36116 |
| `explicit.stat_1202301673@T1` | 1.35405 |
| `explicit.stat_1037193709@T2` | -0.82266 |
| `explicit.stat_55876295@T1` | -0.81626 |
| `explicit.stat_1263695895@T1` | -0.81193 |
| `explicit.stat_1037193709@T1` | -0.81110 |
| `explicit.stat_1368271171@T2` | -0.79187 |
| `explicit.stat_3336890334@T2` | -0.79156 |
| `explicit.stat_669069897@T1` | -0.78781 |
| `explicit.stat_3695891184@T1` | -0.78552 |
| `explicit.stat_2694482655@T1` | -0.78420 |

### weapon.crossbow — n=12082, R²=-1.9466

intercept: `3.7902`  ·  log_price: True  ·  ilvl: `-0.04680`  ·  n_mods: `-0.00625`  ·  n_top_tier: `0.70663`  ·  corrupted: `-0.04474`  ·  n_sockets: `0.01864`  ·  quality: `0.00250`

| stat_id | coef |
|---|---|
| `explicit.stat_2250681686@T2` | -2.56860 |
| `explicit.stat_1980802737@T2` | -1.94798 |
| `explicit.stat_2250681686` | 1.87879 |
| `explicit.stat_1202301673@T1` | 1.55047 |
| `explicit.stat_709508406@T1` | 1.50237 |
| `explicit.stat_1980802737` | 1.20060 |
| `explicit.stat_1263695895@T2` | -0.86437 |
| `crafted.stat_3035140377` | 0.86345 |
| `explicit.stat_1263695895@T1` | -0.81518 |
| `rune.stat_669069897` | -0.78525 |
| `explicit.stat_1202301673@T2` | -0.76010 |
| `explicit.stat_1509134228@T2` | -0.74677 |

### flask.charm — n=9673, R²=-0.451

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.03047`  ·  corrupted: `1.05255`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.75652 |
| `explicit.stat_1056492907` | 3.50115 |
| `explicit.stat_2676834156@T1` | 1.58241 |
| `explicit.stat_2541588185@T1` | 0.24472 |
| `explicit.stat_2678930256` | 0.03219 |
| `explicit.stat_828533480@T2` | -0.03047 |
| `explicit.stat_1366840608@T2` | -0.03047 |
| `explicit.stat_2676834156@T2` | -0.03047 |
| `explicit.stat_1873752457@T2` | -0.03047 |
| `explicit.stat_388617051@T2` | -0.03047 |
| `explicit.stat_1120862500@T2` | -0.03046 |
| `explicit.stat_1873752457@T1` | -0.03046 |

### weapon.warstaff — n=6771, R²=-0.6124

intercept: `-0.5267`  ·  log_price: True  ·  ilvl: `0.00720`  ·  n_mods: `-0.01909`  ·  n_top_tier: `0.28713`  ·  corrupted: `0.04096`  ·  n_sockets: `0.01419`  ·  quality: `0.06668`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.40634 |
| `explicit.stat_9187492@T1` | 1.07130 |
| `rune.stat_731403740` | 0.80361 |
| `explicit.stat_1509134228@T2` | 0.61692 |
| `crafted.stat_210067635@T2` | -0.54638 |
| `crafted.stat_3035140377` | 0.52259 |
| `desecrated.stat_9187492` | 0.50471 |
| `rune.stat_1712188793` | -0.35992 |
| `explicit.stat_328541901@T2` | -0.32361 |
| `explicit.stat_328541901@T1` | -0.32162 |
| `explicit.stat_1509134228@T1` | -0.31462 |
| `explicit.stat_3336890334@T2` | -0.30411 |

### weapon.sceptre — n=6289, R²=-0.5382

intercept: `-8.0366`  ·  log_price: True  ·  ilvl: `0.10059`  ·  n_mods: `-0.01485`  ·  n_top_tier: `0.21711`  ·  corrupted: `0.35038`  ·  n_sockets: `0.19373`  ·  quality: `0.08769`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.82903 |
| `explicit.stat_2162097452@T2` | 1.43424 |
| `explicit.stat_1798257884@T2` | 0.76208 |
| `explicit.stat_4080418644@T1` | -0.66870 |
| `explicit.stat_3057012405@T1` | 0.58111 |
| `explicit.stat_4080418644@T2` | -0.46961 |
| `explicit.stat_1263695895@T2` | -0.44670 |
| `explicit.stat_3984865854@T1` | 0.40601 |
| `explicit.stat_1263695895@T1` | -0.39402 |
| `explicit.stat_3984865854@T2` | 0.37382 |
| `explicit.stat_1574590649@T2` | -0.33905 |
| `explicit.stat_2854751904@T1` | -0.33268 |

### weapon.staff — n=6221, R²=-0.6579

intercept: `-0.9319`  ·  log_price: True  ·  ilvl: `0.01165`  ·  n_mods: `-0.00260`  ·  n_top_tier: `0.31875`  ·  corrupted: `0.23391`  ·  n_sockets: `0.04712`  ·  quality: `0.06240`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 2.77805 |
| `explicit.stat_4226189338@T1` | 2.22096 |
| `explicit.stat_1600707273@T1` | 1.84775 |
| `explicit.stat_2254480358@T1` | 1.84152 |
| `explicit.stat_1545858329@T1` | 1.76226 |
| `explicit.stat_2254480358@T2` | 1.29826 |
| `explicit.stat_124131830@T1` | 1.20180 |
| `explicit.stat_4226189338@T2` | 1.16221 |
| `explicit.stat_2231156303@T2` | 0.56804 |
| `crafted.stat_124131830` | 0.46139 |
| `explicit.stat_3962278098@T2` | 0.38756 |
| `explicit.stat_591105508@T1` | -0.35477 |

### weapon.spear — n=5309, R²=-0.6964

intercept: `-0.1550`  ·  log_price: True  ·  ilvl: `0.00207`  ·  n_mods: `-0.00187`  ·  n_top_tier: `0.24126`  ·  corrupted: `-0.01393`  ·  n_sockets: `0.00646`  ·  quality: `0.09539`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 2.46281 |
| `crafted.stat_210067635@T2` | 1.98111 |
| `explicit.stat_9187492@T1` | 1.81473 |
| `crafted.stat_3035140377` | 1.25332 |
| `crafted.stat_518292764` | 0.69239 |
| `explicit.stat_210067635@T1` | 0.51676 |
| `explicit.stat_709508406@T1` | 0.37753 |
| `explicit.stat_3336890334@T1` | 0.33754 |
| `explicit.stat_1263695895@T2` | -0.26066 |
| `explicit.stat_1263695895@T1` | -0.25889 |
| `explicit.stat_55876295@T1` | -0.24805 |
| `explicit.stat_691932474@T1` | -0.24337 |

### armour.focus — n=4325, R²=-0.5268

intercept: `-6.1274`  ·  log_price: True  ·  ilvl: `0.07565`  ·  n_mods: `-0.01599`  ·  n_top_tier: `0.79637`  ·  corrupted: `0.65637`  ·  n_sockets: `0.23109`  ·  quality: `0.06827`

| stat_id | coef |
|---|---|
| `desecrated.stat_378817135@T1` | 7.01161 |
| `crafted.stat_737908626@T2` | -1.34952 |
| `explicit.stat_1671376347@T1` | 1.06439 |
| `explicit.stat_4220027924@T2` | -1.03531 |
| `explicit.stat_4220027924@T1` | -1.01226 |
| `explicit.stat_736967255@T2` | -0.99265 |
| `explicit.stat_124131830@T2` | -0.99250 |
| `explicit.stat_3291658075@T1` | -0.89648 |
| `explicit.stat_2891184298@T2` | -0.88993 |
| `explicit.stat_2891184298@T1` | -0.87821 |
| `crafted.stat_2974417149@T1` | 0.85812 |
| `explicit.stat_737908626@T1` | -0.85251 |

### armour.quiver — n=4063, R²=-0.5519

intercept: `-5.7852`  ·  log_price: True  ·  ilvl: `0.06859`  ·  n_mods: `-0.00060`  ·  n_top_tier: `0.83090`  ·  corrupted: `0.34394`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 9.62569 |
| `explicit.stat_681332047@T2` | -1.05835 |
| `explicit.stat_2194114101@T2` | -1.03947 |
| `explicit.stat_2321178454@T2` | -0.97408 |
| `explicit.stat_1368271171@T2` | -0.95431 |
| `explicit.stat_1573130764@T1` | -0.94883 |
| `explicit.stat_3261801346@T1` | -0.89774 |
| `explicit.stat_3714003708@T2` | -0.88431 |
| `explicit.stat_1573130764@T2` | -0.87460 |
| `explicit.stat_2321178454@T1` | -0.85886 |
| `explicit.stat_3261801346@T2` | -0.79927 |
| `explicit.stat_4067062424@T2` | -0.77197 |

### armour.shield — n=3521, R²=-0.6484

intercept: `-2.7087`  ·  log_price: True  ·  ilvl: `0.03386`  ·  n_mods: `-0.00412`  ·  n_top_tier: `0.49013`  ·  corrupted: `0.08512`  ·  n_sockets: `-0.00334`  ·  quality: `0.06014`

| stat_id | coef |
|---|---|
| `explicit.stat_3676141501@T1` | 0.86413 |
| `explicit.stat_1978899297@T1` | 0.80735 |
| `explicit.stat_328541901@T1` | -0.74220 |
| `explicit.stat_2339757871@T1` | -0.72757 |
| `explicit.stat_1011760251@T1` | -0.71605 |
| `explicit.stat_1011760251@T2` | -0.66769 |
| `explicit.stat_328541901@T2` | -0.66570 |
| `explicit.stat_2481353198@T1` | -0.63668 |
| `explicit.stat_2481353198@T2` | -0.63204 |
| `explicit.stat_3362812763@T1` | -0.63016 |
| `explicit.stat_1978899297@T2` | -0.62766 |
| `explicit.stat_53045048@T2` | -0.60395 |

### weapon.twomace — n=3195, R²=-0.5539

intercept: `-4.5092`  ·  log_price: True  ·  ilvl: `0.05791`  ·  n_mods: `-0.03922`  ·  n_top_tier: `0.71104`  ·  corrupted: `0.35466`  ·  n_sockets: `0.10439`  ·  quality: `0.02140`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.34207 |
| `explicit.stat_1037193709@T1` | -1.15228 |
| `crafted.stat_3035140377` | 1.08154 |
| `explicit.stat_3336890334@T1` | -1.02373 |
| `explicit.stat_1037193709@T2` | -0.94629 |
| `explicit.stat_387439868@T2` | -0.90680 |
| `explicit.stat_210067635@T1` | 0.88736 |
| `explicit.stat_1263695895@T2` | -0.86718 |
| `explicit.stat_691932474@T1` | -0.85712 |
| `explicit.stat_821021828@T2` | -0.83572 |
| `explicit.stat_669069897@T1` | -0.81597 |
| `explicit.stat_3695891184@T1` | -0.80047 |

## Coverage (listings per base)

- … **Sapphire** — 18128 listings (18103 priced) [0.3–7553463.8 ex]
- … **Emerald** — 17901 listings (17881 priced) [0.3–7553463.8 ex]
- … **Ruby** — 13802 listings (13790 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 7871 listings (7862 priced) [0.2–3985176410.3 ex]
- … **Prismatic Ring** — 6283 listings (6276 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 6109 listings (6098 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 6023 listings (6019 priced) [0.2–19945827.9 ex]
- … **Stellar Amulet** — 5840 listings (5837 priced) [0.3–35690283.3 ex]
- … **Gold Amulet** — 5781 listings (5771 priced) [0.3–27924159.0 ex]
- … **Gold Ring** — 5626 listings (5620 priced) [0.2–24532814.5 ex]
- … **Dueling Wand** — 4966 listings (4954 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 4687 listings (4682 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 4559 listings (4556 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 4536 listings (4534 priced) [0.2–37474957.5 ex]
- … **Plate Belt** — 4140 listings (4134 priced) [0.3–5286174.1 ex]
- … **Lapis Amulet** — 4066 listings (4062 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 4000 listings (3993 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 3960 listings (3958 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 3939 listings (3935 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 3882 listings (3881 priced) [0.2–24532814.5 ex]
- … **Obliterator Bow** — 3825 listings (3814 priced) [0.3–42622633798.0 ex]
- … **Bloodstone Amulet** — 3773 listings (3769 priced) [0.3–4275054.0 ex]
- … **Heavy Belt** — 3755 listings (3753 priced) [0.3–4877938.3 ex]
- … **Pearl Ring** — 3641 listings (3638 priced) [0.2–275252424.7 ex]
- … **Lunar Amulet** — 3583 listings (3579 priced) [0.3–4877938.3 ex]
