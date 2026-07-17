# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-17T16:41:56+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **586659** (584963 priced in exalted)
- Distinct bases: 988 · distinct mods: 3212 · mod rows: 2777598
- Sold signals: **25274** sold · 332630 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-17T16:33:54+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×25.42** (median |log error| 3.2357)
- Within ±30% of asking price: **14%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 80% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.14** · typical error ×61.13 · ±30% 5% · n=85073
- Premium segment (60ex+): skill **+0.14** · typical error ×246.14 · ±30% 0% · n=57538

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 12056 | ×55.82 | 21% | +0.03 | +0.04 |
| jewel | 11388 | ×10.86 | 5% | +0.07 | +0.10 |
| accessory.amulet | 10993 | ×50.67 | 20% | +0.04 | +0.04 |
| accessory.belt | 8152 | ×16.29 | 4% | +0.03 | +0.04 |
| armour.chest | 7870 | ×20.78 | 12% | +0.09 | +0.12 |
| armour.helmet | 7729 | ×18.19 | 6% | +0.10 | +0.12 |
| armour.boots | 7202 | ×36.97 | 16% | +0.11 | +0.13 |
| armour.gloves | 7016 | ×33.66 | 8% | +0.12 | +0.14 |
| other | 6748 | ×5.99 | 40% | +0.09 | +0.15 |
| weapon.wand | 4338 | ×47.85 | 16% | +0.07 | +0.09 |
| weapon.bow | 3431 | ×30.37 | 14% | +0.14 | +0.16 |
| weapon.crossbow | 3218 | ×33.57 | 16% | +0.09 | +0.12 |
| weapon.warstaff | 2046 | ×30.34 | 8% | +0.16 | +0.14 |
| weapon.staff | 1949 | ×49.67 | 6% | +0.13 | +0.12 |
| weapon.sceptre | 1886 | ×35.49 | 5% | +0.18 | +0.19 |
| weapon.spear | 1534 | ×41.05 | 13% | +0.09 | +0.09 |
| armour.focus | 1281 | ×23.30 | 6% | +0.15 | +0.16 |
| armour.quiver | 1238 | ×27.43 | 7% | +0.14 | +0.15 |
| flask.charm | 1051 | ×15.00 | 32% | +0.05 | +0.08 |
| armour.shield | 1009 | ×18.82 | 7% | +0.05 | +0.08 |
| weapon.twomace | 923 | ×9.73 | 11% | +0.08 | +0.07 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=62119, R²=-0.95

intercept: `-1.8494`  ·  log_price: True  ·  ilvl: `0.02557`  ·  n_mods: `0.86535`  ·  n_top_tier: `-0.33892`  ·  corrupted: `0.28160`  ·  quality: `0.22482`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.59312 |
| `explicit.stat_3374165039@T1` | -2.23466 |
| `explicit.stat_3485067555@T1` | 2.22062 |
| `explicit.stat_1869147066@T1` | -2.16572 |
| `explicit.stat_1805182458@T1` | -2.16024 |
| `explicit.stat_2301718443@T1` | 2.13383 |
| `explicit.stat_239367161@T1` | -1.46724 |
| `explicit.stat_3166958180@T1` | -1.44400 |
| `explicit.stat_4147897060@T1` | -1.39471 |
| `explicit.stat_491450213@T1` | 1.37131 |
| `explicit.stat_3787460122@T1` | 1.33074 |
| `explicit.stat_3119612865@T1` | -1.25957 |

### other — n=56187, R²=-0.4952

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00003`  ·  n_top_tier: `0.62767`  ·  corrupted: `0.22684`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_789117908@T1` | -0.79067 |
| `explicit.stat_2106365538@T1` | -0.77600 |
| `explicit.stat_3299347043@T1` | 0.43832 |
| `explicit.stat_1050105434@T1` | -0.34239 |
| `explicit.stat_2974417149@T1` | 0.27029 |
| `explicit.stat_2482852589@T1` | -0.23898 |
| `implicit.stat_3879011313` | 0.23026 |
| `implicit.stat_2219129443` | 0.23026 |
| `implicit.stat_4041853756` | 0.23026 |
| `explicit.stat_3291658075@T1` | 0.19349 |
| `explicit.stat_1589917703@T1` | 0.14886 |
| `implicit.stat_2923486259` | -0.12940 |

