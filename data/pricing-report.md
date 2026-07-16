# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-16T04:27:56+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **535157** (533798 priced in exalted)
- Distinct bases: 986 · distinct mods: 3147 · mod rows: 2537346
- Sold signals: **25891** sold · 300978 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-16T04:20:24+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×25.63** (median |log error| 3.2437)
- Within ±30% of asking price: **18%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.13** · typical error ×72.27 · ±30% 5% · n=77313
- Premium segment (60ex+): skill **+0.12** · typical error ×331.56 · ±30% 0% · n=51765

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 10773 | ×52.35 | 22% | +0.05 | +0.07 |
| jewel | 10099 | ×9.79 | 5% | +0.05 | +0.09 |
| accessory.amulet | 9915 | ×46.43 | 20% | +0.03 | +0.03 |
| accessory.belt | 7523 | ×22.90 | 9% | +0.09 | +0.11 |
| armour.chest | 7345 | ×29.67 | 23% | +0.06 | +0.09 |
| armour.helmet | 7142 | ×28.33 | 17% | +0.07 | +0.09 |
| armour.boots | 6643 | ×32.24 | 23% | +0.06 | +0.07 |
| armour.gloves | 6511 | ×42.95 | 22% | +0.05 | +0.07 |
| other | 5963 | ×1.85 | 44% | +0.10 | +0.18 |
| weapon.wand | 4117 | ×33.94 | 17% | +0.07 | +0.08 |
| weapon.bow | 3207 | ×29.81 | 17% | +0.11 | +0.11 |
| weapon.crossbow | 3023 | ×26.05 | 18% | +0.09 | +0.12 |
| weapon.warstaff | 1842 | ×33.21 | 13% | +0.13 | +0.11 |
| weapon.sceptre | 1779 | ×46.03 | 6% | +0.16 | +0.16 |
| weapon.staff | 1752 | ×57.15 | 11% | +0.10 | +0.10 |
| weapon.spear | 1437 | ×53.04 | 16% | +0.09 | +0.09 |
| armour.focus | 1203 | ×38.94 | 7% | +0.14 | +0.17 |
| armour.quiver | 1140 | ×27.81 | 8% | +0.11 | +0.13 |
| flask.charm | 964 | ×29.97 | 34% | +0.04 | +0.07 |
| armour.shield | 948 | ×24.21 | 12% | +0.03 | +0.05 |
| weapon.twomace | 851 | ×16.50 | 13% | +0.07 | +0.07 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=54703, R²=-0.9246

intercept: `-1.7478`  ·  log_price: True  ·  ilvl: `0.02673`  ·  n_mods: `0.71340`  ·  n_top_tier: `-0.23541`  ·  corrupted: `0.32517`  ·  quality: `0.23113`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.12817 |
| `explicit.stat_2301718443@T1` | 3.00692 |
| `explicit.stat_3485067555@T1` | 2.17801 |
| `explicit.stat_3780644166@T1` | -2.09797 |
| `explicit.stat_627767961@T1` | -2.08746 |
| `explicit.stat_1805182458@T1` | -1.96573 |
| `explicit.stat_872504239@T1` | 1.76266 |
| `explicit.stat_3596695232@T1` | 1.62441 |
| `explicit.stat_239367161@T1` | -1.55368 |
| `explicit.stat_1697951953@T1` | -1.52948 |
| `explicit.stat_234296660@T1` | -1.50148 |
| `explicit.stat_1062710370@T1` | -1.47762 |

