# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-20T04:42:38+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **672740** (670646 priced in exalted)
- Distinct bases: 998 · distinct mods: 3294 · mod rows: 3185004
- Sold signals: **24453** sold · 383177 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-20T04:29:52+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×24.63** (median |log error| 3.2038)
- Within ±30% of asking price: **20%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.12** · typical error ×79.99 · ±30% 4% · n=98177
- Premium segment (60ex+): skill **+0.12** · typical error ×380.09 · ±30% 0% · n=66065

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 14189 | ×49.82 | 21% | +0.03 | +0.06 |
| jewel | 13548 | ×56.23 | 21% | +0.03 | +0.03 |
| accessory.amulet | 12815 | ×25.37 | 18% | +0.04 | +0.04 |
| accessory.belt | 9292 | ×23.45 | 19% | +0.05 | +0.07 |
| armour.chest | 8957 | ×17.42 | 23% | +0.07 | +0.09 |
| armour.helmet | 8770 | ×27.36 | 22% | +0.06 | +0.10 |
| armour.boots | 8164 | ×25.39 | 20% | +0.09 | +0.12 |
| armour.gloves | 7981 | ×35.95 | 18% | +0.06 | +0.09 |
| other | 7930 | ×1.81 | 43% | +0.12 | +0.19 |
| weapon.wand | 4755 | ×41.51 | 16% | +0.09 | +0.12 |
| weapon.bow | 3717 | ×27.91 | 13% | +0.15 | +0.16 |
| weapon.crossbow | 3531 | ×29.31 | 14% | +0.11 | +0.16 |
| weapon.warstaff | 2423 | ×16.75 | 7% | +0.21 | +0.20 |
| weapon.staff | 2280 | ×20.04 | 6% | +0.18 | +0.16 |
| weapon.sceptre | 2262 | ×20.87 | 5% | +0.10 | +0.10 |
| weapon.spear | 1799 | ×18.14 | 8% | +0.12 | +0.13 |
| armour.focus | 1481 | ×17.91 | 6% | +0.11 | +0.13 |
| armour.quiver | 1401 | ×21.25 | 7% | +0.16 | +0.17 |
| armour.shield | 1149 | ×16.49 | 7% | +0.09 | +0.11 |
| flask.charm | 1145 | ×14.87 | 29% | -0.01 | +0.02 |
| weapon.twomace | 1079 | ×9.47 | 8% | +0.11 | +0.12 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=73863, R²=-1.8833

intercept: `-0.0712`  ·  log_price: True  ·  ilvl: `0.00088`  ·  n_mods: `1.02332`  ·  n_top_tier: `-0.88143`  ·  corrupted: `1.20265`  ·  quality: `0.21900`

| stat_id | coef |
|---|---|
| `explicit.stat_3714003708@T1` | 3.23449 |
| `explicit.stat_3485067555@T1` | 2.96920 |
| `explicit.stat_3473929743@T1` | -2.40266 |
| `explicit.stat_1604736568@T1` | -2.37413 |
| `explicit.stat_1604736568` | 2.25011 |
| `explicit.stat_1854213750@T1` | 1.19179 |
| `explicit.stat_3174700878@T1` | 1.02751 |
| `explicit.stat_274716455@T1` | -0.93309 |
| `explicit.stat_587431675@T1` | -0.91175 |
| `explicit.stat_1697447343@T1` | -0.78803 |
| `explicit.stat_2194114101@T1` | -0.64475 |
| `explicit.stat_2231156303@T1` | 0.64115 |

### accessory.ring — n=64923, R²=-2.0371

intercept: `3.4646`  ·  log_price: True  ·  ilvl: `-0.04322`  ·  n_mods: `0.00123`  ·  n_top_tier: `1.07795`  ·  corrupted: `0.01304`  ·  n_sockets: `1.90918`  ·  quality: `0.02938`

| stat_id | coef |
|---|---|
| `explicit.stat_4220027924@T2` | -1.11009 |
| `explicit.stat_1573130764@T2` | -1.11009 |
| `explicit.stat_1573130764@T1` | -1.10539 |
| `explicit.stat_2231156303@T1` | -1.10386 |
| `explicit.stat_803737631@T1` | -1.10381 |
| `explicit.stat_4080418644@T1` | -1.09731 |
| `explicit.stat_789117908@T2` | -1.09076 |
| `explicit.stat_2144192055@T1` | -1.09032 |
| `explicit.stat_789117908@T1` | -1.09014 |
| `explicit.stat_2923486259@T2` | -1.08971 |
| `explicit.stat_736967255@T2` | -1.08959 |
| `explicit.stat_3291658075@T2` | -1.08836 |