### accessory.ring — n=55181, R²=-2.0338

intercept: `3.3437`  ·  log_price: True  ·  ilvl: `-0.04133`  ·  n_mods: `-0.00033`  ·  n_top_tier: `0.98358`  ·  corrupted: `0.02127`  ·  n_sockets: `2.19777`  ·  quality: `0.07535`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -1.02032 |
| `explicit.stat_1573130764@T1` | -1.01202 |
| `explicit.stat_1368271171@T2` | -1.00386 |
| `explicit.stat_1573130764@T2` | -1.00238 |
| `explicit.stat_803737631@T1` | -1.00233 |
| `explicit.stat_2231156303@T2` | -1.00222 |
| `explicit.stat_1263695895@T2` | -1.00198 |
| `explicit.stat_2144192055@T1` | -1.00194 |
| `explicit.stat_4220027924@T2` | -1.00184 |
| `explicit.stat_1368271171@T1` | -0.99866 |
| `explicit.stat_1263695895@T1` | -0.99819 |
| `explicit.stat_3325883026@T1` | -0.99689 |

### accessory.amulet — n=50335, R²=-2.1681

intercept: `3.6214`  ·  log_price: True  ·  ilvl: `-0.04418`  ·  n_mods: `-0.01846`  ·  n_top_tier: `1.07846`  ·  corrupted: `0.06501`  ·  n_sockets: `-0.13804`  ·  quality: `0.05780`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.26898 |
| `explicit.stat_3299347043@T2` | -1.15700 |
| `explicit.stat_472520716@T2` | -1.14276 |
| `explicit.stat_803737631@T1` | -1.13925 |
| `explicit.stat_2866361420@T2` | -1.13247 |
| `explicit.stat_2974417149@T1` | -1.13031 |
| `explicit.stat_2974417149@T2` | -1.12978 |
| `explicit.stat_587431675@T2` | -1.12582 |
| `explicit.stat_1050105434@T2` | -1.12506 |
| `explicit.stat_803737631@T2` | -1.11782 |
| `explicit.stat_2866361420@T1` | -1.11131 |
| `explicit.stat_1671376347@T2` | -1.10305 |

### accessory.belt — n=37509, R²=-0.8443

intercept: `6.7683`  ·  log_price: True  ·  ilvl: `-0.06008`  ·  n_mods: `-0.38685`  ·  n_top_tier: `0.75460`  ·  corrupted: `0.96514`  ·  n_sockets: `0.06424`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.80129 |
| `explicit.stat_3299347043@T2` | -1.41918 |
| `implicit.stat_731781020` | -1.22229 |
| `explicit.stat_2881298780@T1` | -1.19055 |
| `explicit.stat_644456512@T1` | -1.13743 |
| `explicit.stat_809229260@T2` | -1.00372 |
| `explicit.stat_4220027924@T2` | -0.95918 |
| `explicit.stat_1389754388@T1` | -0.91102 |
| `explicit.stat_51994685@T1` | -0.88828 |
| `explicit.stat_809229260@T1` | -0.85919 |
| `explicit.stat_3372524247@T2` | -0.81745 |
| `explicit.stat_915769802@T2` | -0.78588 |

### armour.chest — n=37254, R²=-1.4595

intercept: `4.0186`  ·  log_price: True  ·  ilvl: `-0.04804`  ·  n_mods: `-0.06256`  ·  n_top_tier: `0.53125`  ·  corrupted: `0.18403`  ·  n_sockets: `0.11833`  ·  quality: `0.06048`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.86016 |
| `explicit.stat_3981240776@T1` | 1.04748 |
| `explicit.stat_3033371881@T1` | 0.81607 |
| `explicit.stat_986397080@T2` | -0.78150 |
| `explicit.stat_3484657501@T1` | -0.69085 |
| `explicit.stat_2339757871@T2` | -0.67917 |
| `explicit.stat_986397080@T1` | -0.67037 |
| `explicit.stat_124859000@T1` | -0.63436 |
| `explicit.stat_1692879867@T1` | -0.61334 |
| `explicit.stat_915769802@T2` | -0.61001 |
| `explicit.stat_1692879867@T2` | -0.60594 |
| `explicit.stat_3301100256@T2` | -0.59307 |

