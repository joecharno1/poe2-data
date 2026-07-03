# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-03T03:25:26+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **32250** (32250 priced in exalted)
- Distinct bases: 688 · distinct mods: 1197 · mod rows: 168377
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-03T03:06:00+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×56.74** (median |log error| 4.0385)
- Within ±30% of asking price: **26%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 74% of actuals above prediction (target ≈ 75%)

| group | n_test | ×err | ±30% | skill |
|---|---|---|---|---|
| accessory.belt | 540 | ×55.45 | 28% | +0.12 |
| armour.gloves | 534 | ×299.98 | 23% | -0.01 |
| armour.chest | 527 | ×79.26 | 11% | +0.10 |
| armour.boots | 526 | ×93.45 | 23% | +0.09 |
| armour.helmet | 513 | ×359.32 | 24% | +0.08 |
| accessory.amulet | 452 | ×47.46 | 3% | +0.20 |
| weapon.wand | 436 | ×339.51 | 20% | +0.14 |
| accessory.ring | 425 | ×13.46 | 4% | -1.17 |
| weapon.crossbow | 367 | ×188.48 | 17% | +0.11 |
| weapon.bow | 355 | ×50.58 | 24% | +0.05 |
| other | 293 | ×4.20 | 25% | +0.43 |
| weapon.spear | 143 | ×1.00 | 100% | n/a |
| armour.focus | 141 | ×1.00 | 100% | n/a |
| weapon.sceptre | 123 | ×1.00 | 99% | +0.00 |
| armour.shield | 110 | ×1.00 | 100% | n/a |
| jewel | 96 | ×245.35 | 2% | +0.11 |
| flask.charm | 10 | ×1.08 | 90% | -0.44 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### accessory.belt — n=2610, R²=-0.8535

intercept: `1.4562`  ·  log_price: True  ·  ilvl: `-0.01770`  ·  n_mods: `-0.00986`  ·  n_top_tier: `0.03319`  ·  corrupted: `0.02546`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 0.59275 |
| `pseudo.total_ele_res>=80` | 0.26317 |
| `explicit.stat_2639966148` | 0.19470 |
| `implicit.stat_731781020` | 0.15474 |
| `explicit.stat_174664100` | 0.13588 |
| `explicit.stat_1014398896` | 0.12098 |
| `explicit.stat_3299347043@T1` | 0.09972 |
| `explicit.stat_3811191316` | 0.09961 |
| `explicit.stat_2923486259@T2` | -0.07221 |
| `explicit.stat_770672621` | 0.06313 |
| `explicit.stat_3299347043@T2` | 0.05848 |
| `explicit.stat_3742865955` | 0.05661 |

### armour.boots — n=2544, R²=-0.7244

intercept: `7.5430`  ·  log_price: True  ·  ilvl: `-0.09331`  ·  n_mods: `-0.04870`  ·  n_top_tier: `0.49156`  ·  corrupted: `0.24870`  ·  n_sockets: `0.05081`  ·  quality: `0.01353`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 5.59901 |
| `explicit.stat_3261801346@T2` | -0.78924 |
| `explicit.stat_124859000@T2` | -0.67875 |
| `explicit.stat_3321629045@T1` | -0.64287 |
| `explicit.stat_3484657501@T2` | -0.62229 |
| `explicit.stat_1062208444@T1` | -0.59171 |
| `explicit.stat_3321629045@T2` | -0.57169 |
| `explicit.stat_124859000@T1` | -0.56802 |
| `explicit.stat_3261801346@T1` | -0.56558 |
| `explicit.stat_2451402625@T1` | -0.56079 |
| `explicit.stat_2923486259@T2` | -0.56074 |
| `explicit.stat_3917489142@T2` | -0.55844 |

### other — n=2543, R²=0.3098