### other — n=64026, R²=-0.6169

intercept: `1.6092`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.08217`  ·  n_top_tier: `0.26440`  ·  corrupted: `0.07726`  ·  n_sockets: `-0.00004`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.31793 |
| `explicit.stat_3299347043@T1` | -0.27846 |
| `implicit.stat_718638445` | 0.24656 |
| `implicit.stat_3182714256` | 0.24655 |
| `implicit.stat_2219129443` | 0.22204 |
| `implicit.stat_3879011313` | 0.22203 |
| `implicit.stat_4041853756` | 0.22203 |
| `explicit.stat_2974417149@T1` | 0.17634 |
| `implicit.stat_958696139` | -0.08216 |
| `explicit.stat_789117908@T1` | -0.06899 |
| `explicit.stat_736967255@T1` | -0.06197 |
| `explicit.stat_3917489142@T1` | -0.05933 |

### accessory.amulet — n=58637, R²=-2.1129

intercept: `3.5021`  ·  log_price: True  ·  ilvl: `-0.04346`  ·  n_mods: `-0.02389`  ·  n_top_tier: `1.23712`  ·  corrupted: `0.07272`  ·  n_sockets: `-0.17167`  ·  quality: `0.02721`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.74421 |
| `explicit.stat_3299347043@T2` | -1.73023 |
| `explicit.stat_587431675@T2` | -1.41670 |
| `explicit.stat_2974417149@T1` | -1.36747 |
| `explicit.stat_803737631@T1` | -1.36285 |
| `explicit.stat_2866361420@T2` | -1.32616 |
| `explicit.stat_2866361420@T1` | -1.30535 |
| `explicit.stat_803737631@T2` | -1.30244 |
| `explicit.stat_1050105434@T2` | -1.30172 |
| `explicit.stat_2974417149@T2` | -1.30144 |
| `explicit.stat_2748665614@T1` | -1.29960 |
| `explicit.stat_2901986750@T1` | -1.28092 |

### accessory.belt — n=42535, R²=-1.6768

intercept: `4.0971`  ·  log_price: True  ·  ilvl: `-0.04898`  ·  n_mods: `-0.03023`  ·  n_top_tier: `0.43260`  ·  corrupted: `1.14563`  ·  n_sockets: `1.31804`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 1.10258 |
| `explicit.stat_3299347043@T1` | -0.58015 |
| `explicit.stat_4220027924@T1` | 0.55191 |
| `explicit.stat_3299347043@T2` | -0.48670 |
| `explicit.stat_3372524247@T1` | 0.48644 |
| `explicit.stat_2881298780@T1` | -0.48076 |
| `explicit.stat_4220027924@T2` | -0.46404 |
| `explicit.stat_51994685@T1` | -0.46030 |
| `explicit.stat_915769802@T1` | -0.44947 |
| `explicit.stat_1570770415@T2` | -0.44646 |
| `explicit.stat_3325883026@T1` | -0.44393 |
| `explicit.stat_3372524247@T2` | -0.43704 |

### armour.chest — n=42167, R²=-1.8059

intercept: `3.1638`  ·  log_price: True  ·  ilvl: `-0.03914`  ·  n_mods: `-0.01062`  ·  n_top_tier: `0.35669`  ·  corrupted: `0.05060`  ·  n_sockets: `0.01546`  ·  quality: `0.07306`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.66382 |
| `explicit.stat_3981240776@T1` | 0.66883 |
| `explicit.stat_986397080@T2` | -0.43131 |
| `explicit.stat_986397080@T1` | -0.41949 |
| `explicit.stat_1692879867@T2` | -0.39158 |
| `explicit.stat_4080418644@T1` | -0.38088 |
| `explicit.stat_3484657501@T1` | -0.37835 |
| `explicit.stat_915769802@T2` | -0.37822 |
| `explicit.stat_4080418644@T2` | -0.37706 |
| `explicit.stat_1692879867@T1` | -0.37490 |
| `explicit.stat_915769802@T1` | -0.37090 |
| `explicit.stat_3299347043@T2` | -0.36726 |

### armour.helmet — n=41015, R²=-1.8612

intercept: `3.1027`  ·  log_price: True  ·  ilvl: `-0.03898`  ·  n_mods: `-0.01281`  ·  n_top_tier: `0.45163`  ·  corrupted: `0.67391`  ·  n_sockets: `0.02454`  ·  quality: `0.07274`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.05726 |
| `explicit.stat_1263695895@T1` | -0.63779 |
| `explicit.stat_2162097452@T2` | -0.61112 |
| `explicit.stat_3917489142@T2` | -0.59693 |
| `explicit.stat_1263695895@T2` | -0.54012 |
| `explicit.stat_3917489142@T1` | -0.52809 |
| `explicit.stat_1999113824@T1` | -0.48378 |
| `explicit.stat_4052037485@T2` | -0.47566 |
| `explicit.stat_53045048@T1` | -0.47562 |
| `explicit.stat_803737631@T1` | -0.47458 |
| `explicit.stat_3321629045@T2` | -0.47162 |
| `explicit.stat_3362812763@T1` | -0.46879 |

### armour.boots — n=38135, R²=-1.7733

intercept: `3.3108`  ·  log_price: True  ·  ilvl: `-0.04087`  ·  n_mods: `-0.01534`  ·  n_top_tier: `0.50946`  ·  corrupted: `0.10122`  ·  n_sockets: `0.03629`  ·  quality: `0.06315`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.69067 |
| `crafted.stat_3917489142@T1` | 1.57047 |
| `explicit.stat_2339757871@T1` | -1.15320 |
| `explicit.stat_3299347043@T1` | -0.59239 |
| `explicit.stat_3917489142@T2` | -0.57162 |
| `explicit.stat_2923486259@T2` | -0.56827 |
| `explicit.stat_1874553720@T1` | -0.55991 |
| `explicit.stat_2160282525@T1` | -0.54759 |
| `explicit.stat_1671376347@T2` | -0.54539 |
| `explicit.stat_124859000@T1` | -0.54108 |
| `explicit.stat_328541901@T2` | -0.53341 |
| `explicit.stat_1874553720@T2` | -0.53191 |

### armour.gloves — n=37061, R²=-1.8765

intercept: `3.5487`  ·  log_price: True  ·  ilvl: `-0.04559`  ·  n_mods: `-0.01172`  ·  n_top_tier: `0.67750`  ·  corrupted: `-0.02799`  ·  n_sockets: `0.08604`  ·  quality: `0.06245`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 4.22007 |
| `explicit.stat_2923486259@T1` | -0.99096 |
| `explicit.stat_3484657501@T2` | -0.83094 |
| `explicit.stat_4052037485@T1` | -0.82457 |
| `explicit.stat_3321629045@T2` | -0.82137 |
| `explicit.stat_4015621042@T2` | -0.82113 |
| `explicit.stat_9187492@T2` | -0.81999 |
| `explicit.stat_803737631@T2` | -0.79896 |
| `explicit.stat_4052037485@T2` | -0.76408 |
| `explicit.stat_803737631@T1` | -0.74932 |
| `explicit.stat_3484657501@T1` | -0.72530 |
| `explicit.stat_1754445556@T2` | -0.72344 |

### weapon.wand — n=22255, R²=-1.9991

intercept: `3.8395`  ·  log_price: True  ·  ilvl: `-0.04748`  ·  n_mods: `-0.06110`  ·  n_top_tier: `0.25226`  ·  corrupted: `-0.03139`  ·  n_sockets: `0.04122`  ·  quality: `0.03953`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.98674 |
| `explicit.stat_2254480358@T1` | 2.72123 |
| `rune.stat_124131830` | -2.68650 |
| `explicit.stat_124131830@T1` | 2.35979 |
| `explicit.stat_591105508@T1` | 2.07548 |
| `explicit.stat_4226189338@T1` | 2.02406 |
| `explicit.stat_736967255@T2` | 1.96631 |
| `explicit.stat_2254480358@T2` | 1.48251 |
| `crafted.stat_124131830` | 1.22771 |
| `explicit.stat_4226189338@T2` | 1.15181 |
| `explicit.stat_1600707273@T1` | 0.97104 |
| `explicit.stat_1545858329@T2` | 0.67865 |

### flask.charm — n=18613, R²=-0.6415

intercept: `0.1056`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.55641`  ·  corrupted: `1.58076`  ·  quality: `0.00410`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.67554 |
| `explicit.stat_1056492907` | 2.71206 |
| `explicit.stat_1120862500@T2` | -1.55644 |
| `explicit.stat_828533480@T2` | -1.55644 |
| `explicit.stat_1873752457@T2` | -1.55641 |
| `explicit.stat_3196823591@T2` | -1.55638 |
| `explicit.stat_2365392475@T2` | -1.55637 |
| `explicit.stat_388617051@T2` | -1.55631 |
| `explicit.stat_2676834156@T2` | -1.55441 |
| `explicit.stat_1873752457@T1` | -1.55394 |
| `explicit.stat_828533480@T1` | -1.55059 |
| `explicit.stat_2541588185@T2` | -1.54184 |

