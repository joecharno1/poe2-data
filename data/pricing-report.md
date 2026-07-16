# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-16T07:31:20+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **539238** (537799 priced in exalted)
- Distinct bases: 986 · distinct mods: 3151 · mod rows: 2555927
- Sold signals: **25830** sold · 302895 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-16T07:23:36+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×27.26** (median |log error| 3.3054)
- Within ±30% of asking price: **20%**
- Skill vs constant-price guess: **+0.06** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.11** · typical error ×80.19 · ±30% 4% · n=78236
- Premium segment (60ex+): skill **+0.11** · typical error ×361.19 · ±30% 0% · n=52446

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 10929 | ×54.43 | 22% | +0.05 | +0.06 |
| jewel | 10241 | ×9.69 | 5% | +0.04 | +0.07 |
| accessory.amulet | 10025 | ×49.84 | 20% | +0.03 | +0.03 |
| accessory.belt | 7582 | ×30.18 | 23% | +0.05 | +0.07 |
| armour.chest | 7383 | ×32.13 | 24% | +0.06 | +0.09 |
| armour.helmet | 7174 | ×30.33 | 23% | +0.05 | +0.07 |
| armour.boots | 6687 | ×41.16 | 22% | +0.06 | +0.08 |
| armour.gloves | 6554 | ×42.79 | 21% | +0.05 | +0.07 |
| other | 6076 | ×1.97 | 43% | +0.10 | +0.17 |
| weapon.wand | 4130 | ×33.33 | 17% | +0.07 | +0.08 |
| weapon.bow | 3282 | ×31.87 | 17% | +0.11 | +0.10 |
| weapon.crossbow | 3070 | ×28.67 | 19% | +0.09 | +0.12 |
| weapon.warstaff | 1897 | ×33.30 | 13% | +0.13 | +0.12 |
| weapon.staff | 1799 | ×60.99 | 11% | +0.09 | +0.10 |
| weapon.sceptre | 1763 | ×40.78 | 5% | +0.16 | +0.15 |
| weapon.spear | 1427 | ×52.09 | 16% | +0.09 | +0.09 |
| armour.focus | 1168 | ×30.79 | 7% | +0.15 | +0.18 |
| armour.quiver | 1125 | ×25.70 | 8% | +0.11 | +0.14 |
| flask.charm | 988 | ×28.00 | 34% | +0.04 | +0.06 |
| armour.shield | 930 | ×24.28 | 11% | +0.03 | +0.04 |
| weapon.twomace | 857 | ×15.82 | 12% | +0.07 | +0.06 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=55330, R²=-0.9322

intercept: `-1.7117`  ·  log_price: True  ·  ilvl: `0.02653`  ·  n_mods: `0.65621`  ·  n_top_tier: `-0.18316`  ·  corrupted: `0.34283`  ·  quality: `0.23088`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.41409 |
| `explicit.stat_2301718443@T1` | 2.88115 |
| `explicit.stat_3780644166@T1` | -2.34404 |
| `explicit.stat_3485067555@T1` | 2.16667 |
| `explicit.stat_1805182458@T1` | -1.96695 |
| `explicit.stat_234296660@T1` | -1.87656 |
| `explicit.stat_627767961@T1` | -1.79319 |
| `explicit.stat_1062710370@T1` | -1.60535 |
| `explicit.stat_2523933828@T1` | -1.53939 |
| `explicit.stat_1697951953@T1` | -1.49459 |
| `explicit.stat_3166958180@T1` | -1.46524 |
| `explicit.stat_872504239@T1` | 1.45337 |

