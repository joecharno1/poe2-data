# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-21T16:37:16+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **714667** (712402 priced in exalted)
- Distinct bases: 1001 · distinct mods: 3321 · mod rows: 3380658
- Sold signals: **24173** sold · 406910 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-21T16:21:26+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×18.44** (median |log error| 2.9146)
- Within ±30% of asking price: **16%**
- Skill vs constant-price guess: **+0.09** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.16** · typical error ×51.19 · ±30% 5% · n=103975
- Premium segment (60ex+): skill **+0.16** · typical error ×270.62 · ±30% 0% · n=68769

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 15339 | ×50.46 | 21% | +0.04 | +0.07 |
| jewel | 14759 | ×10.00 | 5% | +0.11 | +0.13 |
| accessory.amulet | 13750 | ×33.15 | 17% | +0.05 | +0.04 |
| accessory.belt | 9799 | ×20.23 | 13% | +0.07 | +0.10 |
| armour.chest | 9496 | ×14.23 | 21% | +0.08 | +0.11 |
| armour.helmet | 9295 | ×22.47 | 14% | +0.10 | +0.12 |
| armour.boots | 8558 | ×19.79 | 19% | +0.10 | +0.12 |
| armour.gloves | 8389 | ×30.13 | 14% | +0.08 | +0.11 |
| other | 8342 | ×2.00 | 42% | +0.11 | +0.16 |
| weapon.wand | 4959 | ×34.09 | 14% | +0.12 | +0.11 |
| weapon.bow | 3909 | ×20.01 | 9% | +0.19 | +0.19 |
| weapon.crossbow | 3680 | ×23.66 | 13% | +0.12 | +0.17 |
| weapon.warstaff | 2539 | ×13.25 | 8% | +0.21 | +0.21 |
| weapon.staff | 2460 | ×15.21 | 6% | +0.13 | +0.13 |
| weapon.sceptre | 2398 | ×19.28 | 5% | +0.07 | +0.08 |
| weapon.spear | 1923 | ×11.89 | 6% | +0.12 | +0.15 |
| armour.focus | 1598 | ×13.96 | 7% | +0.12 | +0.14 |
| armour.quiver | 1493 | ×16.05 | 8% | +0.12 | +0.13 |
| armour.shield | 1219 | ×8.46 | 8% | +0.10 | +0.12 |
| flask.charm | 1206 | ×10.00 | 27% | +0.02 | +0.03 |
| weapon.twomace | 1123 | ×8.76 | 7% | +0.10 | +0.10 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=80785, R²=-0.9682

intercept: `-1.9200`  ·  log_price: True  ·  ilvl: `0.02400`  ·  n_mods: `0.86781`  ·  n_top_tier: `-0.29216`  ·  corrupted: `0.30513`  ·  quality: `0.00323`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.16043 |
| `explicit.stat_1594812856@T1` | 1.84442 |
| `explicit.stat_239367161@T1` | -1.73954 |
| `explicit.stat_3485067555@T1` | 1.72964 |
| `explicit.stat_1869147066@T1` | -1.61001 |
| `explicit.stat_3668351662@T1` | -1.54339 |
| `explicit.stat_3028809864@T1` | -1.47956 |
| `explicit.stat_627767961@T1` | -1.34020 |
| `explicit.stat_1697447343@T1` | -1.32793 |
| `explicit.stat_3174700878@T1` | 1.27268 |
| `explicit.stat_234296660@T1` | -1.21891 |
| `explicit.stat_2456523742@T1` | 1.17346 |

### accessory.ring — n=69930, R²=-2.0039

intercept: `3.3322`  ·  log_price: True  ·  ilvl: `-0.04160`  ·  n_mods: `0.00145`  ·  n_top_tier: `1.01424`  ·  corrupted: `0.00359`  ·  n_sockets: `2.20503`  ·  quality: `0.02008`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.05140 |
| `explicit.stat_4080418644@T1` | -1.03525 |
| `explicit.stat_2231156303@T1` | -1.03340 |
| `explicit.stat_803737631@T1` | -1.03241 |
| `explicit.stat_1263695895@T2` | -1.03114 |
| `explicit.stat_4220027924@T2` | -1.03091 |
| `explicit.stat_2923486259@T2` | -1.02818 |
| `explicit.stat_3325883026@T1` | -1.02694 |
| `explicit.stat_2891184298@T2` | -1.02657 |
| `explicit.stat_3291658075@T2` | -1.02551 |
| `explicit.stat_736967255@T2` | -1.02404 |
| `explicit.stat_3962278098@T1` | -1.02314 |

