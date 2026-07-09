# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-09T06:01:21+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **361086** (360505 priced in exalted)
- Distinct bases: 960 · distinct mods: 2902 · mod rows: 1714437
- Sold signals: **29182** sold · 192758 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-09T05:50:43+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×20.77** (median |log error| 3.0336)
- Within ±30% of asking price: **16%**
- Skill vs constant-price guess: **+0.06** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.09** · typical error ×53.53 · ±30% 5% · n=52672
- Premium segment (60ex+): skill **+0.10** · typical error ×281.15 · ±30% 0% · n=32652

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 6949 | ×49.19 | 20% | +0.04 | +0.06 |
| accessory.amulet | 6540 | ×43.08 | 21% | +0.03 | +0.03 |
| jewel | 6188 | ×8.21 | 8% | +0.02 | +0.05 |
| accessory.belt | 5235 | ×11.37 | 5% | +0.02 | +0.03 |
| armour.chest | 5041 | ×11.84 | 7% | +0.08 | +0.11 |
| armour.helmet | 4953 | ×14.12 | 7% | +0.11 | +0.13 |
| armour.boots | 4629 | ×14.90 | 18% | +0.08 | +0.10 |
| armour.gloves | 4562 | ×22.28 | 16% | +0.06 | +0.07 |
| other | 4297 | ×9.80 | 38% | +0.06 | +0.14 |
| weapon.wand | 3014 | ×34.18 | 21% | +0.05 | +0.06 |
| weapon.bow | 2473 | ×23.30 | 19% | +0.09 | +0.09 |
| weapon.crossbow | 2291 | ×20.94 | 21% | +0.10 | +0.10 |
| weapon.warstaff | 1211 | ×55.00 | 17% | +0.07 | +0.07 |
| weapon.sceptre | 1105 | ×31.13 | 12% | +0.09 | +0.10 |
| weapon.staff | 1101 | ×43.33 | 16% | +0.06 | +0.08 |
| weapon.spear | 915 | ×40.00 | 17% | +0.04 | +0.05 |
| armour.focus | 757 | ×82.45 | 12% | +0.04 | +0.11 |
| armour.quiver | 741 | ×64.72 | 12% | +0.03 | +0.08 |
| flask.charm | 617 | ×40.00 | 35% | +0.00 | +0.02 |
| armour.shield | 606 | ×30.00 | 15% | +0.04 | +0.07 |
| weapon.twomace | 556 | ×20.00 | 17% | +0.06 | +0.09 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=36559, R²=-0.5835

