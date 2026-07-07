# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-07T02:34:39+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **255255** (255010 priced in exalted)
- Distinct bases: 938 · distinct mods: 2676 · mod rows: 1212712
- Sold signals: **33560** sold · 133274 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-07T02:27:09+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×15.63** (median |log error| 2.7492)
- Within ±30% of asking price: **20%**
- Skill vs constant-price guess: **+0.03** (> 0 = the mods carry signal)
- Calibration: 76% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.08** · typical error ×32.12 · ±30% 13% · n=36579
- Premium segment (60ex+): skill **+0.08** · typical error ×185.19 · ±30% 0% · n=22229

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 4771 | ×14.06 | 4% | +0.04 | +0.06 |
| accessory.amulet | 4548 | ×56.02 | 21% | +0.02 | +0.02 |
| jewel | 4053 | ×8.95 | 7% | +0.04 | +0.07 |
| accessory.belt | 3811 | ×20.29 | 20% | +0.05 | +0.07 |
| armour.chest | 3681 | ×10.00 | 27% | +0.01 | +0.00 |
| armour.helmet | 3622 | ×10.00 | 24% | +0.00 | +0.01 |
| armour.boots | 3455 | ×10.00 | 25% | +0.00 | +0.02 |
| armour.gloves | 3403 | ×10.00 | 22% | -0.00 | +0.01 |
| other | 3152 | ×9.99 | 37% | +0.05 | +0.18 |
| weapon.wand | 2343 | ×19.67 | 23% | +0.06 | +0.05 |
| weapon.bow | 1957 | ×14.73 | 19% | +0.09 | +0.10 |
| weapon.crossbow | 1844 | ×14.41 | 20% | +0.08 | +0.10 |
| weapon.sceptre | 700 | ×56.00 | 19% | +0.01 | +0.01 |
| weapon.warstaff | 699 | ×40.00 | 27% | +0.01 | +0.01 |
| weapon.staff | 638 | ×50.00 | 24% | +0.03 | +0.00 |
| weapon.spear | 630 | ×50.00 | 21% | +0.01 | +0.00 |
| armour.quiver | 484 | ×62.00 | 16% | +0.00 | +0.03 |
| armour.focus | 482 | ×50.00 | 16% | +0.01 | +0.01 |
| armour.shield | 411 | ×15.00 | 20% | +0.01 | +0.02 |
| weapon.twomace | 358 | ×20.00 | 22% | +0.06 | +0.01 |
| flask.charm | 325 | ×1.00 | 63% | -0.00 | -0.00 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=27588, R²=-0.4918

