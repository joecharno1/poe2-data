# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-15T07:38:19+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **501157** (500112 priced in exalted)
- Distinct bases: 982 · distinct mods: 3095 · mod rows: 2378095
- Sold signals: **26337** sold · 279151 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-15T07:30:42+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×27.11** (median |log error| 3.2999)
- Within ±30% of asking price: **20%**
- Skill vs constant-price guess: **+0.06** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.11** · typical error ×76.96 · ±30% 4% · n=72283
- Premium segment (60ex+): skill **+0.11** · typical error ×356.06 · ±30% 0% · n=48265

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 9981 | ×51.41 | 21% | +0.06 | +0.07 |
| jewel | 9284 | ×9.62 | 5% | +0.04 | +0.07 |
| accessory.amulet | 9151 | ×50.23 | 21% | +0.02 | +0.03 |
| accessory.belt | 7092 | ×26.54 | 17% | +0.06 | +0.09 |
| armour.chest | 6936 | ×29.36 | 24% | +0.05 | +0.08 |
| armour.helmet | 6787 | ×29.52 | 20% | +0.05 | +0.08 |
| armour.boots | 6301 | ×34.95 | 24% | +0.05 | +0.06 |
| armour.gloves | 6168 | ×43.97 | 21% | +0.05 | +0.07 |
| other | 5469 | ×1.97 | 43% | +0.10 | +0.17 |
| weapon.wand | 3932 | ×36.94 | 19% | +0.07 | +0.09 |
| weapon.bow | 3138 | ×30.89 | 18% | +0.10 | +0.09 |
| weapon.crossbow | 2946 | ×28.93 | 20% | +0.08 | +0.11 |
| weapon.warstaff | 1788 | ×34.81 | 16% | +0.10 | +0.10 |
| weapon.staff | 1675 | ×56.86 | 15% | +0.09 | +0.08 |
| weapon.sceptre | 1659 | ×45.33 | 7% | +0.13 | +0.16 |
| weapon.spear | 1321 | ×80.73 | 16% | +0.08 | +0.08 |
| armour.focus | 1127 | ×38.87 | 8% | +0.13 | +0.14 |
| armour.quiver | 1067 | ×33.29 | 9% | +0.09 | +0.13 |
| flask.charm | 907 | ×50.00 | 35% | +0.03 | +0.05 |
| armour.shield | 881 | ×16.42 | 15% | +0.02 | +0.02 |
| weapon.twomace | 802 | ×22.08 | 14% | +0.06 | +0.09 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=50052, R²=-0.897

intercept: `-1.6093`  ·  log_price: True  ·  ilvl: `0.02772`  ·  n_mods: `0.56397`  ·  n_top_tier: `-0.14039`  ·  corrupted: `0.31560`  ·  quality: `0.22919`

| stat_id | coef |
|---|---|
| `explicit.stat_2301718443@T1` | 3.14912 |
| `explicit.stat_3192728503@T1` | -3.08721 |
| `explicit.stat_627767961@T1` | -2.54452 |
| `explicit.stat_3780644166@T1` | -2.38652 |
| `explicit.stat_1697447343@T1` | -2.29063 |
| `explicit.stat_1697951953@T1` | -2.19341 |
| `explicit.stat_924253255@T1` | -1.81608 |
| `explicit.stat_3166958180@T1` | -1.79851 |
| `explicit.stat_3174700878@T1` | 1.76502 |
| `explicit.stat_3091578504@T1` | -1.75861 |
| `explicit.stat_239367161@T1` | -1.71336 |
| `explicit.stat_3485067555@T1` | 1.69490 |

### other — n=48536, R²=-0.6229

intercept: `1.6059`  ·  log_price: True  ·  ilvl: `0.00004`  ·  n_mods: `0.01998`  ·  n_top_tier: `0.32701`  ·  corrupted: `0.29611`  ·  n_sockets: `-0.00006`  ·  quality: `-0.00001`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.45548 |
| `explicit.stat_2974417149@T1` | 0.45293 |
| `explicit.stat_3299347043@T1` | -0.37916 |
| `explicit.stat_2482852589@T1` | -0.30942 |
| `implicit.stat_3879011313` | 0.25305 |
| `explicit.stat_789117908@T1` | -0.24291 |
| `implicit.stat_2219129443` | 0.22836 |
| `implicit.stat_4041853756` | 0.22826 |
| `explicit.stat_2106365538@T1` | -0.14976 |
| `explicit.stat_3917489142@T1` | 0.13603 |
| `explicit.stat_1050105434@T1` | -0.13469 |
| `implicit.stat_1379411836` | -0.13376 |

