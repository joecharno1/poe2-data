# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-17T13:46:37+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **581987** (580371 priced in exalted)
- Distinct bases: 987 · distinct mods: 3208 · mod rows: 2755296
- Sold signals: **25311** sold · 329407 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-17T13:37:57+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×25.31** (median |log error| 3.2311)
- Within ±30% of asking price: **17%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 80% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.14** · typical error ×66.69 · ±30% 5% · n=84432
- Premium segment (60ex+): skill **+0.13** · typical error ×321.37 · ±30% 0% · n=57155

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 11943 | ×56.16 | 22% | +0.03 | +0.05 |
| jewel | 11269 | ×11.13 | 4% | +0.07 | +0.10 |
| accessory.amulet | 10919 | ×49.41 | 20% | +0.03 | +0.04 |
| accessory.belt | 8029 | ×25.39 | 19% | +0.06 | +0.08 |
| armour.chest | 7809 | ×19.78 | 22% | +0.07 | +0.11 |
| armour.helmet | 7630 | ×24.26 | 12% | +0.09 | +0.11 |
| armour.boots | 7187 | ×35.88 | 20% | +0.09 | +0.11 |
| armour.gloves | 6950 | ×38.74 | 14% | +0.09 | +0.12 |
| other | 6612 | ×1.92 | 43% | +0.10 | +0.17 |
| weapon.wand | 4323 | ×47.98 | 17% | +0.07 | +0.10 |
| weapon.bow | 3414 | ×31.66 | 15% | +0.13 | +0.15 |
| weapon.crossbow | 3186 | ×34.23 | 17% | +0.09 | +0.12 |
| weapon.warstaff | 2069 | ×30.20 | 8% | +0.15 | +0.13 |
| weapon.staff | 1947 | ×50.11 | 7% | +0.12 | +0.14 |
| weapon.sceptre | 1897 | ×38.27 | 4% | +0.18 | +0.20 |
| weapon.spear | 1535 | ×38.78 | 13% | +0.08 | +0.12 |
| armour.focus | 1282 | ×25.50 | 6% | +0.16 | +0.18 |
| armour.quiver | 1226 | ×27.26 | 7% | +0.14 | +0.16 |
| flask.charm | 1045 | ×17.76 | 32% | +0.05 | +0.08 |
| armour.shield | 995 | ×19.04 | 7% | +0.04 | +0.07 |
| weapon.twomace | 916 | ×10.15 | 11% | +0.08 | +0.07 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=61477, R²=-0.9381

intercept: `-1.8400`  ·  log_price: True  ·  ilvl: `0.02629`  ·  n_mods: `0.85009`  ·  n_top_tier: `-0.35497`  ·  corrupted: `0.33271`  ·  quality: `0.22651`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.45577 |
| `explicit.stat_2301718443@T1` | 2.68316 |
| `explicit.stat_3374165039@T1` | -2.16526 |
| `explicit.stat_1805182458@T1` | -2.14422 |
| `explicit.stat_3485067555@T1` | 1.85632 |
| `explicit.stat_686254215@T1` | -1.57579 |
| `explicit.stat_491450213@T1` | 1.54117 |
| `explicit.stat_3166958180@T1` | -1.53847 |
| `explicit.stat_1869147066@T1` | -1.47525 |
| `explicit.stat_1697951953@T1` | -1.41572 |
| `explicit.stat_3787460122@T1` | 1.31680 |
| `explicit.stat_3174700878@T1` | 1.31394 |

### other — n=55794, R²=-0.6598

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.34732`  ·  corrupted: `0.32007`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2974417149@T1` | 0.41547 |
| `explicit.stat_3299347043@T1` | -0.34953 |
| `explicit.stat_3291658075@T1` | 0.31955 |
| `implicit.stat_2219129443` | 0.23026 |
| `implicit.stat_3879011313` | 0.23026 |
| `implicit.stat_4041853756` | 0.23025 |
| `explicit.stat_2106365538@T1` | -0.16469 |
| `explicit.stat_1050105434@T1` | -0.14496 |
| `explicit.stat_2482852589@T1` | -0.11611 |
| `explicit.stat_789117908@T1` | -0.11072 |
| `implicit.stat_2923486259` | -0.10724 |
| `pseudo.total_chaos_res` | 0.10724 |

### accessory.ring — n=54664, R²=-2.0256

