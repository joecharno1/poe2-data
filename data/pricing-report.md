# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-21T10:24:27+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **707181** (704944 priced in exalted)
- Distinct bases: 1001 · distinct mods: 3320 · mod rows: 3345475
- Sold signals: **24221** sold · 402471 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-21T10:10:53+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×16.72** (median |log error| 2.8168)
- Within ±30% of asking price: **18%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.14** · typical error ×49.31 · ±30% 7% · n=102876
- Premium segment (60ex+): skill **+0.14** · typical error ×242.26 · ±30% 0% · n=68211

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 15164 | ×47.68 | 21% | +0.04 | +0.06 |
| jewel | 14518 | ×10.00 | 4% | +0.11 | +0.13 |
| accessory.amulet | 13602 | ×10.75 | 23% | +0.01 | +0.01 |
| accessory.belt | 9684 | ×19.99 | 24% | +0.02 | +0.04 |
| armour.chest | 9414 | ×14.73 | 22% | +0.08 | +0.11 |
| armour.helmet | 9175 | ×25.34 | 19% | +0.08 | +0.10 |
| armour.boots | 8460 | ×20.90 | 19% | +0.11 | +0.13 |
| armour.gloves | 8332 | ×31.27 | 13% | +0.08 | +0.11 |
| other | 8304 | ×2.00 | 42% | +0.11 | +0.18 |
| weapon.wand | 4910 | ×35.75 | 15% | +0.11 | +0.11 |
| weapon.bow | 3879 | ×27.03 | 12% | +0.15 | +0.15 |
| weapon.crossbow | 3657 | ×25.85 | 14% | +0.12 | +0.16 |
| weapon.warstaff | 2521 | ×13.69 | 7% | +0.21 | +0.21 |
| weapon.staff | 2424 | ×15.13 | 6% | +0.12 | +0.12 |
| weapon.sceptre | 2382 | ×18.44 | 5% | +0.08 | +0.09 |
| weapon.spear | 1912 | ×13.15 | 7% | +0.11 | +0.15 |
| armour.focus | 1579 | ×13.44 | 7% | +0.12 | +0.13 |
| armour.quiver | 1471 | ×17.13 | 7% | +0.12 | +0.14 |
| armour.shield | 1203 | ×8.18 | 8% | +0.10 | +0.12 |
| flask.charm | 1196 | ×10.00 | 27% | +0.02 | +0.02 |
| weapon.twomace | 1120 | ×9.29 | 7% | +0.10 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=79579, R²=-0.9839

intercept: `-1.8909`  ·  log_price: True  ·  ilvl: `0.02376`  ·  n_mods: `0.85304`  ·  n_top_tier: `-0.27999`  ·  corrupted: `0.31293`  ·  quality: `-0.00085`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -2.91368 |
| `explicit.stat_3485067555@T1` | 1.75563 |
| `explicit.stat_1594812856@T1` | 1.61915 |
| `explicit.stat_3174700878@T1` | 1.57022 |
| `explicit.stat_627767961@T1` | -1.52233 |
| `explicit.stat_239367161@T1` | -1.48224 |
| `explicit.stat_1569101201@T1` | -1.45783 |
| `explicit.stat_1869147066@T1` | -1.43774 |
| `explicit.stat_3668351662@T1` | -1.35224 |
| `explicit.stat_1852872083@T1` | -1.34749 |
| `explicit.stat_1697447343@T1` | -1.18984 |
| `explicit.stat_234296660@T1` | -1.17701 |

### accessory.ring — n=69030, R²=-2.0114

intercept: `3.4466`  ·  log_price: True  ·  ilvl: `-0.04295`  ·  n_mods: `0.00081`  ·  n_top_tier: `0.98392`  ·  corrupted: `0.00929`  ·  n_sockets: `2.17989`  ·  quality: `0.01944`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.03082 |
| `explicit.stat_803737631@T1` | -1.01450 |
| `explicit.stat_4080418644@T1` | -1.00653 |
| `explicit.stat_2231156303@T1` | -1.00550 |
| `explicit.stat_3325883026@T1` | -1.00323 |
| `explicit.stat_4220027924@T2` | -1.00080 |
| `explicit.stat_2891184298@T2` | -1.00062 |
| `explicit.stat_2923486259@T2` | -0.99852 |
| `explicit.stat_1573130764@T2` | -0.99768 |
| `explicit.stat_3291658075@T2` | -0.99766 |
| `explicit.stat_736967255@T2` | -0.99530 |
| `explicit.stat_3962278098@T1` | -0.99394 |