intercept: `1.6078`  ·  log_price: True  ·  ilvl: `0.00002`  ·  n_mods: `0.00372`  ·  n_top_tier: `0.35947`  ·  corrupted: `0.68809`  ·  n_sockets: `-0.00003`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_2974417149@T1` | 0.87963 |
| `explicit.stat_3291658075@T1` | 0.81508 |
| `explicit.stat_101878827@T1` | -0.71394 |
| `explicit.stat_2482852589@T1` | 0.56474 |
| `explicit.stat_1050105434@T1` | -0.50189 |
| `explicit.stat_3917489142@T1` | 0.44883 |
| `explicit.stat_2106365538@T1` | 0.40213 |
| `explicit.stat_2891184298@T1` | 0.38127 |
| `explicit.stat_789117908@T1` | -0.26939 |
| `implicit.stat_1379411836` | -0.23047 |
| `implicit.stat_4041853756` | 0.22990 |
| `implicit.stat_3879011313` | 0.22988 |

### jewel — n=33482, R²=-0.6441

intercept: `-1.2067`  ·  log_price: True  ·  ilvl: `0.03682`  ·  n_mods: `0.21311`  ·  n_top_tier: `-0.07251`  ·  corrupted: `0.16329`  ·  quality: `0.22377`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -4.89960 |
| `explicit.stat_3741323227@T1` | -3.30121 |
| `explicit.stat_1569101201@T1` | 2.85098 |
| `explicit.stat_234296660@T1` | -2.78428 |
| `explicit.stat_3780644166@T1` | -2.72649 |
| `explicit.stat_2527686725@T1` | 2.43692 |
| `explicit.stat_3374165039@T1` | -2.08984 |
| `explicit.stat_1315743832@T1` | 1.93903 |
| `explicit.stat_1697951953@T1` | -1.73975 |
| `explicit.stat_3714003708@T1` | -1.67392 |
| `explicit.stat_1316278494@T1` | -1.64362 |
| `explicit.stat_3485067555@T1` | 1.64055 |

### accessory.ring — n=31911, R²=-1.9531

intercept: `4.2048`  ·  log_price: True  ·  ilvl: `-0.05102`  ·  n_mods: `0.00176`  ·  n_top_tier: `0.00856`  ·  corrupted: `1.06289`  ·  n_sockets: `-0.03828`  ·  quality: `0.06797`

| stat_id | coef |
|---|---|
| `explicit.stat_1671376347@T1` | 0.67599 |
| `explicit.stat_707457662@T1` | 0.45783 |
| `explicit.stat_707457662@T2` | 0.38434 |
| `explicit.stat_2923486259@T1` | 0.29096 |
| `explicit.stat_1573130764@T2` | 0.26268 |
| `explicit.stat_3032590688@T1` | 0.20817 |
| `explicit.stat_1379411836@T1` | -0.18611 |
| `implicit.stat_2748665614` | -0.17557 |
| `explicit.stat_2891184298@T1` | 0.14472 |
| `implicit.stat_2923486259` | -0.14233 |
| `explicit.stat_2923486259` | -0.13731 |
| `pseudo.total_chaos_res` | 0.13635 |

### accessory.amulet — n=30037, R²=-2.0911

intercept: `3.9187`  ·  log_price: True  ·  ilvl: `-0.04716`  ·  n_mods: `-0.02518`  ·  n_top_tier: `0.63605`  ·  corrupted: `0.10420`  ·  n_sockets: `1.76880`  ·  quality: `-0.00286`

| stat_id | coef |
|---|---|
| `explicit.stat_3981240776@T2` | 1.14972 |
| `explicit.stat_983749596@T1` | -1.13473 |
| `explicit.stat_124131830` | 1.08106 |
| `explicit.stat_983749596@T2` | -0.98285 |
| `explicit.stat_3981240776@T1` | 0.93315 |
| `explicit.stat_3299347043@T1` | -0.82074 |
| `explicit.stat_472520716@T2` | -0.70383 |
| `explicit.stat_3917489142@T2` | -0.70083 |
| `explicit.stat_3917489142@T1` | -0.70002 |
| `explicit.stat_2748665614@T2` | -0.69776 |
| `explicit.stat_472520716@T1` | -0.69569 |
| `explicit.stat_3299347043@T2` | -0.69141 |

### accessory.belt — n=23931, R²=-0.4581

intercept: `6.2829`  ·  log_price: True  ·  ilvl: `-0.04423`  ·  n_mods: `-0.43236`  ·  n_top_tier: `0.78405`  ·  corrupted: `0.70300`  ·  n_sockets: `0.00239`

| stat_id | coef |
|---|---|
| `explicit.stat_1389754388@T1` | -1.45339 |
| `explicit.stat_51994685@T1` | -1.20004 |
| `explicit.stat_3325883026@T1` | -1.12000 |
| `explicit.stat_2881298780@T1` | -1.09183 |
| `explicit.stat_1389754388@T2` | -1.00138 |
| `explicit.stat_2881298780@T2` | -0.95742 |
| `explicit.stat_644456512@T1` | -0.94702 |
| `explicit.stat_2923486259@T2` | -0.92821 |
| `explicit.stat_809229260@T2` | -0.88249 |
| `explicit.stat_4220027924@T2` | -0.87474 |
| `explicit.stat_915769802@T2` | -0.87451 |
| `implicit.stat_731781020` | -0.86637 |

### armour.chest — n=23677, R²=-1.0071

intercept: `4.2449`  ·  log_price: True  ·  ilvl: `-0.04959`  ·  n_mods: `-0.09916`  ·  n_top_tier: `0.47538`  ·  corrupted: `0.06401`  ·  n_sockets: `0.10109`  ·  quality: `0.02821`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.03555 |
| `explicit.stat_915769802@T1` | -0.85489 |
| `explicit.stat_2923486259@T1` | -0.77975 |
| `explicit.stat_3325883026@T2` | -0.73247 |
| `explicit.stat_4080418644@T2` | -0.70060 |
| `explicit.stat_4015621042@T2` | -0.66918 |
| `explicit.stat_915769802@T2` | -0.66738 |
| `explicit.stat_3321629045@T1` | -0.65312 |
| `explicit.stat_986397080@T2` | -0.64254 |
| `explicit.stat_4080418644@T1` | -0.62460 |
| `explicit.stat_3484657501@T1` | -0.61030 |
| `explicit.stat_4015621042@T1` | -0.60268 |

### armour.helmet — n=23167, R²=-1.0856

intercept: `4.2893`  ·  log_price: True  ·  ilvl: `-0.05383`  ·  n_mods: `-0.08100`  ·  n_top_tier: `0.49555`  ·  corrupted: `0.81755`  ·  n_sockets: `0.01730`  ·  quality: `0.04019`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 2.86935 |
| `explicit.stat_2339757871@T1` | -2.12922 |
| `explicit.stat_3362812763@T1` | -0.98106 |
| `explicit.stat_53045048@T1` | -0.89875 |
| `explicit.stat_53045048@T2` | -0.88474 |
| `explicit.stat_1263695895@T1` | -0.78512 |
| `explicit.stat_587431675@T2` | -0.75328 |
| `explicit.stat_3372524247@T2` | -0.66511 |
| `explicit.stat_2162097452@T2` | -0.65887 |
| `explicit.stat_1999113824@T1` | -0.64389 |
| `explicit.stat_328541901@T2` | -0.63812 |
| `explicit.stat_803737631@T2` | -0.63562 |

### armour.boots — n=21721, R²=-1.4242

intercept: `3.9329`  ·  log_price: True  ·  ilvl: `-0.04832`  ·  n_mods: `-0.02805`  ·  n_top_tier: `0.48783`  ·  corrupted: `0.19306`  ·  n_sockets: `0.02937`  ·  quality: `0.02575`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | -5.37515 |
| `explicit.stat_2250533757@T1` | 1.70698 |
| `desecrated.stat_2250533757@T2` | -0.84222 |
| `explicit.stat_2923486259@T1` | 0.64988 |
| `explicit.stat_2923486259@T2` | -0.62453 |
| `explicit.stat_3917489142@T2` | -0.60672 |
| `explicit.stat_3362812763@T1` | -0.58843 |
| `explicit.stat_2160282525@T1` | -0.57515 |
| `explicit.stat_1062208444@T2` | -0.57282 |
| `explicit.stat_2339757871@T1` | -0.57214 |
| `explicit.stat_99927264@T1` | -0.55152 |
| `explicit.stat_2160282525@T2` | -0.54786 |

### armour.gloves — n=21168, R²=-1.6095

intercept: `4.0227`  ·  log_price: True  ·  ilvl: `-0.05149`  ·  n_mods: `-0.02756`  ·  n_top_tier: `0.46394`  ·  corrupted: `0.01328`  ·  n_sockets: `0.09328`  ·  quality: `0.03737`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -0.87237 |
| `explicit.stat_681332047@T2` | -0.78518 |
| `explicit.stat_9187492@T1` | 0.74810 |
| `explicit.stat_9187492@T2` | -0.70706 |
| `explicit.stat_803737631@T2` | -0.60811 |
| `explicit.stat_3484657501@T2` | -0.60731 |
| `explicit.stat_3321629045@T1` | -0.59674 |
| `explicit.stat_3032590688@T1` | -0.57962 |
| `explicit.stat_328541901@T2` | -0.54799 |
| `explicit.stat_4080418644@T1` | -0.54297 |
| `explicit.stat_3299347043@T2` | -0.53246 |
| `explicit.stat_803737631@T1` | -0.53144 |

### weapon.wand — n=14234, R²=-2.1834

intercept: `3.3965`  ·  log_price: True  ·  ilvl: `-0.04228`  ·  n_mods: `-0.01008`  ·  n_top_tier: `0.22143`  ·  corrupted: `-0.03755`  ·  n_sockets: `0.02827`  ·  quality: `0.00595`

| stat_id | coef |
|---|---|
| `explicit.stat_2254480358@T1` | 2.65795 |
| `explicit.stat_591105508@T1` | 2.13278 |
| `explicit.stat_4226189338@T1` | 2.12190 |
| `explicit.stat_1545858329@T1` | 2.11395 |
| `explicit.stat_736967255@T2` | 1.91844 |
| `explicit.stat_124131830@T1` | 1.45122 |
| `explicit.stat_1600707273@T1` | 1.16315 |
| `crafted.stat_124131830` | 0.85074 |
| `explicit.stat_1600707273@T2` | 0.74327 |
| `explicit.stat_2974417149@T1` | 0.51384 |
| `explicit.stat_2231156303@T2` | -0.26422 |
| `explicit.stat_2768835289@T2` | -0.26011 |

### weapon.bow — n=11596, R²=-1.9714

intercept: `3.4028`  ·  log_price: True  ·  ilvl: `-0.04204`  ·  n_mods: `-0.01123`  ·  n_top_tier: `0.67700`  ·  corrupted: `0.31337`  ·  n_sockets: `0.00143`  ·  quality: `0.00887`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -2.08764 |
| `explicit.stat_2463230181@T1` | 1.58374 |
| `explicit.stat_1202301673@T1` | 1.46319 |
| `rune.stat_3885405204` | -1.41065 |
| `crafted.stat_3035140377` | 1.36440 |
| `explicit.stat_55876295@T1` | -0.73860 |
| `explicit.stat_1037193709@T1` | -0.72320 |
| `explicit.stat_3261801346@T1` | -0.70721 |
| `explicit.stat_3695891184@T2` | -0.70296 |
| `explicit.stat_3336890334@T2` | -0.70200 |
| `explicit.stat_3695891184@T1` | -0.69739 |
| `explicit.stat_2694482655@T1` | -0.69616 |

### weapon.crossbow — n=10883, R²=-1.9068

intercept: `3.5808`  ·  log_price: True  ·  ilvl: `-0.04432`  ·  n_mods: `-0.00724`  ·  n_top_tier: `0.52875`  ·  corrupted: `-0.04223`  ·  n_sockets: `0.01746`  ·  quality: `0.00144`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.83215 |
| `explicit.stat_1202301673@T1` | 1.67470 |
| `explicit.stat_709508406@T1` | 1.58696 |
| `explicit.stat_2250681686@T2` | -1.42307 |
| `explicit.stat_1980802737` | 1.25636 |
| `explicit.stat_1509134228@T1` | 1.00544 |
| `explicit.stat_2250681686` | 0.89144 |
| `crafted.stat_3035140377` | 0.80916 |
| `rune.stat_669069897` | -0.70435 |
| `explicit.stat_1202301673@T2` | -0.63759 |
| `explicit.stat_1263695895@T2` | -0.61125 |
| `explicit.stat_1509134228@T2` | -0.60735 |

### flask.charm — n=8203, R²=-0.433

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00283`  ·  corrupted: `0.52879`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.38952 |
| `explicit.stat_1056492907` | 3.21882 |
| `explicit.stat_2676834156@T1` | 1.60658 |
| `explicit.stat_2541588185@T1` | 0.06409 |
| `explicit.stat_2678930256` | 0.02192 |
| `explicit.stat_3138344128` | 0.02139 |
| `explicit.stat_1120862500@T2` | -0.00284 |
| `explicit.stat_828533480@T2` | -0.00284 |
| `explicit.stat_1873752457@T2` | -0.00284 |
| `explicit.stat_388617051@T2` | -0.00283 |
| `explicit.stat_3196823591@T2` | -0.00283 |
| `explicit.stat_1873752457@T1` | -0.00283 |

