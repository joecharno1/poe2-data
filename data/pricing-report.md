# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-04T04:38:03+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **85917** (85917 priced in exalted)
- Distinct bases: 845 · distinct mods: 1934 · mod rows: 419278
- Sold signals: **15442** sold · 16130 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-04T04:33:02+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×7.72** (median |log error| 2.0436)
- Within ±30% of asking price: **33%**
- Skill vs constant-price guess: **+0.05** (> 0 = the mods carry signal)
- Calibration: 65% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.09** · typical error ×25.17 · ±30% 18% · n=12340
- Premium segment (60ex+): skill **+0.09** · typical error ×104.38 · ±30% 1% · n=7135
- Sold listings (clearing prices): skill **+0.04** · typical error ×14.18 · ±30% 27% · n=6189

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.belt | 1446 | ×9.21 | 27% | +0.03 | +0.04 |
| accessory.amulet | 1425 | ×15.54 | 6% | -0.07 | -0.10 |
| armour.helmet | 1385 | ×10.00 | 35% | -0.00 | -0.08 |
| accessory.ring | 1361 | ×6.86 | 5% | -0.03 | -0.01 |
| armour.chest | 1359 | ×10.00 | 37% | -0.01 | -0.06 |
| armour.gloves | 1263 | ×10.00 | 33% | -0.00 | -0.02 |
| armour.boots | 1204 | ×10.00 | 27% | -0.02 | -0.02 |
| other | 1159 | ×9.48 | 36% | +0.43 | +0.41 |
| weapon.wand | 1004 | ×8.73 | 39% | +0.04 | +0.06 |
| weapon.bow | 852 | ×7.74 | 36% | +0.06 | +0.09 |
| jewel | 829 | ×6.45 | 10% | +0.07 | +0.13 |
| weapon.crossbow | 765 | ×8.45 | 32% | +0.02 | +0.11 |
| weapon.sceptre | 219 | ×1.00 | 100% | +0.00 | +0.00 |
| weapon.spear | 188 | ×1.00 | 100% | n/a | - |
| armour.focus | 182 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.quiver | 156 | ×1.00 | 97% | +0.00 | +0.00 |
| weapon.warstaff | 151 | ×1.00 | 99% | +0.00 | +0.00 |
| weapon.staff | 143 | ×1.00 | 99% | +0.00 | +0.00 |
| armour.shield | 140 | ×1.00 | 99% | +0.00 | +0.00 |
| weapon.twomace | 94 | ×1.00 | 99% | +0.00 | +0.00 |
| flask.charm | 62 | ×1.00 | 95% | -0.24 | -0.41 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=10036, R²=-0.1678

intercept: `1.5168`  ·  log_price: True  ·  ilvl: `0.00588`  ·  n_mods: `0.03757`  ·  n_top_tier: `0.11706`  ·  corrupted: `0.37656`  ·  n_sockets: `-0.13852`  ·  quality: `-0.01600`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830` | -0.59935 |
| `implicit.stat_718638445` | 0.49072 |
| `implicit.stat_3182714256` | 0.48492 |
| `implicit.stat_1379411836` | -0.29140 |
| `explicit.stat_3917489142@T1` | 0.24345 |
| `implicit.stat_958696139` | -0.24092 |
| `explicit.stat_2974417149@T1` | 0.22644 |
| `explicit.stat_3299347043@T2` | -0.19866 |
| `explicit.stat_4052037485@T1` | -0.19181 |
| `implicit.stat_4041853756` | 0.18929 |
| `implicit.stat_3879011313` | 0.18871 |
| `explicit.stat_3299347043@T1` | -0.16281 |

### accessory.belt — n=6573, R²=-1.2705

intercept: `4.3744`  ·  log_price: True  ·  ilvl: `-0.05257`  ·  n_mods: `-0.02238`  ·  n_top_tier: `0.04663`  ·  corrupted: `0.07372`  ·  n_sockets: `-0.18750`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T2` | 1.21034 |
| `crafted.stat_3249412463` | 1.05787 |
| `explicit.stat_2923486259@T1` | 0.34830 |
| `explicit.stat_3299347043@T1` | -0.28945 |
| `explicit.stat_4220027924@T1` | 0.25841 |
| `implicit.stat_731781020` | -0.24741 |
| `explicit.stat_1836676211@T1` | 0.24407 |
| `explicit.stat_3299347043@T2` | -0.19225 |
| `explicit.stat_1389754388@T1` | -0.12876 |
| `explicit.stat_644456512@T2` | -0.09527 |
| `explicit.stat_2639966148` | 0.08717 |
| `explicit.stat_1389754388@T2` | -0.08689 |