### other — n=68029, R²=-0.6933

intercept: `1.6092`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.01896`  ·  n_top_tier: `0.32762`  ·  corrupted: `0.05915`  ·  n_sockets: `-0.00006`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.43453 |
| `explicit.stat_3299347043@T1` | -0.25454 |
| `explicit.stat_3917489142@T1` | -0.19616 |
| `explicit.stat_2974417149@T1` | 0.10231 |
| `explicit.stat_789117908@T1` | -0.07896 |
| `implicit.stat_3182714256` | 0.05691 |
| `implicit.stat_718638445` | 0.05690 |
| `explicit.stat_736967255@T1` | -0.05354 |
| `explicit.stat_2106365538@T1` | -0.05005 |
| `implicit.stat_2219129443` | 0.04581 |
| `implicit.stat_2901986750` | -0.03876 |
| `implicit.stat_3879011313` | 0.03276 |

### accessory.amulet — n=62757, R²=-2.1317

intercept: `3.3180`  ·  log_price: True  ·  ilvl: `-0.04217`  ·  n_mods: `-0.01529`  ·  n_top_tier: `1.27030`  ·  corrupted: `0.09519`  ·  n_sockets: `-0.04922`  ·  quality: `0.04083`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.88571 |
| `explicit.stat_3299347043@T2` | -1.81021 |
| `explicit.stat_587431675@T2` | -1.37069 |
| `explicit.stat_2866361420@T2` | -1.35336 |
| `explicit.stat_803737631@T1` | -1.35331 |
| `explicit.stat_2866361420@T1` | -1.35268 |
| `explicit.stat_2974417149@T1` | -1.35081 |
| `explicit.stat_2901986750@T1` | -1.33422 |
| `explicit.stat_2748665614@T1` | -1.33064 |
| `explicit.stat_983749596@T1` | -1.32666 |
| `explicit.stat_2974417149@T2` | -1.32511 |
| `explicit.stat_2748665614@T2` | -1.32408 |

### accessory.belt — n=44813, R²=-1.5068

intercept: `5.0382`  ·  log_price: True  ·  ilvl: `-0.05888`  ·  n_mods: `-0.05612`  ·  n_top_tier: `0.52890`  ·  corrupted: `1.24907`  ·  n_sockets: `1.00588`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 1.29116 |
| `explicit.stat_2923486259@T2` | 0.76964 |
| `explicit.stat_3299347043@T1` | -0.70894 |
| `explicit.stat_3299347043@T2` | -0.66992 |
| `explicit.stat_2881298780@T1` | -0.60081 |
| `explicit.stat_51994685@T1` | -0.58692 |
| `explicit.stat_1570770415@T2` | -0.57985 |
| `explicit.stat_3325883026@T1` | -0.55435 |
| `explicit.stat_809229260@T2` | -0.55341 |
| `explicit.stat_915769802@T1` | -0.54540 |
| `explicit.stat_4220027924@T2` | -0.54217 |
| `explicit.stat_2881298780@T2` | -0.53580 |

### armour.chest — n=44397, R²=-1.7717

intercept: `3.3004`  ·  log_price: True  ·  ilvl: `-0.04082`  ·  n_mods: `-0.01302`  ·  n_top_tier: `0.31933`  ·  corrupted: `0.42432`  ·  n_sockets: `0.01988`  ·  quality: `0.07053`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.69590 |
| `explicit.stat_986397080@T2` | -0.38875 |
| `explicit.stat_986397080@T1` | -0.38202 |
| `explicit.stat_3372524247@T1` | 0.37207 |
| `explicit.stat_3484657501@T1` | -0.36658 |
| `explicit.stat_1692879867@T2` | -0.36642 |
| `explicit.stat_4080418644@T2` | -0.36100 |
| `explicit.stat_915769802@T2` | -0.35081 |
| `explicit.stat_4080418644@T1` | -0.34338 |
| `explicit.stat_915769802@T1` | -0.34286 |
| `explicit.stat_3301100256@T2` | -0.33812 |
| `explicit.stat_2339757871@T2` | -0.33772 |

### armour.helmet — n=43201, R²=-1.5695

intercept: `3.5028`  ·  log_price: True  ·  ilvl: `-0.04442`  ·  n_mods: `-0.03486`  ·  n_top_tier: `0.64005`  ·  corrupted: `0.52447`  ·  n_sockets: `0.13262`  ·  quality: `0.06301`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -4.26503 |
| `crafted.stat_3917489142@T1` | 1.84322 |
| `explicit.stat_1263695895@T1` | -0.99855 |
| `explicit.stat_3917489142@T2` | -0.93514 |
| `explicit.stat_3917489142@T1` | -0.82717 |
| `explicit.stat_2162097452@T2` | -0.78889 |
| `explicit.stat_1999113824@T1` | -0.76468 |
| `explicit.stat_1263695895@T2` | -0.74724 |
| `explicit.stat_803737631@T1` | -0.72721 |
| `explicit.stat_4052037485@T2` | -0.72555 |
| `explicit.stat_3321629045@T2` | -0.72225 |
| `explicit.stat_4015621042@T2` | -0.70574 |

### armour.boots — n=39968, R²=-1.7244

intercept: `3.4789`  ·  log_price: True  ·  ilvl: `-0.04295`  ·  n_mods: `-0.02014`  ·  n_top_tier: `0.43718`  ·  corrupted: `0.04821`  ·  n_sockets: `0.05448`  ·  quality: `0.07051`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.71262 |
| `explicit.stat_2339757871@T1` | -1.67834 |
| `crafted.stat_3917489142@T1` | 1.53352 |
| `explicit.stat_2923486259@T1` | 0.87607 |
| `explicit.stat_3299347043@T1` | -0.55722 |
| `explicit.stat_3917489142@T2` | -0.51442 |
| `explicit.stat_2923486259@T2` | -0.49982 |
| `explicit.stat_2160282525@T1` | -0.49811 |
| `explicit.stat_1671376347@T2` | -0.49524 |
| `explicit.stat_1874553720@T1` | -0.49063 |
| `explicit.stat_328541901@T2` | -0.47984 |
| `explicit.stat_3321629045@T2` | -0.46890 |

### armour.gloves — n=38999, R²=-1.6924

intercept: `3.7033`  ·  log_price: True  ·  ilvl: `-0.04881`  ·  n_mods: `-0.00745`  ·  n_top_tier: `0.83489`  ·  corrupted: `-0.03091`  ·  n_sockets: `0.19945`  ·  quality: `0.06037`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -1.49672 |
| `explicit.stat_2923486259@T2` | -1.28590 |
| `explicit.stat_3484657501@T2` | -1.13531 |
| `explicit.stat_4052037485@T1` | -1.07903 |
| `explicit.stat_4052037485@T2` | -1.07592 |
| `explicit.stat_124859000@T1` | -1.02352 |
| `explicit.stat_3321629045@T2` | -0.98286 |
| `explicit.stat_3484657501@T1` | -0.96876 |
| `explicit.stat_9187492@T2` | -0.95821 |
| `explicit.stat_4015621042@T2` | -0.94937 |
| `explicit.stat_124859000@T2` | -0.94137 |
| `explicit.stat_803737631@T2` | -0.94130 |

### weapon.wand — n=23046, R²=-1.8509

intercept: `3.8541`  ·  log_price: True  ·  ilvl: `-0.04765`  ·  n_mods: `-0.07949`  ·  n_top_tier: `0.57396`  ·  corrupted: `0.09813`  ·  n_sockets: `0.02334`  ·  quality: `0.04016`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -4.45628 |
| `explicit.stat_1545858329@T1` | 2.48493 |
| `explicit.stat_2254480358@T1` | 2.38176 |
| `explicit.stat_124131830@T1` | 1.96484 |
| `explicit.stat_591105508@T1` | 1.89495 |
| `explicit.stat_736967255@T2` | 1.56969 |
| `explicit.stat_4226189338@T1` | 1.29857 |
| `explicit.stat_2254480358@T2` | 1.17497 |
| `crafted.stat_124131830` | 1.12089 |
| `explicit.stat_1263695895@T2` | -1.03101 |
| `explicit.stat_3962278098@T2` | -0.96078 |
| `explicit.stat_1263695895@T1` | -0.94283 |

### flask.charm — n=19986, R²=-0.6599

intercept: `0.1066`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00002`  ·  n_top_tier: `1.78235`  ·  corrupted: `1.53364`  ·  quality: `0.00999`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60040 |
| `explicit.stat_1056492907` | 2.59947 |
| `explicit.stat_1120862500@T2` | -1.78239 |
| `explicit.stat_828533480@T2` | -1.78238 |
| `explicit.stat_1873752457@T2` | -1.78235 |
| `explicit.stat_3196823591@T2` | -1.78229 |
| `explicit.stat_2676834156@T2` | -1.78229 |
| `explicit.stat_2365392475@T2` | -1.78227 |
| `explicit.stat_388617051@T2` | -1.78153 |
| `explicit.stat_828533480@T1` | -1.78104 |
| `explicit.stat_3246948616` | 1.78034 |
| `explicit.stat_2541588185@T2` | -1.77915 |