### weapon.warstaff — n=5823, R²=-0.5802

intercept: `-0.0060`  ·  log_price: True  ·  ilvl: `0.00008`  ·  n_mods: `-0.00013`  ·  n_top_tier: `0.37415`  ·  corrupted: `0.50484`  ·  n_sockets: `0.00013`  ·  quality: `0.04031`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.38549 |
| `rune.stat_731403740` | 1.23701 |
| `explicit.stat_9187492@T1` | 1.02746 |
| `crafted.stat_210067635@T2` | -0.62712 |
| `desecrated.stat_9187492` | 0.47709 |
| `rune.stat_1712188793` | -0.47238 |
| `explicit.stat_1509134228@T1` | -0.37452 |
| `explicit.stat_328541901@T1` | -0.37450 |
| `explicit.stat_328541901@T2` | -0.37447 |
| `explicit.stat_821021828@T1` | -0.37439 |
| `explicit.stat_709508406@T1` | -0.37436 |
| `explicit.stat_3336890334@T2` | -0.37435 |

### weapon.staff — n=5384, R²=-0.6199

intercept: `-0.0605`  ·  log_price: True  ·  ilvl: `0.00075`  ·  n_mods: `-0.00011`  ·  n_top_tier: `0.00476`  ·  corrupted: `0.00255`  ·  n_sockets: `0.00245`  ·  quality: `0.00050`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 4.63079 |
| `explicit.stat_4226189338@T1` | 2.36271 |
| `explicit.stat_2254480358@T1` | 1.60188 |
| `explicit.stat_2254480358@T2` | 1.59791 |
| `explicit.stat_2768835289@T2` | 1.58511 |
| `explicit.stat_4226189338@T2` | 1.53293 |
| `explicit.stat_1545858329@T1` | 1.48746 |
| `explicit.stat_3291658075@T2` | 1.09851 |
| `explicit.stat_1600707273@T1` | 1.09284 |
| `explicit.stat_124131830@T1` | 0.82258 |
| `explicit.stat_3962278098@T2` | 0.76837 |
| `explicit.stat_473429811@T1` | 0.69031 |