intercept: `3.5151`  ·  log_price: True  ·  ilvl: `-0.04337`  ·  n_mods: `-0.00096`  ·  n_top_tier: `1.02299`  ·  corrupted: `0.01923`  ·  n_sockets: `2.19080`  ·  quality: `0.07655`

| stat_id | coef |
|---|---|
| `explicit.stat_2231156303@T1` | -1.05826 |
| `explicit.stat_1573130764@T1` | -1.05631 |
| `explicit.stat_1263695895@T2` | -1.05058 |
| `explicit.stat_1263695895@T1` | -1.04715 |
| `explicit.stat_1368271171@T2` | -1.04362 |
| `explicit.stat_2231156303@T2` | -1.04159 |
| `explicit.stat_2144192055@T1` | -1.04095 |
| `explicit.stat_803737631@T1` | -1.04063 |
| `explicit.stat_4220027924@T2` | -1.03870 |
| `explicit.stat_3325883026@T1` | -1.03858 |
| `explicit.stat_1573130764@T2` | -1.03777 |
| `explicit.stat_3291658075@T2` | -1.03647 |

### accessory.amulet — n=49890, R²=-2.165

intercept: `3.6513`  ·  log_price: True  ·  ilvl: `-0.04449`  ·  n_mods: `-0.02416`  ·  n_top_tier: `0.97781`  ·  corrupted: `0.04616`  ·  n_sockets: `-0.13625`  ·  quality: `0.00026`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.18703 |
| `explicit.stat_3299347043@T2` | -1.05339 |
| `explicit.stat_472520716@T2` | -1.04729 |
| `explicit.stat_587431675@T2` | -1.04579 |
| `explicit.stat_2974417149@T1` | -1.04319 |
| `explicit.stat_2866361420@T2` | -1.03324 |
| `explicit.stat_803737631@T1` | -1.03250 |
| `explicit.stat_1050105434@T2` | -1.02457 |
| `explicit.stat_803737631@T2` | -1.02039 |
| `explicit.stat_2974417149@T2` | -1.01869 |
| `explicit.stat_2866361420@T1` | -1.01687 |
| `explicit.stat_472520716@T1` | -1.00861 |

### accessory.belt — n=37212, R²=-1.5924

intercept: `4.3667`  ·  log_price: True  ·  ilvl: `-0.05147`  ·  n_mods: `-0.04330`  ·  n_top_tier: `0.65473`  ·  corrupted: `0.98918`  ·  n_sockets: `0.34949`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -0.86303 |
| `explicit.stat_3299347043@T2` | -0.74194 |
| `explicit.stat_2881298780@T1` | -0.72524 |
| `explicit.stat_4220027924@T2` | -0.71297 |
| `explicit.stat_809229260@T2` | -0.69866 |
| `explicit.stat_1389754388@T1` | -0.68932 |
| `explicit.stat_51994685@T1` | -0.68764 |
| `explicit.stat_3325883026@T1` | -0.67269 |
| `explicit.stat_915769802@T1` | -0.67121 |
| `explicit.stat_3372524247@T2` | -0.66485 |
| `explicit.stat_644456512@T1` | -0.66475 |
| `explicit.stat_915769802@T2` | -0.66084 |

### armour.chest — n=36990, R²=-1.726

intercept: `3.4217`  ·  log_price: True  ·  ilvl: `-0.04193`  ·  n_mods: `-0.02106`  ·  n_top_tier: `0.49465`  ·  corrupted: `0.08615`  ·  n_sockets: `0.03025`  ·  quality: `0.06292`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.66937 |
| `explicit.stat_3981240776@T1` | 1.09546 |
| `explicit.stat_986397080@T2` | -0.57401 |
| `explicit.stat_1692879867@T1` | -0.53832 |
| `explicit.stat_3484657501@T1` | -0.53306 |
| `explicit.stat_915769802@T2` | -0.53057 |
| `explicit.stat_986397080@T1` | -0.52913 |
| `explicit.stat_2339757871@T2` | -0.52877 |
| `explicit.stat_4080418644@T2` | -0.52805 |
| `explicit.stat_1692879867@T2` | -0.52243 |
| `explicit.stat_4080418644@T1` | -0.52084 |
| `explicit.stat_4015621042@T1` | -0.52021 |

### armour.helmet — n=35935, R²=-1.4031