### other — n=51519, R²=-0.6412

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00001`  ·  n_top_tier: `0.34658`  ·  corrupted: `0.34638`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `implicit.stat_3879011313` | 0.37383 |
| `explicit.stat_3291658075@T1` | 0.36786 |
| `explicit.stat_3299347043@T1` | -0.35500 |
| `explicit.stat_2482852589@T1` | -0.29079 |
| `explicit.stat_2974417149@T1` | 0.28482 |
| `implicit.stat_2219129443` | 0.23377 |
| `implicit.stat_4041853756` | 0.23025 |
| `explicit.stat_2106365538@T1` | -0.15417 |
| `explicit.stat_1050105434@T1` | -0.13050 |
| `implicit.stat_1379411836` | -0.12765 |
| `explicit.stat_789117908@T1` | -0.09942 |
| `explicit.stat_3917489142@T1` | 0.09307 |

### accessory.ring — n=49377, R²=-1.9983

intercept: `3.4866`  ·  log_price: True  ·  ilvl: `-0.04301`  ·  n_mods: `0.00118`  ·  n_top_tier: `0.95339`  ·  corrupted: `0.03247`  ·  n_sockets: `2.18621`  ·  quality: `0.07069`

| stat_id | coef |
|---|---|
| `explicit.stat_3325883026@T1` | -0.98112 |
| `explicit.stat_2231156303@T1` | -0.97822 |
| `explicit.stat_803737631@T1` | -0.97695 |
| `explicit.stat_2144192055@T1` | -0.97340 |
| `explicit.stat_1368271171@T2` | -0.97195 |
| `explicit.stat_3325883026@T2` | -0.97076 |
| `explicit.stat_3291658075@T1` | -0.97059 |
| `explicit.stat_2231156303@T2` | -0.96854 |
| `explicit.stat_1263695895@T1` | -0.96759 |
| `explicit.stat_3291658075@T2` | -0.96692 |
| `explicit.stat_2891184298@T2` | -0.96625 |
| `explicit.stat_2901986750@T1` | -0.96541 |

### accessory.amulet — n=45382, R²=-2.1418

intercept: `3.7042`  ·  log_price: True  ·  ilvl: `-0.04540`  ·  n_mods: `-0.02277`  ·  n_top_tier: `0.97109`  ·  corrupted: `0.06844`  ·  n_sockets: `-0.09788`  ·  quality: `-0.00056`

| stat_id | coef |
|---|---|
| `explicit.stat_472520716@T2` | -1.05859 |
| `explicit.stat_2901986750@T1` | -1.04172 |
| `explicit.stat_803737631@T1` | -1.04066 |
| `explicit.stat_587431675@T2` | -1.03832 |
| `explicit.stat_472520716@T1` | -1.03028 |
| `explicit.stat_3299347043@T1` | -1.01883 |
| `explicit.stat_1050105434@T2` | -1.01497 |
| `explicit.stat_803737631@T2` | -1.01354 |
| `explicit.stat_3299347043@T2` | -1.01249 |
| `explicit.stat_2866361420@T2` | -1.01216 |
| `explicit.stat_3917489142@T2` | -1.00986 |
| `explicit.stat_3489782002@T2` | -1.00509 |

### accessory.belt — n=34561, R²=-1.1721

intercept: `5.6228`  ·  log_price: True  ·  ilvl: `-0.06279`  ·  n_mods: `-0.15537`  ·  n_top_tier: `1.22197`  ·  corrupted: `1.04699`  ·  n_sockets: `-0.15651`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T1` | -1.69477 |
| `explicit.stat_1389754388@T1` | -1.51984 |
| `explicit.stat_3299347043@T2` | -1.45693 |
| `explicit.stat_644456512@T1` | -1.42388 |
| `explicit.stat_2881298780@T1` | -1.40061 |
| `explicit.stat_809229260@T2` | -1.38756 |
| `explicit.stat_4220027924@T2` | -1.38377 |
| `explicit.stat_1671376347@T2` | -1.32413 |
| `explicit.stat_3325883026@T1` | -1.30915 |
| `explicit.stat_809229260@T1` | -1.28915 |
| `explicit.stat_644456512@T2` | -1.27958 |
| `explicit.stat_4080418644@T2` | -1.26080 |

### armour.chest — n=34249, R²=-1.7145

intercept: `3.5236`  ·  log_price: True  ·  ilvl: `-0.04350`  ·  n_mods: `-0.01498`  ·  n_top_tier: `0.52567`  ·  corrupted: `0.05957`  ·  n_sockets: `0.02001`  ·  quality: `0.05246`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.97587 |
| `explicit.stat_3981240776@T1` | 1.05248 |
| `explicit.stat_986397080@T2` | -0.60609 |
| `explicit.stat_986397080@T1` | -0.58318 |
| `explicit.stat_4015621042@T1` | -0.57105 |
| `explicit.stat_3484657501@T1` | -0.56489 |
| `explicit.stat_4080418644@T2` | -0.55508 |
| `explicit.stat_2451402625@T2` | -0.55451 |
| `explicit.stat_1692879867@T1` | -0.55436 |
| `explicit.stat_3372524247@T2` | -0.55181 |
| `explicit.stat_4080418644@T1` | -0.55165 |
| `explicit.stat_3261801346@T2` | -0.54497 |

### armour.helmet — n=33235, R²=-1.5933