intercept: `1.4609`  ·  log_price: True  ·  ilvl: `0.00408`  ·  n_mods: `-0.02885`  ·  n_top_tier: `0.27178`  ·  corrupted: `0.32750`  ·  n_sockets: `-0.05929`  ·  quality: `-0.00246`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 2.58412 |
| `explicit.stat_4080418644@T1` | -0.72863 |
| `explicit.stat_124131830` | -0.61658 |
| `crafted.stat_124131830` | -0.60235 |
| `explicit.stat_3484657501@T1` | -0.57914 |
| `explicit.stat_691932474@T2` | -0.49361 |
| `explicit.stat_2901986750@T2` | -0.46504 |
| `explicit.stat_328541901@T2` | -0.46463 |
| `explicit.stat_4052037485@T2` | -0.44123 |
| `explicit.stat_3484657501@T2` | -0.42422 |
| `explicit.stat_915769802@T1` | -0.42393 |
| `explicit.stat_3372524247@T1` | -0.38380 |

### armour.chest — n=2501, R²=-0.8424

intercept: `8.0435`  ·  log_price: True  ·  ilvl: `-0.10276`  ·  n_mods: `-0.00236`  ·  n_top_tier: `0.58323`  ·  corrupted: `-1.23104`  ·  n_sockets: `0.05775`  ·  quality: `0.05027`

| stat_id | coef |
|---|---|
| `rune.stat_836936635` | 7.48856 |
| `explicit.stat_1671376347@T1` | 3.98939 |
| `explicit.stat_3981240776@T1` | 3.62775 |
| `explicit.stat_2339757871@T1` | -2.33769 |
| `explicit.stat_2339757871@T2` | -2.04439 |
| `explicit.stat_3372524247@T1` | 1.45449 |
| `explicit.stat_4220027924@T1` | 1.03087 |
| `explicit.stat_3261801346@T1` | -0.96398 |
| `explicit.stat_4052037485@T1` | -0.85953 |
| `explicit.stat_3301100256@T2` | -0.80252 |
| `explicit.stat_1062208444@T1` | -0.80159 |
| `explicit.stat_4015621042@T2` | -0.76506 |

### armour.helmet — n=2500, R²=-0.9289

intercept: `7.5949`  ·  log_price: True  ·  ilvl: `-0.09668`  ·  n_mods: `-0.02180`  ·  n_top_tier: `0.66431`  ·  corrupted: `1.50514`  ·  n_sockets: `0.06875`  ·  quality: `0.00817`

| stat_id | coef |
|---|---|
| `desecrated.stat_4015621042@T1` | -4.20442 |
| `explicit.stat_4220027924@T1` | 2.31161 |
| `crafted.stat_3917489142@T1` | 2.18724 |
| `desecrated.stat_3299347043@T2` | 1.08495 |
| `explicit.stat_2923486259@T2` | -0.94853 |
| `explicit.stat_3261801346@T2` | -0.90807 |
| `explicit.stat_2923486259@T1` | -0.89591 |
| `explicit.stat_3917489142@T2` | -0.82675 |
| `explicit.stat_3484657501@T1` | -0.78296 |
| `explicit.stat_3321629045@T2` | -0.74082 |
| `explicit.stat_587431675@T2` | -0.72531 |
| `explicit.stat_1999113824@T1` | -0.72293 |

### armour.gloves — n=2432, R²=-0.882

intercept: `7.4973`  ·  log_price: True  ·  ilvl: `-0.09665`  ·  n_mods: `0.05518`  ·  n_top_tier: `0.21400`  ·  corrupted: `2.09418`  ·  n_sockets: `0.02232`  ·  quality: `-0.03744`

| stat_id | coef |
|---|---|
| `explicit.stat_4067062424@T2` | 3.88997 |
| `explicit.stat_3372524247@T1` | 3.33110 |
| `explicit.stat_1671376347@T1` | 2.26197 |
| `rune.stat_201332984` | 1.27223 |
| `explicit.stat_4015621042@T2` | 1.10602 |
| `explicit.stat_9187492@T1` | 1.03977 |
| `explicit.stat_9187492@T2` | -0.75349 |
| `explicit.stat_3362812763@T2` | 0.58342 |
| `explicit.stat_2451402625@T2` | -0.54576 |
| `explicit.stat_9187492` | 0.44308 |
| `explicit.stat_3484657501@T2` | -0.39772 |
| `explicit.stat_3556824919@T1` | 0.38809 |