intercept: `3.7157`  ·  log_price: True  ·  ilvl: `-0.04678`  ·  n_mods: `-0.05764`  ·  n_top_tier: `0.42946`  ·  corrupted: `0.72076`  ·  n_sockets: `0.18314`  ·  quality: `0.04470`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -5.33317 |
| `explicit.stat_3917489142@T2` | -0.89482 |
| `explicit.stat_1263695895@T1` | -0.83455 |
| `explicit.stat_3917489142@T1` | -0.71313 |
| `explicit.stat_1999113824@T1` | -0.67387 |
| `explicit.stat_1263695895@T2` | -0.62764 |
| `explicit.stat_4052037485@T2` | -0.61948 |
| `explicit.stat_2162097452@T2` | -0.61241 |
| `explicit.stat_3321629045@T2` | -0.56262 |
| `explicit.stat_1999113824@T2` | -0.54721 |
| `explicit.stat_1062208444@T2` | -0.51918 |
| `explicit.stat_587431675@T2` | -0.51817 |

### armour.boots — n=33599, R²=-1.7039

intercept: `3.4981`  ·  log_price: True  ·  ilvl: `-0.04273`  ·  n_mods: `-0.02118`  ·  n_top_tier: `0.70031`  ·  corrupted: `0.02627`  ·  n_sockets: `0.02192`  ·  quality: `0.05097`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 3.40384 |
| `explicit.stat_2250533757@T1` | 1.38567 |
| `explicit.stat_2339757871@T1` | -0.97892 |
| `explicit.stat_3299347043@T1` | -0.93280 |
| `explicit.stat_3917489142@T2` | -0.85259 |
| `explicit.stat_3917489142@T1` | -0.76455 |
| `explicit.stat_2923486259@T2` | -0.75719 |
| `explicit.stat_2160282525@T1` | -0.75457 |
| `explicit.stat_3299347043@T2` | -0.75243 |
| `explicit.stat_1062208444@T2` | -0.73158 |
| `explicit.stat_3484657501@T2` | -0.73152 |
| `explicit.stat_1671376347@T2` | -0.72603 |

### armour.gloves — n=32668, R²=-1.6369

intercept: `3.7218`  ·  log_price: True  ·  ilvl: `-0.04756`  ·  n_mods: `-0.02198`  ·  n_top_tier: `0.60859`  ·  corrupted: `0.02096`  ·  n_sockets: `0.09970`  ·  quality: `0.04515`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 1.91856 |
| `rune.stat_836936635` | 1.24730 |
| `explicit.stat_2923486259@T1` | -0.87833 |
| `explicit.stat_1671376347@T1` | 0.84829 |
| `explicit.stat_3321629045@T2` | -0.83416 |
| `explicit.stat_3484657501@T2` | -0.82123 |
| `explicit.stat_9187492@T2` | -0.82105 |
| `explicit.stat_9187492@T1` | 0.78846 |
| `explicit.stat_4052037485@T1` | -0.75875 |
| `explicit.stat_1754445556@T2` | -0.75771 |
| `explicit.stat_3484657501@T1` | -0.73445 |
| `explicit.stat_803737631@T2` | -0.71673 |

### weapon.wand — n=20222, R²=-2.1862

intercept: `3.5023`  ·  log_price: True  ·  ilvl: `-0.04324`  ·  n_mods: `-0.03406`  ·  n_top_tier: `0.52059`  ·  corrupted: `0.05810`  ·  n_sockets: `0.08277`  ·  quality: `0.00815`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.56557 |
| `rune.stat_124131830` | -2.35871 |
| `explicit.stat_2254480358@T1` | 2.22215 |
| `explicit.stat_4226189338@T1` | 2.02745 |
| `explicit.stat_591105508@T1` | 1.76526 |
| `explicit.stat_124131830@T1` | 1.75725 |
| `explicit.stat_736967255@T2` | 1.65497 |
| `crafted.stat_124131830` | 1.25333 |
| `explicit.stat_4226189338@T2` | 0.92732 |
| `explicit.stat_1600707273@T1` | 0.86638 |
| `explicit.stat_2254480358@T2` | 0.78504 |
| `explicit.stat_1263695895@T1` | -0.75397 |

### weapon.bow — n=16233, R²=-1.9317

