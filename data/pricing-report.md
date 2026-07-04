# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-04T21:45:29+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **129175** (129175 priced in exalted)
- Distinct bases: 886 · distinct mods: 2220 · mod rows: 619688
- Sold signals: **34276** sold · 48067 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-04T21:40:09+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×6.68** (median |log error| 1.8987)
- Within ±30% of asking price: **27%**
- Skill vs constant-price guess: **+0.06** (> 0 = the mods carry signal)
- Calibration: 67% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.08** · typical error ×27.55 · ±30% 6% · n=18376
- Premium segment (60ex+): skill **+0.08** · typical error ×148.16 · ±30% 0% · n=10524
- Sold listings (clearing prices): skill **-0.05** · typical error ×2.06 · ±30% 52% · n=6707

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 2207 | ×6.58 | 7% | -0.01 | -0.02 |
| accessory.amulet | 2165 | ×6.45 | 7% | +0.05 | +0.03 |
| accessory.belt | 2091 | ×9.99 | 24% | +0.02 | +0.05 |
| armour.chest | 2025 | ×8.47 | 20% | +0.01 | +0.09 |
| armour.helmet | 2008 | ×8.90 | 21% | +0.01 | +0.08 |
| armour.gloves | 1887 | ×8.63 | 22% | +0.02 | +0.08 |
| armour.boots | 1882 | ×8.66 | 25% | +0.05 | +0.09 |
| other | 1800 | ×6.07 | 35% | +0.41 | +0.37 |
| jewel | 1670 | ×6.77 | 7% | +0.01 | +0.08 |
| weapon.wand | 1415 | ×9.00 | 34% | +0.05 | +0.11 |
| weapon.bow | 1194 | ×8.88 | 35% | +0.08 | +0.10 |
| weapon.crossbow | 1124 | ×8.50 | 30% | +0.07 | +0.12 |
| weapon.sceptre | 294 | ×1.00 | 97% | +0.00 | +0.00 |
| weapon.warstaff | 280 | ×1.00 | 99% | +0.00 | +0.00 |
| weapon.spear | 256 | ×1.00 | 98% | +0.00 | +0.00 |
| weapon.staff | 245 | ×1.00 | 98% | +0.00 | +0.00 |
| armour.focus | 212 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.quiver | 204 | ×1.00 | 96% | +0.00 | +0.00 |
| armour.shield | 185 | ×1.00 | 95% | +0.00 | +0.00 |
| weapon.twomace | 148 | ×1.00 | 97% | +0.00 | +0.00 |
| flask.charm | 99 | ×1.00 | 62% | -0.01 | +0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=15625, R²=-0.3342