### weapon.sceptre — n=5360, R²=-0.601

intercept: `-2.0612`  ·  log_price: True  ·  ilvl: `0.02557`  ·  n_mods: `-0.01427`  ·  n_top_tier: `0.51229`  ·  corrupted: `1.21060`  ·  n_sockets: `0.06028`  ·  quality: `0.07992`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 1.85488 |
| `explicit.stat_3984865854@T1` | 0.92883 |
| `explicit.stat_4080418644@T1` | -0.61607 |
| `explicit.stat_4080418644@T2` | -0.55747 |
| `explicit.stat_1574590649@T1` | -0.55090 |
| `explicit.stat_1263695895@T1` | -0.55006 |
| `explicit.stat_1263695895@T2` | -0.53980 |
| `explicit.stat_2854751904@T1` | -0.53914 |
| `explicit.stat_1574590649@T2` | -0.53834 |
| `explicit.stat_2347036682@T2` | -0.53191 |
| `explicit.stat_1998951374@T1` | -0.52452 |
| `explicit.stat_328541901@T1` | -0.52382 |

### weapon.spear — n=4548, R²=-0.6326

intercept: `-0.0058`  ·  log_price: True  ·  ilvl: `0.00007`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.19532`  ·  corrupted: `-0.00001`  ·  n_sockets: `0.00015`  ·  quality: `0.04563`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673@T1` | 2.07544 |
| `explicit.stat_9187492@T1` | 1.31424 |
| `crafted.stat_3035140377` | 1.26048 |
| `explicit.stat_210067635@T1` | 0.90418 |
| `explicit.stat_3336890334@T1` | 0.72967 |
| `crafted.stat_518292764` | 0.56927 |
| `explicit.stat_55876295@T1` | -0.19548 |
| `explicit.stat_709508406@T2` | -0.19544 |
| `explicit.stat_691932474@T1` | -0.19542 |
| `explicit.stat_1263695895@T2` | -0.19541 |
| `explicit.stat_4080418644@T2` | -0.19540 |
| `explicit.stat_55876295@T2` | -0.19536 |

