# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-03T00:08:52+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **25931** (25931 priced in exalted)
- Distinct bases: 629 · distinct mods: 965 · mod rows: 141332
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-02T23:52:04+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×29.52** (median |log error| 3.385)
- Within ±30% of asking price: **31%**
- Skill vs constant-price guess: **+0.03** (> 0 = the mods carry signal)
- Calibration: 67% of actuals above prediction (target ≈ 75%)

| group | n_test | ×err | ±30% | skill |
|---|---|---|---|---|
| armour.helmet | 464 | ×40.63 | 26% | +0.04 |
| accessory.belt | 458 | ×23.58 | 34% | +0.05 |
| armour.gloves | 442 | ×159.68 | 20% | -0.02 |
| armour.chest | 430 | ×39.20 | 16% | +0.05 |
| armour.boots | 414 | ×87.58 | 27% | +0.14 |
| accessory.amulet | 410 | ×38.73 | 3% | -0.03 |
| weapon.wand | 371 | ×171.43 | 22% | +0.03 |
| accessory.ring | 357 | ×18.98 | 5% | -0.23 |
| weapon.bow | 338 | ×31.64 | 23% | +0.09 |
| weapon.crossbow | 320 | ×109.69 | 22% | +0.09 |
| other | 241 | ×1.00 | 68% | +0.02 |
| armour.focus | 131 | ×1.00 | 99% | +0.00 |
| weapon.sceptre | 125 | ×1.00 | 100% | +0.00 |
| weapon.spear | 124 | ×1.00 | 100% | +0.00 |
| armour.shield | 92 | ×1.00 | 100% | n/a |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### accessory.belt — n=2207, R²=-0.8267

intercept: `1.9579`  ·  log_price: True  ·  ilvl: `-0.02421`  ·  n_mods: `-0.00922`  ·  n_top_tier: `-0.08693`  ·  corrupted: `0.03471`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 0.62684 |
| `explicit.stat_3299347043@T1` | 0.27591 |
| `explicit.stat_3299347043@T2` | 0.22957 |
| `pseudo.total_ele_res>=80` | 0.22009 |
| `implicit.stat_731781020` | 0.21934 |
| `explicit.stat_2639966148` | 0.20578 |
| `explicit.stat_3372524247@T1` | 0.16574 |
| `explicit.stat_174664100` | 0.15296 |
| `explicit.stat_3585532255@T1` | 0.14543 |
| `explicit.stat_51994685@T1` | 0.13805 |
| `explicit.stat_2881298780@T1` | 0.13552 |
| `explicit.stat_2881298780@T2` | 0.13509 |

### armour.boots — n=2146, R²=-0.662

intercept: `7.6061`  ·  log_price: True  ·  ilvl: `-0.09424`  ·  n_mods: `-0.05214`  ·  n_top_tier: `0.63565`  ·  corrupted: `0.26132`  ·  n_sockets: `0.11461`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 5.36496 |
| `crafted.stat_3917489142@T1` | 3.67974 |
| `explicit.stat_3261801346@T2` | -0.92591 |
| `explicit.stat_2451402625@T1` | -0.89916 |
| `explicit.stat_3484657501@T2` | -0.83377 |
| `explicit.stat_124859000@T2` | -0.81277 |
| `explicit.stat_3321629045@T1` | -0.80036 |
| `explicit.stat_3917489142@T2` | -0.78678 |
| `explicit.stat_2923486259@T2` | -0.76076 |
| `explicit.stat_3321629045@T2` | -0.74768 |
| `explicit.stat_3261801346@T1` | -0.74164 |
| `explicit.stat_1062208444@T1` | -0.73920 |

### armour.helmet — n=2119, R²=-0.8783

intercept: `7.4827`  ·  log_price: True  ·  ilvl: `-0.09514`  ·  n_mods: `-0.04054`  ·  n_top_tier: `0.59544`  ·  corrupted: `1.89473`  ·  n_sockets: `0.08118`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | -4.38786 |
| `desecrated.stat_4015621042@T1` | -3.10331 |
| `desecrated.stat_4015621042@T2` | -2.53916 |
| `explicit.stat_4220027924@T1` | 2.34389 |
| `desecrated.stat_3299347043@T2` | 1.71614 |
| `explicit.stat_3261801346@T2` | -0.81250 |
| `explicit.stat_3917489142@T2` | -0.80856 |
| `explicit.stat_1263695895@T1` | -0.80157 |
| `explicit.stat_3484657501@T1` | -0.79721 |
| `explicit.stat_2923486259@T2` | -0.76439 |
| `explicit.stat_1263695895@T2` | -0.75796 |
| `explicit.stat_3917489142@T1` | -0.74885 |