### armour.helmet — n=36180, R²=-1.0683

intercept: `3.8748`  ·  log_price: True  ·  ilvl: `-0.04786`  ·  n_mods: `-0.09970`  ·  n_top_tier: `0.46666`  ·  corrupted: `0.70160`  ·  n_sockets: `0.25988`  ·  quality: `0.04387`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.84199 |
| `explicit.stat_3917489142@T2` | -1.15482 |
| `explicit.stat_1999113824@T1` | -0.96500 |
| `explicit.stat_1263695895@T1` | -0.80197 |
| `explicit.stat_3917489142@T1` | -0.79920 |
| `explicit.stat_4052037485@T2` | -0.74005 |
| `explicit.stat_3321629045@T2` | -0.72248 |
| `explicit.stat_1999113824@T2` | -0.69974 |
| `explicit.stat_2162097452@T2` | -0.67425 |
| `explicit.stat_803737631@T2` | -0.65215 |
| `explicit.stat_1050105434@T2` | -0.59913 |
| `explicit.stat_587431675@T2` | -0.56607 |

### armour.boots — n=33822, R²=-1.4997

intercept: `3.9867`  ·  log_price: True  ·  ilvl: `-0.04860`  ·  n_mods: `-0.04027`  ·  n_top_tier: `0.62914`  ·  corrupted: `0.03128`  ·  n_sockets: `0.06134`  ·  quality: `0.05192`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 3.32357 |
| `explicit.stat_2250533757@T1` | 1.49402 |
| `explicit.stat_3299347043@T1` | -1.03699 |
| `explicit.stat_3917489142@T2` | -0.97540 |
| `explicit.stat_3917489142@T1` | -0.83025 |
| `explicit.stat_2339757871@T1` | -0.77191 |
| `explicit.stat_2923486259@T2` | -0.75364 |
| `explicit.stat_3484657501@T2` | -0.73912 |
| `explicit.stat_2160282525@T1` | -0.73446 |
| `explicit.stat_1999113824@T2` | -0.73227 |
| `explicit.stat_1062208444@T2` | -0.72896 |
| `explicit.stat_4052037485@T2` | -0.71324 |

### armour.gloves — n=32902, R²=-1.3183

intercept: `3.8984`  ·  log_price: True  ·  ilvl: `-0.05031`  ·  n_mods: `-0.04826`  ·  n_top_tier: `0.66234`  ·  corrupted: `0.09295`  ·  n_sockets: `0.20699`  ·  quality: `0.03883`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 1.95522 |
| `explicit.stat_3484657501@T2` | -1.10017 |
| `explicit.stat_3321629045@T2` | -1.08670 |
| `rune.stat_836936635` | 1.07295 |
| `explicit.stat_2923486259@T1` | -1.04441 |
| `explicit.stat_3484657501@T1` | -0.98367 |
| `explicit.stat_3321629045@T1` | -0.91519 |
| `explicit.stat_4052037485@T1` | -0.88201 |
| `explicit.stat_803737631@T2` | -0.87568 |
| `explicit.stat_803737631@T1` | -0.86337 |
| `explicit.stat_1999113824@T2` | -0.85574 |
| `explicit.stat_1754445556@T2` | -0.79758 |

### weapon.wand — n=20329, R²=-2.14

intercept: `3.5655`  ·  log_price: True  ·  ilvl: `-0.04402`  ·  n_mods: `-0.03627`  ·  n_top_tier: `0.50260`  ·  corrupted: `0.10500`  ·  n_sockets: `0.09056`  ·  quality: `0.00858`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.75633 |
| `rune.stat_124131830` | -2.43748 |
| `explicit.stat_2254480358@T1` | 2.22308 |
| `explicit.stat_4226189338@T1` | 1.94218 |
| `explicit.stat_124131830@T1` | 1.82896 |
| `explicit.stat_591105508@T1` | 1.80133 |
| `explicit.stat_736967255@T2` | 1.60696 |
| `explicit.stat_1600707273@T1` | 1.29221 |
| `crafted.stat_124131830` | 1.25218 |
| `explicit.stat_4226189338@T2` | 0.98248 |
| `explicit.stat_2254480358@T2` | 0.89842 |
| `explicit.stat_1600707273@T2` | -0.72472 |

