# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-15T04:35:15+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **496477** (495437 priced in exalted)
- Distinct bases: 980 · distinct mods: 3090 · mod rows: 2356310
- Sold signals: **26408** sold · 276684 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-15T04:27:08+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×24.93** (median |log error| 3.2162)
- Within ±30% of asking price: **19%**
- Skill vs constant-price guess: **+0.06** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.11** · typical error ×69.54 · ±30% 4% · n=71266
- Premium segment (60ex+): skill **+0.10** · typical error ×341.83 · ±30% 0% · n=47263

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 9873 | ×52.54 | 21% | +0.06 | +0.08 |
| jewel | 9193 | ×9.37 | 5% | +0.02 | +0.06 |
| accessory.amulet | 9071 | ×50.21 | 20% | +0.03 | +0.03 |
| accessory.belt | 7027 | ×23.09 | 16% | +0.07 | +0.09 |
| armour.chest | 6842 | ×23.45 | 23% | +0.06 | +0.09 |
| armour.helmet | 6700 | ×24.72 | 20% | +0.06 | +0.08 |
| armour.boots | 6243 | ×25.32 | 24% | +0.05 | +0.07 |
| armour.gloves | 6085 | ×34.82 | 21% | +0.05 | +0.07 |
| other | 5365 | ×2.40 | 42% | +0.10 | +0.16 |
| weapon.wand | 3906 | ×34.88 | 19% | +0.07 | +0.08 |
| weapon.bow | 3114 | ×27.33 | 19% | +0.09 | +0.10 |
| weapon.crossbow | 2944 | ×26.41 | 20% | +0.08 | +0.12 |
| weapon.warstaff | 1771 | ×32.45 | 17% | +0.10 | +0.10 |
| weapon.staff | 1646 | ×49.86 | 16% | +0.08 | +0.10 |
| weapon.sceptre | 1627 | ×41.38 | 7% | +0.13 | +0.14 |
| weapon.spear | 1336 | ×72.71 | 16% | +0.08 | +0.09 |
| armour.focus | 1114 | ×45.24 | 8% | +0.12 | +0.14 |
| armour.quiver | 1043 | ×34.74 | 9% | +0.09 | +0.12 |
| armour.shield | 880 | ×16.57 | 15% | +0.02 | +0.01 |
| flask.charm | 878 | ×50.00 | 35% | +0.03 | +0.05 |
| weapon.twomace | 799 | ×20.60 | 15% | +0.06 | +0.08 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=49397, R²=-0.8695

intercept: `-1.6314`  ·  log_price: True  ·  ilvl: `0.02909`  ·  n_mods: `0.52660`  ·  n_top_tier: `-0.12481`  ·  corrupted: `0.30132`  ·  quality: `0.22785`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.51941 |
| `explicit.stat_2301718443@T1` | 3.11142 |
| `explicit.stat_627767961@T1` | -2.48821 |
| `explicit.stat_3780644166@T1` | -2.31770 |
| `explicit.stat_1697447343@T1` | -2.25359 |
| `explicit.stat_3166958180@T1` | -1.93455 |
| `explicit.stat_1697951953@T1` | -1.91642 |
| `explicit.stat_3091578504@T1` | -1.89639 |
| `explicit.stat_3485067555@T1` | 1.85334 |
| `explicit.stat_239367161@T1` | -1.82900 |
| `explicit.stat_2594634307@T1` | 1.54765 |
| `explicit.stat_169946467@T1` | -1.54113 |

### other — n=48082, R²=-0.6134

intercept: `1.6058`  ·  log_price: True  ·  ilvl: `0.00005`  ·  n_mods: `0.01263`  ·  n_top_tier: `0.34283`  ·  corrupted: `0.33503`  ·  n_sockets: `-0.00005`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.49876 |
| `explicit.stat_2974417149@T1` | 0.48032 |
| `explicit.stat_3299347043@T1` | -0.37093 |
| `explicit.stat_2482852589@T1` | -0.35773 |
| `explicit.stat_789117908@T1` | -0.29769 |
| `implicit.stat_3879011313` | 0.23064 |
| `implicit.stat_2219129443` | 0.22899 |
| `implicit.stat_4041853756` | 0.22899 |
| `explicit.stat_3917489142@T1` | 0.21067 |
| `explicit.stat_3141070085@T1` | -0.20098 |
| `explicit.stat_2106365538@T1` | -0.18234 |
| `implicit.stat_1379411836` | -0.15484 |