### weapon.bow — n=17719, R²=-1.7874

intercept: `4.0731`  ·  log_price: True  ·  ilvl: `-0.04827`  ·  n_mods: `-0.08575`  ·  n_top_tier: `0.72131`  ·  corrupted: `0.56951`  ·  n_sockets: `0.07805`  ·  quality: `0.03001`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.96493 |
| `crafted.stat_3035140377` | 1.30037 |
| `explicit.stat_3336890334@T1` | 1.29662 |
| `explicit.stat_1263695895@T1` | -1.02065 |
| `explicit.stat_1263695895@T2` | -1.01799 |
| `explicit.stat_709508406@T1` | 1.01414 |
| `explicit.stat_1509134228@T1` | -0.88306 |
| `explicit.stat_210067635@T2` | -0.81699 |
| `explicit.stat_3695891184@T2` | -0.81053 |
| `explicit.stat_3639275092@T1` | -0.80404 |
| `explicit.stat_1368271171@T2` | -0.80325 |
| `explicit.stat_3695891184@T1` | -0.76278 |

### weapon.crossbow — n=16636, R²=-1.7164

intercept: `4.0524`  ·  log_price: True  ·  ilvl: `-0.04924`  ·  n_mods: `-0.07586`  ·  n_top_tier: `0.39974`  ·  corrupted: `0.14577`  ·  n_sockets: `0.10120`  ·  quality: `0.02859`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 1.52169 |
| `explicit.stat_1980802737` | 1.32938 |
| `explicit.stat_1980802737@T2` | -1.18708 |
| `explicit.stat_2250681686@T2` | -1.03182 |
| `crafted.stat_3035140377` | 0.78465 |
| `explicit.stat_2250681686` | 0.76290 |
| `explicit.stat_1509134228@T1` | 0.68740 |
| `explicit.stat_3336890334@T2` | -0.64036 |
| `explicit.stat_709508406@T1` | 0.63773 |
| `explicit.stat_1037193709@T1` | -0.62296 |
| `explicit.stat_3336890334@T1` | -0.60441 |
| `explicit.stat_1263695895@T2` | -0.59938 |