intercept: `1.6064`  ·  log_price: True  ·  ilvl: `0.00004`  ·  n_mods: `0.03523`  ·  n_top_tier: `0.46325`  ·  corrupted: `2.13611`  ·  n_sockets: `-0.00011`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_2106365538@T1` | 3.99837 |
| `explicit.stat_3291658075@T1` | 3.24495 |
| `explicit.stat_101878827@T1` | 2.63182 |
| `explicit.stat_1589917703@T1` | 2.00308 |
| `explicit.stat_2891184298@T1` | 1.36571 |
| `explicit.stat_2974417149@T1` | 0.90902 |
| `explicit.stat_3917489142@T1` | 0.87705 |
| `explicit.stat_1050105434@T1` | -0.86077 |
| `explicit.stat_3141070085@T1` | -0.76175 |
| `explicit.stat_789117908@T1` | -0.35779 |
| `implicit.stat_1379411836` | -0.27404 |
| `implicit.stat_4041853756` | 0.22672 |

### accessory.ring — n=21794, R²=-1.259

intercept: `4.6492`  ·  log_price: True  ·  ilvl: `-0.04108`  ·  n_mods: `-0.16131`  ·  n_top_tier: `-0.13005`  ·  corrupted: `0.65936`  ·  n_sockets: `0.59282`  ·  quality: `0.05367`

| stat_id | coef |
|---|---|
| `explicit.stat_707457662@T1` | 5.62964 |
| `explicit.stat_707457662@T2` | 4.26869 |
| `explicit.stat_1379411836@T1` | -2.17715 |
| `explicit.stat_1379411836@T2` | -1.76323 |
| `explicit.stat_2923486259@T2` | 1.11470 |
| `explicit.stat_736967255@T1` | 0.89925 |
| `explicit.stat_707457662` | -0.78398 |
| `explicit.stat_328541901@T1` | 0.76575 |
| `explicit.stat_1368271171@T2` | -0.74210 |
| `explicit.stat_1754445556@T1` | 0.71724 |
| `explicit.stat_4080418644@T2` | 0.63656 |
| `explicit.stat_1573130764@T1` | -0.58997 |

### jewel — n=21629, R²=-0.6069

intercept: `-1.0933`  ·  log_price: True  ·  ilvl: `0.03876`  ·  n_mods: `0.08772`  ·  n_top_tier: `-0.01865`  ·  corrupted: `0.30206`  ·  quality: `0.20968`

| stat_id | coef |
|---|---|
| `explicit.stat_3714003708@T1` | -3.50925 |
| `explicit.stat_1569101201@T1` | 3.48992 |
| `explicit.stat_1316278494@T1` | -3.46294 |
| `explicit.stat_1697951953@T1` | -3.42364 |
| `explicit.stat_1869147066@T1` | 3.12135 |
| `explicit.stat_153777645@T1` | 2.83200 |
| `explicit.stat_21071013@T1` | -2.64871 |
| `explicit.stat_3192728503@T1` | -1.97514 |
| `explicit.stat_3473929743@T1` | 1.90838 |
| `explicit.stat_293638271@T1` | 1.89818 |
| `explicit.stat_3544800472@T1` | -1.72986 |
| `explicit.stat_3174700878@T1` | 1.71495 |

### accessory.amulet — n=20827, R²=-2.0706

intercept: `4.3598`  ·  log_price: True  ·  ilvl: `-0.05304`  ·  n_mods: `-0.02376`  ·  n_top_tier: `1.12537`  ·  corrupted: `0.33704`  ·  n_sockets: `2.20218`  ·  quality: `-0.01130`

| stat_id | coef |
|---|---|
| `explicit.stat_983749596@T1` | -1.91217 |
| `explicit.stat_1202301673@T2` | -1.88371 |
| `explicit.stat_983749596@T2` | -1.76793 |
| `explicit.stat_3299347043@T1` | -1.70202 |
| `explicit.stat_3299347043@T2` | -1.37097 |
| `explicit.stat_2748665614@T2` | -1.24877 |
| `explicit.stat_2748665614@T1` | -1.24186 |
| `explicit.stat_3325883026@T1` | -1.22281 |
| `explicit.stat_3917489142@T1` | -1.21505 |
| `explicit.stat_3917489142@T2` | -1.21325 |
| `explicit.stat_3489782002@T2` | -1.20557 |
| `explicit.stat_1671376347@T2` | -1.19954 |

### accessory.belt — n=17432, R²=-1.3838

intercept: `3.6923`  ·  log_price: True  ·  ilvl: `-0.04429`  ·  n_mods: `-0.02087`  ·  n_top_tier: `0.58407`  ·  corrupted: `0.69044`  ·  n_sockets: `-0.13054`

| stat_id | coef |
|---|---|
| `crafted.stat_3249412463` | 3.15618 |
| `explicit.stat_809229260@T2` | -0.62538 |
| `explicit.stat_2881298780@T1` | -0.61928 |
| `explicit.stat_1389754388@T1` | -0.61671 |
| `explicit.stat_4220027924@T2` | -0.61439 |
| `explicit.stat_3299347043@T2` | -0.61095 |
| `explicit.stat_3299347043@T1` | -0.60848 |
| `explicit.stat_3325883026@T1` | -0.60547 |
| `explicit.stat_51994685@T1` | -0.60441 |
| `explicit.stat_644456512@T2` | -0.60184 |
| `explicit.stat_915769802@T2` | -0.60072 |
| `explicit.stat_915769802@T1` | -0.59400 |

### armour.chest — n=17246, R²=-0.2335

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.02717`  ·  corrupted: `0.00006`  ·  n_sockets: `-0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_3981240776` | 0.03446 |
| `desecrated.stat_4220027924` | -0.03262 |
| `desecrated.stat_3372524247` | -0.03012 |
| `pseudo.total_ele_res` | 0.02989 |
| `implicit.stat_4220027924` | -0.02989 |
| `explicit.stat_1671376347` | -0.02989 |
| `rune.stat_1671376347` | -0.02989 |
| `explicit.stat_3372524247` | -0.02989 |
| `rune.stat_4220027924` | -0.02989 |
| `explicit.stat_4220027924` | -0.02989 |
| `implicit.stat_1671376347` | -0.02989 |
| `implicit.stat_3372524247` | -0.02989 |