### accessory.amulet — n=6456, R²=-2.3264

intercept: `5.7577`  ·  log_price: True  ·  ilvl: `-0.05864`  ·  n_mods: `-0.26005`  ·  n_top_tier: `0.15268`  ·  corrupted: `-0.20754`  ·  n_sockets: `-0.46959`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -3.90906 |
| `explicit.stat_1202301673@T2` | 2.83414 |
| `explicit.stat_983749596@T2` | -2.59780 |
| `explicit.stat_2923486259@T1` | -1.89110 |
| `explicit.stat_3299347043@T1` | -1.76972 |
| `explicit.stat_2923486259@T2` | -1.54111 |
| `explicit.stat_9187492@T2` | -1.51958 |
| `explicit.stat_9187492` | 1.33241 |
| `explicit.stat_1671376347@T1` | 1.30149 |
| `explicit.stat_2162097452` | 1.26888 |
| `explicit.stat_124131830` | 1.24544 |
| `explicit.stat_587431675@T2` | -1.20463 |

### accessory.ring — n=6340, R²=-2.0085

intercept: `4.9385`  ·  log_price: True  ·  ilvl: `-0.03902`  ·  n_mods: `-0.25088`  ·  n_top_tier: `0.78964`  ·  corrupted: `0.33493`  ·  n_sockets: `3.23323`  ·  quality: `0.02555`

| stat_id | coef |
|---|---|
| `explicit.stat_1263695895@T2` | -2.10853 |
| `explicit.stat_3299347043@T1` | -1.97198 |
| `explicit.stat_1573130764@T2` | -1.70006 |
| `explicit.stat_2231156303@T2` | -1.68271 |
| `explicit.stat_1368271171@T1` | -1.63227 |
| `explicit.stat_1263695895@T1` | -1.62626 |
| `explicit.stat_2923486259@T2` | -1.50794 |
| `explicit.stat_1050105434@T2` | -1.45967 |
| `explicit.stat_1050105434@T1` | -1.35916 |
| `explicit.stat_789117908@T1` | -1.30281 |
| `explicit.stat_2231156303@T1` | -1.22322 |
| `explicit.stat_1368271171@T2` | -1.20985 |

### armour.chest — n=6336, R²=-0.279

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00686`  ·  corrupted: `0.00007`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 0.50272 |
| `desecrated.stat_4220027924` | -0.03790 |
| `desecrated.stat_3372524247` | -0.03751 |
| `desecrated.stat_1671376347` | -0.03744 |
| `crafted.stat_1671376347` | -0.03741 |
| `implicit.stat_4220027924` | -0.03728 |
| `pseudo.total_ele_res` | 0.03728 |
| `explicit.stat_1671376347` | -0.03728 |
| `explicit.stat_3372524247` | -0.03728 |
| `explicit.stat_4220027924` | -0.03728 |
| `implicit.stat_3372524247` | -0.03728 |
| `rune.stat_1671376347` | -0.03727 |

### armour.helmet — n=6330, R²=-0.2146

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.50891`  ·  corrupted: `0.00373`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 1.33769 |
| `explicit.stat_2339757871@T1` | -0.50895 |
| `explicit.stat_803737631@T2` | -0.50894 |
| `explicit.stat_3321629045@T1` | -0.50894 |
| `explicit.stat_3362812763@T2` | -0.50894 |
| `explicit.stat_803737631@T1` | -0.50894 |
| `explicit.stat_1062208444@T2` | -0.50893 |
| `explicit.stat_328541901@T1` | -0.50893 |
| `explicit.stat_3362812763@T1` | -0.50893 |
| `explicit.stat_3261801346@T2` | -0.50893 |
| `explicit.stat_328541901@T2` | -0.50892 |
| `explicit.stat_2451402625@T1` | -0.50892 |