### weapon.bow — n=18400, R²=-1.6156

intercept: `3.8625`  ·  log_price: True  ·  ilvl: `-0.04527`  ·  n_mods: `-0.11523`  ·  n_top_tier: `0.72624`  ·  corrupted: `0.70743`  ·  n_sockets: `0.08763`  ·  quality: `0.02764`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 3.41435 |
| `desecrated.stat_210067635@T1` | -1.87525 |
| `explicit.stat_1263695895@T1` | -1.47093 |
| `explicit.stat_1263695895@T2` | -1.31936 |
| `crafted.stat_210067635@T2` | -1.22925 |
| `crafted.stat_3035140377` | 1.08601 |
| `explicit.stat_2463230181@T2` | -1.04318 |
| `explicit.stat_1509134228@T1` | -0.99210 |
| `explicit.stat_3695891184@T1` | -0.94956 |
| `explicit.stat_3695891184@T2` | -0.89681 |
| `explicit.stat_1368271171@T2` | -0.86807 |
| `explicit.stat_210067635@T2` | -0.86619 |

### weapon.crossbow — n=17226, R²=-1.6491

intercept: `4.0886`  ·  log_price: True  ·  ilvl: `-0.04913`  ·  n_mods: `-0.09450`  ·  n_top_tier: `0.33915`  ·  corrupted: `-0.06603`  ·  n_sockets: `0.07510`  ·  quality: `0.01747`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.78074 |
| `explicit.stat_1980802737` | 1.43163 |
| `explicit.stat_1202301673@T1` | 1.38149 |
| `explicit.stat_2250681686@T2` | -1.36694 |
| `explicit.stat_1509134228@T1` | 1.23375 |
| `explicit.stat_2250681686` | 1.07565 |
| `explicit.stat_709508406@T1` | 0.95147 |
| `crafted.stat_3035140377` | 0.82942 |
| `explicit.stat_3695891184@T1` | -0.66728 |
| `explicit.stat_3695891184@T2` | -0.61930 |
| `explicit.stat_1263695895@T2` | -0.59988 |
| `explicit.stat_3336890334@T2` | -0.59932 |