### accessory.ring — n=45114, R²=-1.9762

intercept: `3.4222`  ·  log_price: True  ·  ilvl: `-0.04229`  ·  n_mods: `0.00199`  ·  n_top_tier: `0.76887`  ·  corrupted: `0.12792`  ·  n_sockets: `-0.06074`  ·  quality: `0.07019`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -0.80739 |
| `explicit.stat_1263695895@T1` | -0.80593 |
| `explicit.stat_2231156303@T1` | -0.80315 |
| `explicit.stat_3325883026@T1` | -0.79527 |
| `explicit.stat_1263695895@T2` | -0.79305 |
| `explicit.stat_2144192055@T1` | -0.79194 |
| `explicit.stat_803737631@T1` | -0.79144 |
| `explicit.stat_1368271171@T2` | -0.79018 |
| `explicit.stat_4220027924@T2` | -0.78683 |
| `explicit.stat_3291658075@T1` | -0.78614 |
| `explicit.stat_3291658075@T2` | -0.78500 |
| `explicit.stat_3962278098@T2` | -0.78421 |

### accessory.amulet — n=41755, R²=-2.1418

intercept: `3.8846`  ·  log_price: True  ·  ilvl: `-0.04753`  ·  n_mods: `-0.02501`  ·  n_top_tier: `0.98192`  ·  corrupted: `0.07020`  ·  n_sockets: `-0.11520`  ·  quality: `-0.00114`

| stat_id | coef |
|---|---|
| `explicit.stat_472520716@T2` | -1.05810 |
| `explicit.stat_472520716@T1` | -1.05514 |
| `explicit.stat_2901986750@T1` | -1.03406 |
| `explicit.stat_1050105434@T2` | -1.03363 |
| `explicit.stat_3917489142@T2` | -1.03122 |
| `explicit.stat_803737631@T1` | -1.02762 |
| `explicit.stat_2974417149@T1` | -1.02535 |
| `explicit.stat_2866361420@T2` | -1.02495 |
| `explicit.stat_2748665614@T1` | -1.02303 |
| `explicit.stat_2866361420@T1` | -1.01991 |
| `explicit.stat_2482852589@T2` | -1.01883 |
| `explicit.stat_2974417149@T2` | -1.01293 |

### accessory.belt — n=32242, R²=-1.4376

intercept: `4.6446`  ·  log_price: True  ·  ilvl: `-0.05589`  ·  n_mods: `-0.05130`  ·  n_top_tier: `1.31390`  ·  corrupted: `0.73472`  ·  n_sockets: `1.39281`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.90392 |
| `explicit.stat_3299347043@T2` | -1.42654 |
| `explicit.stat_1389754388@T1` | -1.42378 |
| `explicit.stat_2881298780@T1` | -1.42074 |
| `explicit.stat_51994685@T1` | -1.38828 |
| `explicit.stat_809229260@T2` | -1.38651 |
| `explicit.stat_3325883026@T1` | -1.35678 |
| `explicit.stat_1671376347@T2` | -1.35007 |
| `explicit.stat_4220027924@T2` | -1.34931 |
| `explicit.stat_644456512@T1` | -1.34448 |
| `explicit.stat_644456512@T2` | -1.33697 |
| `explicit.stat_915769802@T2` | -1.33415 |

### armour.chest — n=31883, R²=-1.7184

intercept: `3.5056`  ·  log_price: True  ·  ilvl: `-0.04325`  ·  n_mods: `-0.01560`  ·  n_top_tier: `0.34917`  ·  corrupted: `0.27216`  ·  n_sockets: `0.01808`  ·  quality: `0.03900`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.67765 |
| `explicit.stat_3981240776@T1` | 1.16578 |
| `explicit.stat_3033371881@T1` | 0.53675 |
| `explicit.stat_986397080@T2` | -0.40566 |
| `explicit.stat_4080418644@T2` | -0.38938 |
| `explicit.stat_3484657501@T1` | -0.38151 |
| `explicit.stat_986397080@T1` | -0.37810 |
| `explicit.stat_4080418644@T1` | -0.37701 |
| `explicit.stat_915769802@T2` | -0.37331 |
| `explicit.stat_3372524247@T2` | -0.37234 |
| `explicit.stat_2923486259@T2` | -0.37217 |
| `explicit.stat_2451402625@T2` | -0.37089 |

### armour.helmet — n=31060, R²=-1.6888