### weapon.bow — n=16303, R²=-1.8377

intercept: `3.7898`  ·  log_price: True  ·  ilvl: `-0.04412`  ·  n_mods: `-0.08869`  ·  n_top_tier: `0.61717`  ·  corrupted: `0.35484`  ·  n_sockets: `0.04502`  ·  quality: `0.03228`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -2.11092 |
| `desecrated.stat_210067635@T1` | -1.64774 |
| `explicit.stat_1202301673@T1` | 1.43759 |
| `crafted.stat_3035140377` | 1.41207 |
| `explicit.stat_2463230181@T1` | -1.12806 |
| `explicit.stat_3336890334@T1` | 1.06906 |
| `explicit.stat_1263695895@T1` | -1.02930 |
| `explicit.stat_1263695895@T2` | -0.98436 |
| `explicit.stat_518292764@T2` | -0.89489 |
| `explicit.stat_2463230181@T2` | -0.80089 |
| `explicit.stat_3695891184@T1` | -0.79546 |
| `explicit.stat_3695891184@T2` | -0.77187 |

### flask.charm — n=15736, R²=-0.5807

intercept: `0.0714`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `2.73851`  ·  corrupted: `1.60925`  ·  quality: `0.00009`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.85936 |
| `explicit.stat_1056492907` | 3.00439 |
| `explicit.stat_828533480@T2` | -2.73853 |
| `explicit.stat_1873752457@T2` | -2.73851 |
| `explicit.stat_388617051@T2` | -2.73850 |
| `explicit.stat_1120862500@T2` | -2.73850 |
| `explicit.stat_1873752457@T1` | -2.73849 |
| `explicit.stat_2676834156@T2` | -2.73849 |
| `explicit.stat_3196823591@T2` | -2.73849 |
| `explicit.stat_2365392475@T2` | -2.73847 |
| `explicit.stat_1366840608@T2` | -2.73804 |
| `explicit.stat_828533480@T1` | -2.73720 |

### weapon.crossbow — n=15290, R²=-1.8557

intercept: `3.7667`  ·  log_price: True  ·  ilvl: `-0.04554`  ·  n_mods: `-0.06523`  ·  n_top_tier: `0.57115`  ·  corrupted: `0.05957`  ·  n_sockets: `0.06007`  ·  quality: `0.02506`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.72839 |
| `explicit.stat_1980802737` | 1.28511 |
| `explicit.stat_2250681686@T2` | -1.22984 |
| `explicit.stat_1202301673@T1` | 1.10475 |
| `explicit.stat_2250681686` | 0.87413 |
| `explicit.stat_1263695895@T2` | -0.75994 |
| `explicit.stat_709508406@T1` | 0.73665 |
| `crafted.stat_3035140377` | 0.72127 |
| `explicit.stat_1263695895@T1` | -0.71870 |
| `explicit.stat_1509134228@T2` | -0.71202 |
| `explicit.stat_1037193709@T1` | -0.70753 |
| `explicit.stat_2694482655@T1` | -0.69952 |

### weapon.warstaff — n=9953, R²=-0.3588

intercept: `-10.5531`  ·  log_price: True  ·  ilvl: `0.14453`  ·  n_mods: `-0.24475`  ·  n_top_tier: `0.34237`  ·  corrupted: `0.34485`  ·  n_sockets: `0.18999`  ·  quality: `0.06069`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | 1.42080 |
| `explicit.stat_1037193709@T1` | 1.06406 |
| `rune.stat_243313994` | 0.87838 |
| `explicit.stat_328541901@T1` | -0.87470 |
| `desecrated.stat_2231156303@T1` | 0.85614 |
| `desecrated.stat_2527686725@T1` | 0.85614 |
| `explicit.stat_328541901@T2` | -0.81068 |
| `desecrated.stat_9187492` | 0.77860 |
| `explicit.stat_9187492@T1` | 0.68122 |
| `explicit.stat_1509134228@T1` | 0.66339 |
| `explicit.stat_748522257@T2` | 0.57389 |
| `explicit.stat_821021828@T2` | -0.54688 |

### weapon.staff — n=9291, R²=-0.3961