### armour.focus — n=3666, R²=-0.613

intercept: `-1.9685`  ·  log_price: True  ·  ilvl: `0.02429`  ·  n_mods: `-0.00388`  ·  n_top_tier: `0.73180`  ·  corrupted: `-0.00193`  ·  n_sockets: `0.07423`  ·  quality: `0.08872`

| stat_id | coef |
|---|---|
| `crafted.stat_737908626@T2` | -8.35541 |
| `crafted.stat_2974417149@T1` | -4.17098 |
| `explicit.stat_124131830@T2` | -0.79009 |
| `explicit.stat_789117908@T2` | -0.78504 |
| `explicit.stat_4220027924@T2` | -0.78034 |
| `explicit.stat_2974417149@T1` | -0.77383 |
| `explicit.stat_736967255@T2` | -0.77067 |
| `explicit.stat_2891184298@T2` | -0.76846 |
| `explicit.stat_2231156303@T2` | -0.76464 |
| `explicit.stat_4052037485@T2` | -0.75636 |
| `explicit.stat_328541901@T2` | -0.74685 |
| `explicit.stat_2923486259@T1` | -0.74403 |

### armour.quiver — n=3475, R²=-0.6076

intercept: `-1.4292`  ·  log_price: True  ·  ilvl: `0.01676`  ·  n_mods: `0.01015`  ·  n_top_tier: `1.16851`  ·  corrupted: `0.46486`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 12.17033 |
| `explicit.stat_2463230181@T2` | -1.68218 |
| `explicit.stat_681332047@T2` | -1.30604 |
| `explicit.stat_681332047@T1` | -1.26778 |
| `explicit.stat_1573130764@T1` | -1.23455 |
| `explicit.stat_1573130764@T2` | -1.22475 |
| `explicit.stat_2194114101@T2` | -1.22404 |
| `explicit.stat_1368271171@T2` | -1.21579 |
| `explicit.stat_1368271171@T1` | -1.18787 |
| `explicit.stat_3714003708@T2` | -1.18528 |
| `explicit.stat_2321178454@T2` | -1.18249 |
| `explicit.stat_3261801346@T1` | -1.17206 |