### armour.helmet — n=16877, R²=-0.24

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.18357`  ·  corrupted: `1.06591`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_4080418644@T2` | -0.18359 |
| `explicit.stat_3362812763@T1` | -0.18359 |
| `explicit.stat_53045048@T2` | -0.18358 |
| `explicit.stat_1062208444@T2` | -0.18358 |
| `explicit.stat_3362812763@T2` | -0.18358 |
| `explicit.stat_2451402625@T1` | -0.18358 |
| `explicit.stat_1263695895@T2` | -0.18358 |
| `explicit.stat_53045048@T1` | -0.18358 |
| `explicit.stat_328541901@T2` | -0.18358 |
| `explicit.stat_2451402625@T2` | -0.18358 |
| `explicit.stat_803737631@T2` | -0.18357 |
| `explicit.stat_1263695895@T1` | -0.18357 |

### armour.boots — n=15877, R²=-0.262

intercept: `2.3028`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.10368`  ·  corrupted: `0.00008`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -0.10381 |
| `explicit.stat_1062208444@T2` | -0.10373 |
| `desecrated.stat_2250533757@T2` | -0.10373 |
| `explicit.stat_3261801346@T2` | -0.10372 |
| `explicit.stat_3362812763@T1` | -0.10372 |
| `explicit.stat_2451402625@T2` | -0.10371 |
| `explicit.stat_2923486259@T2` | -0.10371 |
| `explicit.stat_3917489142@T2` | -0.10371 |
| `explicit.stat_3362812763@T2` | -0.10370 |
| `explicit.stat_3033371881@T2` | -0.10370 |
| `explicit.stat_99927264@T1` | -0.10370 |
| `explicit.stat_1999113824@T1` | -0.10370 |

### armour.gloves — n=15624, R²=-0.3063

intercept: `2.3065`  ·  log_price: True  ·  ilvl: `-0.00017`  ·  n_mods: `-0.00067`  ·  n_top_tier: `0.00207`  ·  corrupted: `0.00130`  ·  n_sockets: `0.00112`  ·  quality: `0.00005`

| stat_id | coef |
|---|---|
| `desecrated.stat_3032590688` | 0.09674 |
| `desecrated.stat_4067062424` | 0.04402 |
| `explicit.stat_2339757871@T1` | -0.01783 |
| `explicit.stat_3484657501@T2` | -0.00615 |
| `explicit.stat_2797971005@T2` | -0.00591 |
| `rune.stat_789117908` | -0.00575 |
| `explicit.stat_803737631@T2` | -0.00547 |
| `explicit.stat_3362812763@T2` | -0.00434 |
| `explicit.stat_681332047@T2` | -0.00410 |
| `explicit.stat_2451402625@T2` | -0.00397 |
| `explicit.stat_3917489142@T1` | -0.00360 |
| `explicit.stat_3033371881@T2` | -0.00360 |

### weapon.wand — n=10995, R²=-1.9823

intercept: `3.4942`  ·  log_price: True  ·  ilvl: `-0.04368`  ·  n_mods: `-0.00368`  ·  n_top_tier: `0.28911`  ·  corrupted: `0.10797`  ·  n_sockets: `0.00112`  ·  quality: `0.01044`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 2.16406 |
| `explicit.stat_2254480358@T1` | 2.15931 |
| `explicit.stat_591105508@T1` | 2.10294 |
| `explicit.stat_4226189338@T1` | 2.10085 |
| `explicit.stat_1600707273@T1` | 1.84847 |
| `explicit.stat_736967255@T2` | 1.27103 |
| `crafted.stat_124131830` | 0.77489 |
| `explicit.stat_1600707273@T2` | 0.63289 |
| `explicit.stat_1545858329@T1` | 0.55303 |
| `rune.stat_3278136794` | 0.38313 |
| `explicit.stat_737908626@T1` | -0.34904 |
| `explicit.stat_3962278098@T2` | -0.34147 |

### weapon.bow — n=9031, R²=-1.7916

intercept: `3.4899`  ·  log_price: True  ·  ilvl: `-0.04321`  ·  n_mods: `-0.01225`  ·  n_top_tier: `0.49387`  ·  corrupted: `-0.01080`  ·  n_sockets: `0.00518`  ·  quality: `0.00566`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.80206 |
| `explicit.stat_2463230181@T1` | 1.77770 |
| `explicit.stat_1202301673@T1` | 1.72077 |
| `explicit.stat_518292764@T1` | 1.49608 |
| `crafted.stat_3035140377` | 1.13966 |
| `desecrated.stat_666077204@T1` | -0.63545 |
| `explicit.stat_55876295@T1` | -0.59976 |
| `explicit.stat_55876295@T2` | -0.55672 |
| `explicit.stat_3261801346@T1` | -0.54353 |
| `explicit.stat_2694482655@T1` | -0.53538 |
| `explicit.stat_1037193709@T1` | -0.53375 |
| `explicit.stat_3695891184@T2` | -0.52936 |

### weapon.crossbow — n=8550, R²=-1.7094

intercept: `3.6628`  ·  log_price: True  ·  ilvl: `-0.04569`  ·  n_mods: `-0.00176`  ·  n_top_tier: `0.47140`  ·  corrupted: `-0.05115`  ·  n_sockets: `0.01082`  ·  quality: `0.00440`

| stat_id | coef |
|---|---|
| `explicit.stat_709508406@T1` | 1.77772 |
| `explicit.stat_1037193709@T1` | 1.74831 |
| `explicit.stat_1202301673@T1` | 1.72459 |
| `explicit.stat_2250681686@T2` | -1.37750 |
| `rune.stat_55876295` | 1.25988 |
| `rune.stat_2246411426` | -1.13361 |
| `crafted.stat_3035140377` | 1.12870 |
| `explicit.stat_1509134228@T1` | 1.11872 |
| `explicit.stat_2250681686` | 0.96688 |
| `explicit.stat_1202301673@T2` | -0.55440 |
| `explicit.stat_669069897@T1` | -0.52668 |
| `explicit.stat_669069897@T2` | -0.52634 |

### flask.charm — n=4754, R²=-0.178

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00003`  ·  corrupted: `0.00004`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 5.04344 |
| `explicit.stat_1056492907` | 2.99572 |
| `explicit.stat_3138344128` | 0.02162 |
| `explicit.stat_1873752457@T2` | -0.00004 |
| `explicit.stat_828533480@T2` | -0.00003 |
| `explicit.stat_828533480@T1` | -0.00003 |
| `explicit.stat_1873752457@T1` | -0.00003 |
| `explicit.stat_3196823591@T2` | -0.00003 |
| `explicit.stat_1873752457` | 0.00003 |
| `explicit.stat_2541588185@T2` | -0.00003 |
| `explicit.stat_388617051@T2` | -0.00003 |
| `explicit.stat_2676834156@T2` | -0.00003 |

