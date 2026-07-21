# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-21T02:27:04+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **698863** (696660 priced in exalted)
- Distinct bases: 1000 · distinct mods: 3313 · mod rows: 3307139
- Sold signals: **24286** sold · 397736 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-21T02:14:03+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×23.22** (median |log error| 3.1449)
- Within ±30% of asking price: **19%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.12** · typical error ×74.07 · ±30% 4% · n=101487
- Premium segment (60ex+): skill **+0.12** · typical error ×377.93 · ±30% 0% · n=67546

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 14896 | ×49.63 | 21% | +0.04 | +0.06 |
| jewel | 14231 | ×54.83 | 22% | +0.02 | +0.03 |
| accessory.amulet | 13400 | ×29.41 | 17% | +0.04 | +0.05 |
| accessory.belt | 9612 | ×20.68 | 21% | +0.03 | +0.05 |
| armour.chest | 9260 | ×14.55 | 23% | +0.08 | +0.10 |
| armour.helmet | 9080 | ×24.78 | 19% | +0.08 | +0.10 |
| armour.boots | 8396 | ×24.07 | 21% | +0.09 | +0.12 |
| armour.gloves | 8240 | ×32.33 | 14% | +0.08 | +0.10 |
| other | 8147 | ×1.96 | 42% | +0.11 | +0.18 |
| weapon.wand | 4887 | ×39.16 | 16% | +0.10 | +0.11 |
| weapon.bow | 3842 | ×27.27 | 12% | +0.15 | +0.16 |
| weapon.crossbow | 3638 | ×22.97 | 17% | +0.10 | +0.15 |
| weapon.warstaff | 2517 | ×14.12 | 7% | +0.22 | +0.21 |
| weapon.staff | 2383 | ×15.55 | 6% | +0.12 | +0.12 |
| weapon.sceptre | 2348 | ×20.20 | 4% | +0.09 | +0.09 |
| weapon.spear | 1873 | ×13.12 | 7% | +0.15 | +0.15 |
| armour.focus | 1549 | ×13.28 | 7% | +0.12 | +0.13 |
| armour.quiver | 1465 | ×17.75 | 7% | +0.12 | +0.13 |
| armour.shield | 1204 | ×9.81 | 7% | +0.10 | +0.12 |
| flask.charm | 1192 | ×10.00 | 28% | -0.01 | -0.00 |
| weapon.twomace | 1115 | ×9.47 | 8% | +0.10 | +0.11 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=78085, R²=-1.8806

intercept: `-0.0813`  ·  log_price: True  ·  ilvl: `0.00101`  ·  n_mods: `1.02329`  ·  n_top_tier: `-0.91706`  ·  corrupted: `1.06309`  ·  quality: `0.22528`

| stat_id | coef |
|---|---|
| `explicit.stat_3485067555@T1` | 3.79605 |
| `explicit.stat_1604736568@T1` | -2.34634 |
| `explicit.stat_1604736568` | 2.24349 |
| `explicit.stat_3473929743@T1` | -1.56256 |
| `explicit.stat_3174700878@T1` | 1.17170 |
| `explicit.stat_2194114101@T1` | -0.94347 |
| `explicit.stat_681332047@T1` | -0.90622 |
| `explicit.stat_3556824919@T1` | 0.70104 |
| `explicit.stat_587431675@T1` | -0.69178 |
| `explicit.stat_274716455@T1` | -0.63448 |
| `explicit.stat_4045894391@T1` | -0.61721 |
| `explicit.stat_3091578504@T1` | -0.53906 |

### accessory.ring — n=67950, R²=-2.019

intercept: `3.4216`  ·  log_price: True  ·  ilvl: `-0.04271`  ·  n_mods: `0.00128`  ·  n_top_tier: `0.94725`  ·  corrupted: `0.01148`  ·  n_sockets: `1.92172`  ·  quality: `0.01868`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -0.98525 |
| `explicit.stat_803737631@T1` | -0.97410 |
| `explicit.stat_4080418644@T1` | -0.96938 |
| `explicit.stat_2231156303@T1` | -0.96733 |
| `explicit.stat_3325883026@T1` | -0.96641 |
| `explicit.stat_2891184298@T2` | -0.96513 |
| `explicit.stat_4220027924@T2` | -0.96291 |
| `explicit.stat_736967255@T2` | -0.96195 |
| `explicit.stat_2923486259@T2` | -0.96135 |
| `explicit.stat_1573130764@T2` | -0.95951 |
| `explicit.stat_3291658075@T2` | -0.95832 |
| `explicit.stat_3917489142@T2` | -0.95694 |