### weapon.warstaff — n=12047, R²=-0.3436

intercept: `-10.1590`  ·  log_price: True  ·  ilvl: `0.13750`  ·  n_mods: `-0.22768`  ·  n_top_tier: `0.49899`  ·  corrupted: `0.21613`  ·  n_sockets: `0.14049`  ·  quality: `0.05430`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | 1.39166 |
| `desecrated.stat_2231156303@T1` | 1.39166 |
| `explicit.stat_328541901@T2` | -0.96630 |
| `explicit.stat_821021828@T2` | -0.95041 |
| `crafted.stat_210067635@T2` | 0.92457 |
| `explicit.stat_328541901@T1` | -0.85621 |
| `explicit.stat_1037193709@T2` | -0.83710 |
| `desecrated.stat_9187492` | 0.76827 |
| `rune.stat_243313994` | 0.76781 |
| `explicit.stat_1368271171@T1` | -0.64859 |
| `explicit.stat_691932474@T2` | -0.63770 |
| `explicit.stat_3336890334@T1` | -0.58271 |

### weapon.staff — n=11474, R²=-0.3592

intercept: `-16.1441`  ·  log_price: True  ·  ilvl: `0.20529`  ·  n_mods: `-0.06464`  ·  n_top_tier: `0.53265`  ·  corrupted: `0.80218`  ·  n_sockets: `0.17339`  ·  quality: `0.03316`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 1.76176 |
| `explicit.stat_124131830@T1` | 1.73090 |
| `explicit.stat_1600707273@T1` | 1.43696 |
| `explicit.stat_591105508@T1` | 1.33174 |
| `explicit.stat_1545858329@T1` | 1.26710 |
| `explicit.stat_293638271@T2` | -1.18291 |
| `explicit.stat_473429811@T2` | -0.80734 |
| `explicit.stat_3962278098@T2` | 0.78440 |
| `rune.stat_124131830` | 0.74626 |
| `explicit.stat_124131830@T2` | 0.71478 |
| `explicit.stat_4226189338@T2` | 0.69766 |
| `explicit.stat_2254480358@T1` | 0.67753 |