intercept: `3.6645`  ·  log_price: True  ·  ilvl: `-0.04606`  ·  n_mods: `-0.02169`  ·  n_top_tier: `0.42374`  ·  corrupted: `0.58784`  ·  n_sockets: `0.02087`  ·  quality: `0.05443`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -4.62201 |
| `crafted.stat_3917489142@T1` | 2.55474 |
| `explicit.stat_1263695895@T1` | -0.68182 |
| `explicit.stat_1263695895@T2` | -0.58800 |
| `explicit.stat_3917489142@T2` | -0.55118 |
| `explicit.stat_2162097452@T2` | -0.51776 |
| `explicit.stat_53045048@T1` | -0.48365 |
| `explicit.stat_3261801346@T2` | -0.46845 |
| `explicit.stat_3917489142@T1` | -0.46817 |
| `explicit.stat_1999113824@T1` | -0.46299 |
| `explicit.stat_3321629045@T2` | -0.45549 |
| `explicit.stat_53045048@T2` | -0.45536 |

### armour.boots — n=29160, R²=-1.7926

intercept: `3.3168`  ·  log_price: True  ·  ilvl: `-0.04095`  ·  n_mods: `-0.01003`  ·  n_top_tier: `0.70031`  ·  corrupted: `-0.01240`  ·  n_sockets: `0.00470`  ·  quality: `0.02219`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.25845 |
| `explicit.stat_2339757871@T1` | -0.80310 |
| `explicit.stat_3917489142@T2` | -0.79360 |
| `explicit.stat_3917489142@T1` | -0.75115 |
| `explicit.stat_2160282525@T1` | -0.73493 |
| `explicit.stat_3484657501@T2` | -0.72204 |
| `explicit.stat_3299347043@T1` | -0.72195 |
| `explicit.stat_3362812763@T1` | -0.72184 |
| `explicit.stat_1671376347@T2` | -0.72066 |
| `explicit.stat_4080418644@T1` | -0.71683 |
| `explicit.stat_53045048@T1` | -0.71658 |
| `desecrated.stat_2250533757@T2` | -0.71615 |

### armour.gloves — n=28414, R²=-1.9134

intercept: `3.4347`  ·  log_price: True  ·  ilvl: `-0.04325`  ·  n_mods: `-0.00487`  ·  n_top_tier: `0.53399`  ·  corrupted: `-0.02122`  ·  n_sockets: `0.02738`  ·  quality: `0.05091`

| stat_id | coef |
|---|---|
| `rune.stat_201332984` | -6.71947 |
| `explicit.stat_9187492@T2` | -0.85870 |
| `explicit.stat_9187492@T1` | 0.85176 |
| `explicit.stat_1671376347@T1` | 0.83182 |
| `explicit.stat_3484657501@T2` | -0.66990 |
| `explicit.stat_4052037485@T1` | -0.60871 |
| `explicit.stat_3917489142@T2` | -0.60165 |
| `explicit.stat_803737631@T2` | -0.60119 |
| `explicit.stat_3484657501@T1` | -0.60069 |
| `explicit.stat_3321629045@T2` | -0.59001 |
| `explicit.stat_803737631@T1` | -0.56845 |
| `explicit.stat_3917489142@T1` | -0.56268 |

### weapon.wand — n=18296, R²=-2.2371

intercept: `3.7014`  ·  log_price: True  ·  ilvl: `-0.04570`  ·  n_mods: `-0.01592`  ·  n_top_tier: `0.58813`  ·  corrupted: `-0.02294`  ·  n_sockets: `0.03690`  ·  quality: `0.00461`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.03223 |
| `rune.stat_124131830` | -2.91266 |
| `explicit.stat_2254480358@T1` | 2.38649 |
| `explicit.stat_4226189338@T1` | 1.75071 |
| `explicit.stat_591105508@T1` | 1.71788 |
| `explicit.stat_124131830@T1` | 1.61721 |
| `explicit.stat_736967255@T2` | 1.26691 |
| `crafted.stat_124131830` | 1.17545 |
| `explicit.stat_2254480358@T2` | 0.73944 |
| `explicit.stat_2968503605@T1` | -0.66544 |
| `explicit.stat_1263695895@T2` | -0.65812 |
| `explicit.stat_737908626@T1` | -0.65360 |

### weapon.bow — n=14736, R²=-2.0113