### armour.chest — n=2109, R²=-0.7442

intercept: `8.3984`  ·  log_price: True  ·  ilvl: `-0.10699`  ·  n_mods: `-0.03805`  ·  n_top_tier: `0.49623`  ·  corrupted: `-1.14097`  ·  n_sockets: `0.04951`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | 7.02650 |
| `explicit.stat_1671376347@T1` | 3.14584 |
| `explicit.stat_3981240776@T1` | 2.98417 |
| `explicit.stat_3372524247@T1` | 1.92653 |
| `desecrated.stat_3299347043@T1` | 1.12969 |
| `explicit.stat_3261801346@T1` | -1.11339 |
| `explicit.stat_3299347043@T1` | 1.10796 |
| `explicit.stat_4220027924@T1` | 1.08193 |
| `explicit.stat_2339757871@T1` | -1.04741 |
| `explicit.stat_2339757871@T2` | -1.02278 |
| `explicit.stat_328541901@T1` | 0.94919 |
| `explicit.stat_124859000@T1` | -0.89027 |

### armour.gloves — n=2079, R²=-0.8891

intercept: `7.5535`  ·  log_price: True  ·  ilvl: `-0.09674`  ·  n_mods: `0.03855`  ·  n_top_tier: `0.23351`  ·  corrupted: `-0.06892`  ·  n_sockets: `0.00756`

| stat_id | coef |
|---|---|
| `explicit.stat_3372524247@T1` | 4.95866 |
| `explicit.stat_4067062424@T2` | 4.74743 |
| `rune.stat_201332984` | 0.99706 |
| `explicit.stat_2451402625@T2` | -0.62428 |
| `explicit.stat_9187492@T1` | 0.51084 |
| `explicit.stat_124859000@T2` | -0.47860 |
| `explicit.stat_9187492@T2` | -0.45417 |
| `explicit.stat_1671376347@T2` | -0.40400 |
| `explicit.stat_124859000@T1` | -0.35478 |
| `explicit.stat_4052037485@T2` | -0.34959 |
| `explicit.stat_681332047@T1` | 0.34566 |
| `explicit.stat_2797971005@T2` | -0.32820 |

### accessory.amulet — n=1946, R²=-0.8382

intercept: `9.7054`  ·  log_price: True  ·  ilvl: `-0.10737`  ·  n_mods: `-0.50797`  ·  n_top_tier: `1.51520`  ·  corrupted: `-0.71099`  ·  n_sockets: `0.00611`

| stat_id | coef |
|---|---|
| `explicit.stat_9187492@T2` | -4.95954 |
| `explicit.stat_2748665614@T2` | -4.90145 |
| `explicit.stat_1050105434@T1` | -4.82120 |
| `explicit.stat_2748665614@T1` | -4.67893 |
| `explicit.stat_2923486259@T2` | -3.50591 |
| `explicit.stat_2923486259@T1` | -3.45951 |
| `explicit.stat_1202301673@T2` | 3.42748 |
| `explicit.stat_328541901@T1` | -3.42695 |
| `explicit.stat_2482852589@T1` | -3.37309 |
| `explicit.stat_1444556985@T1` | 3.26146 |
| `explicit.stat_4220027924@T2` | -3.23911 |
| `explicit.stat_2482852589@T2` | -3.23056 |

### weapon.wand — n=1762, R²=-0.8704

intercept: `7.5610`  ·  log_price: True  ·  ilvl: `-0.09379`  ·  n_mods: `-0.03742`  ·  n_top_tier: `0.29303`  ·  corrupted: `0.52547`  ·  n_sockets: `-0.09184`

| stat_id | coef |
|---|---|
| `explicit.stat_1600707273@T1` | 6.20529 |
| `explicit.stat_1545858329@T1` | 5.97577 |
| `explicit.stat_2254480358@T1` | 5.95732 |
| `explicit.stat_591105508@T1` | 5.90488 |
| `explicit.stat_274716455@T2` | 5.22391 |
| `explicit.stat_2231156303@T1` | 4.80465 |
| `explicit.stat_124131830@T1` | 4.77564 |
| `explicit.stat_4226189338@T1` | 4.65454 |
| `crafted.stat_124131830` | 1.61840 |
| `explicit.stat_2974417149@T1` | 0.92795 |
| `explicit.stat_124131830@T2` | -0.85996 |
| `explicit.stat_1263695895@T2` | -0.71571 |

### accessory.ring — n=1756, R²=-0.2646