intercept: `3.7427`  ·  log_price: True  ·  ilvl: `-0.04737`  ·  n_mods: `-0.03101`  ·  n_top_tier: `0.45040`  ·  corrupted: `0.79897`  ·  n_sockets: `0.06012`  ·  quality: `0.05634`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -5.74998 |
| `crafted.stat_3917489142@T1` | 0.85342 |
| `explicit.stat_3917489142@T2` | -0.67965 |
| `explicit.stat_1263695895@T1` | -0.64026 |
| `explicit.stat_1263695895@T2` | -0.60817 |
| `explicit.stat_4052037485@T2` | -0.56723 |
| `explicit.stat_3917489142@T1` | -0.55856 |
| `explicit.stat_1999113824@T1` | -0.54561 |
| `explicit.stat_2162097452@T2` | -0.53583 |
| `explicit.stat_3321629045@T2` | -0.51639 |
| `explicit.stat_803737631@T1` | -0.50420 |
| `explicit.stat_3261801346@T1` | -0.49913 |

### armour.boots — n=31133, R²=-1.799

intercept: `3.2871`  ·  log_price: True  ·  ilvl: `-0.04055`  ·  n_mods: `-0.00983`  ·  n_top_tier: `0.70723`  ·  corrupted: `-0.00908`  ·  n_sockets: `0.01891`  ·  quality: `0.03408`

| stat_id | coef |
|---|---|
| `explicit.stat_2250533757@T1` | 1.16539 |
| `crafted.stat_3917489142@T1` | 0.91561 |
| `explicit.stat_2339757871@T1` | -0.84626 |
| `explicit.stat_3917489142@T2` | -0.80256 |
| `explicit.stat_3299347043@T1` | -0.76765 |
| `explicit.stat_2923486259@T2` | -0.74249 |
| `explicit.stat_3917489142@T1` | -0.73757 |
| `explicit.stat_2160282525@T1` | -0.73643 |
| `explicit.stat_1671376347@T2` | -0.73054 |
| `explicit.stat_99927264@T1` | -0.72720 |
| `explicit.stat_3484657501@T2` | -0.72694 |
| `explicit.stat_1062208444@T2` | -0.72576 |

### armour.gloves — n=30296, R²=-1.9663

intercept: `3.5498`  ·  log_price: True  ·  ilvl: `-0.04450`  ·  n_mods: `-0.00740`  ·  n_top_tier: `0.50862`  ·  corrupted: `0.01291`  ·  n_sockets: `0.02411`  ·  quality: `0.03918`

| stat_id | coef |
|---|---|
| `rune.stat_201332984` | -2.17036 |
| `explicit.stat_2339757871@T1` | 1.06089 |
| `explicit.stat_1671376347@T1` | 1.00816 |
| `explicit.stat_9187492@T1` | 0.89301 |
| `explicit.stat_9187492@T2` | -0.79859 |
| `explicit.stat_3484657501@T2` | -0.60622 |
| `explicit.stat_3321629045@T2` | -0.58092 |
| `explicit.stat_3484657501@T1` | -0.56446 |
| `explicit.stat_803737631@T2` | -0.56341 |
| `explicit.stat_4052037485@T1` | -0.55157 |
| `explicit.stat_3917489142@T2` | -0.54043 |
| `explicit.stat_3321629045@T1` | -0.53280 |

### weapon.wand — n=19229, R²=-2.2156

intercept: `3.6023`  ·  log_price: True  ·  ilvl: `-0.04447`  ·  n_mods: `-0.01912`  ·  n_top_tier: `0.68282`  ·  corrupted: `0.02913`  ·  n_sockets: `0.02938`  ·  quality: `0.00374`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -2.69642 |
| `explicit.stat_1545858329@T1` | 2.57482 |
| `explicit.stat_2254480358@T1` | 2.27976 |
| `explicit.stat_4226189338@T1` | 1.72418 |
| `explicit.stat_591105508@T1` | 1.67672 |
| `explicit.stat_124131830@T1` | 1.62141 |
| `explicit.stat_736967255@T2` | 1.58661 |
| `crafted.stat_124131830` | 1.15549 |
| `explicit.stat_2254480358@T2` | 0.84177 |
| `explicit.stat_1263695895@T2` | -0.80265 |
| `explicit.stat_1600707273@T2` | -0.78144 |
| `explicit.stat_1263695895@T1` | -0.77645 |

### weapon.bow — n=15409, R²=-1.9715