intercept: `3.4065`  ·  log_price: True  ·  ilvl: `-0.04096`  ·  n_mods: `-0.03740`  ·  n_top_tier: `0.66786`  ·  corrupted: `-0.07125`  ·  n_sockets: `-0.00239`  ·  quality: `0.03211`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.06378 |
| `explicit.stat_1202301673@T1` | 1.52039 |
| `desecrated.stat_666077204@T1` | 1.39457 |
| `crafted.stat_3035140377` | 1.29940 |
| `explicit.stat_1263695895@T1` | -0.86626 |
| `explicit.stat_1263695895@T2` | -0.78302 |
| `explicit.stat_3695891184@T2` | -0.72795 |
| `explicit.stat_1368271171@T2` | -0.72651 |
| `explicit.stat_1509134228@T1` | -0.71288 |
| `explicit.stat_2694482655@T2` | -0.70305 |
| `explicit.stat_3695891184@T1` | -0.70236 |
| `explicit.stat_669069897@T1` | -0.69991 |

### weapon.crossbow — n=13935, R²=-1.959

intercept: `3.8259`  ·  log_price: True  ·  ilvl: `-0.04672`  ·  n_mods: `-0.01789`  ·  n_top_tier: `0.76391`  ·  corrupted: `0.03849`  ·  n_sockets: `0.02156`  ·  quality: `0.00730`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -2.02436 |
| `explicit.stat_2250681686@T2` | -1.73146 |
| `explicit.stat_709508406@T1` | 1.48180 |
| `explicit.stat_1202301673@T1` | 1.38306 |
| `explicit.stat_1980802737` | 1.17990 |
| `explicit.stat_2250681686` | 1.05859 |
| `explicit.stat_1263695895@T2` | -0.95655 |
| `explicit.stat_1263695895@T1` | -0.92139 |
| `crafted.stat_3035140377` | 0.89001 |
| `explicit.stat_1202301673@T2` | -0.82693 |
| `explicit.stat_669069897@T1` | -0.82687 |
| `explicit.stat_2694482655@T1` | -0.81745 |

### flask.charm — n=12648, R²=-0.5329

intercept: `0.0046`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `2.86128`  ·  corrupted: `2.06550`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.38357 |
| `explicit.stat_1056492907` | 3.36819 |
| `explicit.stat_828533480@T2` | -2.86129 |
| `explicit.stat_2541588185@T2` | -2.86128 |
| `explicit.stat_828533480@T1` | -2.86127 |
| `explicit.stat_1120862500@T2` | -2.86127 |
| `explicit.stat_2676834156@T2` | -2.86127 |
| `explicit.stat_1873752457@T2` | -2.86127 |
| `explicit.stat_3196823591@T2` | -2.86126 |
| `explicit.stat_388617051@T2` | -2.86126 |
| `explicit.stat_1873752457@T1` | -2.86126 |
| `explicit.stat_1366840608@T2` | -2.86126 |

### weapon.warstaff — n=8459, R²=-0.4903

intercept: `-5.9838`  ·  log_price: True  ·  ilvl: `0.08252`  ·  n_mods: `-0.16703`  ·  n_top_tier: `0.59595`  ·  corrupted: `0.15764`  ·  n_sockets: `0.09073`  ·  quality: `0.05473`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.47746 |
| `explicit.stat_328541901@T2` | -1.06049 |
| `explicit.stat_328541901@T1` | -1.05192 |
| `explicit.stat_1037193709@T1` | 1.04122 |
| `explicit.stat_55876295@T2` | -0.77676 |
| `desecrated.stat_9187492` | 0.71381 |
| `explicit.stat_210067635@T1` | -0.68648 |
| `explicit.stat_1037193709@T2` | -0.67908 |
| `explicit.stat_1940865751@T1` | -0.67676 |
| `explicit.stat_55876295@T1` | -0.65191 |
| `crafted.stat_210067635@T2` | 0.65040 |
| `explicit.stat_791928121@T2` | -0.60756 |

### weapon.staff — n=7881, R²=-0.4764

intercept: `-9.3561`  ·  log_price: True  ·  ilvl: `0.12151`  ·  n_mods: `-0.10833`  ·  n_top_tier: `0.40757`  ·  corrupted: `0.13617`  ·  n_sockets: `0.18873`  ·  quality: `0.04545`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 1.51165 |
| `explicit.stat_124131830@T1` | 1.50866 |
| `explicit.stat_124131830@T2` | 1.13236 |
| `explicit.stat_1545858329@T1` | 1.12949 |
| `explicit.stat_2768835289@T2` | 1.12818 |
| `explicit.stat_2254480358@T1` | 1.01772 |
| `explicit.stat_4226189338@T2` | 0.98835 |
| `explicit.stat_1600707273@T1` | 0.97095 |
| `explicit.stat_293638271@T2` | -0.72658 |
| `explicit.stat_2254480358@T2` | 0.57145 |
| `explicit.stat_3962278098@T2` | 0.56423 |
| `explicit.stat_2974417149@T1` | -0.55968 |