intercept: `10.0266`  ·  log_price: True  ·  ilvl: `-0.05250`  ·  n_mods: `-0.39654`  ·  n_top_tier: `0.46777`  ·  corrupted: `1.24978`  ·  n_sockets: `0.78291`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T2` | -5.57436 |
| `explicit.stat_3695891184@T1` | -3.93993 |
| `explicit.stat_1263695895@T1` | -3.47737 |
| `explicit.stat_2923486259@T2` | -3.37711 |
| `explicit.stat_707457662@T2` | 2.90830 |
| `explicit.stat_3299347043@T1` | -2.82504 |
| `explicit.stat_1379411836@T2` | -2.62207 |
| `explicit.stat_1379411836@T1` | -2.13660 |
| `explicit.stat_707457662@T1` | 1.88031 |
| `explicit.stat_1263695895@T2` | -1.86860 |
| `explicit.stat_3261801346@T1` | 1.72137 |
| `explicit.stat_1050105434@T1` | -1.70982 |

### weapon.bow — n=1535, R²=-0.7714

intercept: `7.7065`  ·  log_price: True  ·  ilvl: `-0.09461`  ·  n_mods: `-0.08594`  ·  n_top_tier: `-0.04965`  ·  corrupted: `0.62831`  ·  n_sockets: `0.05830`

| stat_id | coef |
|---|---|
| `desecrated.stat_1200678966@T1` | -5.51151 |
| `explicit.stat_2463230181@T1` | 5.42695 |
| `explicit.stat_1037193709@T1` | 4.95786 |
| `desecrated.stat_666077204@T1` | -4.32820 |
| `explicit.stat_518292764@T1` | 3.64292 |
| `explicit.stat_1202301673@T1` | 2.82394 |
| `rune.stat_3885405204` | -2.51837 |
| `desecrated.stat_210067635@T1` | 2.48520 |
| `explicit.stat_210067635@T2` | 1.31974 |
| `explicit.stat_1263695895@T1` | 1.20016 |
| `explicit.stat_1263695895@T2` | 1.03111 |
| `explicit.stat_1509134228@T1` | 1.01231 |

### weapon.crossbow — n=1497, R²=-0.7599

intercept: `8.0292`  ·  log_price: True  ·  ilvl: `-0.10070`  ·  n_mods: `-0.02911`  ·  n_top_tier: `0.51714`  ·  corrupted: `0.47849`  ·  n_sockets: `0.02958`

| stat_id | coef |
|---|---|
| `desecrated.stat_2760344900@T1` | -12.60482 |
| `explicit.stat_1037193709@T1` | 5.73562 |
| `crafted.stat_210067635@T2` | -4.98973 |
| `explicit.stat_3336890334@T1` | 4.83264 |
| `explicit.stat_709508406@T1` | 3.66473 |
| `explicit.stat_1980802737@T2` | 2.89564 |
| `explicit.stat_1980802737` | 2.89564 |
| `explicit.stat_1967051901@T2` | 1.40151 |
| `explicit.stat_1967051901@T1` | -1.16981 |
| `desecrated.stat_2760344900` | 0.83306 |
| `explicit.stat_709508406@T2` | 0.82320 |
| `explicit.stat_3695891184@T2` | -0.77991 |

### other — n=1148, R²=-0.1058

intercept: `0.0001`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_1368271171@T1` | 0.69306 |
| `rune.stat_3990135792` | -0.08180 |
| `rune.stat_2974417149` | 0.03272 |
| `explicit.stat_124131830@T1` | 0.01747 |
| `explicit.stat_3962278098` | 0.01110 |
| `explicit.stat_3291658075` | 0.00503 |
| `crafted.stat_210067635@T2` | 0.00031 |
| `explicit.stat_1368271171@T2` | -0.00014 |
| `explicit.stat_55876295@T1` | -0.00010 |
| `explicit.stat_2974417149@T1` | 0.00008 |
| `explicit.stat_803737631@T2` | -0.00008 |
| `explicit.stat_789117908@T2` | 0.00007 |

### weapon.sceptre — n=688, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_1798257884` | 0.00000 |
| `desecrated.stat_3984865854` | 0.00000 |
| `explicit.stat_101878827` | 0.00000 |
| `explicit.stat_101878827@T1` | 0.00000 |
| `explicit.stat_101878827@T2` | 0.00000 |
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_1250712710` | 0.00000 |
| `explicit.stat_1250712710@T1` | 0.00000 |
| `explicit.stat_1250712710@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |

### weapon.spear — n=620, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_1509134228` | 0.00000 |
| `desecrated.stat_691932474` | 0.00000 |
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1202301673` | 0.00000 |
| `explicit.stat_1202301673@T1` | 0.00000 |
| `explicit.stat_1202301673@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1263695895@T2` | -0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |

### armour.focus — n=600, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_1671376347` | 0.00000 |
| `desecrated.stat_2891184298` | 0.00000 |
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_124131830` | 0.00000 |
| `explicit.stat_124131830@T1` | -0.00000 |
| `explicit.stat_124131830@T2` | 0.00000 |
| `explicit.stat_1671376347` | 0.00000 |
| `explicit.stat_1671376347@T1` | 0.00000 |
| `explicit.stat_1671376347@T2` | 0.00000 |
| `explicit.stat_2231156303` | 0.00000 |

### armour.shield — n=507, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  n_sockets: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1568848828` | 0.00000 |
| `explicit.stat_1011760251` | 0.00000 |
| `explicit.stat_1011760251@T1` | -0.00000 |
| `explicit.stat_1011760251@T2` | -0.00000 |
| `explicit.stat_1062208444` | 0.00000 |
| `explicit.stat_1062208444@T1` | 0.00000 |
| `explicit.stat_1062208444@T2` | 0.00000 |
| `explicit.stat_1301765461` | 0.00000 |
| `explicit.stat_1301765461@T2` | 0.00000 |
| `explicit.stat_1671376347` | 0.00000 |
| `explicit.stat_1671376347@T1` | 0.00000 |
| `explicit.stat_1671376347@T2` | 0.00000 |

### jewel — n=180, R²=-0.338

intercept: `-0.0990`  ·  log_price: True  ·  ilvl: `0.00488`  ·  n_mods: `0.60751`  ·  n_top_tier: `-0.46079`

| stat_id | coef |
|---|---|
| `explicit.stat_3141070085@T1` | 8.28278 |
| `explicit.stat_2843214518@T1` | 6.18276 |
| `explicit.stat_1589917703@T1` | 4.93842 |
| `explicit.stat_1062710370@T1` | 3.34058 |
| `explicit.stat_1423639565@T1` | -3.09216 |
| `explicit.stat_3962278098@T1` | -2.98858 |
| `explicit.stat_1002362373@T1` | 2.36757 |
| `explicit.stat_416040624@T1` | 2.18953 |
| `explicit.stat_101878827@T1` | 2.09484 |
| `explicit.stat_4045894391@T1` | -1.64971 |
| `explicit.stat_44972811@T1` | 1.50408 |
| `explicit.stat_2440073079@T1` | 1.31643 |

### armour.quiver — n=90, R²=-0.0328

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_681332047@T2` | -0.00005 |
| `explicit.stat_4067062424@T2` | -0.00003 |
| `explicit.stat_681332047@T1` | -0.00002 |
| `explicit.stat_3032590688@T2` | 0.00002 |
| `explicit.stat_3695891184@T1` | 0.00002 |
| `explicit.stat_1368271171@T1` | 0.00002 |
| `explicit.stat_1573130764@T2` | 0.00001 |
| `explicit.stat_1368271171@T2` | 0.00001 |
| `explicit.stat_3261801346@T1` | -0.00001 |
| `explicit.stat_3759663284@T2` | 0.00000 |
| `explicit.stat_2321178454@T2` | 0.00000 |
| `explicit.stat_681332047` | 0.00000 |

### weapon.staff — n=90, R²=-0.0645

intercept: `0.0005`  ·  log_price: True  ·  ilvl: `-0.00001`  ·  n_mods: `0.00001`  ·  n_top_tier: `-0.00002`  ·  n_sockets: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_1263695895@T1` | 0.00024 |
| `explicit.stat_3695891184@T1` | -0.00015 |
| `explicit.stat_3695891184@T2` | -0.00009 |
| `explicit.stat_3278136794@T2` | 0.00006 |
| `explicit.stat_1368271171@T1` | -0.00005 |
| `explicit.stat_3639275092@T1` | 0.00004 |
| `explicit.stat_2505884597@T1` | 0.00004 |
| `explicit.stat_1050105434@T2` | 0.00003 |
| `explicit.stat_328541901@T1` | -0.00003 |
| `explicit.stat_1050105434@T1` | 0.00002 |
| `explicit.stat_789117908@T2` | 0.00002 |
| `explicit.stat_1263695895` | -0.00002 |

### weapon.warstaff — n=90, R²=-0.1151

intercept: `0.0005`  ·  log_price: True  ·  ilvl: `-0.00001`  ·  n_mods: `0.00003`  ·  n_top_tier: `0.00001`  ·  corrupted: `-0.00015`  ·  n_sockets: `0.00004`