intercept: `1.5282`  ·  log_price: True  ·  ilvl: `0.00477`  ·  n_mods: `0.02877`  ·  n_top_tier: `0.16518`  ·  corrupted: `0.42914`  ·  n_sockets: `-0.10853`  ·  quality: `-0.01241`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830` | -0.79662 |
| `implicit.stat_3182714256` | 0.38216 |
| `implicit.stat_718638445` | 0.38204 |
| `implicit.stat_1379411836` | -0.31303 |
| `explicit.stat_1050105434@T1` | -0.27027 |
| `implicit.stat_958696139` | 0.26212 |
| `explicit.stat_3917489142@T1` | -0.23188 |
| `explicit.stat_2974417149@T1` | 0.22978 |
| `implicit.stat_4041853756` | 0.19781 |
| `implicit.stat_3879011313` | 0.19780 |
| `explicit.stat_2891184298@T1` | 0.11873 |
| `implicit.stat_462041840` | -0.09814 |

### accessory.ring — n=10099, R²=-1.9118

intercept: `2.5341`  ·  log_price: True  ·  ilvl: `-0.02688`  ·  n_mods: `0.03648`  ·  n_top_tier: `0.24328`  ·  corrupted: `0.23629`  ·  n_sockets: `3.88993`  ·  quality: `0.00976`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 6.11712 |
| `explicit.stat_707457662@T2` | 5.43161 |
| `explicit.stat_2557965901@T2` | 4.06321 |
| `explicit.stat_2557965901@T1` | 4.05151 |
| `explicit.stat_1573130764@T1` | -1.78202 |
| `explicit.stat_1379411836@T1` | -1.50410 |
| `explicit.stat_3695891184@T2` | -1.41075 |
| `explicit.stat_3962278098@T2` | -1.36316 |
| `explicit.stat_1379411836@T2` | -1.16556 |
| `explicit.stat_3299347043@T1` | -1.12133 |
| `explicit.stat_707457662` | -0.95009 |
| `implicit.stat_958696139` | 0.86994 |

### accessory.amulet — n=10005, R²=-1.6895

intercept: `3.8455`  ·  log_price: True  ·  ilvl: `-0.03633`  ·  n_mods: `-0.23813`  ·  n_top_tier: `0.29151`  ·  corrupted: `0.37394`  ·  n_sockets: `-0.45989`  ·  quality: `0.16314`

| stat_id | coef |
|---|---|
| `explicit.stat_2748665614@T1` | -2.54180 |
| `explicit.stat_2748665614@T2` | -1.74684 |
| `explicit.stat_2923486259@T1` | -1.64711 |
| `explicit.stat_3556824919@T2` | -1.56647 |
| `explicit.stat_2162097452@T2` | -1.45763 |
| `explicit.stat_803737631@T1` | -1.32745 |
| `explicit.stat_1202301673@T2` | 1.30275 |
| `explicit.stat_4220027924@T1` | -1.27125 |
| `explicit.stat_803737631@T2` | -1.21702 |
| `explicit.stat_1444556985@T1` | -1.21270 |
| `explicit.stat_1671376347@T2` | -1.14629 |
| `explicit.stat_4080418644@T1` | -1.09027 |

### accessory.belt — n=9558, R²=-1.2366

intercept: `3.9872`  ·  log_price: True  ·  ilvl: `-0.04798`  ·  n_mods: `-0.02293`  ·  n_top_tier: `-0.00131`  ·  corrupted: `0.09851`  ·  n_sockets: `-0.15107`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 2.71758 |
| `explicit.stat_2923486259@T1` | 1.94840 |
| `explicit.stat_2923486259@T2` | 0.90189 |
| `explicit.stat_1836676211@T1` | 0.65552 |
| `explicit.stat_3299347043@T1` | -0.32990 |
| `explicit.stat_3372524247@T1` | 0.23054 |
| `explicit.stat_4220027924@T1` | 0.22313 |
| `explicit.stat_3299347043@T2` | -0.18688 |
| `implicit.stat_731781020` | -0.15796 |
| `pseudo.total_ele_res>=80` | 0.13915 |
| `explicit.stat_2639966148` | 0.12149 |
| `explicit.stat_1671376347@T1` | 0.10935 |

### armour.chest — n=9320, R²=-1.3445

intercept: `4.1593`  ·  log_price: True  ·  ilvl: `-0.05118`  ·  n_mods: `-0.02739`  ·  n_top_tier: `0.55058`  ·  corrupted: `-0.05345`  ·  n_sockets: `0.00128`  ·  quality: `0.01763`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.93156 |
| `explicit.stat_3981240776@T1` | 1.47903 |
| `explicit.stat_3362812763@T1` | 1.07548 |
| `explicit.stat_4015621042@T2` | -0.70588 |
| `explicit.stat_3261801346@T2` | -0.67609 |
| `explicit.stat_4015621042@T1` | -0.64618 |
| `explicit.stat_4080418644@T2` | -0.63803 |
| `explicit.stat_2923486259@T1` | -0.63208 |
| `explicit.stat_915769802@T1` | -0.62719 |
| `explicit.stat_3261801346@T1` | -0.62711 |
| `explicit.stat_2339757871@T1` | -0.62431 |
| `explicit.stat_3301100256@T2` | -0.62110 |

### armour.helmet — n=9213, R²=-1.3482

intercept: `4.4061`  ·  log_price: True  ·  ilvl: `-0.05595`  ·  n_mods: `-0.02366`  ·  n_top_tier: `0.78254`  ·  corrupted: `0.15995`  ·  n_sockets: `-0.00962`  ·  quality: `0.01983`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 5.25939 |
| `explicit.stat_2339757871@T1` | -1.79949 |
| `explicit.stat_803737631@T2` | -0.92391 |
| `explicit.stat_4052037485@T2` | -0.90234 |
| `explicit.stat_3033371881@T1` | -0.89704 |
| `explicit.stat_3325883026@T1` | -0.88586 |
| `explicit.stat_53045048@T1` | -0.86832 |
| `explicit.stat_3321629045@T2` | -0.86781 |
| `explicit.stat_1062208444@T2` | -0.85802 |
| `explicit.stat_3639275092@T1` | -0.85357 |
| `explicit.stat_3321629045@T1` | -0.84475 |
| `explicit.stat_4015621042@T2` | -0.84398 |

### armour.boots — n=8626, R²=-1.1091

intercept: `4.0853`  ·  log_price: True  ·  ilvl: `-0.05061`  ·  n_mods: `-0.02957`  ·  n_top_tier: `0.59949`  ·  corrupted: `0.05329`  ·  n_sockets: `0.01415`  ·  quality: `0.01856`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.61795 |
| `explicit.stat_2339757871@T1` | -0.93886 |
| `explicit.stat_3362812763@T1` | -0.76148 |
| `explicit.stat_3362812763@T2` | -0.73099 |
| `explicit.stat_3321629045@T1` | -0.69178 |
| `explicit.stat_99927264@T1` | -0.68363 |
| `explicit.stat_1062208444@T1` | -0.66723 |
| `explicit.stat_2160282525@T1` | -0.66517 |
| `explicit.stat_3261801346@T2` | -0.66301 |
| `explicit.stat_1062208444@T2` | -0.65927 |
| `explicit.stat_3033371881@T2` | -0.65903 |
| `explicit.stat_1874553720@T2` | -0.65791 |

### armour.gloves — n=8569, R²=-1.3558

intercept: `4.2647`  ·  log_price: True  ·  ilvl: `-0.05440`  ·  n_mods: `0.00921`  ·  n_top_tier: `1.00276`  ·  corrupted: `-0.00842`  ·  n_sockets: `0.00174`  ·  quality: `0.01577`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -4.21736 |
| `explicit.stat_681332047@T2` | -1.16061 |
| `explicit.stat_9187492@T2` | -1.14165 |
| `explicit.stat_4015621042@T1` | -1.11220 |
| `explicit.stat_124859000@T1` | -1.09357 |
| `explicit.stat_2451402625@T2` | -1.08789 |
| `explicit.stat_3032590688@T1` | -1.07385 |
| `explicit.stat_803737631@T1` | -1.07098 |
| `explicit.stat_803737631@T2` | -1.06956 |
| `explicit.stat_3484657501@T2` | -1.06861 |
| `explicit.stat_53045048@T1` | -1.04964 |
| `explicit.stat_681332047@T1` | -1.04528 |

### jewel — n=8332, R²=-0.9568

intercept: `-1.3248`  ·  log_price: True  ·  ilvl: `0.03595`  ·  n_mods: `0.17885`  ·  n_top_tier: `-0.41609`  ·  corrupted: `0.43237`

| stat_id | coef |
|---|---|
| `explicit.stat_2301718443@T1` | -5.65371 |
| `explicit.stat_1569101201@T1` | 5.20366 |
| `explicit.stat_2011656677@T1` | 3.87206 |
| `explicit.stat_293638271@T1` | -3.59888 |
| `explicit.stat_2456523742@T1` | 3.43115 |
| `explicit.stat_491450213@T1` | 2.68366 |
| `explicit.stat_153777645@T1` | -2.60031 |
| `explicit.stat_3141070085@T1` | 2.58568 |
| `explicit.stat_3851254963@T1` | 2.57957 |
| `explicit.stat_1854213750@T1` | 2.32668 |
| `explicit.stat_1459321413@T1` | 2.32379 |
| `explicit.stat_1316278494@T1` | -2.22852 |

### weapon.wand — n=6516, R²=-1.6379

intercept: `3.4101`  ·  log_price: True  ·  ilvl: `-0.04233`  ·  n_mods: `-0.01452`  ·  n_top_tier: `0.54696`  ·  corrupted: `0.00215`  ·  n_sockets: `-0.00043`  ·  quality: `0.02485`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 2.43456 |
| `explicit.stat_591105508@T1` | 1.79398 |
| `explicit.stat_1545858329@T1` | 1.76042 |
| `explicit.stat_4226189338@T1` | 1.75262 |
| `explicit.stat_2254480358@T1` | 1.70967 |
| `explicit.stat_736967255@T2` | 1.31088 |
| `crafted.stat_124131830` | 1.07050 |
| `explicit.stat_2968503605@T1` | 0.96608 |
| `explicit.stat_3962278098@T2` | -0.66692 |
| `explicit.stat_2768835289@T2` | -0.65326 |
| `explicit.stat_293638271@T2` | -0.64725 |
| `explicit.stat_274716455@T1` | -0.61236 |

### weapon.bow — n=5509, R²=-1.575

intercept: `3.4385`  ·  log_price: True  ·  ilvl: `-0.04268`  ·  n_mods: `-0.02887`  ·  n_top_tier: `0.36008`  ·  corrupted: `-0.04986`  ·  n_sockets: `0.00761`  ·  quality: `0.00033`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -6.47282 |
| `explicit.stat_2463230181@T1` | 1.90088 |
| `explicit.stat_1509134228@T1` | 1.82980 |
| `explicit.stat_518292764@T1` | 1.79286 |
| `explicit.stat_1202301673@T1` | 1.55858 |
| `crafted.stat_3035140377` | 0.69409 |
| `rune.stat_3885405204` | -0.56484 |
| `explicit.stat_821021828@T1` | -0.47920 |
| `explicit.stat_1940865751@T1` | -0.46773 |
| `explicit.stat_1263695895@T1` | -0.43432 |
| `explicit.stat_3261801346@T1` | -0.43316 |
| `explicit.stat_691932474@T2` | -0.43277 |

### weapon.crossbow — n=5231, R²=-1.4361

intercept: `3.4978`  ·  log_price: True  ·  ilvl: `-0.04371`  ·  n_mods: `-0.00557`  ·  n_top_tier: `0.14734`  ·  corrupted: `-0.03750`  ·  n_sockets: `0.02181`  ·  quality: `-0.00468`

| stat_id | coef |
|---|---|
| `explicit.stat_2250681686@T2` | -3.34089 |
| `explicit.stat_2250681686` | 3.20671 |
| `explicit.stat_709508406@T1` | 2.46780 |
| `explicit.stat_3336890334@T1` | 2.09069 |
| `explicit.stat_1037193709@T1` | 2.06896 |
| `explicit.stat_1509134228@T1` | 2.02940 |
| `explicit.stat_1202301673@T1` | 1.56720 |
| `desecrated.stat_3131442032@T1` | -1.35231 |
| `desecrated.stat_1365232741@T1` | -1.35231 |
| `explicit.stat_691932474@T1` | -1.20320 |
| `explicit.stat_1263695895@T1` | 1.07600 |
| `crafted.stat_3035140377` | 1.03798 |

### weapon.sceptre — n=1364, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1798257884` | 0.00000 |
| `desecrated.stat_1050105434` | 0.00000 |
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