intercept: `3.5764`  ·  log_price: True  ·  ilvl: `-0.04321`  ·  n_mods: `-0.03532`  ·  n_top_tier: `0.63029`  ·  corrupted: `-0.03506`  ·  n_sockets: `0.00836`  ·  quality: `0.03230`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.97442 |
| `explicit.stat_1202301673@T1` | 1.60802 |
| `crafted.stat_3035140377` | 1.43879 |
| `explicit.stat_2463230181@T2` | -0.90531 |
| `explicit.stat_1263695895@T2` | -0.87010 |
| `explicit.stat_1263695895@T1` | -0.86737 |
| `explicit.stat_3695891184@T2` | -0.72553 |
| `explicit.stat_518292764@T2` | -0.70471 |
| `explicit.stat_1037193709@T1` | -0.69550 |
| `explicit.stat_3695891184@T1` | -0.69191 |
| `explicit.stat_669069897@T1` | -0.68348 |
| `explicit.stat_2694482655@T2` | -0.67703 |

### weapon.crossbow — n=14504, R²=-1.8726

intercept: `3.7302`  ·  log_price: True  ·  ilvl: `-0.04548`  ·  n_mods: `-0.04185`  ·  n_top_tier: `0.80301`  ·  corrupted: `0.04233`  ·  n_sockets: `0.04518`  ·  quality: `0.00794`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.96267 |
| `explicit.stat_2250681686@T2` | -1.43979 |
| `explicit.stat_709508406@T1` | 1.29685 |
| `explicit.stat_1202301673@T1` | 1.19086 |
| `explicit.stat_1980802737` | 1.14905 |
| `explicit.stat_1263695895@T2` | -1.01279 |
| `explicit.stat_1263695895@T1` | -1.00551 |
| `explicit.stat_2694482655@T1` | -0.93687 |
| `explicit.stat_210067635@T2` | -0.92817 |
| `explicit.stat_1509134228@T2` | -0.91348 |
| `explicit.stat_210067635@T1` | -0.90968 |
| `explicit.stat_3695891184@T1` | -0.88846 |

### flask.charm — n=13994, R²=-0.561

intercept: `0.0164`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `2.94320`  ·  corrupted: `1.91303`  ·  quality: `0.00019`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.54065 |
| `explicit.stat_1056492907` | 3.21990 |
| `explicit.stat_828533480@T2` | -2.94321 |
| `explicit.stat_1120862500@T2` | -2.94319 |
| `explicit.stat_828533480@T1` | -2.94319 |
| `explicit.stat_3196823591@T2` | -2.94319 |
| `explicit.stat_2541588185@T2` | -2.94318 |
| `explicit.stat_2676834156@T2` | -2.94318 |
| `explicit.stat_1873752457@T2` | -2.94318 |
| `explicit.stat_388617051@T2` | -2.94318 |
| `explicit.stat_2365392475@T2` | -2.94316 |
| `explicit.stat_1873752457@T1` | -2.94316 |

### weapon.warstaff — n=9097, R²=-0.4182

intercept: `-8.5619`  ·  log_price: True  ·  ilvl: `0.11607`  ·  n_mods: `-0.17538`  ·  n_top_tier: `0.44160`  ·  corrupted: `0.13353`  ·  n_sockets: `0.16482`  ·  quality: `0.05885`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 1.01860 |
| `explicit.stat_328541901@T1` | -0.93940 |
| `explicit.stat_1037193709@T1` | 0.88315 |
| `explicit.stat_328541901@T2` | -0.78856 |
| `explicit.stat_9187492@T1` | 0.74858 |
| `crafted.stat_210067635@T2` | 0.71494 |
| `desecrated.stat_9187492` | 0.70455 |
| `desecrated.stat_2527686725@T1` | 0.64803 |
| `desecrated.stat_2231156303@T1` | 0.64803 |
| `explicit.stat_518292764@T1` | -0.52260 |
| `crafted.stat_3035140377` | 0.51942 |
| `explicit.stat_1037193709@T2` | -0.47873 |

### weapon.staff — n=8507, R²=-0.4343