### weapon.sceptre — n=7829, R²=-0.4127

intercept: `-14.9502`  ·  log_price: True  ·  ilvl: `0.18921`  ·  n_mods: `-0.03548`  ·  n_top_tier: `0.61724`  ·  corrupted: `0.47844`  ·  n_sockets: `0.23483`  ·  quality: `0.06369`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.15641 |
| `explicit.stat_2162097452@T2` | 1.24773 |
| `explicit.stat_1263695895@T2` | -0.98061 |
| `explicit.stat_1574590649@T2` | -0.93847 |
| `explicit.stat_2347036682@T2` | -0.93813 |
| `explicit.stat_289128254@T2` | -0.89662 |
| `explicit.stat_4080418644@T1` | -0.86812 |
| `explicit.stat_2854751904@T2` | -0.85589 |
| `explicit.stat_1263695895@T1` | -0.80378 |
| `explicit.stat_1050105434@T2` | -0.77569 |
| `explicit.stat_2854751904@T1` | -0.69382 |
| `explicit.stat_789117908@T2` | -0.66535 |

### weapon.spear — n=6492, R²=-0.5373

intercept: `-7.9657`  ·  log_price: True  ·  ilvl: `0.10730`  ·  n_mods: `-0.05707`  ·  n_top_tier: `0.71782`  ·  corrupted: `-0.19418`  ·  n_sockets: `0.20906`  ·  quality: `0.09963`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -2.69596 |
| `explicit.stat_1202301673@T1` | 2.03637 |
| `explicit.stat_9187492@T1` | 1.74613 |
| `crafted.stat_3035140377` | 1.03778 |
| `explicit.stat_1509134228@T1` | 1.02552 |
| `explicit.stat_1263695895@T2` | -1.02452 |
| `desecrated.stat_210067635@T1` | -1.00650 |
| `explicit.stat_55876295@T1` | -0.93642 |
| `explicit.stat_1037193709@T1` | -0.85867 |
| `explicit.stat_55876295@T2` | -0.83296 |
| `explicit.stat_1940865751@T2` | -0.78861 |
| `explicit.stat_3261801346@T2` | -0.76497 |

### armour.focus — n=5296, R²=-0.4302

intercept: `-11.7415`  ·  log_price: True  ·  ilvl: `0.14816`  ·  n_mods: `-0.10527`  ·  n_top_tier: `0.87804`  ·  corrupted: `0.68355`  ·  n_sockets: `0.41350`  ·  quality: `0.06945`

| stat_id | coef |
|---|---|
| `crafted.stat_737908626@T2` | 1.78190 |
| `explicit.stat_4220027924@T2` | -1.34830 |
| `crafted.stat_2974417149@T1` | 1.32355 |
| `explicit.stat_2339757871@T1` | -1.16425 |
| `explicit.stat_2339757871@T2` | -1.10898 |
| `explicit.stat_3962278098@T1` | -1.08251 |
| `explicit.stat_736967255@T2` | -1.07352 |
| `explicit.stat_3962278098@T2` | -1.05619 |
| `explicit.stat_2974417149@T1` | -0.94981 |
| `explicit.stat_4015621042@T1` | -0.93721 |
| `explicit.stat_737908626@T2` | -0.90582 |
| `explicit.stat_2231156303@T1` | -0.90387 |

### armour.quiver — n=4933, R²=-0.3747

intercept: `-10.5797`  ·  log_price: True  ·  ilvl: `0.13227`  ·  n_mods: `-0.07776`  ·  n_top_tier: `0.73362`  ·  corrupted: `0.53122`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.94652 |
| `explicit.stat_2321178454@T2` | -1.19592 |
| `explicit.stat_4067062424@T1` | -1.16702 |
| `explicit.stat_803737631@T2` | -0.95454 |
| `explicit.stat_681332047@T2` | -0.90712 |
| `explicit.stat_1573130764@T2` | -0.83839 |
| `explicit.stat_1573130764@T1` | -0.80555 |
| `explicit.stat_3261801346@T1` | -0.79956 |
| `explicit.stat_2321178454@T1` | -0.73253 |
| `explicit.stat_1241625305@T2` | -0.68017 |
| `explicit.stat_4067062424@T2` | -0.67358 |
| `explicit.stat_2194114101@T2` | -0.65921 |