### weapon.warstaff — n=11462, R²=-0.3456

intercept: `-11.0257`  ·  log_price: True  ·  ilvl: `0.14773`  ·  n_mods: `-0.20333`  ·  n_top_tier: `0.40182`  ·  corrupted: `0.38340`  ·  n_sockets: `0.13778`  ·  quality: `0.05752`

| stat_id | coef |
|---|---|
| `desecrated.stat_2527686725@T1` | 1.65187 |
| `desecrated.stat_2231156303@T1` | 1.65187 |
| `desecrated.stat_473429811@T1` | -1.39565 |
| `desecrated.stat_3291658075@T1` | -1.39565 |
| `crafted.stat_210067635@T2` | 1.19992 |
| `explicit.stat_1368271171@T1` | -0.82502 |
| `explicit.stat_328541901@T2` | -0.79407 |
| `desecrated.stat_9187492` | 0.76572 |
| `explicit.stat_328541901@T1` | -0.75989 |
| `rune.stat_243313994` | 0.69440 |
| `explicit.stat_1509134228@T1` | 0.67346 |
| `explicit.stat_691932474@T2` | -0.67145 |

### weapon.staff — n=10827, R²=-0.3563

intercept: `-15.7812`  ·  log_price: True  ·  ilvl: `0.20329`  ·  n_mods: `-0.08875`  ·  n_top_tier: `0.39770`  ·  corrupted: `0.72279`  ·  n_sockets: `0.18677`  ·  quality: `0.04320`