intercept: `-14.7520`  ·  log_price: True  ·  ilvl: `0.19142`  ·  n_mods: `-0.13355`  ·  n_top_tier: `0.51046`  ·  corrupted: `0.47928`  ·  n_sockets: `0.29291`  ·  quality: `0.03065`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 2.00105 |
| `explicit.stat_1545858329@T1` | 1.93435 |
| `explicit.stat_591105508@T1` | 1.53829 |
| `explicit.stat_124131830@T1` | 1.12462 |
| `explicit.stat_2254480358@T2` | 1.10894 |
| `explicit.stat_293638271@T2` | -1.09863 |
| `explicit.stat_591105508@T2` | 0.90284 |
| `explicit.stat_124131830@T2` | 0.86391 |
| `explicit.stat_4226189338@T2` | 0.75972 |
| `explicit.stat_1600707273@T1` | 0.72205 |
| `explicit.stat_1050105434@T2` | -0.64815 |
| `explicit.stat_2231156303@T2` | 0.62378 |

### weapon.sceptre — n=9179, R²=-0.3479

intercept: `-19.9060`  ·  log_price: True  ·  ilvl: `0.25364`  ·  n_mods: `-0.04003`  ·  n_top_tier: `0.14465`  ·  corrupted: `0.29809`  ·  n_sockets: `0.27761`  ·  quality: `0.03141`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.81767 |
| `explicit.stat_1250712710@T2` | 1.68843 |
| `explicit.stat_2162097452@T2` | 1.63807 |
| `explicit.stat_3057012405@T1` | 1.30174 |
| `explicit.stat_101878827@T1` | 0.90552 |
| `explicit.stat_2347036682@T1` | 0.81768 |
| `explicit.stat_101878827@T2` | 0.66637 |
| `explicit.stat_849987426@T1` | 0.54469 |
| `explicit.stat_1798257884@T2` | 0.51949 |
| `explicit.stat_2347036682@T2` | -0.47885 |
| `explicit.stat_1263695895@T1` | -0.43942 |
| `explicit.stat_328541901@T2` | 0.43870 |

### weapon.spear — n=7482, R²=-0.4116

intercept: `-12.2876`  ·  log_price: True  ·  ilvl: `0.17261`  ·  n_mods: `-0.15563`  ·  n_top_tier: `0.79543`  ·  corrupted: `0.04456`  ·  n_sockets: `0.22091`  ·  quality: `0.06673`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.94818 |
| `explicit.stat_1202301673@T1` | 1.78786 |
| `explicit.stat_1509134228@T1` | 1.57228 |
| `explicit.stat_9187492@T1` | 1.48865 |
| `explicit.stat_4080418644@T2` | -1.06044 |
| `crafted.stat_3035140377` | 1.02194 |
| `explicit.stat_709508406@T1` | 0.99269 |
| `explicit.stat_691932474@T1` | -0.92686 |
| `explicit.stat_3261801346@T1` | -0.91137 |
| `explicit.stat_748522257@T2` | -0.81704 |
| `explicit.stat_3695891184@T2` | -0.77328 |
| `explicit.stat_3261801346@T2` | -0.76308 |

### armour.focus — n=6139, R²=-0.3739

intercept: `-12.4557`  ·  log_price: True  ·  ilvl: `0.16512`  ·  n_mods: `-0.21352`  ·  n_top_tier: `0.89357`  ·  corrupted: `0.26599`  ·  n_sockets: `0.41831`  ·  quality: `0.06490`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 6.49690 |
| `explicit.stat_4220027924@T2` | -1.37727 |
| `explicit.stat_2231156303@T2` | -1.22069 |
| `explicit.stat_2923486259@T1` | -1.14023 |
| `explicit.stat_2231156303@T1` | -1.04042 |
| `explicit.stat_3291658075@T1` | -1.03326 |
| `explicit.stat_4220027924@T1` | -0.99642 |
| `explicit.stat_737908626@T2` | -0.98334 |
| `explicit.stat_2339757871@T2` | -0.97393 |
| `explicit.stat_3962278098@T2` | -0.91784 |
| `explicit.stat_2891184298@T2` | -0.90598 |
| `explicit.stat_3962278098@T1` | -0.87861 |

### armour.quiver — n=5761, R²=-0.3239