### weapon.warstaff — n=1286, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1037193709` | 0.00000 |
| `crafted.stat_1940865751` | 0.00000 |
| `crafted.stat_3035140377` | 0.00000 |
| `crafted.stat_3336890334` | 0.00000 |
| `crafted.stat_518292764` | 0.00000 |
| `desecrated.stat_1037193709` | 0.00000 |
| `desecrated.stat_1368271171` | 0.00000 |
| `desecrated.stat_1509134228` | 0.00000 |
| `desecrated.stat_1940865751` | 0.00000 |
| `desecrated.stat_210067635` | 0.00000 |
| `desecrated.stat_2694482655` | 0.00000 |
| `desecrated.stat_3261801346` | 0.00000 |

### weapon.spear — n=1232, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1940865751` | 0.00000 |
| `desecrated.stat_1509134228` | 0.00000 |
| `desecrated.stat_691932474` | 0.00000 |
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T1` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1202301673` | 0.00000 |
| `explicit.stat_1202301673@T1` | 0.00000 |
| `explicit.stat_1202301673@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1263695895@T2` | 0.00000 |

### weapon.staff — n=1218, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_124131830` | 0.00000 |
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_124131830` | 0.00000 |
| `explicit.stat_124131830@T1` | 0.00000 |
| `explicit.stat_124131830@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1263695895@T2` | 0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |

### flask.charm — n=1042, R²=-0.4845

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00002`  ·  corrupted: `0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2541588185@T2` | 0.12611 |
| `explicit.stat_1120862500@T2` | -0.00006 |
| `explicit.stat_1873752457` | 0.00006 |
| `explicit.stat_828533480@T1` | -0.00003 |
| `explicit.stat_1056492907` | 0.00002 |
| `explicit.stat_2566921799` | 0.00002 |
| `implicit.stat_4010341289` | -0.00002 |
| `explicit.stat_388617051@T2` | -0.00002 |
| `explicit.stat_828533480@T2` | -0.00002 |
| `explicit.stat_1873752457@T2` | -0.00002 |
| `implicit.stat_3676540188` | -0.00001 |
| `implicit.stat_1691862754` | -0.00001 |