### accessory.ring — n=45635, R²=-1.9835

intercept: `3.5577`  ·  log_price: True  ·  ilvl: `-0.04395`  ·  n_mods: `0.00144`  ·  n_top_tier: `0.84247`  ·  corrupted: `0.09828`  ·  n_sockets: `-0.07356`  ·  quality: `0.07004`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -0.89014 |
| `explicit.stat_2231156303@T1` | -0.88019 |
| `explicit.stat_3325883026@T1` | -0.87433 |
| `explicit.stat_1368271171@T2` | -0.87153 |
| `explicit.stat_803737631@T1` | -0.87146 |
| `explicit.stat_1263695895@T1` | -0.86818 |
| `explicit.stat_2144192055@T1` | -0.86727 |
| `explicit.stat_1263695895@T2` | -0.86287 |
| `explicit.stat_4220027924@T2` | -0.86196 |
| `explicit.stat_3962278098@T2` | -0.86076 |
| `explicit.stat_1050105434@T1` | -0.86042 |
| `explicit.stat_3291658075@T2` | -0.86035 |

### accessory.amulet — n=42199, R²=-2.1446

intercept: `3.8271`  ·  log_price: True  ·  ilvl: `-0.04669`  ·  n_mods: `-0.02595`  ·  n_top_tier: `1.03087`  ·  corrupted: `0.07029`  ·  n_sockets: `-0.12339`  ·  quality: `-0.00350`

| stat_id | coef |
|---|---|
| `explicit.stat_472520716@T2` | -1.11926 |
| `explicit.stat_472520716@T1` | -1.11369 |
| `explicit.stat_2748665614@T1` | -1.09811 |
| `explicit.stat_2162097452@T2` | -1.08727 |
| `explicit.stat_1050105434@T2` | -1.08551 |
| `explicit.stat_803737631@T1` | -1.07739 |
| `explicit.stat_2901986750@T1` | -1.07451 |
| `explicit.stat_2866361420@T2` | -1.07383 |
| `explicit.stat_3917489142@T2` | -1.07276 |
| `explicit.stat_2866361420@T1` | -1.07210 |
| `explicit.stat_2748665614@T2` | -1.07161 |
| `explicit.stat_2974417149@T1` | -1.07048 |

### accessory.belt — n=32529, R²=-1.4507

intercept: `4.5960`  ·  log_price: True  ·  ilvl: `-0.05524`  ·  n_mods: `-0.04845`  ·  n_top_tier: `1.25463`  ·  corrupted: `0.82962`  ·  n_sockets: `1.39929`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.95840 |
| `explicit.stat_3299347043@T2` | -1.37106 |
| `explicit.stat_2881298780@T1` | -1.36565 |
| `explicit.stat_1389754388@T1` | -1.35536 |
| `explicit.stat_51994685@T1` | -1.34147 |
| `explicit.stat_809229260@T2` | -1.32276 |
| `explicit.stat_1671376347@T2` | -1.28740 |
| `explicit.stat_4220027924@T2` | -1.28700 |
| `explicit.stat_644456512@T1` | -1.28532 |
| `explicit.stat_3325883026@T1` | -1.28215 |
| `explicit.stat_915769802@T2` | -1.27016 |
| `explicit.stat_51994685@T2` | -1.25961 |

### armour.chest — n=32173, R²=-1.7406

intercept: `3.4820`  ·  log_price: True  ·  ilvl: `-0.04297`  ·  n_mods: `-0.01317`  ·  n_top_tier: `0.40223`  ·  corrupted: `0.18372`  ·  n_sockets: `0.01514`  ·  quality: `0.03668`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.72389 |
| `explicit.stat_3981240776@T1` | 1.02579 |
| `explicit.stat_986397080@T2` | -0.45342 |
| `explicit.stat_4080418644@T1` | -0.44496 |
| `explicit.stat_4080418644@T2` | -0.44482 |
| `explicit.stat_3484657501@T1` | -0.42719 |
| `explicit.stat_3372524247@T2` | -0.42571 |
| `explicit.stat_2923486259@T2` | -0.42539 |
| `explicit.stat_2451402625@T2` | -0.42442 |
| `explicit.stat_986397080@T1` | -0.42407 |
| `explicit.stat_915769802@T2` | -0.42244 |
| `explicit.stat_915769802@T1` | -0.42201 |