intercept: `3.6414`  ·  log_price: True  ·  ilvl: `-0.04295`  ·  n_mods: `-0.06702`  ·  n_top_tier: `0.62591`  ·  corrupted: `0.21585`  ·  n_sockets: `0.03056`  ·  quality: `0.02971`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | -2.53086 |
| `desecrated.stat_210067635@T1` | -1.72554 |
| `crafted.stat_3035140377` | 1.46833 |
| `explicit.stat_1202301673@T1` | 1.45241 |
| `explicit.stat_2463230181@T1` | -1.04729 |
| `explicit.stat_1263695895@T1` | -0.92119 |
| `explicit.stat_3336890334@T1` | 0.90297 |
| `explicit.stat_1263695895@T2` | -0.87154 |
| `explicit.stat_2463230181@T2` | -0.86375 |
| `explicit.stat_3695891184@T2` | -0.75345 |
| `explicit.stat_518292764@T2` | -0.74562 |
| `explicit.stat_1037193709@T1` | -0.74427 |

### flask.charm — n=15555, R²=-0.5797

intercept: `0.0654`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `2.49874`  ·  corrupted: `1.79483`  ·  quality: `0.00009`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.67389 |
| `explicit.stat_1056492907` | 2.87177 |
| `explicit.stat_828533480@T2` | -2.49875 |
| `explicit.stat_1873752457@T2` | -2.49873 |
| `explicit.stat_1120862500@T2` | -2.49872 |
| `explicit.stat_388617051@T2` | -2.49871 |
| `explicit.stat_2676834156@T2` | -2.49871 |
| `explicit.stat_1873752457@T1` | -2.49871 |
| `explicit.stat_3196823591@T2` | -2.49871 |
| `explicit.stat_2365392475@T2` | -2.49869 |
| `explicit.stat_1366840608@T2` | -2.49805 |
| `explicit.stat_828533480@T1` | -2.49587 |

### weapon.crossbow — n=15211, R²=-1.8846

intercept: `3.7455`  ·  log_price: True  ·  ilvl: `-0.04557`  ·  n_mods: `-0.05687`  ·  n_top_tier: `0.65225`  ·  corrupted: `0.05971`  ·  n_sockets: `0.04842`  ·  quality: `0.02308`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.78902 |
| `explicit.stat_2250681686@T2` | -1.35557 |
| `explicit.stat_1202301673@T1` | 1.32386 |
| `explicit.stat_1980802737` | 1.22882 |
| `explicit.stat_2250681686` | 0.83611 |
| `explicit.stat_1263695895@T2` | -0.80111 |
| `explicit.stat_709508406@T2` | -0.76835 |
| `explicit.stat_2694482655@T1` | -0.76264 |
| `crafted.stat_3035140377` | 0.76043 |
| `explicit.stat_1509134228@T2` | -0.76013 |
| `explicit.stat_1037193709@T1` | -0.74626 |
| `explicit.stat_669069897@T1` | -0.73265 |

### weapon.warstaff — n=9857, R²=-0.3588

intercept: `-10.2850`  ·  log_price: True  ·  ilvl: `0.14123`  ·  n_mods: `-0.23034`  ·  n_top_tier: `0.34993`  ·  corrupted: `0.28080`  ·  n_sockets: `0.17911`  ·  quality: `0.06259`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | 1.09902 |
| `explicit.stat_1037193709@T1` | 0.88242 |
| `rune.stat_243313994` | 0.83336 |
| `explicit.stat_328541901@T1` | -0.80192 |
| `explicit.stat_1509134228@T1` | 0.74964 |
| `explicit.stat_328541901@T2` | -0.74947 |
| `desecrated.stat_9187492` | 0.71310 |
| `explicit.stat_9187492@T1` | 0.56844 |
| `explicit.stat_748522257@T2` | 0.55914 |
| `explicit.stat_691932474@T2` | -0.52207 |
| `explicit.stat_1368271171@T1` | -0.51005 |
| `explicit.stat_1037193709@T2` | -0.50275 |

### weapon.staff — n=9220, R²=-0.3918

intercept: `-14.7879`  ·  log_price: True  ·  ilvl: `0.19139`  ·  n_mods: `-0.13427`  ·  n_top_tier: `0.46782`  ·  corrupted: `0.60608`  ·  n_sockets: `0.28352`  ·  quality: `0.03853`