### accessory.amulet — n=2214, R²=-0.4959

intercept: `10.4723`  ·  log_price: True  ·  ilvl: `-0.09979`  ·  n_mods: `-0.72855`  ·  n_top_tier: `1.65462`  ·  corrupted: `-1.73527`  ·  n_sockets: `-1.58157`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -6.16153 |
| `explicit.stat_2923486259@T2` | -5.63862 |
| `explicit.stat_2748665614@T2` | -5.14661 |
| `explicit.stat_983749596@T1` | -4.77702 |
| `explicit.stat_2482852589@T1` | -4.73384 |
| `explicit.stat_4220027924@T2` | -4.71579 |
| `explicit.stat_328541901@T1` | -4.21467 |
| `explicit.stat_2482852589@T2` | -4.16017 |
| `explicit.stat_1050105434@T1` | -3.73258 |
| `explicit.stat_1671376347@T2` | -3.56082 |
| `explicit.stat_2748665614@T1` | -3.52196 |
| `explicit.stat_4080418644@T1` | -3.52077 |

### weapon.wand — n=2088, R²=-0.9863

intercept: `7.6125`  ·  log_price: True  ·  ilvl: `-0.09404`  ·  n_mods: `-0.04773`  ·  n_top_tier: `0.23342`  ·  corrupted: `0.08252`  ·  n_sockets: `0.00305`  ·  quality: `0.02724`

| stat_id | coef |
|---|---|
| `explicit.stat_1600707273@T1` | 6.24686 |
| `explicit.stat_591105508@T1` | 6.10604 |
| `explicit.stat_1545858329@T1` | 6.06601 |
| `explicit.stat_2254480358@T1` | 5.89489 |
| `explicit.stat_4226189338@T1` | 5.48989 |
| `explicit.stat_124131830@T1` | 4.87826 |
| `explicit.stat_2974417149@T1` | 1.60131 |
| `crafted.stat_124131830` | 1.59439 |
| `explicit.stat_2254480358@T2` | 0.86951 |
| `explicit.stat_124131830@T2` | -0.83949 |
| `explicit.stat_274716455@T2` | 0.62285 |
| `rune.stat_3278136794` | 0.55355 |

### accessory.ring — n=2027, R²=-0.2349

intercept: `6.6733`  ·  log_price: True  ·  ilvl: `-0.00391`  ·  n_mods: `-0.03373`  ·  n_top_tier: `0.03795`  ·  corrupted: `0.16200`  ·  n_sockets: `0.76185`  ·  quality: `0.00636`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T2` | -5.80670 |
| `explicit.stat_803737631@T2` | -4.65109 |
| `explicit.stat_3325883026@T2` | -3.57764 |
| `explicit.stat_1050105434@T1` | -2.74497 |
| `explicit.stat_3325883026@T1` | 2.61570 |
| `explicit.stat_2923486259@T2` | -1.35318 |
| `explicit.stat_707457662@T2` | 1.01039 |
| `explicit.stat_707457662@T1` | 0.93620 |
| `explicit.stat_3299347043@T1` | -0.47175 |
| `explicit.stat_2557965901@T1` | -0.37748 |
| `explicit.stat_2557965901@T2` | -0.34821 |
| `explicit.stat_1368271171@T1` | 0.31745 |

### weapon.bow — n=1752, R²=-0.7988

intercept: `8.0089`  ·  log_price: True  ·  ilvl: `-0.09927`  ·  n_mods: `-0.05836`  ·  n_top_tier: `0.08129`  ·  corrupted: `1.63914`  ·  n_sockets: `0.04687`  ·  quality: `-0.15424`

| stat_id | coef |
|---|---|
| `desecrated.stat_1200678966@T1` | -8.40421 |
| `explicit.stat_1202301673@T1` | 4.55344 |
| `explicit.stat_2463230181@T1` | 4.43573 |
| `explicit.stat_518292764@T1` | 4.21524 |
| `explicit.stat_1037193709@T1` | 4.14148 |
| `rune.stat_3885405204` | -3.11313 |
| `desecrated.stat_210067635@T1` | 2.09949 |
| `explicit.stat_1509134228@T1` | 1.86501 |
| `explicit.stat_210067635@T2` | 1.06039 |
| `explicit.stat_1263695895@T1` | 1.03912 |
| `crafted.stat_3035140377` | 0.83559 |
| `explicit.stat_1263695895@T2` | 0.81706 |

### weapon.crossbow — n=1680, R²=-0.8464

intercept: `8.3089`  ·  log_price: True  ·  ilvl: `-0.10384`  ·  n_mods: `-0.02400`  ·  n_top_tier: `0.59493`  ·  corrupted: `0.28739`  ·  n_sockets: `-0.00485`  ·  quality: `-0.04686`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709@T1` | 5.71315 |
| `explicit.stat_3336890334@T1` | 5.60264 |
| `explicit.stat_709508406@T1` | 5.32590 |
| `explicit.stat_1037193709@T2` | 2.27873 |
| `explicit.stat_1980802737` | 1.62479 |
| `explicit.stat_1980802737@T2` | 1.62479 |
| `desecrated.stat_3131442032@T1` | 1.61097 |
| `desecrated.stat_1365232741@T1` | 1.61097 |
| `explicit.stat_1263695895@T2` | -0.99196 |
| `crafted.stat_3035140377` | 0.90568 |
| `explicit.stat_691932474@T1` | -0.88269 |
| `explicit.stat_1940865751@T1` | -0.82861 |