### armour.helmet — n=31338, R²=-1.7049

intercept: `3.6426`  ·  log_price: True  ·  ilvl: `-0.04585`  ·  n_mods: `-0.02181`  ·  n_top_tier: `0.44051`  ·  corrupted: `0.73641`  ·  n_sockets: `0.01668`  ·  quality: `0.05302`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -4.01888 |
| `crafted.stat_3917489142@T1` | 2.54075 |
| `explicit.stat_1263695895@T1` | -0.69906 |
| `explicit.stat_1263695895@T2` | -0.61962 |
| `explicit.stat_3917489142@T2` | -0.57389 |
| `explicit.stat_3917489142@T1` | -0.49070 |
| `explicit.stat_53045048@T1` | -0.48968 |
| `explicit.stat_3261801346@T2` | -0.48945 |
| `explicit.stat_2162097452@T2` | -0.48191 |
| `explicit.stat_4052037485@T2` | -0.47864 |
| `explicit.stat_1999113824@T1` | -0.47712 |
| `explicit.stat_587431675@T2` | -0.47491 |

### armour.boots — n=29424, R²=-1.8079

intercept: `3.2917`  ·  log_price: True  ·  ilvl: `-0.04064`  ·  n_mods: `-0.00991`  ·  n_top_tier: `0.69374`  ·  corrupted: `-0.00900`  ·  n_sockets: `0.00789`  ·  quality: `0.02075`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.28040 |
| `explicit.stat_2339757871@T1` | -0.81625 |
| `explicit.stat_3917489142@T2` | -0.78347 |
| `desecrated.stat_2250533757@T2` | -0.75398 |
| `explicit.stat_3917489142@T1` | -0.73699 |
| `explicit.stat_2160282525@T1` | -0.72842 |
| `explicit.stat_3299347043@T1` | -0.71844 |
| `explicit.stat_4080418644@T1` | -0.71537 |
| `explicit.stat_2923486259@T2` | -0.71218 |
| `explicit.stat_3484657501@T2` | -0.71197 |
| `explicit.stat_1671376347@T2` | -0.71110 |
| `explicit.stat_53045048@T1` | -0.70965 |

### armour.gloves — n=28658, R²=-1.947

intercept: `3.5193`  ·  log_price: True  ·  ilvl: `-0.04425`  ·  n_mods: `-0.00460`  ·  n_top_tier: `0.52125`  ·  corrupted: `-0.00996`  ·  n_sockets: `0.02023`  ·  quality: `0.04895`

| stat_id | coef |
|---|---|
| `rune.stat_201332984` | -6.64198 |
| `explicit.stat_9187492@T1` | 0.87587 |
| `explicit.stat_1671376347@T1` | 0.86691 |
| `explicit.stat_9187492@T2` | -0.85143 |
| `explicit.stat_3484657501@T2` | -0.65951 |
| `explicit.stat_3484657501@T1` | -0.59411 |
| `explicit.stat_803737631@T2` | -0.58943 |
| `explicit.stat_4052037485@T1` | -0.58271 |
| `explicit.stat_3321629045@T2` | -0.58134 |
| `explicit.stat_803737631@T1` | -0.54719 |
| `explicit.stat_3321629045@T1` | -0.53771 |
| `explicit.stat_1573130764@T1` | -0.53424 |

### weapon.wand — n=18407, R²=-2.2817

intercept: `3.7823`  ·  log_price: True  ·  ilvl: `-0.04670`  ·  n_mods: `-0.01613`  ·  n_top_tier: `0.49849`  ·  corrupted: `-0.00706`  ·  n_sockets: `0.03744`  ·  quality: `0.00505`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 3.27135 |
| `rune.stat_124131830` | -3.16796 |
| `explicit.stat_2254480358@T1` | 2.78602 |
| `explicit.stat_4226189338@T1` | 1.85494 |
| `explicit.stat_591105508@T1` | 1.81251 |
| `explicit.stat_124131830@T1` | 1.75087 |
| `explicit.stat_736967255@T2` | 1.39587 |
| `crafted.stat_124131830` | 1.22614 |
| `explicit.stat_1263695895@T2` | -0.60941 |
| `explicit.stat_1263695895@T1` | -0.56911 |
| `explicit.stat_737908626@T1` | -0.56548 |
| `explicit.stat_2968503605@T1` | -0.55873 |

### weapon.bow — n=14808, R²=-1.9832