| stat_id | coef |
|---|---|
| `explicit.stat_591105508@T1` | 2.33447 |
| `explicit.stat_4226189338@T1` | 2.15718 |
| `explicit.stat_1545858329@T1` | 2.03962 |
| `explicit.stat_124131830@T1` | 1.50858 |
| `explicit.stat_2254480358@T1` | 1.32011 |
| `explicit.stat_1600707273@T1` | 1.30596 |
| `explicit.stat_293638271@T2` | -1.14844 |
| `explicit.stat_2254480358@T2` | 0.87358 |
| `explicit.stat_3962278098@T2` | 0.76276 |
| `explicit.stat_591105508@T2` | 0.67562 |
| `explicit.stat_4226189338@T2` | 0.64234 |
| `explicit.stat_473429811@T2` | -0.63461 |

### weapon.sceptre — n=10657, R²=-0.3368

intercept: `-21.8185`  ·  log_price: True  ·  ilvl: `0.27771`  ·  n_mods: `0.03018`  ·  n_top_tier: `0.20944`  ·  corrupted: `0.19224`  ·  n_sockets: `0.21669`  ·  quality: `0.02682`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.33857 |
| `explicit.stat_3057012405@T1` | 1.42366 |
| `explicit.stat_1263695895@T2` | -1.28331 |
| `explicit.stat_2162097452@T2` | 1.07409 |
| `explicit.stat_1798257884@T2` | 0.97982 |
| `explicit.stat_1263695895@T1` | -0.95504 |
| `explicit.stat_101878827@T2` | 0.83278 |
| `explicit.stat_2854751904@T2` | -0.79365 |
| `explicit.stat_101878827@T1` | 0.79284 |
| `explicit.stat_849987426@T1` | 0.71527 |
| `explicit.stat_1250712710@T2` | 0.67330 |
| `explicit.stat_289128254@T1` | 0.56765 |

### weapon.spear — n=8614, R²=-0.3647

intercept: `-13.7381`  ·  log_price: True  ·  ilvl: `0.18738`  ·  n_mods: `-0.14083`  ·  n_top_tier: `0.55297`  ·  corrupted: `-0.44985`  ·  n_sockets: `0.24656`  ·  quality: `0.07912`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.95413 |
| `explicit.stat_1202301673@T1` | 1.49857 |
| `explicit.stat_1509134228@T1` | 1.38924 |
| `explicit.stat_9187492@T1` | 1.31938 |
| `explicit.stat_1940865751@T2` | -1.08687 |
| `explicit.stat_4080418644@T2` | -0.85050 |
| `explicit.stat_3336890334@T2` | -0.75680 |
| `crafted.stat_3035140377` | 0.74000 |
| `explicit.stat_691932474@T2` | -0.73198 |
| `explicit.stat_748522257@T2` | -0.71579 |
| `explicit.stat_691932474@T1` | -0.71212 |
| `explicit.stat_1037193709@T2` | -0.66951 |

### armour.focus — n=7025, R²=-0.3424

intercept: `-15.1782`  ·  log_price: True  ·  ilvl: `0.19374`  ·  n_mods: `-0.15042`  ·  n_top_tier: `1.01910`  ·  corrupted: `0.11331`  ·  n_sockets: `0.27375`  ·  quality: `0.04823`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 3.44918 |
| `explicit.stat_2923486259@T1` | -1.77718 |
| `explicit.stat_4220027924@T1` | -1.65269 |
| `explicit.stat_4220027924@T2` | -1.32298 |
| `explicit.stat_2923486259@T2` | -1.16913 |
| `explicit.stat_2339757871@T2` | -1.16639 |
| `explicit.stat_2231156303@T1` | -1.13752 |
| `explicit.stat_4015621042@T1` | -1.07047 |
| `explicit.stat_274716455@T1` | -1.06372 |
| `explicit.stat_274716455@T2` | -1.05606 |
| `explicit.stat_1050105434@T2` | -1.04460 |
| `explicit.stat_1050105434@T1` | -1.04455 |

### armour.quiver — n=6577, R²=-0.2897