### weapon.warstaff — n=3498, R²=-0.4377

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.00001`  ·  corrupted: `-0.00002`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `desecrated.stat_2231156303@T1` | -3.84874 |
| `desecrated.stat_2527686725@T1` | -3.84874 |
| `rune.stat_243313994` | 3.28921 |
| `rune.stat_731403740` | 1.62903 |
| `rune.stat_1712188793` | -1.29912 |
| `desecrated.stat_9187492` | 0.74875 |
| `rune.stat_1037193709` | 0.27305 |
| `desecrated.stat_2527686725` | 0.26630 |
| `rune.stat_3336890334` | 0.22886 |
| `rune.stat_2430860292` | -0.11823 |
| `rune.stat_1817052494` | -0.10922 |
| `desecrated.stat_2231156303` | 0.04306 |

### weapon.sceptre — n=3339, R²=-0.4272

intercept: `-0.0007`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00001`  ·  corrupted: `0.05854`  ·  n_sockets: `0.00001`  ·  quality: `0.03639`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 1.64237 |
| `rune.stat_1611856026` | 0.07494 |
| `rune.stat_3984865854` | 0.05804 |
| `rune.stat_3412619569` | 0.02187 |
| `rune.stat_1798257884` | 0.02187 |
| `desecrated.stat_1050105434` | 0.00771 |
| `explicit.stat_1798257884@T2` | 0.00014 |
| `explicit.stat_1263695895@T1` | 0.00006 |
| `explicit.stat_1250712710@T1` | -0.00004 |
| `explicit.stat_101878827@T1` | -0.00003 |
| `explicit.stat_3984865854@T2` | -0.00003 |
| `explicit.stat_2347036682@T2` | -0.00003 |