intercept: `3.4831`  ·  log_price: True  ·  ilvl: `-0.04188`  ·  n_mods: `-0.03719`  ·  n_top_tier: `0.62421`  ·  corrupted: `-0.09451`  ·  n_sockets: `0.00197`  ·  quality: `0.03228`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.07107 |
| `explicit.stat_1202301673@T1` | 1.58850 |
| `crafted.stat_3035140377` | 1.33337 |
| `explicit.stat_1263695895@T1` | -0.81349 |
| `explicit.stat_1263695895@T2` | -0.75707 |
| `explicit.stat_3695891184@T2` | -0.70168 |
| `explicit.stat_2463230181@T2` | -0.69902 |
| `explicit.stat_1509134228@T1` | -0.68226 |
| `explicit.stat_518292764@T2` | -0.68135 |
| `explicit.stat_3695891184@T1` | -0.68041 |
| `explicit.stat_1368271171@T2` | -0.67753 |
| `explicit.stat_2694482655@T2` | -0.66593 |

### weapon.crossbow — n=13987, R²=-1.9765

intercept: `3.9420`  ·  log_price: True  ·  ilvl: `-0.04821`  ·  n_mods: `-0.01636`  ·  n_top_tier: `0.74867`  ·  corrupted: `0.01557`  ·  n_sockets: `0.01679`  ·  quality: `0.00813`

| stat_id | coef |
|---|---|
| `explicit.stat_2250681686@T2` | -2.98896 |
| `explicit.stat_2250681686` | 2.32195 |
| `explicit.stat_1980802737@T2` | -2.01492 |
| `explicit.stat_709508406@T1` | 1.51585 |
| `explicit.stat_1202301673@T1` | 1.46959 |
| `explicit.stat_1980802737` | 1.19596 |
| `explicit.stat_1263695895@T2` | -0.93152 |
| `crafted.stat_3035140377` | 0.92645 |
| `explicit.stat_1263695895@T1` | -0.91127 |
| `explicit.stat_669069897@T1` | -0.80573 |
| `explicit.stat_1037193709@T1` | -0.78949 |
| `explicit.stat_1202301673@T2` | -0.78581 |

### flask.charm — n=12790, R²=-0.5369

intercept: `0.0046`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `2.78802`  ·  corrupted: `2.12442`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.34316 |
| `explicit.stat_1056492907` | 3.35105 |
| `explicit.stat_828533480@T2` | -2.78803 |
| `explicit.stat_2541588185@T2` | -2.78802 |
| `explicit.stat_2676834156@T2` | -2.78802 |
| `explicit.stat_1120862500@T2` | -2.78801 |
| `explicit.stat_1873752457@T2` | -2.78801 |
| `explicit.stat_828533480@T1` | -2.78801 |
| `explicit.stat_3196823591@T2` | -2.78800 |
| `explicit.stat_1873752457@T1` | -2.78800 |
| `explicit.stat_388617051@T2` | -2.78800 |
| `explicit.stat_1366840608@T2` | -2.78799 |

### weapon.warstaff — n=8515, R²=-0.4792

intercept: `-6.4959`  ·  log_price: True  ·  ilvl: `0.08930`  ·  n_mods: `-0.17270`  ·  n_top_tier: `0.66857`  ·  corrupted: `0.17865`  ·  n_sockets: `0.10565`  ·  quality: `0.05320`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.42889 |
| `explicit.stat_328541901@T1` | -1.17945 |
| `explicit.stat_328541901@T2` | -1.15101 |
| `explicit.stat_1037193709@T1` | 0.92192 |
| `explicit.stat_1037193709@T2` | -0.85428 |
| `explicit.stat_55876295@T2` | -0.84672 |
| `explicit.stat_1940865751@T1` | -0.73283 |
| `explicit.stat_55876295@T1` | -0.72617 |
| `desecrated.stat_9187492` | 0.72008 |
| `explicit.stat_210067635@T1` | -0.70629 |
| `explicit.stat_3695891184@T2` | -0.66291 |
| `explicit.stat_791928121@T2` | -0.66000 |

### weapon.staff — n=7959, R²=-0.4604