| stat_id | coef |
|---|---|
| `explicit.stat_1263695895@T1` | -0.00009 |
| `explicit.stat_691932474@T1` | 0.00007 |
| `explicit.stat_3695891184@T1` | -0.00007 |
| `explicit.stat_791928121@T2` | 0.00004 |
| `explicit.stat_669069897@T1` | 0.00003 |
| `explicit.stat_748522257@T1` | -0.00003 |
| `explicit.stat_55876295@T2` | -0.00003 |
| `explicit.stat_748522257@T2` | -0.00002 |
| `explicit.stat_518292764` | -0.00002 |
| `explicit.stat_387439868@T2` | -0.00001 |
| `explicit.stat_669069897` | -0.00001 |
| `explicit.stat_1263695895` | -0.00001 |

### weapon.twomace — n=90, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  n_sockets: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1509134228` | 0.00000 |
| `explicit.stat_1509134228@T2` | 0.00000 |
| `explicit.stat_1940865751` | 0.00000 |
| `explicit.stat_210067635` | 0.00000 |
| `explicit.stat_2694482655` | 0.00000 |
| `explicit.stat_3336890334` | 0.00000 |
| `explicit.stat_3336890334@T2` | 0.00000 |
| `explicit.stat_3639275092` | 0.00000 |

### flask.charm — n=90, R²=-0.3905

intercept: `0.4470`  ·  log_price: True  ·  ilvl: `0.00008`  ·  n_mods: `-0.00029`  ·  n_top_tier: `-0.00022`

| stat_id | coef |
|---|---|
| `implicit.stat_2994271459` | -0.14550 |
| `explicit.stat_2566921799` | -0.00397 |
| `explicit.stat_1873752457` | 0.00357 |
| `implicit.stat_1412682799` | -0.00105 |
| `implicit.stat_2778646494` | 0.00079 |
| `implicit.stat_3854901951` | 0.00027 |
| `implicit.stat_2016937536` | 0.00023 |
| `implicit.stat_3699444296` | 0.00018 |
| `explicit.stat_2365392475` | 0.00004 |
| `explicit.stat_1366840608` | 0.00002 |
| `explicit.stat_2541588185` | -0.00001 |
| `explicit.stat_388617051` | 0.00001 |

## Coverage (listings per base)

- … **Dueling Wand** — 550 listings (550 priced) [1.0–719.7 ex]
- … **Obliterator Bow** — 448 listings (448 priced) [0.5–719.7 ex]
- … **Utility Belt** — 404 listings (404 priced) [1.0–737.3 ex]
- … **Siphoning Wand** — 329 listings (329 priced) [1.0–719.7 ex]
- … **Warmonger Bow** — 323 listings (323 priced) [1.0–719.7 ex]
- … **Solar Amulet** — 320 listings (320 priced) [1.0–737.3 ex]
- … **Plate Belt** — 318 listings (318 priced) [1.0–737.3 ex]
- … **Gold Amulet** — 312 listings (312 priced) [0.3–737.3 ex]
- … **Galvanic Wand** — 305 listings (305 priced) [1.0–719.7 ex]
- … **Attuned Wand** — 300 listings (300 priced) [0.3–719.7 ex]
- … **Ancestral Tiara** — 291 listings (291 priced) [1.0–737.3 ex]
- … **Withered Wand** — 277 listings (277 priced) [1.0–719.7 ex]
- … **Trarthan Cannon** — 272 listings (272 priced) [0.7–719.7 ex]
- … **Desolate Crossbow** — 261 listings (261 priced) [1.0–719.7 ex]
- … **Heavy Belt** — 258 listings (258 priced) [0.5–737.3 ex]
- … **Long Belt** — 252 listings (252 priced) [1.0–737.3 ex]
- … **Rawhide Belt** — 244 listings (244 priced) [1.0–737.3 ex]
- … **Prismatic Ring** — 241 listings (241 priced) [0.4–737.3 ex]
- … **Siege Crossbow** — 239 listings (239 priced) [0.3–719.7 ex]
- … **Amber Amulet** — 238 listings (238 priced) [0.3–737.3 ex]
- … **Rattling Sceptre** — 238 listings (238 priced) [1.0–1.3 ex]
- … **Stellar Amulet** — 237 listings (237 priced) [1.0–737.3 ex]
- … **Lapis Amulet** — 236 listings (236 priced) [0.6–737.3 ex]
- … **Gemini Bow** — 229 listings (229 priced) [1.0–719.7 ex]
- … **Amethyst Ring** — 228 listings (228 priced) [1.0–737.3 ex]