### armour.gloves — n=5743, R²=-0.2487

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00015`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.18777 |
| `explicit.stat_2923486259` | -0.05513 |
| `pseudo.total_chaos_res` | 0.05513 |
| `desecrated.stat_3299347043` | 0.00816 |
| `explicit.stat_4067062424@T1` | 0.00526 |
| `explicit.stat_2339757871@T1` | -0.00095 |
| `rune.stat_3299347043` | -0.00063 |
| `explicit.stat_3299347043` | -0.00063 |
| `pseudo.total_life` | 0.00063 |
| `explicit.stat_3372524247@T1` | 0.00025 |
| `explicit.stat_4052037485@T1` | -0.00021 |
| `explicit.stat_2451402625@T2` | -0.00019 |

### armour.boots — n=5743, R²=-0.1928

intercept: `2.3028`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.21761`  ·  corrupted: `-0.00002`  ·  n_sockets: `-0.00001`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_4080418644@T1` | -1.92135 |
| `explicit.stat_1062208444@T2` | -0.34190 |
| `explicit.stat_2339757871@T1` | -0.21788 |
| `explicit.stat_3362812763@T2` | -0.21771 |
| `explicit.stat_3362812763@T1` | -0.21769 |
| `explicit.stat_3261801346@T2` | -0.21769 |
| `explicit.stat_3639275092@T1` | -0.21769 |
| `explicit.stat_3484657501@T2` | -0.21767 |
| `explicit.stat_1062208444@T1` | -0.21767 |
| `explicit.stat_3321629045@T2` | -0.21766 |
| `explicit.stat_3484657501@T1` | -0.21765 |
| `explicit.stat_3033371881@T2` | -0.21764 |

### weapon.wand — n=4644, R²=-1.5823

intercept: `3.3439`  ·  log_price: True  ·  ilvl: `-0.04178`  ·  n_mods: `-0.01100`  ·  n_top_tier: `0.04981`  ·  corrupted: `0.02084`  ·  n_sockets: `0.00199`  ·  quality: `0.03233`

| stat_id | coef |
|---|---|
| `explicit.stat_591105508@T1` | 2.32358 |
| `explicit.stat_1545858329@T1` | 2.27906 |
| `explicit.stat_124131830@T1` | 2.24324 |
| `explicit.stat_1600707273@T1` | 2.22480 |
| `explicit.stat_736967255@T2` | 2.17866 |
| `explicit.stat_1600707273@T2` | 1.68941 |
| `crafted.stat_124131830` | 1.25442 |
| `explicit.stat_4226189338@T1` | 0.70806 |
| `explicit.stat_2254480358@T1` | 0.31623 |
| `explicit.stat_2974417149@T1` | 0.30279 |
| `rune.stat_3990135792` | -0.17352 |
| `rune.stat_3278136794` | 0.15878 |

### jewel — n=4075, R²=-0.9749

intercept: `-1.4194`  ·  log_price: True  ·  ilvl: `0.03500`  ·  n_mods: `0.22174`  ·  n_top_tier: `-0.51089`  ·  corrupted: `0.44353`

| stat_id | coef |
|---|---|
| `explicit.stat_274716455@T1` | -5.43525 |
| `explicit.stat_2011656677@T1` | 5.33201 |
| `explicit.stat_3851254963@T1` | 5.20614 |
| `explicit.stat_1569101201@T1` | 4.88748 |
| `explicit.stat_2301718443@T1` | -4.74576 |
| `explicit.stat_429143663@T1` | 4.12010 |
| `explicit.stat_2456523742@T1` | 4.04285 |
| `explicit.stat_1459321413@T1` | 3.76975 |
| `explicit.stat_1714971114@T1` | 3.63898 |
| `explicit.stat_1697447343@T1` | -3.61683 |
| `explicit.stat_3174700878@T1` | 3.49547 |
| `explicit.stat_2527686725@T1` | 3.45160 |

### weapon.bow — n=4015, R²=-1.4667

intercept: `3.2982`  ·  log_price: True  ·  ilvl: `-0.04080`  ·  n_mods: `-0.02370`  ·  n_top_tier: `0.45004`  ·  corrupted: `0.07253`  ·  n_sockets: `0.01214`  ·  quality: `-0.00510`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -6.64953 |
| `explicit.stat_2463230181@T1` | 1.81035 |
| `explicit.stat_1509134228@T1` | 1.80487 |
| `explicit.stat_1202301673@T1` | 1.18308 |
| `explicit.stat_518292764@T1` | 0.91245 |
| `desecrated.stat_210067635@T1` | -0.82362 |
| `explicit.stat_821021828@T1` | -0.73921 |
| `crafted.stat_3035140377` | 0.73396 |
| `explicit.stat_821021828@T2` | -0.68170 |
| `rune.stat_3885405204` | -0.59644 |
| `explicit.stat_1263695895@T1` | -0.53490 |
| `explicit.stat_1940865751@T1` | -0.52824 |

### weapon.crossbow — n=3781, R²=-1.4361

intercept: `3.3845`  ·  log_price: True  ·  ilvl: `-0.04280`  ·  n_mods: `0.00981`  ·  n_top_tier: `0.46182`  ·  corrupted: `0.03300`  ·  n_sockets: `0.02221`  ·  quality: `-0.01240`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709@T1` | 1.86518 |
| `explicit.stat_3336890334@T1` | 1.86160 |
| `explicit.stat_709508406@T1` | 1.80354 |
| `explicit.stat_691932474@T1` | -1.48461 |
| `explicit.stat_1967051901@T1` | 1.29155 |
| `crafted.stat_3035140377` | 0.81909 |
| `explicit.stat_1509134228@T1` | 0.63424 |
| `explicit.stat_1263695895@T1` | 0.62001 |
| `explicit.stat_1263695895@T2` | -0.55718 |
| `explicit.stat_1202301673@T2` | -0.52130 |
| `explicit.stat_3261801346@T1` | -0.51931 |
| `explicit.stat_2694482655@T1` | -0.50400 |