intercept: `-12.8097`  ·  log_price: True  ·  ilvl: `0.16658`  ·  n_mods: `-0.12000`  ·  n_top_tier: `0.54636`  ·  corrupted: `0.48825`  ·  n_sockets: `0.21416`  ·  quality: `0.04039`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 1.70309 |
| `explicit.stat_4226189338@T1` | 1.28907 |
| `explicit.stat_591105508@T1` | 1.21760 |
| `explicit.stat_293638271@T2` | -1.12740 |
| `explicit.stat_124131830@T2` | 1.09523 |
| `explicit.stat_124131830@T1` | 1.09292 |
| `explicit.stat_4226189338@T2` | 0.85846 |
| `explicit.stat_3962278098@T2` | 0.75024 |
| `explicit.stat_2505884597@T2` | -0.72214 |
| `explicit.stat_1263695895@T2` | -0.70557 |
| `explicit.stat_3291658075@T2` | 0.64547 |
| `explicit.stat_2974417149@T1` | -0.60018 |

### weapon.sceptre — n=8429, R²=-0.3639

intercept: `-18.2738`  ·  log_price: True  ·  ilvl: `0.23252`  ·  n_mods: `-0.03644`  ·  n_top_tier: `0.16294`  ·  corrupted: `0.52927`  ·  n_sockets: `0.24761`  ·  quality: `0.04691`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.94526 |
| `explicit.stat_2162097452@T2` | 1.81438 |
| `explicit.stat_1250712710@T2` | 1.41639 |
| `explicit.stat_3057012405@T1` | 1.32451 |
| `explicit.stat_2347036682@T1` | 0.69852 |
| `explicit.stat_1574590649@T1` | -0.65884 |
| `explicit.stat_1263695895@T1` | -0.64254 |
| `explicit.stat_849987426@T1` | 0.63106 |
| `explicit.stat_101878827@T1` | 0.59818 |
| `explicit.stat_328541901@T2` | 0.57049 |
| `explicit.stat_2347036682@T2` | -0.57044 |
| `explicit.stat_1263695895@T2` | -0.50868 |

### weapon.spear — n=6945, R²=-0.4792

intercept: `-9.7213`  ·  log_price: True  ·  ilvl: `0.13275`  ·  n_mods: `-0.08219`  ·  n_top_tier: `0.69848`  ·  corrupted: `0.00635`  ·  n_sockets: `0.25537`  ·  quality: `0.08869`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.03912 |
| `explicit.stat_1202301673@T1` | 2.13044 |
| `explicit.stat_9187492@T1` | 1.54913 |
| `explicit.stat_1509134228@T1` | 1.49261 |
| `explicit.stat_1263695895@T2` | -1.17420 |
| `explicit.stat_1037193709@T1` | -1.12983 |
| `crafted.stat_3035140377` | 0.97912 |
| `explicit.stat_691932474@T1` | -0.87916 |
| `explicit.stat_55876295@T1` | -0.85915 |
| `explicit.stat_1940865751@T2` | -0.80194 |
| `explicit.stat_210067635@T1` | 0.72153 |
| `explicit.stat_55876295@T2` | -0.70778 |

### armour.focus — n=5681, R²=-0.3914

intercept: `-12.3095`  ·  log_price: True  ·  ilvl: `0.15794`  ·  n_mods: `-0.16926`  ·  n_top_tier: `0.75769`  ·  corrupted: `0.70647`  ·  n_sockets: `0.48883`  ·  quality: `0.07468`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 4.49388 |
| `explicit.stat_3962278098@T1` | -1.46907 |
| `explicit.stat_4220027924@T2` | -1.27264 |
| `explicit.stat_3291658075@T1` | -0.97553 |
| `explicit.stat_2231156303@T1` | -0.97547 |
| `explicit.stat_2231156303@T2` | -0.95509 |
| `explicit.stat_736967255@T2` | -0.94392 |
| `explicit.stat_2974417149@T2` | -0.94359 |
| `explicit.stat_2923486259@T1` | -0.88801 |
| `explicit.stat_3962278098@T2` | -0.87189 |
| `crafted.stat_737908626@T2` | 0.83069 |
| `explicit.stat_737908626@T2` | -0.82721 |

### armour.quiver — n=5309, R²=-0.3595

intercept: `-13.2716`  ·  log_price: True  ·  ilvl: `0.16066`  ·  n_mods: `-0.10193`  ·  n_top_tier: `0.79047`  ·  corrupted: `0.51346`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.38658 |
| `explicit.stat_2463230181@T1` | 1.69903 |
| `explicit.stat_4067062424@T1` | -1.20719 |
| `explicit.stat_2321178454@T2` | -1.20441 |
| `explicit.stat_681332047@T2` | -1.15711 |
| `explicit.stat_1573130764@T1` | -1.04959 |
| `explicit.stat_803737631@T2` | -1.02730 |
| `explicit.stat_2194114101@T2` | -0.98557 |
| `explicit.stat_4067062424@T2` | -0.91139 |
| `explicit.stat_803737631@T1` | -0.91125 |
| `explicit.stat_1573130764@T2` | -0.86652 |
| `explicit.stat_2321178454@T1` | -0.86394 |