### weapon.sceptre — n=11228, R²=-0.3447

intercept: `-20.4422`  ·  log_price: True  ·  ilvl: `0.25907`  ·  n_mods: `-0.03364`  ·  n_top_tier: `0.06133`  ·  corrupted: `0.35601`  ·  n_sockets: `0.20472`  ·  quality: `0.03926`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.93740 |
| `explicit.stat_2162097452@T2` | 1.57568 |
| `explicit.stat_3057012405@T1` | 1.19017 |
| `explicit.stat_1263695895@T1` | -1.14578 |
| `explicit.stat_1263695895@T2` | -1.08921 |
| `explicit.stat_101878827@T2` | 0.94374 |
| `explicit.stat_101878827@T1` | 0.94046 |
| `explicit.stat_1798257884@T2` | 0.84968 |
| `explicit.stat_2854751904@T2` | -0.70154 |
| `explicit.stat_849987426@T1` | 0.53306 |
| `explicit.stat_2347036682@T2` | -0.50271 |
| `explicit.stat_2347036682@T1` | 0.48543 |

### weapon.spear — n=9094, R²=-0.3862

intercept: `-13.1015`  ·  log_price: True  ·  ilvl: `0.17816`  ·  n_mods: `-0.12886`  ·  n_top_tier: `0.55039`  ·  corrupted: `-0.48779`  ·  n_sockets: `0.16610`  ·  quality: `0.07564`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -4.84091 |
| `crafted.stat_210067635@T2` | -3.14342 |
| `explicit.stat_9187492@T1` | 1.00550 |
| `explicit.stat_1202301673@T1` | 0.95239 |
| `crafted.stat_3035140377` | 0.93779 |
| `explicit.stat_3336890334@T2` | -0.93417 |
| `explicit.stat_4080418644@T2` | -0.92567 |
| `explicit.stat_1940865751@T2` | -0.91140 |
| `explicit.stat_748522257@T2` | -0.87675 |
| `desecrated.stat_210067635@T1` | -0.82018 |
| `explicit.stat_691932474@T2` | -0.81491 |
| `explicit.stat_1037193709@T1` | -0.78184 |

### armour.focus — n=7456, R²=-0.3327

intercept: `-15.7406`  ·  log_price: True  ·  ilvl: `0.19960`  ·  n_mods: `-0.12558`  ·  n_top_tier: `0.93063`  ·  corrupted: `0.07131`  ·  n_sockets: `0.26407`  ·  quality: `0.03208`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 2.49303 |
| `explicit.stat_4220027924@T1` | -1.47010 |
| `explicit.stat_2923486259@T1` | -1.27437 |
| `explicit.stat_2923486259@T2` | -1.16567 |
| `explicit.stat_4220027924@T2` | -1.11526 |
| `explicit.stat_2231156303@T2` | -1.10972 |
| `explicit.stat_2339757871@T2` | -1.06823 |
| `explicit.stat_2768835289@T1` | -1.05184 |
| `explicit.stat_4015621042@T1` | -1.03678 |
| `explicit.stat_1050105434@T2` | -1.00859 |
| `explicit.stat_2231156303@T1` | -0.99881 |
| `explicit.stat_3291658075@T2` | -0.97062 |

### armour.quiver — n=6934, R²=-0.2893