### weapon.sceptre — n=764, R²=0.0

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

### weapon.spear — n=673, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

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

### armour.focus — n=662, R²=0.0

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

### armour.shield — n=541, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  n_sockets: `0.00000`

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

### jewel — n=460, R²=0.1286

intercept: `-1.7279`  ·  log_price: True  ·  ilvl: `0.02854`  ·  n_mods: `1.49027`  ·  n_top_tier: `-0.17415`  ·  corrupted: `0.81547`

| stat_id | coef |
|---|---|
| `explicit.stat_293638271@T1` | 9.75708 |
| `explicit.stat_1782086450@T1` | -9.41951 |
| `explicit.stat_2011656677@T1` | 9.24935 |
| `explicit.stat_473429811@T1` | -8.03674 |
| `explicit.stat_1310194496@T1` | 7.70615 |
| `explicit.stat_1181419800@T1` | -7.55143 |
| `explicit.stat_680068163@T1` | 7.43843 |
| `explicit.stat_1459321413@T1` | 6.55040 |
| `explicit.stat_3596695232@T1` | -6.13310 |
| `explicit.stat_818778753@T1` | -6.03106 |
| `explicit.stat_3417711605@T1` | -5.88824 |
| `explicit.stat_3291658075@T1` | -5.65762 |

### armour.quiver — n=253, R²=0.0

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

### weapon.staff — n=226, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434` | 0.00000 |
| `explicit.stat_1050105434@T1` | 0.00000 |
| `explicit.stat_1050105434@T2` | 0.00000 |
| `explicit.stat_124131830` | 0.00000 |
| `explicit.stat_124131830@T2` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | 0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1545858329` | 0.00000 |
| `explicit.stat_1545858329@T1` | 0.00000 |

### weapon.warstaff — n=221, R²=-0.0315

intercept: `0.0001`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_821021828@T1` | -0.00004 |
| `explicit.stat_2694482655@T1` | 0.00003 |
| `explicit.stat_3261801346@T2` | -0.00002 |
| `explicit.stat_387439868@T2` | 0.00002 |
| `explicit.stat_791928121@T1` | -0.00002 |
| `explicit.stat_3639275092@T2` | -0.00002 |
| `explicit.stat_1368271171@T1` | 0.00002 |
| `explicit.stat_328541901@T2` | -0.00002 |
| `explicit.stat_210067635@T2` | -0.00001 |
| `explicit.stat_1509134228@T2` | -0.00001 |
| `explicit.stat_3336890334@T2` | 0.00001 |
| `explicit.stat_1368271171@T2` | 0.00001 |