### weapon.staff — n=3306, R²=-0.4458

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 7.64580 |
| `rune.stat_3990135792` | -0.14240 |
| `explicit.stat_2254480358@T1` | 0.13137 |
| `rune.stat_975988108` | -0.11612 |
| `rune.stat_2974417149` | 0.08043 |
| `crafted.stat_124131830` | 0.04009 |
| `explicit.stat_473429811@T1` | 0.00132 |
| `explicit.stat_124131830@T1` | 0.00005 |
| `explicit.stat_1600707273@T1` | 0.00004 |
| `explicit.stat_3962278098@T2` | 0.00004 |
| `explicit.stat_124131830@T2` | 0.00004 |
| `explicit.stat_2254480358@T2` | 0.00003 |

### weapon.spear — n=2926, R²=-0.4677

intercept: `-0.0003`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `-0.00001`  ·  corrupted: `-0.00002`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 1.71695 |
| `rune.stat_1039491398` | 0.17394 |
| `rune.stat_1509134228` | -0.17255 |
| `explicit.stat_210067635@T1` | 0.06336 |
| `explicit.stat_2694482655@T1` | 0.00004 |
| `explicit.stat_709508406@T1` | 0.00004 |
| `explicit.stat_3639275092@T1` | 0.00003 |
| `explicit.stat_3639275092@T2` | 0.00003 |
| `explicit.stat_1509134228@T1` | 0.00003 |
| `explicit.stat_3336890334@T2` | 0.00003 |
| `explicit.stat_1263695895@T2` | -0.00003 |
| `explicit.stat_210067635@T2` | 0.00003 |

### armour.focus — n=2316, R²=-0.3457

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.00002`  ·  corrupted: `0.00000`  ·  n_sockets: `0.00001`  ·  quality: `0.00008`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 2.16564 |
| `crafted.stat_737908626@T2` | -1.45469 |
| `desecrated.stat_2910761524@T1` | 0.91576 |
| `desecrated.stat_378817135@T1` | -0.25929 |
| `desecrated.stat_2910761524` | -0.10775 |
| `crafted.stat_737908626` | 0.08326 |
| `crafted.stat_4015621042` | 0.06670 |
| `desecrated.stat_378817135` | 0.05942 |
| `rune.stat_3523867985` | 0.02028 |
| `crafted.stat_2974417149` | 0.00998 |
| `desecrated.stat_4015621042` | 0.00959 |
| `desecrated.stat_2891184298` | 0.00562 |

### armour.quiver — n=2230, R²=-0.4855

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00002`  ·  corrupted: `0.00003`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 1.90925 |
| `desecrated.stat_2194114101` | 0.18535 |
| `desecrated.stat_3932115504` | 0.13563 |
| `explicit.stat_3759663284@T1` | 0.00554 |
| `desecrated.stat_3714003708` | 0.00039 |
| `explicit.stat_2463230181@T1` | -0.00009 |
| `explicit.stat_2463230181@T2` | -0.00004 |
| `explicit.stat_681332047@T2` | -0.00004 |
| `explicit.stat_803737631@T2` | -0.00004 |
| `explicit.stat_681332047@T1` | -0.00004 |
| `explicit.stat_2321178454@T2` | -0.00003 |
| `explicit.stat_1368271171@T2` | -0.00003 |

### armour.shield — n=1987, R²=-0.4263