### weapon.sceptre — n=1108, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1798257884` | 0.00000 |
| `desecrated.stat_1050105434` | 0.00000 |
| `desecrated.stat_1250712710` | 0.00000 |
| `desecrated.stat_1798257884` | 0.00000 |
| `desecrated.stat_3984865854` | 0.00000 |
| `explicit.stat_101878827` | 0.00000 |
| `explicit.stat_101878827@T1` | 0.00000 |
| `explicit.stat_101878827@T2` | 0.00000 |
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_1250712710` | 0.00000 |

### weapon.spear — n=999, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_1940865751` | 0.00000 |
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

### armour.focus — n=881, R²=0.0

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

### weapon.warstaff — n=853, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 0.00000 |
| `crafted.stat_3336890334` | 0.00000 |
| `crafted.stat_518292764` | 0.00000 |
| `desecrated.stat_1509134228` | 0.00000 |
| `desecrated.stat_3336890334` | 0.00000 |
| `desecrated.stat_691932474` | 0.00000 |
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1037193709@T1` | 0.00000 |
| `explicit.stat_1037193709@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1263695895@T2` | 0.00000 |

### weapon.staff — n=826, R²=0.0

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

### armour.shield — n=752, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

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

### armour.quiver — n=720, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673` | 0.00000 |
| `explicit.stat_1202301673@T1` | 0.00000 |
| `explicit.stat_1241625305` | 0.00000 |
| `explicit.stat_1241625305@T1` | 0.00000 |
| `explicit.stat_1241625305@T2` | 0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | -0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1573130764` | 0.00000 |
| `explicit.stat_1573130764@T1` | 0.00000 |
| `explicit.stat_1573130764@T2` | 0.00000 |
| `explicit.stat_1754445556` | 0.00000 |

### flask.charm — n=621, R²=-0.5275

intercept: `0.0001`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.18039`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1873752457@T1` | -0.19211 |
| `explicit.stat_1873752457` | 0.00023 |
| `explicit.stat_1120862500@T2` | -0.00012 |
| `explicit.stat_2541588185@T2` | -0.00012 |
| `explicit.stat_3196823591@T2` | -0.00010 |
| `explicit.stat_828533480@T2` | -0.00006 |
| `explicit.stat_1873752457@T2` | -0.00005 |
| `explicit.stat_828533480@T1` | -0.00004 |
| `explicit.stat_388617051@T2` | -0.00003 |
| `explicit.stat_3849649145` | -0.00003 |
| `implicit.stat_3699444296` | -0.00003 |
| `implicit.stat_4010341289` | -0.00002 |

### weapon.twomace — n=515, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

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

- … **Emerald** — 2273 listings (2273 priced) [0.5–802.8 ex]
- … **Sapphire** — 2191 listings (2191 priced) [0.5–802.8 ex]
- … **Utility Belt** — 2064 listings (2064 priced) [0.3–11927.4 ex]
- … **Ruby** — 1794 listings (1794 priced) [0.3–802.8 ex]
- … **Stellar Amulet** — 1548 listings (1548 priced) [0.3–37188.0 ex]
- … **Dueling Wand** — 1454 listings (1454 priced) [0.8–802.8 ex]
- … **Solar Amulet** — 1206 listings (1206 priced) [1.0–802.8 ex]
- … **Gold Amulet** — 1189 listings (1189 priced) [0.3–802.8 ex]
- … **Obliterator Bow** — 1156 listings (1156 priced) [0.4–802.8 ex]
- … **Prismatic Ring** — 1119 listings (1119 priced) [0.3–802.8 ex]
- … **Amethyst Ring** — 1100 listings (1100 priced) [0.8–802.8 ex]
- … **Gold Ring** — 1032 listings (1032 priced) [0.7–802.8 ex]
- … **Plate Belt** — 1005 listings (1005 priced) [1.0–802.8 ex]
- … **Heavy Belt** — 928 listings (928 priced) [0.5–802.8 ex]
- … **Ancestral Tiara** — 924 listings (924 priced) [1.0–802.8 ex]
- … **Sapphire Ring** — 887 listings (887 priced) [0.5–802.8 ex]
- … **Topaz Ring** — 887 listings (887 priced) [1.0–802.8 ex]
- … **Galvanic Wand** — 858 listings (858 priced) [1.0–802.8 ex]
- … **Ruby Ring** — 849 listings (849 priced) [0.4–802.8 ex]
- … **Warmonger Bow** — 831 listings (831 priced) [0.9–802.8 ex]
- … **Lapis Amulet** — 812 listings (812 priced) [0.6–802.8 ex]
- … **Siphoning Wand** — 809 listings (809 priced) [1.0–802.8 ex]
- … **Jade Amulet** — 790 listings (790 priced) [0.3–802.8 ex]
- … **Amber Amulet** — 788 listings (788 priced) [0.3–802.8 ex]
- … **Attuned Wand** — 779 listings (779 priced) [0.3–802.8 ex]