### other — n=67341, R²=-0.6621

intercept: `1.6092`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.05642`  ·  n_top_tier: `0.29015`  ·  corrupted: `0.01502`  ·  n_sockets: `-0.00003`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.39321 |
| `explicit.stat_3299347043@T1` | -0.23824 |
| `implicit.stat_2219129443` | 0.22461 |
| `implicit.stat_718638445` | 0.16930 |
| `implicit.stat_3182714256` | 0.16929 |
| `explicit.stat_3917489142@T1` | -0.15434 |
| `explicit.stat_2974417149@T1` | 0.11671 |
| `explicit.stat_789117908@T1` | -0.07346 |
| `implicit.stat_3879011313` | 0.07070 |
| `implicit.stat_958696139` | -0.05641 |
| `explicit.stat_736967255@T1` | -0.04094 |
| `implicit.stat_4041853756` | 0.02901 |

### accessory.amulet — n=61994, R²=-0.485

intercept: `2.3026`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `1.11713`  ·  corrupted: `0.00000`  ·  n_sockets: `1.79162`  ·  quality: `0.03954`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T2` | -1.34237 |
| `explicit.stat_124131830@T2` | -1.30786 |
| `explicit.stat_2162097452@T2` | -1.15625 |
| `explicit.stat_3299347043@T2` | -1.11716 |
| `explicit.stat_983749596@T2` | -1.11716 |
| `explicit.stat_803737631@T1` | -1.11716 |
| `explicit.stat_803737631@T2` | -1.11716 |
| `explicit.stat_789117908@T1` | -1.11715 |
| `explicit.stat_789117908@T2` | -1.11715 |
| `explicit.stat_4080418644@T2` | -1.11714 |
| `explicit.stat_3325883026@T1` | -1.11714 |
| `explicit.stat_2891184298@T1` | -1.11714 |

### accessory.belt — n=44418, R²=-2.1132

intercept: `0.1034`  ·  log_price: True  ·  ilvl: `-0.00125`  ·  n_mods: `-0.00056`  ·  n_top_tier: `0.65608`  ·  corrupted: `0.77336`  ·  n_sockets: `1.60621`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -0.65692 |
| `explicit.stat_51994685@T1` | -0.65677 |
| `explicit.stat_3299347043@T2` | -0.65672 |
| `explicit.stat_915769802@T1` | -0.65670 |
| `explicit.stat_2881298780@T1` | -0.65662 |
| `explicit.stat_809229260@T2` | -0.65659 |
| `explicit.stat_3325883026@T1` | -0.65638 |
| `explicit.stat_3372524247@T2` | -0.65634 |
| `explicit.stat_1570770415@T2` | -0.65629 |
| `explicit.stat_1389754388@T1` | -0.65623 |
| `explicit.stat_4220027924@T2` | -0.65621 |
| `explicit.stat_915769802@T2` | -0.65611 |

### armour.chest — n=44047, R²=-1.7865

intercept: `3.3026`  ·  log_price: True  ·  ilvl: `-0.04083`  ·  n_mods: `-0.01266`  ·  n_top_tier: `0.33192`  ·  corrupted: `0.34347`  ·  n_sockets: `0.01940`  ·  quality: `0.06987`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.71077 |
| `explicit.stat_986397080@T2` | -0.40834 |
| `explicit.stat_986397080@T1` | -0.39914 |
| `explicit.stat_1692879867@T2` | -0.37504 |
| `explicit.stat_915769802@T2` | -0.36158 |
| `explicit.stat_3484657501@T1` | -0.36025 |
| `explicit.stat_4080418644@T2` | -0.35858 |
| `explicit.stat_4080418644@T1` | -0.35650 |
| `explicit.stat_2339757871@T2` | -0.35440 |
| `explicit.stat_3301100256@T2` | -0.35419 |
| `explicit.stat_915769802@T1` | -0.35409 |
| `explicit.stat_1062208444@T2` | -0.34361 |

### armour.helmet — n=42775, R²=-1.7695