intercept: `-18.1042`  ·  log_price: True  ·  ilvl: `0.21653`  ·  n_mods: `-0.03049`  ·  n_top_tier: `0.69945`  ·  corrupted: `0.96111`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.70396 |
| `explicit.stat_681332047@T2` | -1.49037 |
| `explicit.stat_681332047@T1` | -1.26472 |
| `explicit.stat_1573130764@T2` | -1.01911 |
| `explicit.stat_1573130764@T1` | -0.94819 |
| `explicit.stat_2194114101@T2` | -0.78801 |
| `explicit.stat_4067062424@T1` | -0.72837 |
| `explicit.stat_2321178454@T2` | -0.70230 |
| `explicit.stat_803737631@T1` | -0.66324 |
| `explicit.stat_3261801346@T1` | -0.61893 |
| `explicit.stat_2463230181@T1` | 0.61614 |
| `explicit.stat_4067062424@T2` | -0.51530 |

### armour.shield — n=5966, R²=-0.4281

intercept: `-12.5583`  ·  log_price: True  ·  ilvl: `0.16684`  ·  n_mods: `-0.15931`  ·  n_top_tier: `0.68101`  ·  corrupted: `-0.29021`  ·  n_sockets: `0.40501`  ·  quality: `0.03854`

| stat_id | coef |
|---|---|
| `explicit.stat_3855016469@T1` | -1.39234 |
| `explicit.stat_2901986750@T1` | -1.19511 |
| `explicit.stat_2481353198@T1` | -1.07294 |
| `explicit.stat_3321629045@T2` | -1.06200 |
| `explicit.stat_328541901@T1` | -1.04739 |
| `explicit.stat_2481353198@T2` | -1.02506 |
| `explicit.stat_4095671657@T2` | -1.02266 |
| `explicit.stat_4095671657@T1` | -1.00369 |
| `explicit.stat_4220027924@T1` | -0.98183 |
| `explicit.stat_1011760251@T1` | -0.97594 |
| `explicit.stat_328541901@T2` | -0.97276 |
| `explicit.stat_2923486259@T1` | -0.94454 |

### weapon.twomace — n=5440, R²=-0.4492

intercept: `-11.8433`  ·  log_price: True  ·  ilvl: `0.15655`  ·  n_mods: `-0.20265`  ·  n_top_tier: `0.51232`  ·  corrupted: `0.75130`  ·  n_sockets: `0.11739`  ·  quality: `0.06786`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.68093 |
| `explicit.stat_1037193709@T1` | -1.82647 |
| `explicit.stat_1263695895@T2` | -1.49174 |
| `explicit.stat_3336890334@T1` | -1.43341 |
| `explicit.stat_9187492@T1` | -1.12793 |
| `explicit.stat_1263695895@T1` | -1.04713 |
| `explicit.stat_2694482655@T1` | 0.88770 |
| `explicit.stat_3695891184@T1` | -0.84323 |
| `explicit.stat_518292764@T2` | -0.82231 |
| `explicit.stat_3695891184@T2` | -0.81095 |
| `explicit.stat_821021828@T1` | -0.77564 |
| `explicit.stat_691932474@T1` | -0.72455 |

## Coverage (listings per base)

- … **Sapphire** — 37135 listings (37076 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 36184 listings (36138 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 27673 listings (27642 priced) [0.3–3985176410.3 ex]
- … **Utility Belt** — 12797 listings (12779 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 11735 listings (11711 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 11399 listings (11373 priced) [1.0–3985176410.3 ex]
- … **Amethyst Ring** — 11265 listings (11253 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 10578 listings (10552 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 10523 listings (10500 priced) [0.2–3985176410.3 ex]
- … **Stellar Amulet** — 9989 listings (9976 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 8735 listings (8720 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 8378 listings (8369 priced) [0.3–3985176410.3 ex]
- … **Ruby Ring** — 8318 listings (8309 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7433 listings (7410 priced) [0.3–4297682211.9 ex]
- … **Unset Ring** — 7225 listings (7206 priced) [0.2–39887666593.4 ex]
- … **Lapis Amulet** — 7211 listings (7204 priced) [0.3–3985176410.3 ex]
- … **Jade Amulet** — 7151 listings (7136 priced) [0.3–4275054.0 ex]
- … **Amber Amulet** — 7072 listings (7064 priced) [0.3–3985176410.3 ex]
- … **Plate Belt** — 6979 listings (6950 priced) [0.3–398912568423.8 ex]
- … **Pearl Ring** — 6953 listings (6944 priced) [0.2–275252424.7 ex]
- … **Ancestral Tiara** — 6922 listings (6893 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 6838 listings (6828 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6534 listings (6531 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6424 listings (6410 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 6194 listings (6182 priced) [0.3–398912568423.8 ex]