intercept: `-0.0004`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `0.00000`  ·  n_top_tier: `0.15565`  ·  corrupted: `0.00001`  ·  n_sockets: `0.00001`  ·  quality: `0.00011`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.85899 |
| `explicit.stat_1978899297@T2` | -0.34172 |
| `explicit.stat_1301765461@T1` | 0.20267 |
| `explicit.stat_1978899297` | 0.18605 |
| `explicit.stat_1011760251@T1` | -0.15574 |
| `explicit.stat_2481353198@T1` | -0.15570 |
| `explicit.stat_1011760251@T2` | -0.15570 |
| `explicit.stat_2481353198@T2` | -0.15569 |
| `explicit.stat_3484657501@T1` | -0.15568 |
| `explicit.stat_1301765461@T2` | -0.15567 |
| `explicit.stat_2923486259@T2` | -0.15567 |
| `explicit.stat_3639275092@T1` | -0.15566 |

### weapon.twomace — n=1702, R²=-0.4003

intercept: `-0.0005`  ·  log_price: True  ·  ilvl: `0.00001`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.24124`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00001`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_518292764@T1` | 1.10496 |
| `explicit.stat_1037193709@T1` | -0.24129 |
| `explicit.stat_3336890334@T1` | -0.24129 |
| `explicit.stat_387439868@T2` | -0.24127 |
| `explicit.stat_1037193709@T2` | -0.24127 |
| `explicit.stat_691932474@T2` | -0.24126 |
| `explicit.stat_1940865751@T2` | -0.24126 |
| `explicit.stat_9187492@T1` | -0.24126 |
| `explicit.stat_669069897@T2` | -0.24126 |
| `explicit.stat_669069897@T1` | -0.24126 |
| `explicit.stat_1940865751@T1` | -0.24125 |
| `explicit.stat_821021828@T1` | -0.24125 |

## Coverage (listings per base)

- … **Emerald** — 10431 listings (10423 priced) [0.7–7553463.8 ex]
- … **Sapphire** — 10369 listings (10357 priced) [0.4–7553463.8 ex]
- … **Ruby** — 8090 listings (8080 priced) [0.3–7553463.8 ex]
- … **Utility Belt** — 5218 listings (5214 priced) [0.3–4877938.3 ex]
- … **Stellar Amulet** — 3931 listings (3931 priced) [0.3–35690283.3 ex]
- … **Prismatic Ring** — 3816 listings (3815 priced) [0.3–24532814.5 ex]
- … **Solar Amulet** — 3730 listings (3725 priced) [0.4–66666666.0 ex]
- … **Amethyst Ring** — 3646 listings (3645 priced) [0.4–71450.3 ex]
- … **Gold Amulet** — 3597 listings (3597 priced) [0.4–292542.5 ex]
- … **Gold Ring** — 3482 listings (3481 priced) [0.4–24532814.5 ex]
- … **Dueling Wand** — 3416 listings (3412 priced) [0.8–3736768402.2 ex]
- … **Sapphire Ring** — 2881 listings (2880 priced) [0.4–24532814.5 ex]
- … **Topaz Ring** — 2843 listings (2843 priced) [1.0–24532814.5 ex]
- … **Ruby Ring** — 2801 listings (2801 priced) [0.4–146119.1 ex]
- … **Plate Belt** — 2645 listings (2643 priced) [0.4–4877938.3 ex]
- … **Obliterator Bow** — 2599 listings (2593 priced) [0.4–22139622146.9 ex]
- … **Lapis Amulet** — 2542 listings (2542 priced) [0.4–4547453.5 ex]
- … **Ancestral Tiara** — 2535 listings (2533 priced) [0.6–5125681.0 ex]
- … **Amber Amulet** — 2494 listings (2494 priced) [0.4–4547453.5 ex]
- … **Heavy Belt** — 2493 listings (2493 priced) [0.4–4877938.3 ex]
- … **Jade Amulet** — 2474 listings (2473 priced) [0.4–4547453.5 ex]
- … **Unset Ring** — 2321 listings (2321 priced) [0.4–24532814.5 ex]
- … **Bloodstone Amulet** — 2301 listings (2301 priced) [0.4–14638.0 ex]
- … **Pearl Ring** — 2263 listings (2263 priced) [0.4–24532814.5 ex]
- … **Azure Amulet** — 2225 listings (2225 priced) [0.4–4877938.3 ex]