| stat_id | coef |
|---|---|
| `explicit.stat_4226189338@T1` | 1.91507 |
| `explicit.stat_1545858329@T1` | 1.70841 |
| `explicit.stat_591105508@T1` | 1.50511 |
| `explicit.stat_293638271@T2` | -1.11610 |
| `explicit.stat_2254480358@T2` | 1.11059 |
| `explicit.stat_124131830@T1` | 0.93753 |
| `explicit.stat_591105508@T2` | 0.86042 |
| `explicit.stat_124131830@T2` | 0.77231 |
| `explicit.stat_2254480358@T1` | 0.70734 |
| `explicit.stat_2231156303@T2` | 0.70075 |
| `explicit.stat_4226189338@T2` | 0.66522 |
| `explicit.stat_1600707273@T1` | 0.65437 |

### weapon.sceptre — n=9115, R²=-0.3402

intercept: `-20.0871`  ·  log_price: True  ·  ilvl: `0.25712`  ·  n_mods: `-0.06393`  ·  n_top_tier: `0.18238`  ·  corrupted: `0.22372`  ·  n_sockets: `0.25823`  ·  quality: `0.03637`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.79340 |
| `explicit.stat_1250712710@T2` | 1.80182 |
| `explicit.stat_2162097452@T2` | 1.65335 |
| `explicit.stat_3057012405@T1` | 1.25292 |
| `explicit.stat_101878827@T1` | 0.94382 |
| `explicit.stat_2347036682@T1` | 0.67777 |
| `explicit.stat_849987426@T1` | 0.63650 |
| `explicit.stat_101878827@T2` | 0.62441 |
| `explicit.stat_2347036682@T2` | -0.62164 |
| `explicit.stat_1263695895@T1` | -0.47161 |
| `explicit.stat_1798257884@T2` | 0.45331 |
| `explicit.stat_289128254@T2` | -0.42024 |

### weapon.spear — n=7429, R²=-0.4176

intercept: `-11.8979`  ·  log_price: True  ·  ilvl: `0.16801`  ·  n_mods: `-0.14990`  ·  n_top_tier: `0.79793`  ·  corrupted: `-0.10481`  ·  n_sockets: `0.20610`  ·  quality: `0.06598`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -4.12417 |
| `explicit.stat_1202301673@T1` | 1.72822 |
| `explicit.stat_1509134228@T1` | 1.61838 |
| `explicit.stat_9187492@T1` | 1.18072 |
| `crafted.stat_3035140377` | 1.05202 |
| `explicit.stat_709508406@T1` | 1.03483 |
| `explicit.stat_4080418644@T2` | -0.99324 |
| `explicit.stat_3261801346@T1` | -0.90380 |
| `explicit.stat_691932474@T1` | -0.87045 |
| `explicit.stat_9187492@T2` | -0.84187 |
| `explicit.stat_748522257@T2` | -0.82190 |
| `explicit.stat_691932474@T2` | -0.77090 |

### armour.focus — n=6094, R²=-0.3686

intercept: `-12.8352`  ·  log_price: True  ·  ilvl: `0.17000`  ·  n_mods: `-0.19975`  ·  n_top_tier: `0.81903`  ·  corrupted: `0.35033`  ·  n_sockets: `0.40132`  ·  quality: `0.06997`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 5.28252 |
| `explicit.stat_4220027924@T2` | -1.34685 |
| `explicit.stat_3962278098@T1` | -1.08926 |
| `explicit.stat_2231156303@T2` | -0.96506 |
| `explicit.stat_4220027924@T1` | -0.93726 |
| `explicit.stat_3291658075@T1` | -0.91213 |
| `explicit.stat_737908626@T2` | -0.91080 |
| `explicit.stat_736967255@T2` | -0.89657 |
| `explicit.stat_2891184298@T2` | -0.89528 |
| `explicit.stat_2339757871@T2` | -0.86569 |
| `explicit.stat_2231156303@T1` | -0.83020 |
| `explicit.stat_2339757871@T1` | -0.78933 |

### armour.quiver — n=5717, R²=-0.316