### other — n=51928, R²=-0.6362

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.34676`  ·  corrupted: `0.34634`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.36615 |
| `explicit.stat_3299347043@T1` | -0.31216 |
| `explicit.stat_2482852589@T1` | -0.30231 |
| `explicit.stat_2974417149@T1` | 0.24692 |
| `implicit.stat_3879011313` | 0.23541 |
| `implicit.stat_2219129443` | 0.23026 |
| `implicit.stat_4041853756` | 0.23025 |
| `explicit.stat_789117908@T1` | -0.18058 |
| `explicit.stat_2106365538@T1` | -0.15259 |
| `explicit.stat_3917489142@T1` | 0.10700 |
| `explicit.stat_1050105434@T1` | -0.09631 |
| `explicit.stat_3141070085@T1` | -0.09173 |

### accessory.ring — n=49853, R²=-2.003

intercept: `3.5081`  ·  log_price: True  ·  ilvl: `-0.04331`  ·  n_mods: `0.00088`  ·  n_top_tier: `0.93287`  ·  corrupted: `0.11210`  ·  n_sockets: `2.18505`  ·  quality: `0.07115`

| stat_id | coef |
|---|---|
| `explicit.stat_2557965901@T1` | -0.98535 |
| `explicit.stat_2557965901@T2` | -0.97242 |
| `explicit.stat_2231156303@T1` | -0.96716 |
| `explicit.stat_3325883026@T1` | -0.96103 |
| `explicit.stat_2144192055@T1` | -0.95467 |
| `explicit.stat_803737631@T1` | -0.95446 |
| `explicit.stat_2231156303@T2` | -0.95381 |
| `explicit.stat_2891184298@T2` | -0.95101 |
| `explicit.stat_3291658075@T1` | -0.95091 |
| `explicit.stat_3325883026@T2` | -0.95029 |
| `explicit.stat_1368271171@T2` | -0.94879 |
| `explicit.stat_1263695895@T1` | -0.94815 |

### accessory.amulet — n=45797, R²=-2.143

intercept: `3.7445`  ·  log_price: True  ·  ilvl: `-0.04585`  ·  n_mods: `-0.02074`  ·  n_top_tier: `0.94128`  ·  corrupted: `0.06347`  ·  n_sockets: `-0.09312`  ·  quality: `-0.00035`

| stat_id | coef |
|---|---|
| `explicit.stat_472520716@T2` | -1.02274 |
| `explicit.stat_803737631@T1` | -1.00583 |
| `explicit.stat_587431675@T2` | -1.00239 |
| `explicit.stat_2866361420@T2` | -0.98917 |
| `explicit.stat_2901986750@T1` | -0.98683 |
| `explicit.stat_3299347043@T1` | -0.98325 |
| `explicit.stat_1050105434@T2` | -0.98189 |
| `explicit.stat_2974417149@T2` | -0.97884 |
| `explicit.stat_803737631@T2` | -0.97875 |
| `explicit.stat_472520716@T1` | -0.97704 |
| `explicit.stat_3917489142@T2` | -0.97514 |
| `explicit.stat_2974417149@T1` | -0.97353 |

### accessory.belt — n=34795, R²=-1.6763

intercept: `3.2697`  ·  log_price: True  ·  ilvl: `-0.03952`  ·  n_mods: `-0.02145`  ·  n_top_tier: `1.32423`  ·  corrupted: `0.72544`  ·  n_sockets: `0.17443`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.35753 |
| `explicit.stat_1389754388@T1` | -1.35741 |
| `explicit.stat_809229260@T2` | -1.35116 |
| `explicit.stat_4220027924@T2` | -1.35045 |
| `explicit.stat_3325883026@T1` | -1.34435 |
| `explicit.stat_3299347043@T2` | -1.34288 |
| `explicit.stat_51994685@T1` | -1.33871 |
| `explicit.stat_644456512@T2` | -1.33794 |
| `explicit.stat_2881298780@T1` | -1.33772 |
| `explicit.stat_1671376347@T2` | -1.33096 |
| `explicit.stat_644456512@T1` | -1.33050 |
| `explicit.stat_915769802@T2` | -1.32772 |

### armour.chest — n=34467, R²=-1.7426

intercept: `3.4067`  ·  log_price: True  ·  ilvl: `-0.04206`  ·  n_mods: `-0.01250`  ·  n_top_tier: `0.55262`  ·  corrupted: `0.03185`  ·  n_sockets: `0.01647`  ·  quality: `0.05083`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.92374 |
| `explicit.stat_3981240776@T1` | 1.01168 |
| `explicit.stat_986397080@T2` | -0.61367 |
| `explicit.stat_4015621042@T1` | -0.58794 |
| `explicit.stat_986397080@T1` | -0.58690 |
| `explicit.stat_4080418644@T2` | -0.58437 |
| `explicit.stat_4080418644@T1` | -0.58387 |
| `explicit.stat_3484657501@T1` | -0.58047 |
| `explicit.stat_3372524247@T2` | -0.57881 |
| `explicit.stat_2451402625@T2` | -0.57736 |
| `explicit.stat_1692879867@T1` | -0.57272 |
| `explicit.stat_915769802@T2` | -0.57099 |

### armour.helmet — n=33444, R²=-1.8009

intercept: `3.4476`  ·  log_price: True  ·  ilvl: `-0.04328`  ·  n_mods: `-0.01432`  ·  n_top_tier: `0.37618`  ·  corrupted: `0.86344`  ·  n_sockets: `0.01391`  ·  quality: `0.05741`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -5.20447 |
| `crafted.stat_3917489142@T1` | 1.28260 |
| `explicit.stat_3917489142@T2` | -0.49044 |
| `explicit.stat_1263695895@T1` | -0.47809 |
| `explicit.stat_1263695895@T2` | -0.47196 |
| `explicit.stat_3917489142@T1` | -0.42950 |
| `explicit.stat_4052037485@T2` | -0.42024 |
| `explicit.stat_1999113824@T1` | -0.41387 |
| `explicit.stat_2162097452@T2` | -0.41101 |
| `explicit.stat_3321629045@T2` | -0.40684 |
| `explicit.stat_3261801346@T1` | -0.40189 |
| `explicit.stat_803737631@T1` | -0.39593 |

### armour.boots — n=31339, R²=-1.7772

intercept: `3.3416`  ·  log_price: True  ·  ilvl: `-0.04115`  ·  n_mods: `-0.01106`  ·  n_top_tier: `0.65960`  ·  corrupted: `-0.00788`  ·  n_sockets: `0.01894`  ·  quality: `0.03947`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 1.80173 |
| `explicit.stat_2250533757@T1` | 1.34508 |
| `explicit.stat_3917489142@T2` | -0.76749 |
| `explicit.stat_3299347043@T1` | -0.74391 |
| `explicit.stat_2339757871@T1` | -0.73991 |
| `explicit.stat_2923486259@T2` | -0.70556 |
| `explicit.stat_2160282525@T1` | -0.69579 |
| `explicit.stat_3917489142@T1` | -0.69498 |
| `explicit.stat_1671376347@T2` | -0.68684 |
| `explicit.stat_1062208444@T2` | -0.68214 |
| `explicit.stat_3484657501@T2` | -0.68076 |
| `explicit.stat_53045048@T1` | -0.67466 |

### armour.gloves — n=30485, R²=-1.9274

intercept: `3.6224`  ·  log_price: True  ·  ilvl: `-0.04555`  ·  n_mods: `-0.00659`  ·  n_top_tier: `0.47324`  ·  corrupted: `0.02243`  ·  n_sockets: `0.02965`  ·  quality: `0.04387`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 2.44162 |
| `rune.stat_201332984` | -2.25161 |
| `explicit.stat_1671376347@T1` | 1.10766 |
| `explicit.stat_9187492@T1` | 0.89794 |
| `explicit.stat_9187492@T2` | -0.76233 |
| `explicit.stat_1999113824@T1` | 0.60639 |
| `explicit.stat_3484657501@T2` | -0.59002 |
| `explicit.stat_3321629045@T2` | -0.55164 |
| `explicit.stat_3484657501@T1` | -0.54513 |
| `explicit.stat_803737631@T2` | -0.53123 |
| `explicit.stat_4052037485@T1` | -0.51245 |
| `explicit.stat_1999113824@T2` | -0.50624 |

### weapon.wand — n=19329, R²=-2.1956

intercept: `3.5769`  ·  log_price: True  ·  ilvl: `-0.04416`  ·  n_mods: `-0.02016`  ·  n_top_tier: `0.68856`  ·  corrupted: `0.03083`  ·  n_sockets: `0.03540`  ·  quality: `0.00701`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -2.49971 |
| `explicit.stat_1545858329@T1` | 2.44615 |
| `explicit.stat_2254480358@T1` | 2.42624 |
| `explicit.stat_4226189338@T1` | 1.72117 |
| `explicit.stat_591105508@T1` | 1.65663 |
| `explicit.stat_124131830@T1` | 1.62573 |
| `explicit.stat_736967255@T2` | 1.53642 |
| `crafted.stat_124131830` | 1.22902 |
| `explicit.stat_1600707273@T2` | -0.85820 |
| `explicit.stat_1263695895@T2` | -0.81316 |
| `explicit.stat_1263695895@T1` | -0.78378 |
| `explicit.stat_737908626@T1` | -0.78211 |

### weapon.bow — n=15477, R²=-1.9472

intercept: `3.7164`  ·  log_price: True  ·  ilvl: `-0.04498`  ·  n_mods: `-0.03677`  ·  n_top_tier: `0.61881`  ·  corrupted: `-0.06157`  ·  n_sockets: `0.00379`  ·  quality: `0.03524`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.12369 |
| `explicit.stat_1202301673@T1` | 1.64766 |
| `crafted.stat_3035140377` | 1.45317 |
| `explicit.stat_2463230181@T2` | -0.90946 |
| `explicit.stat_1263695895@T2` | -0.83901 |
| `explicit.stat_1263695895@T1` | -0.82870 |
| `explicit.stat_1940865751@T1` | 0.75455 |
| `explicit.stat_518292764@T2` | -0.73901 |
| `explicit.stat_3695891184@T2` | -0.72949 |
| `explicit.stat_3695891184@T1` | -0.69275 |
| `explicit.stat_1037193709@T1` | -0.68639 |
| `explicit.stat_1509134228@T1` | -0.68579 |

### weapon.crossbow — n=14546, R²=-1.8955

intercept: `3.8886`  ·  log_price: True  ·  ilvl: `-0.04752`  ·  n_mods: `-0.03608`  ·  n_top_tier: `0.80656`  ·  corrupted: `0.03838`  ·  n_sockets: `0.04171`  ·  quality: `0.00649`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.95380 |
| `explicit.stat_2250681686@T2` | -1.63720 |
| `explicit.stat_1202301673@T1` | 1.25645 |
| `explicit.stat_1980802737` | 1.14106 |
| `explicit.stat_1263695895@T1` | -1.02469 |
| `explicit.stat_1263695895@T2` | -1.02364 |
| `explicit.stat_2250681686` | 0.93466 |
| `crafted.stat_3035140377` | 0.92212 |
| `explicit.stat_2694482655@T1` | -0.90839 |
| `explicit.stat_1509134228@T2` | -0.89570 |
| `explicit.stat_3695891184@T1` | -0.87380 |
| `explicit.stat_669069897@T1` | -0.86966 |

### flask.charm — n=14090, R²=-0.5645

intercept: `0.0192`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `2.91982`  ·  corrupted: `1.93902`  ·  quality: `0.00015`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.51654 |
| `explicit.stat_1056492907` | 3.15101 |
| `explicit.stat_828533480@T2` | -2.91984 |
| `explicit.stat_1120862500@T2` | -2.91982 |
| `explicit.stat_828533480@T1` | -2.91981 |
| `explicit.stat_3196823591@T2` | -2.91980 |
| `explicit.stat_2676834156@T2` | -2.91980 |
| `explicit.stat_2541588185@T2` | -2.91980 |
| `explicit.stat_1873752457@T2` | -2.91980 |
| `explicit.stat_388617051@T2` | -2.91980 |
| `explicit.stat_2365392475@T2` | -2.91978 |
| `explicit.stat_1873752457@T1` | -2.91978 |

### weapon.warstaff — n=9147, R²=-0.419

intercept: `-8.4997`  ·  log_price: True  ·  ilvl: `0.11526`  ·  n_mods: `-0.17782`  ·  n_top_tier: `0.43137`  ·  corrupted: `0.15815`  ·  n_sockets: `0.17782`  ·  quality: `0.05597`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.05508 |
| `crafted.stat_210067635@T2` | 0.97604 |
| `explicit.stat_328541901@T1` | -0.89660 |
| `explicit.stat_328541901@T2` | -0.76526 |
| `desecrated.stat_9187492` | 0.69690 |
| `explicit.stat_9187492@T1` | 0.63931 |
| `explicit.stat_1037193709@T1` | 0.63930 |
| `desecrated.stat_2231156303@T1` | 0.60815 |
| `desecrated.stat_2527686725@T1` | 0.60815 |
| `explicit.stat_1940865751@T1` | -0.55187 |
| `explicit.stat_518292764@T1` | -0.50651 |
| `crafted.stat_3035140377` | 0.48754 |

### weapon.staff — n=8560, R²=-0.4362

intercept: `-12.6421`  ·  log_price: True  ·  ilvl: `0.16446`  ·  n_mods: `-0.12319`  ·  n_top_tier: `0.49900`  ·  corrupted: `0.40657`  ·  n_sockets: `0.21799`  ·  quality: `0.04425`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 1.91036 |
| `explicit.stat_591105508@T1` | 1.35928 |
| `explicit.stat_4226189338@T1` | 1.17669 |
| `explicit.stat_293638271@T2` | -1.07355 |
| `explicit.stat_124131830@T2` | 1.03365 |
| `explicit.stat_3962278098@T2` | 0.95193 |
| `explicit.stat_124131830@T1` | 0.92428 |
| `explicit.stat_4226189338@T2` | 0.91773 |
| `explicit.stat_1263695895@T2` | -0.72437 |
| `explicit.stat_2505884597@T2` | -0.67049 |
| `explicit.stat_2968503605@T1` | -0.66832 |
| `explicit.stat_3291658075@T2` | 0.65987 |

### weapon.sceptre — n=8477, R²=-0.3676

intercept: `-18.0732`  ·  log_price: True  ·  ilvl: `0.22921`  ·  n_mods: `-0.03845`  ·  n_top_tier: `0.33773`  ·  corrupted: `0.50560`  ·  n_sockets: `0.22242`  ·  quality: `0.05159`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.61915 |
| `explicit.stat_2162097452@T2` | 1.59403 |
| `explicit.stat_1250712710@T2` | 1.24087 |
| `explicit.stat_3057012405@T1` | 1.13613 |
| `explicit.stat_1263695895@T1` | -0.93190 |
| `explicit.stat_1574590649@T1` | -0.80640 |
| `explicit.stat_1263695895@T2` | -0.79538 |
| `explicit.stat_2347036682@T2` | -0.70826 |
| `explicit.stat_289128254@T2` | -0.62005 |
| `explicit.stat_2854751904@T2` | -0.59183 |
| `explicit.stat_2347036682@T1` | 0.57500 |
| `explicit.stat_849987426@T1` | 0.52945 |

### weapon.spear — n=6985, R²=-0.4738

intercept: `-10.1255`  ·  log_price: True  ·  ilvl: `0.13806`  ·  n_mods: `-0.08475`  ·  n_top_tier: `0.67898`  ·  corrupted: `-0.00213`  ·  n_sockets: `0.28653`  ·  quality: `0.09300`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -2.52828 |
| `explicit.stat_1202301673@T1` | 2.10582 |
| `explicit.stat_1509134228@T1` | 1.48174 |
| `explicit.stat_9187492@T1` | 1.27338 |
| `explicit.stat_1037193709@T1` | -1.15910 |
| `explicit.stat_210067635@T1` | 1.04138 |
| `explicit.stat_1263695895@T2` | -0.99532 |
| `crafted.stat_3035140377` | 0.96907 |
| `explicit.stat_691932474@T1` | -0.87947 |
| `explicit.stat_1940865751@T2` | -0.85323 |
| `explicit.stat_55876295@T1` | -0.83092 |
| `explicit.stat_1037193709@T2` | -0.67033 |

### armour.focus — n=5712, R²=-0.3918

intercept: `-12.1551`  ·  log_price: True  ·  ilvl: `0.15640`  ·  n_mods: `-0.16763`  ·  n_top_tier: `0.79855`  ·  corrupted: `0.37726`  ·  n_sockets: `0.48884`  ·  quality: `0.08339`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 5.88199 |
| `crafted.stat_737908626@T2` | 1.71125 |
| `explicit.stat_3962278098@T1` | -1.39703 |
| `explicit.stat_3291658075@T1` | -1.26057 |
| `explicit.stat_4220027924@T2` | -1.22207 |
| `explicit.stat_2231156303@T2` | -1.06628 |
| `explicit.stat_2231156303@T1` | -1.02079 |
| `explicit.stat_2974417149@T2` | -0.94740 |
| `explicit.stat_736967255@T2` | -0.93598 |
| `explicit.stat_2974417149@T1` | -0.88277 |
| `explicit.stat_2339757871@T1` | -0.87722 |
| `explicit.stat_2923486259@T1` | -0.87179 |

### armour.quiver — n=5354, R²=-0.3537

intercept: `-13.2939`  ·  log_price: True  ·  ilvl: `0.16091`  ·  n_mods: `-0.10584`  ·  n_top_tier: `0.72661`  ·  corrupted: `0.57048`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.26496 |
| `explicit.stat_2463230181@T1` | 1.91132 |
| `explicit.stat_4067062424@T1` | -1.12573 |
| `explicit.stat_2321178454@T2` | -1.10111 |
| `explicit.stat_681332047@T2` | -1.05406 |
| `explicit.stat_1573130764@T1` | -1.03334 |
| `explicit.stat_803737631@T2` | -1.01661 |
| `explicit.stat_2194114101@T2` | -0.92643 |
| `explicit.stat_2463230181@T2` | 0.89082 |
| `explicit.stat_4067062424@T2` | -0.86349 |
| `explicit.stat_2321178454@T1` | -0.81255 |
| `explicit.stat_803737631@T1` | -0.79590 |

### armour.shield — n=4659, R²=-0.5196

intercept: `-9.5183`  ·  log_price: True  ·  ilvl: `0.12440`  ·  n_mods: `-0.07585`  ·  n_top_tier: `0.55053`  ·  corrupted: `-0.31496`  ·  n_sockets: `0.15616`  ·  quality: `0.06249`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.61205 |
| `explicit.stat_3484657501@T2` | -1.12282 |
| `explicit.stat_3484657501@T1` | -1.06042 |
| `explicit.stat_2481353198@T2` | -1.02385 |
| `explicit.stat_1011760251@T2` | -0.96942 |
| `explicit.stat_2339757871@T1` | -0.92257 |
| `explicit.stat_2481353198@T1` | -0.91857 |
| `explicit.stat_2923486259@T2` | -0.88311 |
| `explicit.stat_3299347043@T1` | -0.88270 |
| `explicit.stat_3033371881@T2` | -0.84275 |
| `explicit.stat_3321629045@T2` | -0.82527 |
| `explicit.stat_3855016469@T1` | -0.80783 |

### weapon.twomace — n=4267, R²=-0.5115

intercept: `-8.8380`  ·  log_price: True  ·  ilvl: `0.11909`  ·  n_mods: `-0.17072`  ·  n_top_tier: `0.28880`  ·  corrupted: `0.06356`  ·  n_sockets: `0.12302`  ·  quality: `0.04321`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.27109 |
| `desecrated.stat_1509134228@T1` | 3.17772 |
| `explicit.stat_1037193709@T1` | -1.58092 |
| `explicit.stat_3336890334@T1` | -0.89083 |
| `crafted.stat_3035140377` | 0.88354 |
| `explicit.stat_387439868@T2` | -0.70558 |
| `explicit.stat_1037193709@T2` | -0.69916 |
| `explicit.stat_518292764@T2` | -0.61225 |
| `explicit.stat_210067635@T2` | 0.60176 |
| `explicit.stat_210067635@T1` | 0.45936 |
| `explicit.stat_9187492@T1` | -0.44024 |
| `explicit.stat_691932474@T1` | -0.43211 |

## Coverage (listings per base)

- … **Sapphire** — 25768 listings (25722 priced) [0.3–87761642.7 ex]
- … **Emerald** — 25231 listings (25199 priced) [0.3–87761642.7 ex]
- … **Ruby** — 19334 listings (19314 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 10097 listings (10082 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 8513 listings (8497 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 8278 listings (8257 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 8149 listings (8142 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 7731 listings (7716 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 7601 listings (7583 priced) [0.2–91750808.2 ex]
- … **Stellar Amulet** — 7592 listings (7583 priced) [0.3–91750808.2 ex]
- … **Sapphire Ring** — 6340 listings (6332 priced) [0.2–307202867.9 ex]
- … **Dueling Wand** — 6170 listings (6152 priced) [0.3–4297682211.9 ex]
- … **Topaz Ring** — 6078 listings (6073 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 6065 listings (6059 priced) [0.2–91750808.2 ex]
- … **Plate Belt** — 5405 listings (5382 priced) [0.3–398912568423.8 ex]
- … **Lapis Amulet** — 5382 listings (5377 priced) [0.3–19945827.9 ex]
- … **Amber Amulet** — 5254 listings (5248 priced) [0.3–3985176410.3 ex]
- … **Jade Amulet** — 5238 listings (5229 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 5235 listings (5222 priced) [0.2–24532814.5 ex]
- … **Ancestral Tiara** — 5222 listings (5204 priced) [0.6–398912568423.8 ex]
- … **Bloodstone Amulet** — 5070 listings (5062 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 4932 listings (4925 priced) [0.2–275252424.7 ex]
- … **Heavy Belt** — 4813 listings (4805 priced) [0.3–398912568423.8 ex]
- … **Azure Amulet** — 4802 listings (4800 priced) [0.3–123132003.2 ex]
- … **Lunar Amulet** — 4763 listings (4752 priced) [0.3–91750808.2 ex]