intercept: `-9.8419`  ·  log_price: True  ·  ilvl: `0.12838`  ·  n_mods: `-0.12842`  ·  n_top_tier: `0.45925`  ·  corrupted: `0.04244`  ·  n_sockets: `0.20067`  ·  quality: `0.04205`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830@T1` | 1.44547 |
| `explicit.stat_4226189338@T1` | 1.40829 |
| `explicit.stat_4226189338@T2` | 1.24809 |
| `explicit.stat_2254480358@T1` | 1.19893 |
| `explicit.stat_1600707273@T1` | 1.19257 |
| `explicit.stat_124131830@T2` | 1.17755 |
| `explicit.stat_1545858329@T1` | 1.14230 |
| `explicit.stat_2768835289@T2` | 1.02482 |
| `explicit.stat_591105508@T1` | 0.92589 |
| `explicit.stat_1263695895@T2` | -0.80059 |
| `explicit.stat_293638271@T2` | -0.78540 |
| `explicit.stat_3962278098@T2` | 0.68707 |

### weapon.sceptre — n=7884, R²=-0.4044

intercept: `-15.4888`  ·  log_price: True  ·  ilvl: `0.19609`  ·  n_mods: `-0.03860`  ·  n_top_tier: `0.52361`  ·  corrupted: `0.45839`  ·  n_sockets: `0.22910`  ·  quality: `0.05459`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.24124 |
| `explicit.stat_2162097452@T2` | 1.24600 |
| `explicit.stat_1263695895@T2` | -0.90204 |
| `explicit.stat_2347036682@T2` | -0.90144 |
| `explicit.stat_1263695895@T1` | -0.76550 |
| `explicit.stat_1574590649@T2` | -0.73373 |
| `explicit.stat_289128254@T2` | -0.71957 |
| `explicit.stat_1250712710@T2` | 0.70813 |
| `explicit.stat_4080418644@T1` | -0.65653 |
| `explicit.stat_2854751904@T1` | -0.65440 |
| `explicit.stat_1050105434@T2` | -0.63771 |
| `explicit.stat_3057012405@T1` | 0.61119 |

### weapon.spear — n=6532, R²=-0.5245

intercept: `-8.5052`  ·  log_price: True  ·  ilvl: `0.11493`  ·  n_mods: `-0.05831`  ·  n_top_tier: `0.72822`  ·  corrupted: `-0.15069`  ·  n_sockets: `0.20731`  ·  quality: `0.09788`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -2.39395 |
| `explicit.stat_1202301673@T1` | 1.91553 |
| `explicit.stat_9187492@T1` | 1.84131 |
| `explicit.stat_1263695895@T2` | -1.14560 |
| `desecrated.stat_210067635@T1` | -1.04462 |
| `crafted.stat_3035140377` | 1.03489 |
| `explicit.stat_55876295@T1` | -0.97395 |
| `explicit.stat_1509134228@T1` | 0.92229 |
| `explicit.stat_55876295@T2` | -0.84350 |
| `explicit.stat_1940865751@T2` | -0.82761 |
| `explicit.stat_1037193709@T1` | -0.81395 |
| `explicit.stat_3261801346@T2` | -0.79057 |

### armour.focus — n=5356, R²=-0.4293

intercept: `-11.0056`  ·  log_price: True  ·  ilvl: `0.14047`  ·  n_mods: `-0.15036`  ·  n_top_tier: `0.94216`  ·  corrupted: `0.75926`  ·  n_sockets: `0.42036`  ·  quality: `0.06705`

| stat_id | coef |
|---|---|
| `crafted.stat_737908626@T2` | 1.80105 |
| `explicit.stat_4220027924@T2` | -1.39624 |
| `explicit.stat_3962278098@T1` | -1.28710 |
| `explicit.stat_736967255@T2` | -1.23895 |
| `explicit.stat_3962278098@T2` | -1.23874 |
| `explicit.stat_2923486259@T1` | -1.18107 |
| `explicit.stat_3291658075@T1` | -1.13764 |
| `explicit.stat_737908626@T2` | -1.11766 |
| `explicit.stat_2974417149@T2` | -1.04592 |
| `explicit.stat_4015621042@T1` | -1.01236 |
| `explicit.stat_2231156303@T2` | -0.99322 |
| `explicit.stat_2231156303@T1` | -0.95548 |

### armour.quiver — n=4987, R²=-0.3764

intercept: `-11.1071`  ·  log_price: True  ·  ilvl: `0.13538`  ·  n_mods: `-0.05878`  ·  n_top_tier: `0.81519`  ·  corrupted: `0.45689`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 7.00294 |
| `explicit.stat_4067062424@T1` | -1.28310 |
| `explicit.stat_2321178454@T2` | -1.26033 |
| `explicit.stat_681332047@T2` | -1.15110 |
| `explicit.stat_803737631@T2` | -0.95911 |
| `explicit.stat_1573130764@T2` | -0.93479 |
| `explicit.stat_1573130764@T1` | -0.88009 |
| `explicit.stat_4067062424@T2` | -0.83760 |
| `explicit.stat_3261801346@T1` | -0.82948 |
| `explicit.stat_2321178454@T1` | -0.77404 |
| `explicit.stat_2463230181@T1` | 0.75313 |
| `explicit.stat_1241625305@T2` | -0.72467 |

### armour.shield — n=4345, R²=-0.5617

intercept: `-8.3929`  ·  log_price: True  ·  ilvl: `0.10885`  ·  n_mods: `-0.06374`  ·  n_top_tier: `0.46939`  ·  corrupted: `-0.10928`  ·  n_sockets: `0.10009`  ·  quality: `0.06100`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.17749 |
| `explicit.stat_2481353198@T2` | -0.91739 |
| `explicit.stat_2481353198@T1` | -0.88379 |
| `explicit.stat_1011760251@T1` | -0.86025 |
| `explicit.stat_1011760251@T2` | -0.83923 |
| `explicit.stat_2923486259@T2` | -0.77449 |
| `explicit.stat_328541901@T1` | -0.74933 |
| `explicit.stat_1978899297@T2` | -0.74008 |
| `explicit.stat_2339757871@T1` | -0.72428 |
| `explicit.stat_4095671657@T1` | -0.70763 |
| `explicit.stat_53045048@T1` | -0.67653 |
| `explicit.stat_3321629045@T2` | -0.66925 |

### weapon.twomace — n=4004, R²=-0.4969

intercept: `-9.1682`  ·  log_price: True  ·  ilvl: `0.12180`  ·  n_mods: `-0.16335`  ·  n_top_tier: `0.53431`  ·  corrupted: `0.43515`  ·  n_sockets: `0.17759`  ·  quality: `0.04061`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.13281 |
| `desecrated.stat_1509134228@T1` | 2.11297 |
| `explicit.stat_1037193709@T1` | -1.86553 |
| `explicit.stat_3336890334@T1` | -1.45088 |
| `crafted.stat_3035140377` | 1.12597 |
| `explicit.stat_518292764@T2` | -1.04416 |
| `explicit.stat_1263695895@T1` | -1.02953 |
| `explicit.stat_1263695895@T2` | -0.94399 |
| `explicit.stat_387439868@T2` | -0.91579 |
| `explicit.stat_1037193709@T2` | -0.86693 |
| `explicit.stat_3639275092@T1` | -0.83833 |
| `explicit.stat_3695891184@T1` | -0.74309 |

## Coverage (listings per base)

- … **Sapphire** — 23327 listings (23292 priced) [0.3–7553463.8 ex]
- … **Emerald** — 22945 listings (22915 priced) [0.3–7553463.8 ex]
- … **Ruby** — 17588 listings (17573 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 9519 listings (9510 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 7818 listings (7808 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 7620 listings (7607 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 7498 listings (7491 priced) [0.2–19945827.9 ex]
- … **Gold Amulet** — 7153 listings (7143 priced) [0.3–39887666593.4 ex]
- … **Stellar Amulet** — 7072 listings (7068 priced) [0.3–91750808.2 ex]
- … **Gold Ring** — 6999 listings (6986 priced) [0.2–91750808.2 ex]
- … **Dueling Wand** — 5858 listings (5842 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 5846 listings (5840 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 5596 listings (5591 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 5571 listings (5568 priced) [0.2–37474957.5 ex]
- … **Plate Belt** — 5050 listings (5034 priced) [0.3–398912568423.8 ex]
- … **Lapis Amulet** — 4997 listings (4992 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 4877 listings (4865 priced) [0.6–398912568423.8 ex]
- … **Amber Amulet** — 4853 listings (4849 priced) [0.3–3985176410.3 ex]
- … **Jade Amulet** — 4851 listings (4845 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 4809 listings (4802 priced) [0.2–24532814.5 ex]
- … **Bloodstone Amulet** — 4703 listings (4698 priced) [0.3–4275054.0 ex]
- … **Heavy Belt** — 4512 listings (4508 priced) [0.3–398912568423.8 ex]
- … **Pearl Ring** — 4508 listings (4502 priced) [0.2–275252424.7 ex]
- … **Obliterator Bow** — 4431 listings (4418 priced) [0.3–42622633798.0 ex]
- … **Azure Amulet** — 4423 listings (4423 priced) [0.3–123132003.2 ex]