intercept: `3.2283`  ·  log_price: True  ·  ilvl: `-0.04086`  ·  n_mods: `-0.01545`  ·  n_top_tier: `0.59256`  ·  corrupted: `0.55705`  ·  n_sockets: `0.04817`  ·  quality: `0.07002`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -4.24602 |
| `explicit.stat_3917489142@T2` | -0.77052 |
| `explicit.stat_1263695895@T1` | -0.75984 |
| `explicit.stat_2162097452@T2` | -0.74000 |
| `explicit.stat_3917489142@T1` | -0.70338 |
| `explicit.stat_4052037485@T2` | -0.65015 |
| `explicit.stat_4015621042@T2` | -0.64650 |
| `explicit.stat_1999113824@T1` | -0.64254 |
| `explicit.stat_1263695895@T2` | -0.63907 |
| `explicit.stat_803737631@T1` | -0.63615 |
| `explicit.stat_803737631@T2` | -0.62891 |
| `explicit.stat_53045048@T1` | -0.62470 |

### armour.boots — n=39619, R²=-1.6786

intercept: `3.7032`  ·  log_price: True  ·  ilvl: `-0.04571`  ·  n_mods: `-0.02625`  ·  n_top_tier: `0.41349`  ·  corrupted: `0.04800`  ·  n_sockets: `0.06785`  ·  quality: `0.06708`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.81070 |
| `crafted.stat_3917489142@T1` | 1.57809 |
| `explicit.stat_2339757871@T1` | -1.27058 |
| `explicit.stat_2923486259@T1` | 0.86075 |
| `explicit.stat_3299347043@T1` | -0.54793 |
| `explicit.stat_2923486259@T2` | -0.50046 |
| `explicit.stat_3917489142@T2` | -0.49241 |
| `explicit.stat_2160282525@T1` | -0.48563 |
| `explicit.stat_1999113824@T2` | -0.47813 |
| `explicit.stat_1874553720@T1` | -0.47667 |
| `explicit.stat_1671376347@T2` | -0.47257 |
| `explicit.stat_328541901@T2` | -0.46860 |

### armour.gloves — n=38632, R²=-1.6583

intercept: `3.7221`  ·  log_price: True  ·  ilvl: `-0.04932`  ·  n_mods: `-0.00608`  ·  n_top_tier: `0.80183`  ·  corrupted: `-0.01888`  ·  n_sockets: `0.18639`  ·  quality: `0.05924`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 2.95472 |
| `explicit.stat_2923486259@T1` | -1.27907 |
| `explicit.stat_2923486259@T2` | -1.20313 |
| `explicit.stat_3484657501@T2` | -1.08767 |
| `explicit.stat_4052037485@T2` | -1.03202 |
| `explicit.stat_4015621042@T2` | -1.01133 |
| `explicit.stat_4052037485@T1` | -0.99462 |
| `explicit.stat_124859000@T1` | -0.98296 |
| `explicit.stat_3484657501@T1` | -0.98103 |
| `explicit.stat_3321629045@T2` | -0.96796 |
| `explicit.stat_803737631@T2` | -0.94207 |
| `explicit.stat_9187492@T2` | -0.93946 |

### weapon.wand — n=22892, R²=-1.9424

intercept: `3.9764`  ·  log_price: True  ·  ilvl: `-0.04913`  ·  n_mods: `-0.06005`  ·  n_top_tier: `0.41513`  ·  corrupted: `0.00979`  ·  n_sockets: `0.02394`  ·  quality: `0.04728`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -4.01423 |
| `explicit.stat_1545858329@T1` | 2.86027 |
| `explicit.stat_2254480358@T1` | 2.56796 |
| `explicit.stat_124131830@T1` | 2.16530 |
| `explicit.stat_591105508@T1` | 1.98158 |
| `explicit.stat_736967255@T2` | 1.73185 |
| `explicit.stat_4226189338@T1` | 1.60809 |
| `explicit.stat_2254480358@T2` | 1.38395 |
| `crafted.stat_124131830` | 1.18337 |
| `explicit.stat_1600707273@T1` | 0.90368 |
| `explicit.stat_4226189338@T2` | 0.84610 |
| `explicit.stat_1263695895@T2` | -0.83531 |

### flask.charm — n=19790, R²=-0.6552