### armour.shield — n=2981, R²=-0.6007

intercept: `-0.0969`  ·  log_price: True  ·  ilvl: `0.00121`  ·  n_mods: `0.00027`  ·  n_top_tier: `0.49704`  ·  corrupted: `0.18971`  ·  n_sockets: `0.00064`  ·  quality: `0.06952`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297@T1` | 0.83933 |
| `explicit.stat_1978899297@T2` | -0.63344 |
| `explicit.stat_1011760251@T2` | -0.51119 |
| `explicit.stat_2339757871@T1` | -0.50341 |
| `explicit.stat_328541901@T1` | -0.50305 |
| `explicit.stat_3484657501@T1` | -0.50250 |
| `explicit.stat_2481353198@T2` | -0.50166 |
| `explicit.stat_2481353198@T1` | -0.50151 |
| `explicit.stat_328541901@T2` | -0.50086 |
| `explicit.stat_3484657501@T2` | -0.50021 |
| `explicit.stat_3372524247@T2` | -0.49998 |
| `explicit.stat_3033371881@T1` | -0.49942 |

### weapon.twomace — n=2671, R²=-0.6035

intercept: `-0.1822`  ·  log_price: True  ·  ilvl: `0.00231`  ·  n_mods: `-0.00055`  ·  n_top_tier: `0.75832`  ·  corrupted: `0.15406`  ·  n_sockets: `0.00490`  ·  quality: `0.00789`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.62447 |
| `crafted.stat_3035140377` | 1.24016 |
| `explicit.stat_3336890334@T1` | -0.77148 |
| `explicit.stat_1037193709@T1` | -0.76678 |
| `explicit.stat_387439868@T2` | -0.76622 |
| `explicit.stat_1263695895@T1` | -0.76411 |
| `explicit.stat_1263695895@T2` | -0.76394 |
| `explicit.stat_1037193709@T2` | -0.76243 |
| `explicit.stat_1509134228@T2` | -0.76229 |
| `explicit.stat_821021828@T2` | -0.76192 |
| `explicit.stat_3639275092@T2` | -0.76152 |
| `explicit.stat_691932474@T1` | -0.76136 |

## Coverage (listings per base)

- … **Sapphire** — 15836 listings (15814 priced) [0.2–7553463.8 ex]
- … **Emerald** — 15705 listings (15691 priced) [0.4–7553463.8 ex]
- … **Ruby** — 12150 listings (12138 priced) [0.2–308559482.1 ex]
- … **Utility Belt** — 7012 listings (7006 priced) [0.2–5288620.9 ex]
- … **Prismatic Ring** — 5549 listings (5543 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 5415 listings (5405 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 5314 listings (5311 priced) [0.2–4323655.9 ex]
- … **Stellar Amulet** — 5272 listings (5269 priced) [0.3–35690283.3 ex]
- … **Gold Amulet** — 5136 listings (5129 priced) [0.3–4894457.0 ex]
- … **Gold Ring** — 4945 listings (4941 priced) [0.2–24532814.5 ex]
- … **Dueling Wand** — 4479 listings (4470 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 4144 listings (4139 priced) [0.2–307202867.9 ex]
- … **Ruby Ring** — 4022 listings (4020 priced) [0.2–37474957.5 ex]
- … **Topaz Ring** — 4015 listings (4012 priced) [1.0–307202867.9 ex]
- … **Plate Belt** — 3653 listings (3648 priced) [0.2–5286174.1 ex]
- … **Lapis Amulet** — 3613 listings (3611 priced) [0.2–5286174.1 ex]
- … **Ancestral Tiara** — 3572 listings (3567 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 3535 listings (3534 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 3520 listings (3519 priced) [0.2–4547453.5 ex]
- … **Obliterator Bow** — 3441 listings (3432 priced) [0.4–42622633798.0 ex]
- … **Unset Ring** — 3402 listings (3401 priced) [0.2–24532814.5 ex]
- … **Heavy Belt** — 3391 listings (3390 priced) [0.2–4877938.3 ex]
- … **Bloodstone Amulet** — 3293 listings (3292 priced) [0.2–4275054.0 ex]
- … **Pearl Ring** — 3225 listings (3223 priced) [0.2–24532814.5 ex]
- … **Lunar Amulet** — 3151 listings (3149 priced) [0.2–4877938.3 ex]