### armour.shield — n=4642, R²=-0.5167

intercept: `-9.7943`  ·  log_price: True  ·  ilvl: `0.12844`  ·  n_mods: `-0.08843`  ·  n_top_tier: `0.55152`  ·  corrupted: `-0.31447`  ·  n_sockets: `0.13123`  ·  quality: `0.06245`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.59694 |
| `explicit.stat_3484657501@T2` | -1.08617 |
| `explicit.stat_1011760251@T2` | -1.00731 |
| `explicit.stat_2481353198@T2` | -0.95694 |
| `explicit.stat_3484657501@T1` | -0.95365 |
| `explicit.stat_2339757871@T1` | -0.94951 |
| `explicit.stat_3299347043@T1` | -0.93403 |
| `explicit.stat_3033371881@T2` | -0.89603 |
| `explicit.stat_3855016469@T1` | -0.89342 |
| `explicit.stat_2923486259@T2` | -0.88816 |
| `explicit.stat_3676141501@T1` | 0.88119 |
| `explicit.stat_3321629045@T2` | -0.85399 |

### weapon.twomace — n=4237, R²=-0.5153

intercept: `-9.8159`  ·  log_price: True  ·  ilvl: `0.13137`  ·  n_mods: `-0.17193`  ·  n_top_tier: `0.24986`  ·  corrupted: `0.11248`  ·  n_sockets: `0.11062`  ·  quality: `0.04001`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.31640 |
| `desecrated.stat_1509134228@T1` | 3.05889 |
| `explicit.stat_1037193709@T1` | -1.53561 |
| `crafted.stat_3035140377` | 0.91166 |
| `explicit.stat_3336890334@T1` | -0.85328 |
| `explicit.stat_210067635@T1` | 0.63885 |
| `explicit.stat_387439868@T2` | -0.62893 |
| `explicit.stat_1037193709@T2` | -0.61700 |
| `explicit.stat_518292764@T2` | -0.55541 |
| `explicit.stat_210067635@T2` | 0.54115 |
| `explicit.stat_9187492@T1` | -0.51115 |
| `explicit.stat_518292764@T1` | 0.47237 |

## Coverage (listings per base)

- … **Sapphire** — 25480 listings (25434 priced) [0.3–87761642.7 ex]
- … **Emerald** — 24961 listings (24929 priced) [0.3–87761642.7 ex]
- … **Ruby** — 19142 listings (19122 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 10035 listings (10020 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 8439 listings (8423 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 8195 listings (8176 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 8080 listings (8073 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 7665 listings (7651 priced) [0.3–39887666593.4 ex]
- … **Stellar Amulet** — 7547 listings (7538 priced) [0.3–91750808.2 ex]
- … **Gold Ring** — 7520 listings (7502 priced) [0.2–91750808.2 ex]
- … **Sapphire Ring** — 6291 listings (6283 priced) [0.2–307202867.9 ex]
- … **Dueling Wand** — 6133 listings (6115 priced) [0.3–4297682211.9 ex]
- … **Topaz Ring** — 6029 listings (6024 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 6005 listings (5999 priced) [0.2–91750808.2 ex]
- … **Plate Belt** — 5376 listings (5353 priced) [0.3–398912568423.8 ex]
- … **Lapis Amulet** — 5342 listings (5337 priced) [0.3–19945827.9 ex]
- … **Amber Amulet** — 5204 listings (5198 priced) [0.3–3985176410.3 ex]
- … **Jade Amulet** — 5202 listings (5194 priced) [0.3–4547453.5 ex]
- … **Ancestral Tiara** — 5195 listings (5177 priced) [0.6–398912568423.8 ex]
- … **Unset Ring** — 5186 listings (5173 priced) [0.2–24532814.5 ex]
- … **Bloodstone Amulet** — 5022 listings (5014 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 4878 listings (4871 priced) [0.2–275252424.7 ex]
- … **Heavy Belt** — 4791 listings (4784 priced) [0.3–398912568423.8 ex]
- … **Azure Amulet** — 4759 listings (4758 priced) [0.3–123132003.2 ex]
- … **Lunar Amulet** — 4719 listings (4709 priced) [0.3–91750808.2 ex]