intercept: `0.1056`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00002`  ·  n_top_tier: `1.60955`  ·  corrupted: `1.55467`  ·  quality: `0.00783`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.60510 |
| `explicit.stat_1056492907` | 2.66934 |
| `explicit.stat_3246948616` | 1.61060 |
| `explicit.stat_1120862500@T2` | -1.60960 |
| `explicit.stat_828533480@T2` | -1.60958 |
| `explicit.stat_1873752457@T2` | -1.60955 |
| `explicit.stat_3196823591@T2` | -1.60950 |
| `explicit.stat_2676834156@T2` | -1.60950 |
| `explicit.stat_2365392475@T2` | -1.60949 |
| `explicit.stat_828533480@T1` | -1.60885 |
| `explicit.stat_2541588185@T2` | -1.60652 |
| `explicit.stat_388617051@T2` | -1.60346 |

### weapon.bow — n=18234, R²=-1.8242

intercept: `3.8337`  ·  log_price: True  ·  ilvl: `-0.04611`  ·  n_mods: `-0.07268`  ·  n_top_tier: `0.73809`  ·  corrupted: `0.66980`  ·  n_sockets: `0.04914`  ·  quality: `0.02939`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 2.04603 |
| `desecrated.stat_210067635@T1` | -1.81312 |
| `explicit.stat_1263695895@T1` | -1.29466 |
| `explicit.stat_1263695895@T2` | -1.22498 |
| `crafted.stat_3035140377` | 1.20642 |
| `explicit.stat_709508406@T1` | 1.07280 |
| `explicit.stat_1509134228@T1` | -0.97592 |
| `explicit.stat_3336890334@T1` | 0.90947 |
| `explicit.stat_2463230181@T2` | -0.84882 |
| `explicit.stat_3695891184@T2` | -0.84636 |
| `explicit.stat_3695891184@T1` | -0.83614 |
| `explicit.stat_1368271171@T2` | -0.81409 |

### weapon.crossbow — n=17129, R²=-1.6945

intercept: `4.0269`  ·  log_price: True  ·  ilvl: `-0.04878`  ·  n_mods: `-0.07416`  ·  n_top_tier: `0.32055`  ·  corrupted: `0.06543`  ·  n_sockets: `0.06539`  ·  quality: `0.03502`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.77709 |
| `explicit.stat_1202301673@T1` | 1.50865 |
| `explicit.stat_1980802737` | 1.41245 |
| `explicit.stat_2250681686@T2` | -1.37085 |
| `explicit.stat_2250681686` | 1.09938 |
| `explicit.stat_1509134228@T1` | 1.01994 |
| `explicit.stat_709508406@T1` | 0.86181 |
| `crafted.stat_3035140377` | 0.79083 |
| `explicit.stat_387439868@T1` | 0.61628 |
| `explicit.stat_1263695895@T2` | -0.60062 |
| `explicit.stat_518292764@T1` | 0.56880 |
| `explicit.stat_3695891184@T1` | -0.55304 |

### weapon.warstaff — n=11951, R²=-0.3415

intercept: `-10.3417`  ·  log_price: True  ·  ilvl: `0.13919`  ·  n_mods: `-0.21520`  ·  n_top_tier: `0.42855`  ·  corrupted: `0.26201`  ·  n_sockets: `0.13332`  ·  quality: `0.05541`

| stat_id | coef |
|---|---|
| `desecrated.stat_2231156303@T1` | 1.29104 |
| `desecrated.stat_2527686725@T1` | 1.29104 |
| `crafted.stat_210067635@T2` | 1.05726 |
| `explicit.stat_328541901@T2` | -0.97476 |
| `explicit.stat_328541901@T1` | -0.81948 |
| `explicit.stat_821021828@T2` | -0.80795 |
| `desecrated.stat_9187492` | 0.80058 |
| `rune.stat_243313994` | 0.72646 |
| `explicit.stat_1037193709@T2` | -0.64730 |
| `explicit.stat_691932474@T2` | -0.59163 |
| `explicit.stat_9187492@T2` | -0.53214 |
| `explicit.stat_2694482655@T1` | 0.52943 |

### weapon.staff — n=11341, R²=-0.3612

intercept: `-15.5800`  ·  log_price: True  ·  ilvl: `0.19802`  ·  n_mods: `-0.06267`  ·  n_top_tier: `0.48046`  ·  corrupted: `0.70976`  ·  n_sockets: `0.14555`  ·  quality: `0.03356`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.17231 |
| `explicit.stat_1600707273@T1` | 1.48276 |
| `explicit.stat_1545858329@T1` | 1.45603 |
| `explicit.stat_124131830@T1` | 1.40758 |
| `explicit.stat_591105508@T1` | 1.31129 |
| `explicit.stat_2254480358@T1` | 1.08620 |
| `explicit.stat_293638271@T2` | -1.05793 |
| `rune.stat_124131830` | 0.98223 |
| `explicit.stat_3962278098@T2` | 0.89340 |
| `explicit.stat_1263695895@T2` | -0.66377 |
| `explicit.stat_473429811@T2` | -0.65041 |
| `crafted.stat_124131830` | 0.60701 |

### weapon.sceptre — n=11122, R²=-0.351

intercept: `-20.8563`  ·  log_price: True  ·  ilvl: `0.26397`  ·  n_mods: `0.00173`  ·  n_top_tier: `0.00206`  ·  corrupted: `0.29972`  ·  n_sockets: `0.19849`  ·  quality: `0.03607`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.69766 |
| `explicit.stat_2162097452@T2` | 1.45906 |
| `explicit.stat_3057012405@T1` | 1.11933 |
| `explicit.stat_1798257884@T2` | 1.04747 |
| `explicit.stat_101878827@T2` | 1.03862 |
| `explicit.stat_101878827@T1` | 0.93911 |
| `explicit.stat_1263695895@T2` | -0.84945 |
| `explicit.stat_849987426@T1` | 0.66449 |
| `explicit.stat_1263695895@T1` | -0.66328 |
| `explicit.stat_2347036682@T1` | 0.65185 |
| `explicit.stat_2854751904@T2` | -0.60242 |
| `explicit.stat_849987426@T2` | 0.59282 |

### weapon.spear — n=9013, R²=-0.3852

intercept: `-13.4507`  ·  log_price: True  ·  ilvl: `0.18237`  ·  n_mods: `-0.12420`  ·  n_top_tier: `0.63226`  ·  corrupted: `-0.62533`  ·  n_sockets: `0.18265`  ·  quality: `0.07018`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -4.61503 |
| `crafted.stat_210067635@T2` | -3.71921 |
| `explicit.stat_1202301673@T1` | 1.09778 |
| `explicit.stat_9187492@T1` | 1.03630 |
| `crafted.stat_3035140377` | 0.97851 |
| `explicit.stat_1940865751@T2` | -0.96551 |
| `explicit.stat_4080418644@T2` | -0.95802 |
| `explicit.stat_3336890334@T2` | -0.93858 |
| `desecrated.stat_210067635@T1` | -0.93854 |
| `explicit.stat_691932474@T2` | -0.82752 |
| `explicit.stat_748522257@T2` | -0.82496 |
| `explicit.stat_9187492@T2` | -0.78336 |

### armour.focus — n=7382, R²=-0.3406

intercept: `-15.7638`  ·  log_price: True  ·  ilvl: `0.19952`  ·  n_mods: `-0.12036`  ·  n_top_tier: `0.91864`  ·  corrupted: `0.06261`  ·  n_sockets: `0.25368`  ·  quality: `0.02755`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -1.59679 |
| `explicit.stat_4220027924@T1` | -1.36479 |
| `explicit.stat_2923486259@T2` | -1.09508 |
| `explicit.stat_4220027924@T2` | -1.08349 |
| `crafted.stat_2974417149@T1` | 1.08126 |
| `explicit.stat_2231156303@T2` | -1.06336 |
| `explicit.stat_4015621042@T1` | -1.05005 |
| `explicit.stat_2768835289@T1` | -1.03019 |
| `explicit.stat_2231156303@T1` | -1.02623 |
| `explicit.stat_2339757871@T2` | -0.98267 |
| `explicit.stat_737908626@T2` | -0.97846 |
| `explicit.stat_3291658075@T1` | -0.96728 |

### armour.quiver — n=6864, R²=-0.2892

intercept: `-18.1359`  ·  log_price: True  ·  ilvl: `0.21514`  ·  n_mods: `-0.03379`  ·  n_top_tier: `0.70523`  ·  corrupted: `0.94941`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.66933 |
| `explicit.stat_681332047@T2` | -1.53156 |
| `explicit.stat_681332047@T1` | -1.28975 |
| `explicit.stat_1573130764@T2` | -1.10676 |
| `explicit.stat_1573130764@T1` | -1.09730 |
| `explicit.stat_2194114101@T2` | -0.81417 |
| `explicit.stat_803737631@T1` | -0.79217 |
| `explicit.stat_4067062424@T1` | -0.70815 |
| `explicit.stat_2321178454@T2` | -0.61205 |
| `explicit.stat_3261801346@T1` | -0.60289 |
| `explicit.stat_803737631@T2` | -0.59795 |
| `explicit.stat_4067062424@T2` | -0.48706 |

### armour.shield — n=5915, R²=-0.4334

intercept: `-12.2042`  ·  log_price: True  ·  ilvl: `0.16228`  ·  n_mods: `-0.15356`  ·  n_top_tier: `0.65173`  ·  corrupted: `-0.25509`  ·  n_sockets: `0.41435`  ·  quality: `0.05273`

| stat_id | coef |
|---|---|
| `explicit.stat_328541901@T1` | -1.27426 |
| `explicit.stat_3855016469@T1` | -1.25470 |
| `explicit.stat_2901986750@T1` | -1.18829 |
| `explicit.stat_2339757871@T1` | -1.16166 |
| `explicit.stat_328541901@T2` | -1.09264 |
| `explicit.stat_2481353198@T1` | -1.07401 |
| `explicit.stat_3321629045@T2` | -1.05823 |
| `explicit.stat_1011760251@T1` | -1.01934 |
| `explicit.stat_4220027924@T1` | -0.98749 |
| `explicit.stat_2481353198@T2` | -0.97366 |
| `explicit.stat_2923486259@T1` | -0.97158 |
| `explicit.stat_4095671657@T1` | -0.95852 |

### weapon.twomace — n=5400, R²=-0.4484

intercept: `-11.4667`  ·  log_price: True  ·  ilvl: `0.15191`  ·  n_mods: `-0.19770`  ·  n_top_tier: `0.38941`  ·  corrupted: `0.74433`  ·  n_sockets: `0.14057`  ·  quality: `0.06952`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.97771 |
| `explicit.stat_1037193709@T1` | -1.61417 |
| `explicit.stat_3336890334@T1` | -1.40396 |
| `explicit.stat_1263695895@T2` | -1.22807 |
| `explicit.stat_2694482655@T1` | 1.10383 |
| `explicit.stat_9187492@T1` | -0.89929 |
| `explicit.stat_1263695895@T1` | -0.75937 |
| `explicit.stat_3695891184@T1` | -0.74806 |
| `explicit.stat_518292764@T2` | -0.71292 |
| `explicit.stat_1509134228@T1` | 0.70688 |
| `explicit.stat_691932474@T1` | -0.64344 |
| `explicit.stat_3695891184@T2` | -0.58142 |

## Coverage (listings per base)

- … **Sapphire** — 36596 listings (36537 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 35664 listings (35619 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 27279 listings (27248 priced) [0.3–3985176410.3 ex]
- … **Utility Belt** — 12700 listings (12682 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 11597 listings (11573 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 11253 listings (11227 priced) [1.0–3985176410.3 ex]
- … **Amethyst Ring** — 11126 listings (11114 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 10461 listings (10436 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 10415 listings (10392 priced) [0.2–3985176410.3 ex]
- … **Stellar Amulet** — 9885 listings (9872 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 8642 listings (8627 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 8285 listings (8276 priced) [0.3–3985176410.3 ex]
- … **Ruby Ring** — 8217 listings (8208 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7380 listings (7357 priced) [0.3–4297682211.9 ex]
- … **Unset Ring** — 7133 listings (7114 priced) [0.2–39887666593.4 ex]
- … **Lapis Amulet** — 7127 listings (7120 priced) [0.3–3985176410.3 ex]
- … **Jade Amulet** — 7062 listings (7047 priced) [0.3–4275054.0 ex]
- … **Amber Amulet** — 6998 listings (6990 priced) [0.3–3985176410.3 ex]
- … **Plate Belt** — 6921 listings (6893 priced) [0.3–398912568423.8 ex]
- … **Pearl Ring** — 6865 listings (6856 priced) [0.2–275252424.7 ex]
- … **Ancestral Tiara** — 6834 listings (6805 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 6781 listings (6771 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6445 listings (6442 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6351 listings (6337 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 6134 listings (6122 priced) [0.3–398912568423.8 ex]