### armour.shield — n=4315, R²=-0.5625

intercept: `-7.8656`  ·  log_price: True  ·  ilvl: `0.10184`  ·  n_mods: `-0.04564`  ·  n_top_tier: `0.52749`  ·  corrupted: `-0.03521`  ·  n_sockets: `0.11785`  ·  quality: `0.05615`

| stat_id | coef |
|---|---|
| `explicit.stat_3676141501@T1` | 0.98080 |
| `explicit.stat_2923486259@T2` | -0.87780 |
| `explicit.stat_2481353198@T2` | -0.83957 |
| `explicit.stat_1301765461@T1` | 0.83859 |
| `explicit.stat_328541901@T1` | -0.82737 |
| `explicit.stat_2481353198@T1` | -0.82288 |
| `explicit.stat_1011760251@T2` | -0.81877 |
| `explicit.stat_2339757871@T1` | -0.79816 |
| `explicit.stat_1011760251@T1` | -0.78936 |
| `explicit.stat_1978899297@T2` | -0.77758 |
| `explicit.stat_53045048@T1` | -0.71947 |
| `explicit.stat_2881298780@T1` | -0.71093 |

### weapon.twomace — n=3986, R²=-0.5124

intercept: `-9.1627`  ·  log_price: True  ·  ilvl: `0.12162`  ·  n_mods: `-0.15635`  ·  n_top_tier: `0.51497`  ·  corrupted: `0.39213`  ·  n_sockets: `0.15489`  ·  quality: `0.03863`

| stat_id | coef |
|---|---|
| `desecrated.stat_1509134228@T1` | 2.34786 |
| `desecrated.stat_210067635@T1` | -2.34747 |
| `explicit.stat_1037193709@T1` | -1.74390 |
| `explicit.stat_3336890334@T1` | -1.39970 |
| `crafted.stat_3035140377` | 1.13379 |
| `explicit.stat_1263695895@T1` | -1.05311 |
| `explicit.stat_518292764@T2` | -1.00846 |
| `explicit.stat_1263695895@T2` | -0.90918 |
| `explicit.stat_387439868@T2` | -0.88643 |
| `explicit.stat_1037193709@T2` | -0.84651 |
| `explicit.stat_3639275092@T1` | -0.81504 |
| `explicit.stat_1509134228@T1` | -0.72034 |

## Coverage (listings per base)

- … **Sapphire** — 23024 listings (22989 priced) [0.3–7553463.8 ex]
- … **Emerald** — 22671 listings (22641 priced) [0.3–7553463.8 ex]
- … **Ruby** — 17360 listings (17345 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 9415 listings (9406 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 7719 listings (7709 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 7550 listings (7537 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 7426 listings (7419 priced) [0.2–19945827.9 ex]
- … **Gold Amulet** — 7070 listings (7060 priced) [0.3–39887666593.4 ex]
- … **Stellar Amulet** — 6995 listings (6991 priced) [0.3–91750808.2 ex]
- … **Gold Ring** — 6927 listings (6914 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 5825 listings (5809 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 5783 listings (5777 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 5538 listings (5533 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 5508 listings (5505 priced) [0.2–37474957.5 ex]
- … **Plate Belt** — 5009 listings (4993 priced) [0.3–398912568423.8 ex]
- … **Lapis Amulet** — 4936 listings (4931 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 4836 listings (4824 priced) [0.6–398912568423.8 ex]
- … **Amber Amulet** — 4797 listings (4793 priced) [0.3–3985176410.3 ex]
- … **Jade Amulet** — 4795 listings (4789 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 4745 listings (4738 priced) [0.2–24532814.5 ex]
- … **Bloodstone Amulet** — 4648 listings (4643 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 4465 listings (4459 priced) [0.2–275252424.7 ex]
- … **Heavy Belt** — 4458 listings (4455 priced) [0.3–398912568423.8 ex]
- … **Obliterator Bow** — 4412 listings (4399 priced) [0.3–42622633798.0 ex]
- … **Azure Amulet** — 4390 listings (4390 priced) [0.3–123132003.2 ex]