### other — n=66497, R²=-0.6601

intercept: `1.6092`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.07266`  ·  n_top_tier: `0.27392`  ·  corrupted: `0.04961`  ·  n_sockets: `-0.00003`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.35918 |
| `explicit.stat_3299347043@T1` | -0.26155 |
| `implicit.stat_2219129443` | 0.22298 |
| `implicit.stat_718638445` | 0.21799 |
| `implicit.stat_3182714256` | 0.21799 |
| `explicit.stat_3917489142@T1` | -0.16750 |
| `explicit.stat_2974417149@T1` | 0.12991 |
| `implicit.stat_958696139` | -0.07264 |
| `explicit.stat_789117908@T1` | -0.06458 |
| `implicit.stat_3879011313` | 0.06444 |
| `implicit.stat_1416292992` | -0.04844 |
| `pseudo.total_ele_res>=40` | -0.04346 |

### accessory.amulet — n=61092, R²=-2.1346

intercept: `3.4393`  ·  log_price: True  ·  ilvl: `-0.04337`  ·  n_mods: `-0.02329`  ·  n_top_tier: `1.20650`  ·  corrupted: `0.13540`  ·  n_sockets: `-0.11362`  ·  quality: `0.05382`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.71736 |
| `explicit.stat_3299347043@T2` | -1.58241 |
| `explicit.stat_587431675@T2` | -1.35722 |
| `explicit.stat_2866361420@T2` | -1.32410 |
| `explicit.stat_2866361420@T1` | -1.31143 |
| `explicit.stat_2974417149@T1` | -1.30932 |
| `explicit.stat_803737631@T1` | -1.30670 |
| `explicit.stat_2974417149@T2` | -1.28149 |
| `explicit.stat_1050105434@T2` | -1.26164 |
| `explicit.stat_4080418644@T1` | -1.25893 |
| `explicit.stat_1050105434@T1` | -1.25161 |
| `explicit.stat_803737631@T2` | -1.25155 |

### accessory.belt — n=43949, R²=-1.8787

intercept: `3.0968`  ·  log_price: True  ·  ilvl: `-0.03718`  ·  n_mods: `-0.01655`  ·  n_top_tier: `0.33674`  ·  corrupted: `1.19669`  ·  n_sockets: `1.48341`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 1.16465 |
| `explicit.stat_51994685@T1` | -0.35619 |
| `explicit.stat_2881298780@T1` | -0.35604 |
| `explicit.stat_3299347043@T2` | -0.35447 |
| `explicit.stat_809229260@T2` | -0.35181 |
| `explicit.stat_3299347043@T1` | -0.35048 |
| `explicit.stat_915769802@T1` | -0.35046 |
| `explicit.stat_3325883026@T1` | -0.34886 |
| `explicit.stat_3372524247@T2` | -0.34491 |
| `explicit.stat_1570770415@T2` | -0.34461 |
| `explicit.stat_4220027924@T2` | -0.34259 |
| `explicit.stat_1389754388@T1` | -0.33718 |

### armour.chest — n=43620, R²=-1.8074

intercept: `3.1222`  ·  log_price: True  ·  ilvl: `-0.03865`  ·  n_mods: `-0.01094`  ·  n_top_tier: `0.36190`  ·  corrupted: `0.26293`  ·  n_sockets: `0.01641`  ·  quality: `0.07003`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.67734 |
| `explicit.stat_986397080@T2` | -0.43870 |
| `explicit.stat_986397080@T1` | -0.42695 |
| `explicit.stat_915769802@T2` | -0.39228 |
| `explicit.stat_3484657501@T1` | -0.39025 |
| `explicit.stat_4080418644@T2` | -0.38962 |
| `explicit.stat_4080418644@T1` | -0.38928 |
| `explicit.stat_1692879867@T2` | -0.38663 |
| `explicit.stat_915769802@T1` | -0.38438 |
| `explicit.stat_2339757871@T2` | -0.37459 |
| `explicit.stat_3301100256@T2` | -0.37221 |
| `explicit.stat_1062208444@T2` | -0.37053 |

### armour.helmet — n=42402, R²=-1.7856

intercept: `3.1965`  ·  log_price: True  ·  ilvl: `-0.04044`  ·  n_mods: `-0.01445`  ·  n_top_tier: `0.59961`  ·  corrupted: `0.53553`  ·  n_sockets: `0.03940`  ·  quality: `0.06864`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -4.52460 |
| `explicit.stat_1263695895@T1` | -0.89701 |
| `explicit.stat_3917489142@T2` | -0.77804 |
| `explicit.stat_1263695895@T2` | -0.73771 |
| `explicit.stat_2162097452@T2` | -0.73539 |
| `explicit.stat_3917489142@T1` | -0.70596 |
| `explicit.stat_4015621042@T2` | -0.67954 |
| `explicit.stat_4052037485@T2` | -0.65876 |
| `explicit.stat_53045048@T1` | -0.64111 |
| `explicit.stat_3321629045@T2` | -0.63702 |
| `explicit.stat_1999113824@T1` | -0.63520 |
| `explicit.stat_803737631@T1` | -0.63424 |

### armour.boots — n=39287, R²=-1.7654

intercept: `3.3971`  ·  log_price: True  ·  ilvl: `-0.04194`  ·  n_mods: `-0.01649`  ·  n_top_tier: `0.42827`  ·  corrupted: `0.03586`  ·  n_sockets: `0.03975`  ·  quality: `0.06918`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.80906 |
| `crafted.stat_3917489142@T1` | 1.51655 |
| `explicit.stat_2339757871@T1` | -1.27758 |
| `explicit.stat_2923486259@T1` | 0.65467 |
| `explicit.stat_3917489142@T2` | -0.52282 |
| `explicit.stat_3299347043@T1` | -0.51485 |
| `explicit.stat_2923486259@T2` | -0.48792 |
| `explicit.stat_328541901@T2` | -0.46659 |
| `explicit.stat_1671376347@T2` | -0.46409 |
| `explicit.stat_2160282525@T1` | -0.45968 |
| `explicit.stat_1874553720@T1` | -0.45882 |
| `explicit.stat_3321629045@T2` | -0.45578 |

### armour.gloves — n=38287, R²=-1.7169

intercept: `3.6861`  ·  log_price: True  ·  ilvl: `-0.04842`  ·  n_mods: `-0.00130`  ·  n_top_tier: `0.73483`  ·  corrupted: `-0.06104`  ·  n_sockets: `0.15819`  ·  quality: `0.05730`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 2.09162 |
| `rune.stat_201332984` | 1.04174 |
| `explicit.stat_2923486259@T2` | -0.98658 |
| `explicit.stat_4052037485@T1` | -0.96533 |
| `explicit.stat_4052037485@T2` | -0.95014 |
| `explicit.stat_2923486259@T1` | -0.93621 |
| `explicit.stat_3484657501@T2` | -0.93568 |
| `explicit.stat_9187492@T2` | -0.93190 |
| `explicit.stat_4015621042@T2` | -0.91627 |
| `explicit.stat_3321629045@T2` | -0.88329 |
| `explicit.stat_3484657501@T1` | -0.87928 |
| `explicit.stat_803737631@T2` | -0.86640 |

### weapon.wand — n=22753, R²=-2.035

intercept: `3.9719`  ·  log_price: True  ·  ilvl: `-0.04929`  ·  n_mods: `-0.04647`  ·  n_top_tier: `0.34139`  ·  corrupted: `0.00770`  ·  n_sockets: `0.02847`  ·  quality: `0.04172`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -3.96444 |
| `explicit.stat_1545858329@T1` | 3.05742 |
| `explicit.stat_2254480358@T1` | 2.63451 |
| `explicit.stat_124131830@T1` | 2.19634 |
| `explicit.stat_591105508@T1` | 2.01884 |
| `explicit.stat_736967255@T2` | 1.83792 |
| `explicit.stat_4226189338@T1` | 1.82989 |
| `explicit.stat_2254480358@T2` | 1.30147 |
| `crafted.stat_124131830` | 1.23399 |
| `explicit.stat_4226189338@T2` | 1.01653 |
| `explicit.stat_1545858329@T2` | 0.73419 |
| `explicit.stat_1263695895@T2` | -0.65846 |

### flask.charm — n=19525, R²=-0.6533

intercept: `0.1037`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `1.60927`  ·  corrupted: `1.51274`  ·  quality: `0.00613`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.78263 |
| `explicit.stat_1056492907` | 2.67664 |
| `explicit.stat_3246948616` | 1.60938 |
| `explicit.stat_1120862500@T2` | -1.60930 |
| `explicit.stat_828533480@T2` | -1.60929 |
| `explicit.stat_1873752457@T2` | -1.60927 |
| `explicit.stat_3196823591@T2` | -1.60922 |
| `explicit.stat_2676834156@T2` | -1.60922 |
| `explicit.stat_2365392475@T2` | -1.60921 |
| `explicit.stat_388617051@T2` | -1.60802 |
| `explicit.stat_2541588185@T2` | -1.60418 |
| `explicit.stat_828533480@T1` | -1.60234 |

### weapon.bow — n=18137, R²=-1.8158

intercept: `3.9426`  ·  log_price: True  ·  ilvl: `-0.04741`  ·  n_mods: `-0.07213`  ·  n_top_tier: `0.76448`  ·  corrupted: `0.74067`  ·  n_sockets: `0.03411`  ·  quality: `0.03126`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 3.06114 |
| `desecrated.stat_210067635@T1` | -1.82380 |
| `explicit.stat_1263695895@T1` | -1.28103 |
| `crafted.stat_3035140377` | 1.24437 |
| `explicit.stat_1263695895@T2` | -1.14290 |
| `explicit.stat_709508406@T1` | 1.10038 |
| `explicit.stat_1368271171@T2` | -0.83394 |
| `explicit.stat_210067635@T2` | -0.82730 |
| `explicit.stat_3695891184@T2` | -0.82718 |
| `explicit.stat_2463230181@T2` | -0.82401 |
| `explicit.stat_3639275092@T2` | -0.81969 |
| `explicit.stat_821021828@T2` | -0.81386 |

### weapon.crossbow — n=17025, R²=-1.8404

intercept: `3.8661`  ·  log_price: True  ·  ilvl: `-0.04727`  ·  n_mods: `-0.05430`  ·  n_top_tier: `0.32260`  ·  corrupted: `0.05690`  ·  n_sockets: `0.04286`  ·  quality: `0.02689`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.71207 |
| `explicit.stat_1202301673@T1` | 1.54516 |
| `explicit.stat_1980802737` | 1.39030 |
| `explicit.stat_2250681686@T2` | -1.26712 |
| `explicit.stat_1509134228@T1` | 1.06763 |
| `explicit.stat_2250681686` | 1.04766 |
| `crafted.stat_3035140377` | 0.85212 |
| `explicit.stat_387439868@T1` | 0.62039 |
| `explicit.stat_518292764@T1` | 0.56097 |
| `explicit.stat_1263695895@T2` | -0.53247 |
| `explicit.stat_2694482655@T2` | 0.52078 |
| `explicit.stat_3336890334@T2` | -0.47889 |

### weapon.warstaff — n=11855, R²=-0.3347

intercept: `-10.5818`  ·  log_price: True  ·  ilvl: `0.14242`  ·  n_mods: `-0.21651`  ·  n_top_tier: `0.43491`  ·  corrupted: `0.22983`  ·  n_sockets: `0.10954`  ·  quality: `0.05855`

| stat_id | coef |
|---|---|
| `explicit.stat_328541901@T2` | -1.12175 |
| `crafted.stat_210067635@T2` | 1.08581 |
| `explicit.stat_328541901@T1` | -0.90257 |
| `desecrated.stat_2527686725@T1` | 0.88275 |
| `desecrated.stat_2231156303@T1` | 0.88275 |
| `rune.stat_243313994` | 0.83424 |
| `desecrated.stat_9187492` | 0.79955 |
| `explicit.stat_691932474@T2` | -0.63314 |
| `explicit.stat_1037193709@T1` | 0.63126 |
| `explicit.stat_1368271171@T1` | -0.61216 |
| `explicit.stat_821021828@T2` | -0.59470 |
| `explicit.stat_2694482655@T1` | 0.56693 |

### weapon.staff — n=11248, R²=-0.3577

intercept: `-15.6555`  ·  log_price: True  ·  ilvl: `0.20052`  ·  n_mods: `-0.08496`  ·  n_top_tier: `0.48176`  ·  corrupted: `0.72015`  ·  n_sockets: `0.16574`  ·  quality: `0.03369`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.09586 |
| `explicit.stat_591105508@T1` | 1.55363 |
| `explicit.stat_1600707273@T1` | 1.54530 |
| `explicit.stat_1545858329@T1` | 1.46101 |
| `explicit.stat_124131830@T1` | 1.43883 |
| `explicit.stat_293638271@T2` | -1.06091 |
| `explicit.stat_2254480358@T1` | 1.00694 |
| `rune.stat_124131830` | 0.97523 |
| `explicit.stat_3962278098@T2` | 0.76807 |
| `explicit.stat_473429811@T2` | -0.73182 |
| `explicit.stat_1263695895@T2` | -0.68550 |
| `crafted.stat_124131830` | 0.60042 |

### weapon.sceptre — n=11030, R²=-0.3406

intercept: `-21.1820`  ·  log_price: True  ·  ilvl: `0.26812`  ·  n_mods: `0.02843`  ·  n_top_tier: `0.10202`  ·  corrupted: `0.18820`  ·  n_sockets: `0.23438`  ·  quality: `0.03085`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.76005 |
| `explicit.stat_2162097452@T2` | 1.45382 |
| `explicit.stat_1263695895@T2` | -0.99848 |
| `explicit.stat_3057012405@T1` | 0.97275 |
| `explicit.stat_101878827@T2` | 0.95923 |
| `explicit.stat_1798257884@T2` | 0.90698 |
| `explicit.stat_849987426@T1` | 0.89010 |
| `explicit.stat_101878827@T1` | 0.86714 |
| `explicit.stat_2854751904@T2` | -0.83066 |
| `explicit.stat_1263695895@T1` | -0.80494 |
| `explicit.stat_2347036682@T1` | 0.60018 |
| `explicit.stat_1998951374@T1` | 0.57794 |

### weapon.spear — n=8943, R²=-0.3783

intercept: `-13.1852`  ·  log_price: True  ·  ilvl: `0.17965`  ·  n_mods: `-0.13246`  ·  n_top_tier: `0.58024`  ·  corrupted: `-0.51859`  ·  n_sockets: `0.17220`  ·  quality: `0.07321`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -3.83398 |
| `crafted.stat_210067635@T2` | -3.35437 |
| `explicit.stat_1202301673@T1` | 1.29562 |
| `explicit.stat_4080418644@T2` | -1.06628 |
| `crafted.stat_3035140377` | 0.98684 |
| `explicit.stat_9187492@T1` | 0.96729 |
| `explicit.stat_1940865751@T2` | -0.94776 |
| `desecrated.stat_210067635@T1` | -0.84480 |
| `explicit.stat_3336890334@T2` | -0.81520 |
| `explicit.stat_3261801346@T1` | -0.75514 |
| `explicit.stat_691932474@T2` | -0.74804 |
| `explicit.stat_4080418644@T1` | -0.71676 |

### armour.focus — n=7305, R²=-0.3349

intercept: `-16.4676`  ·  log_price: True  ·  ilvl: `0.20779`  ·  n_mods: `-0.09615`  ·  n_top_tier: `0.87177`  ·  corrupted: `0.04575`  ·  n_sockets: `0.35083`  ·  quality: `0.03147`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 1.64366 |
| `explicit.stat_2923486259@T1` | -1.55760 |
| `explicit.stat_4220027924@T1` | -1.35196 |
| `explicit.stat_2231156303@T1` | -1.08195 |
| `explicit.stat_4015621042@T1` | -1.06432 |
| `explicit.stat_2768835289@T1` | -1.04651 |
| `explicit.stat_4220027924@T2` | -1.04200 |
| `explicit.stat_2923486259@T2` | -1.02854 |
| `explicit.stat_2231156303@T2` | -0.96042 |
| `explicit.stat_2339757871@T2` | -0.93168 |
| `explicit.stat_737908626@T2` | -0.92360 |
| `explicit.stat_1050105434@T2` | -0.90423 |

### armour.quiver — n=6805, R²=-0.2934

intercept: `-17.6949`  ·  log_price: True  ·  ilvl: `0.20993`  ·  n_mods: `-0.04156`  ·  n_top_tier: `0.69841`  ·  corrupted: `0.95063`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.85727 |
| `explicit.stat_681332047@T2` | -1.64405 |
| `explicit.stat_681332047@T1` | -1.39577 |
| `explicit.stat_1573130764@T2` | -1.11310 |
| `explicit.stat_1573130764@T1` | -1.05320 |
| `explicit.stat_4067062424@T1` | -0.77370 |
| `explicit.stat_2194114101@T2` | -0.76902 |
| `explicit.stat_803737631@T1` | -0.70780 |
| `explicit.stat_3261801346@T1` | -0.61063 |
| `explicit.stat_803737631@T2` | -0.58384 |
| `explicit.stat_2321178454@T2` | -0.56915 |
| `explicit.stat_4067062424@T2` | -0.51894 |

### armour.shield — n=5860, R²=-0.4366

intercept: `-12.5328`  ·  log_price: True  ·  ilvl: `0.16625`  ·  n_mods: `-0.10765`  ·  n_top_tier: `0.56689`  ·  corrupted: `-0.42226`  ·  n_sockets: `0.40407`  ·  quality: `0.05844`

| stat_id | coef |
|---|---|
| `explicit.stat_3855016469@T1` | -1.29607 |
| `explicit.stat_4095671657@T1` | -1.19351 |
| `explicit.stat_4095671657@T2` | -1.11729 |
| `explicit.stat_2339757871@T1` | -1.07963 |
| `explicit.stat_2901986750@T1` | -1.06635 |
| `explicit.stat_3321629045@T2` | -0.94580 |
| `explicit.stat_328541901@T1` | -0.94143 |
| `explicit.stat_1011760251@T1` | -0.83804 |
| `explicit.stat_2451402625@T1` | -0.80920 |
| `explicit.stat_3033371881@T2` | -0.80911 |
| `explicit.stat_2481353198@T2` | -0.80741 |
| `explicit.stat_2481353198@T1` | -0.80632 |

### weapon.twomace — n=5359, R²=-0.4498

intercept: `-11.2288`  ·  log_price: True  ·  ilvl: `0.14961`  ·  n_mods: `-0.19382`  ·  n_top_tier: `0.39669`  ·  corrupted: `0.63915`  ·  n_sockets: `0.12101`  ·  quality: `0.06682`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.20918 |
| `explicit.stat_1263695895@T2` | -1.52050 |
| `explicit.stat_1037193709@T1` | -1.50356 |
| `explicit.stat_3336890334@T1` | -1.36193 |
| `explicit.stat_2694482655@T1` | 1.12648 |
| `explicit.stat_1263695895@T1` | -0.91859 |
| `explicit.stat_9187492@T1` | -0.80032 |
| `explicit.stat_3695891184@T1` | -0.78589 |
| `explicit.stat_3695891184@T2` | -0.70946 |
| `explicit.stat_518292764@T1` | 0.60423 |
| `explicit.stat_691932474@T1` | -0.58239 |
| `explicit.stat_387439868@T2` | -0.56669 |

## Coverage (listings per base)

- … **Sapphire** — 35905 listings (35849 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 35008 listings (34965 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 26806 listings (26775 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 12571 listings (12553 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 11436 listings (11412 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 11075 listings (11050 priced) [0.3–3985176410.3 ex]
- … **Amethyst Ring** — 10972 listings (10960 priced) [0.2–3985176410.3 ex]
- … **Gold Amulet** — 10320 listings (10295 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 10248 listings (10225 priced) [0.2–3985176410.3 ex]
- … **Stellar Amulet** — 9731 listings (9718 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 8520 listings (8505 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 8181 listings (8172 priced) [0.3–3985176410.3 ex]
- … **Ruby Ring** — 8115 listings (8106 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7325 listings (7302 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 7032 listings (7025 priced) [0.3–3985176410.3 ex]
- … **Unset Ring** — 7015 listings (6996 priced) [0.2–39887666593.4 ex]
- … **Jade Amulet** — 6967 listings (6952 priced) [0.3–4275054.0 ex]
- … **Amber Amulet** — 6900 listings (6893 priced) [0.3–3985176410.3 ex]
- … **Plate Belt** — 6852 listings (6824 priced) [0.3–398912568423.8 ex]
- … **Ancestral Tiara** — 6774 listings (6745 priced) [0.3–398912568423.8 ex]
- … **Pearl Ring** — 6755 listings (6746 priced) [0.2–275252424.7 ex]
- … **Bloodstone Amulet** — 6697 listings (6687 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6357 listings (6354 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6249 listings (6235 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 6085 listings (6074 priced) [0.3–398912568423.8 ex]