### weapon.twomace — n=184, R²=0.0

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00000`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1037193709` | 0.00000 |
| `explicit.stat_1263695895` | 0.00000 |
| `explicit.stat_1263695895@T1` | -0.00000 |
| `explicit.stat_1368271171` | 0.00000 |
| `explicit.stat_1368271171@T1` | 0.00000 |
| `explicit.stat_1368271171@T2` | 0.00000 |
| `explicit.stat_1509134228` | 0.00000 |
| `explicit.stat_1509134228@T2` | 0.00000 |
| `explicit.stat_1940865751` | 0.00000 |
| `explicit.stat_1940865751@T2` | 0.00000 |
| `explicit.stat_210067635` | 0.00000 |
| `explicit.stat_210067635@T2` | 0.00000 |

### flask.charm — n=167, R²=-0.227

intercept: `0.2728`  ·  log_price: True  ·  ilvl: `0.00091`  ·  n_mods: `-0.01654`  ·  n_top_tier: `-0.04342`  ·  quality: `-0.02330`

| stat_id | coef |
|---|---|
| `implicit.stat_3676540188` | -1.31938 |
| `implicit.stat_3854901951` | 0.06291 |
| `implicit.stat_3699444296` | -0.05460 |
| `explicit.stat_1873752457` | -0.04753 |
| `explicit.stat_2566921799` | 0.03150 |
| `implicit.stat_2778646494` | 0.02716 |
| `implicit.stat_1412682799` | -0.02326 |
| `implicit.stat_2994271459` | 0.00808 |
| `implicit.stat_2016937536` | 0.00552 |
| `explicit.stat_388617051` | -0.00194 |
| `explicit.stat_828533480` | 0.00189 |
| `explicit.stat_2541588185` | 0.00189 |

## Coverage (listings per base)

- … **Utility Belt** — 706 listings (706 priced) [1.0–737.3 ex]
- … **Dueling Wand** — 672 listings (672 priced) [1.0–726.1 ex]
- … **Obliterator Bow** — 513 listings (513 priced) [0.5–726.1 ex]
- … **Stellar Amulet** — 453 listings (453 priced) [0.3–737.3 ex]
- … **Solar Amulet** — 390 listings (390 priced) [1.0–737.3 ex]
- … **Siphoning Wand** — 384 listings (384 priced) [1.0–726.1 ex]
- … **Warmonger Bow** — 383 listings (383 priced) [1.0–726.1 ex]
- … **Gold Amulet** — 374 listings (374 priced) [0.3–737.3 ex]
- … **Plate Belt** — 367 listings (367 priced) [1.0–737.3 ex]
- … **Galvanic Wand** — 364 listings (364 priced) [1.0–726.1 ex]
- … **Ancestral Tiara** — 354 listings (354 priced) [1.0–737.3 ex]
- … **Attuned Wand** — 348 listings (348 priced) [0.3–726.1 ex]
- … **Heavy Belt** — 327 listings (327 priced) [0.5–737.3 ex]
- … **Withered Wand** — 326 listings (326 priced) [1.0–726.1 ex]
- … **Trarthan Cannon** — 313 listings (313 priced) [0.7–726.1 ex]
- … **Amethyst Ring** — 311 listings (311 priced) [1.0–737.3 ex]
- … **Long Belt** — 307 listings (307 priced) [1.0–737.3 ex]
- … **Prismatic Ring** — 302 listings (302 priced) [0.4–737.3 ex]
- … **Amber Amulet** — 292 listings (292 priced) [0.3–737.3 ex]
- … **Rawhide Belt** — 290 listings (290 priced) [1.0–737.3 ex]
- … **Emerald** — 288 listings (288 priced) [1.0–726.1 ex]
- … **Lapis Amulet** — 282 listings (282 priced) [0.6–737.3 ex]
- … **Desolate Crossbow** — 280 listings (280 priced) [1.0–726.1 ex]
- … **Gold Ring** — 280 listings (280 priced) [0.7–737.3 ex]
- … **Sapphire Ring** — 272 listings (272 priced) [0.5–737.3 ex]