intercept: `-13.1158`  ·  log_price: True  ·  ilvl: `0.16309`  ·  n_mods: `-0.14367`  ·  n_top_tier: `0.89793`  ·  corrupted: `0.74997`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 7.14469 |
| `explicit.stat_2463230181@T1` | 3.34785 |
| `explicit.stat_2463230181@T2` | 1.69595 |
| `explicit.stat_681332047@T2` | -1.24929 |
| `explicit.stat_1573130764@T1` | -1.24139 |
| `explicit.stat_803737631@T2` | -1.22212 |
| `explicit.stat_2321178454@T2` | -1.07448 |
| `explicit.stat_1573130764@T2` | -1.02801 |
| `explicit.stat_4067062424@T1` | -0.99605 |
| `explicit.stat_803737631@T1` | -0.96555 |
| `explicit.stat_3261801346@T1` | -0.88262 |
| `explicit.stat_2321178454@T1` | -0.84286 |

### armour.shield — n=4975, R²=-0.487

intercept: `-10.8926`  ·  log_price: True  ·  ilvl: `0.14670`  ·  n_mods: `-0.12360`  ·  n_top_tier: `0.74625`  ·  corrupted: `-0.25069`  ·  n_sockets: `0.31380`  ·  quality: `0.06014`

| stat_id | coef |
|---|---|
| `explicit.stat_3484657501@T1` | -1.50705 |
| `explicit.stat_328541901@T1` | -1.24169 |
| `explicit.stat_3484657501@T2` | -1.17306 |
| `explicit.stat_3321629045@T2` | -1.16666 |
| `explicit.stat_4095671657@T1` | -1.16662 |
| `explicit.stat_3855016469@T1` | -1.08219 |
| `explicit.stat_2923486259@T2` | -1.06989 |
| `explicit.stat_3033371881@T2` | -1.03559 |
| `explicit.stat_2481353198@T2` | -1.02281 |
| `explicit.stat_2901986750@T1` | -0.99243 |
| `explicit.stat_2451402625@T1` | -0.97145 |
| `explicit.stat_328541901@T2` | -0.95407 |

### weapon.twomace — n=4564, R²=-0.493

intercept: `-8.9067`  ·  log_price: True  ·  ilvl: `0.12389`  ·  n_mods: `-0.19496`  ·  n_top_tier: `0.40744`  ·  corrupted: `-0.00203`  ·  n_sockets: `0.16753`  ·  quality: `0.05999`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.84199 |
| `explicit.stat_1037193709@T1` | -1.42366 |
| `desecrated.stat_1509134228@T1` | 1.36618 |
| `crafted.stat_3035140377` | 0.91862 |
| `explicit.stat_1263695895@T2` | -0.86682 |
| `explicit.stat_387439868@T2` | -0.81281 |
| `explicit.stat_691932474@T1` | -0.74956 |
| `explicit.stat_1037193709@T2` | -0.67705 |
| `explicit.stat_9187492@T1` | -0.65158 |
| `explicit.stat_669069897@T1` | -0.61009 |
| `explicit.stat_1509134228@T1` | 0.58320 |
| `explicit.stat_518292764@T2` | -0.56099 |

## Coverage (listings per base)

- … **Sapphire** — 28801 listings (28751 priced) [0.3–885594757.8 ex]
- … **Emerald** — 28187 listings (28148 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 21535 listings (21511 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 10765 listings (10750 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 9404 listings (9386 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 9067 listings (9048 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 8982 listings (8974 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 8520 listings (8504 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 8380 listings (8361 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 8239 listings (8228 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 6968 listings (6958 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 6687 listings (6681 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 6653 listings (6647 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 6516 listings (6495 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 5875 listings (5868 priced) [0.3–19945827.9 ex]
- … **Plate Belt** — 5842 listings (5817 priced) [0.3–398912568423.8 ex]
- … **Unset Ring** — 5769 listings (5752 priced) [0.2–24532814.5 ex]
- … **Jade Amulet** — 5758 listings (5747 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 5718 listings (5711 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 5691 listings (5666 priced) [0.6–398912568423.8 ex]
- … **Bloodstone Amulet** — 5570 listings (5561 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 5470 listings (5463 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5247 listings (5244 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 5218 listings (5206 priced) [0.3–91750808.2 ex]
- … **Heavy Belt** — 5201 listings (5192 priced) [0.3–398912568423.8 ex]