intercept: `-13.9989`  ·  log_price: True  ·  ilvl: `0.17237`  ·  n_mods: `-0.15860`  ·  n_top_tier: `0.87142`  ·  corrupted: `0.81858`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 7.10510 |
| `explicit.stat_2463230181@T1` | 3.43559 |
| `explicit.stat_2463230181@T2` | 1.67809 |
| `explicit.stat_681332047@T2` | -1.34995 |
| `explicit.stat_1573130764@T1` | -1.29229 |
| `explicit.stat_803737631@T2` | -1.12809 |
| `explicit.stat_2321178454@T2` | -1.12343 |
| `explicit.stat_1573130764@T2` | -0.99640 |
| `explicit.stat_803737631@T1` | -0.98100 |
| `explicit.stat_4067062424@T1` | -0.95754 |
| `explicit.stat_2321178454@T1` | -0.93442 |
| `explicit.stat_3261801346@T1` | -0.81448 |

### armour.shield — n=4940, R²=-0.4861

intercept: `-10.9381`  ·  log_price: True  ·  ilvl: `0.14620`  ·  n_mods: `-0.11069`  ·  n_top_tier: `0.66335`  ·  corrupted: `-0.34188`  ·  n_sockets: `0.27121`  ·  quality: `0.06536`

| stat_id | coef |
|---|---|
| `explicit.stat_328541901@T1` | -1.36389 |
| `explicit.stat_3484657501@T1` | -1.30777 |
| `explicit.stat_2339757871@T1` | -1.30758 |
| `explicit.stat_328541901@T2` | -1.27289 |
| `explicit.stat_4095671657@T1` | -1.23376 |
| `explicit.stat_3321629045@T2` | -1.07298 |
| `explicit.stat_3484657501@T2` | -1.05613 |
| `explicit.stat_3033371881@T2` | -0.99228 |
| `explicit.stat_2901986750@T1` | -0.98212 |
| `explicit.stat_1671376347@T1` | -0.95212 |
| `explicit.stat_2923486259@T2` | -0.93170 |
| `explicit.stat_3855016469@T1` | -0.90391 |

### weapon.twomace — n=4531, R²=-0.4888

intercept: `-9.2809`  ·  log_price: True  ·  ilvl: `0.12814`  ·  n_mods: `-0.17845`  ·  n_top_tier: `0.52017`  ·  corrupted: `-0.01772`  ·  n_sockets: `0.15902`  ·  quality: `0.05525`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -3.92145 |
| `desecrated.stat_1509134228@T1` | 1.95079 |
| `explicit.stat_1037193709@T1` | -1.56300 |
| `explicit.stat_387439868@T2` | -0.96646 |
| `crafted.stat_3035140377` | 0.96470 |
| `explicit.stat_691932474@T1` | -0.86585 |
| `explicit.stat_1263695895@T2` | -0.85295 |
| `explicit.stat_9187492@T1` | -0.81589 |
| `explicit.stat_1037193709@T2` | -0.79326 |
| `explicit.stat_3336890334@T1` | -0.69215 |
| `explicit.stat_669069897@T1` | -0.63861 |
| `explicit.stat_669069897@T2` | -0.63818 |

## Coverage (listings per base)

- … **Sapphire** — 28479 listings (28431 priced) [0.3–885594757.8 ex]
- … **Emerald** — 27927 listings (27888 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 21336 listings (21312 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 10701 listings (10686 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 9319 listings (9301 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 8997 listings (8978 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 8903 listings (8895 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 8455 listings (8439 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 8317 listings (8298 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 8181 listings (8170 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 6911 listings (6901 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 6626 listings (6620 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 6598 listings (6592 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 6480 listings (6460 priced) [0.3–4297682211.9 ex]
- … **Lapis Amulet** — 5827 listings (5820 priced) [0.3–19945827.9 ex]
- … **Plate Belt** — 5795 listings (5771 priced) [0.3–398912568423.8 ex]
- … **Unset Ring** — 5716 listings (5699 priced) [0.2–24532814.5 ex]
- … **Jade Amulet** — 5706 listings (5695 priced) [0.3–4547453.5 ex]
- … **Amber Amulet** — 5674 listings (5667 priced) [0.3–3985176410.3 ex]
- … **Ancestral Tiara** — 5629 listings (5608 priced) [0.6–398912568423.8 ex]
- … **Bloodstone Amulet** — 5518 listings (5509 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 5415 listings (5408 priced) [0.2–275252424.7 ex]
- … **Azure Amulet** — 5203 listings (5201 priced) [0.3–3985176410.3 ex]
- … **Heavy Belt** — 5165 listings (5156 priced) [0.3–398912568423.8 ex]
- … **Lunar Amulet** — 5153 listings (5141 priced) [0.3–91750808.2 ex]