intercept: `-16.8998`  ·  log_price: True  ·  ilvl: `0.20708`  ·  n_mods: `-0.13238`  ·  n_top_tier: `0.72873`  ·  corrupted: `0.84429`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 6.10868 |
| `explicit.stat_2463230181@T1` | 1.78792 |
| `explicit.stat_681332047@T2` | -1.44919 |
| `explicit.stat_1573130764@T1` | -1.30250 |
| `explicit.stat_681332047@T1` | -1.20137 |
| `explicit.stat_1573130764@T2` | -1.07036 |
| `explicit.stat_2463230181@T2` | 1.01071 |
| `explicit.stat_4067062424@T1` | -0.94924 |
| `explicit.stat_803737631@T1` | -0.89245 |
| `explicit.stat_4067062424@T2` | -0.81152 |
| `explicit.stat_2321178454@T2` | -0.75986 |
| `explicit.stat_803737631@T2` | -0.74061 |

### armour.shield — n=5652, R²=-0.4231

intercept: `-13.9071`  ·  log_price: True  ·  ilvl: `0.18325`  ·  n_mods: `-0.10715`  ·  n_top_tier: `0.76201`  ·  corrupted: `-0.35533`  ·  n_sockets: `0.38974`  ·  quality: `0.05795`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.04396 |
| `explicit.stat_2339757871@T2` | -1.31009 |
| `explicit.stat_3855016469@T1` | -1.24947 |
| `explicit.stat_3321629045@T2` | -1.23441 |
| `explicit.stat_3484657501@T1` | -1.19429 |
| `explicit.stat_2451402625@T1` | -1.11798 |
| `explicit.stat_4095671657@T2` | -1.09043 |
| `explicit.stat_2901986750@T1` | -1.02997 |
| `explicit.stat_3484657501@T2` | -1.00073 |
| `explicit.stat_2481353198@T1` | -0.97214 |
| `explicit.stat_2481353198@T2` | -0.96897 |
| `explicit.stat_328541901@T1` | -0.94274 |

### weapon.twomace — n=5201, R²=-0.4449

intercept: `-10.3756`  ·  log_price: True  ·  ilvl: `0.14175`  ·  n_mods: `-0.21894`  ·  n_top_tier: `0.38497`  ·  corrupted: `0.52172`  ·  n_sockets: `0.13601`  ·  quality: `0.06400`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.23241 |
| `explicit.stat_1037193709@T1` | -1.58834 |
| `explicit.stat_1263695895@T2` | -1.19101 |
| `explicit.stat_3336890334@T1` | -1.15955 |
| `explicit.stat_2694482655@T1` | 1.01104 |
| `explicit.stat_9187492@T1` | -0.85954 |
| `explicit.stat_518292764@T1` | 0.81145 |
| `explicit.stat_691932474@T1` | -0.76498 |
| `explicit.stat_3695891184@T1` | -0.71322 |
| `explicit.stat_3695891184@T2` | -0.71231 |
| `explicit.stat_387439868@T2` | -0.67358 |
| `crafted.stat_3035140377` | 0.57558 |

## Coverage (listings per base)

- … **Sapphire** — 34040 listings (33984 priced) [0.3–3985176410.3 ex]
- … **Emerald** — 33186 listings (33144 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 25452 listings (25421 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 12150 listings (12132 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 10958 listings (10934 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 10602 listings (10577 priced) [1.0–3985176410.3 ex]
- … **Amethyst Ring** — 10497 listings (10486 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 9901 listings (9879 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 9804 listings (9782 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 9386 listings (9373 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 8135 listings (8120 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 7826 listings (7817 priced) [0.3–3985176410.3 ex]
- … **Ruby Ring** — 7742 listings (7733 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7149 listings (7127 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 6769 listings (6762 priced) [0.3–19945827.9 ex]
- … **Unset Ring** — 6694 listings (6675 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 6689 listings (6675 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 6650 listings (6643 priced) [0.3–3985176410.3 ex]
- … **Plate Belt** — 6635 listings (6607 priced) [0.3–398912568423.8 ex]
- … **Ancestral Tiara** — 6543 listings (6514 priced) [0.3–398912568423.8 ex]
- … **Pearl Ring** — 6451 listings (6442 priced) [0.2–275252424.7 ex]
- … **Bloodstone Amulet** — 6442 listings (6432 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6123 listings (6120 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6024 listings (6010 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5879 listings (5869 priced) [0.3–398912568423.8 ex]