### armour.focus — n=1010, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

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

### armour.quiver — n=959, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_1241625305` | 0.00000 |
| `desecrated.stat_3032590688` | 0.00000 |
| `desecrated.stat_3714003708` | 0.00000 |
| `explicit.stat_1202301673` | 0.00000 |
| `explicit.stat_1202301673@T1` | 0.00000 |
| `explicit.stat_1241625305` | 0.00000 |
| `explicit.stat_1241625305@T1` | 0.00000 |
| `explicit.stat_1241625305@T2` | 0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | -0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1573130764` | 0.00000 |

### armour.shield — n=882, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `-0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1568848828` | 0.00000 |
| `explicit.stat_1011760251` | 0.00000 |
| `explicit.stat_1011760251@T1` | -0.00000 |
| `explicit.stat_1011760251@T2` | 0.00000 |
| `explicit.stat_1062208444` | 0.00000 |
| `explicit.stat_1062208444@T1` | 0.00000 |
| `explicit.stat_1062208444@T2` | 0.00000 |
| `explicit.stat_1301765461` | 0.00000 |
| `explicit.stat_1301765461@T2` | 0.00000 |
| `explicit.stat_1671376347` | 0.00000 |
| `explicit.stat_1671376347@T1` | 0.00000 |
| `explicit.stat_1671376347@T2` | 0.00000 |

### weapon.twomace — n=685, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T1` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1509134228` | 0.00000 |
| `explicit.stat_1509134228@T2` | 0.00000 |
| `explicit.stat_1940865751` | 0.00000 |
| `explicit.stat_1940865751@T1` | 0.00000 |

## Coverage (listings per base)

- … **Emerald** — 4344 listings (4344 priced) [0.8–856.7 ex]
- … **Sapphire** — 4276 listings (4276 priced) [0.7–856.7 ex]
- … **Ruby** — 3491 listings (3491 priced) [0.3–856.7 ex]
- … **Utility Belt** — 2993 listings (2993 priced) [0.3–77723.4 ex]
- … **Stellar Amulet** — 2246 listings (2246 priced) [0.3–38371.8 ex]
- … **Dueling Wand** — 2037 listings (2037 priced) [1.0–856.7 ex]
- … **Solar Amulet** — 1867 listings (1867 priced) [1.0–856.7 ex]
- … **Gold Amulet** — 1854 listings (1854 priced) [0.6–856.7 ex]
- … **Prismatic Ring** — 1845 listings (1845 priced) [0.3–856.7 ex]
- … **Amethyst Ring** — 1744 listings (1744 priced) [0.8–856.7 ex]
- … **Gold Ring** — 1687 listings (1687 priced) [0.9–856.7 ex]
- … **Obliterator Bow** — 1549 listings (1549 priced) [1.0–856.7 ex]
- … **Plate Belt** — 1479 listings (1479 priced) [1.0–856.7 ex]
- … **Topaz Ring** — 1385 listings (1385 priced) [1.0–856.7 ex]
- … **Heavy Belt** — 1366 listings (1366 priced) [0.5–856.7 ex]
- … **Sapphire Ring** — 1366 listings (1366 priced) [0.9–856.7 ex]
- … **Ruby Ring** — 1344 listings (1344 priced) [1.0–856.7 ex]
- … **Ancestral Tiara** — 1307 listings (1307 priced) [1.0–856.7 ex]
- … **Lapis Amulet** — 1243 listings (1243 priced) [0.6–856.7 ex]
- … **Amber Amulet** — 1206 listings (1206 priced) [0.6–856.7 ex]
- … **Jade Amulet** — 1197 listings (1197 priced) [0.6–856.7 ex]
- … **Galvanic Wand** — 1169 listings (1169 priced) [0.8–856.7 ex]
- … **Siphoning Wand** — 1158 listings (1158 priced) [1.0–856.7 ex]
- … **Warmonger Bow** — 1102 listings (1102 priced) [1.0–856.7 ex]
- … **Attuned Wand** — 1086 listings (1086 priced) [0.3–856.7 ex]
