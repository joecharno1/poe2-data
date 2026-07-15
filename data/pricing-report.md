# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-15T22:32:36+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **526326** (525006 priced in exalted)
- Distinct bases: 984 · distinct mods: 3133 · mod rows: 2496531
- Sold signals: **25996** sold · 295151 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-15T22:22:51+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×25.07** (median |log error| 3.2216)
- Within ±30% of asking price: **14%**
- Skill vs constant-price guess: **+0.07** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.12** · typical error ×60.21 · ±30% 5% · n=76010
- Premium segment (60ex+): skill **+0.12** · typical error ×245.30 · ±30% 0% · n=50760

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 10557 | ×53.92 | 22% | +0.06 | +0.08 |
| jewel | 9888 | ×9.87 | 5% | +0.04 | +0.07 |
| accessory.amulet | 9700 | ×51.17 | 19% | +0.03 | +0.03 |
| accessory.belt | 7373 | ×15.20 | 4% | +0.01 | +0.02 |
| armour.chest | 7227 | ×22.85 | 8% | +0.10 | +0.12 |
| armour.helmet | 7074 | ×21.46 | 6% | +0.09 | +0.11 |
| armour.boots | 6558 | ×37.00 | 18% | +0.09 | +0.11 |
| armour.gloves | 6448 | ×30.85 | 9% | +0.10 | +0.13 |
| other | 5804 | ×4.05 | 41% | +0.09 | +0.15 |
| weapon.wand | 4049 | ×35.46 | 19% | +0.07 | +0.08 |
| weapon.bow | 3197 | ×29.53 | 15% | +0.12 | +0.12 |
| weapon.crossbow | 3036 | ×25.59 | 17% | +0.09 | +0.13 |
| weapon.warstaff | 1835 | ×33.75 | 14% | +0.12 | +0.11 |
| weapon.sceptre | 1728 | ×43.17 | 6% | +0.15 | +0.14 |
| weapon.staff | 1705 | ×59.76 | 11% | +0.09 | +0.10 |
| weapon.spear | 1403 | ×58.96 | 16% | +0.09 | +0.10 |
| armour.focus | 1172 | ×36.77 | 7% | +0.13 | +0.15 |
| armour.quiver | 1107 | ×30.42 | 9% | +0.11 | +0.14 |
| armour.shield | 928 | ×20.78 | 14% | +0.03 | +0.04 |
| flask.charm | 926 | ×25.00 | 35% | +0.03 | +0.06 |
| weapon.twomace | 845 | ×17.62 | 13% | +0.07 | +0.06 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=53388, R²=-0.9227

intercept: `-1.7007`  ·  log_price: True  ·  ilvl: `0.02654`  ·  n_mods: `0.58936`  ·  n_top_tier: `-0.11943`  ·  corrupted: `0.30837`  ·  quality: `0.22951`

| stat_id | coef |
|---|---|
| `explicit.stat_3192728503@T1` | -3.07781 |
| `explicit.stat_2301718443@T1` | 2.98166 |
| `explicit.stat_627767961@T1` | -2.30240 |
| `explicit.stat_1805182458@T1` | -2.13895 |
| `explicit.stat_3485067555@T1` | 2.07706 |
| `explicit.stat_3780644166@T1` | -1.81394 |
| `explicit.stat_234296660@T1` | -1.63944 |
| `explicit.stat_1569101201@T1` | 1.61251 |
| `explicit.stat_239367161@T1` | -1.60752 |
| `explicit.stat_3119612865@T1` | -1.58187 |
| `explicit.stat_3473929743@T1` | -1.57746 |
| `explicit.stat_1062710370@T1` | -1.55828 |

### other — n=50671, R²=-0.6097

intercept: `1.6094`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00004`  ·  n_top_tier: `0.37412`  ·  corrupted: `0.34100`  ·  n_sockets: `-0.00002`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_3291658075@T1` | 0.57520 |
| `explicit.stat_2974417149@T1` | 0.46527 |
| `explicit.stat_789117908@T1` | -0.32134 |
| `explicit.stat_2482852589@T1` | -0.29974 |
| `explicit.stat_3299347043@T1` | -0.29215 |
| `explicit.stat_2968503605@T1` | 0.25911 |
| `explicit.stat_2106365538@T1` | -0.23889 |
| `explicit.stat_3141070085@T1` | -0.23661 |
| `implicit.stat_3879011313` | 0.23249 |
| `implicit.stat_2219129443` | 0.23026 |
| `implicit.stat_4041853756` | 0.23026 |
| `explicit.stat_1589917703@T1` | -0.20226 |

### accessory.ring — n=48331, R²=-1.9857

intercept: `3.6018`  ·  log_price: True  ·  ilvl: `-0.04445`  ·  n_mods: `0.00111`  ·  n_top_tier: `0.96450`  ·  corrupted: `0.03303`  ·  n_sockets: `1.26908`  ·  quality: `0.07060`

| stat_id | coef |
|---|---|
| `explicit.stat_3325883026@T1` | -0.99430 |
| `explicit.stat_2231156303@T1` | -0.99027 |
| `explicit.stat_803737631@T1` | -0.99010 |
| `explicit.stat_3291658075@T2` | -0.98646 |
| `explicit.stat_1368271171@T2` | -0.98510 |
| `explicit.stat_1263695895@T1` | -0.98499 |
| `explicit.stat_3291658075@T1` | -0.98445 |
| `explicit.stat_3325883026@T2` | -0.98405 |
| `explicit.stat_2144192055@T1` | -0.98307 |
| `explicit.stat_3962278098@T2` | -0.97753 |
| `explicit.stat_1050105434@T1` | -0.97722 |
| `explicit.stat_1050105434@T2` | -0.97667 |

### accessory.amulet — n=44504, R²=-2.1401

intercept: `3.7144`  ·  log_price: True  ·  ilvl: `-0.04531`  ·  n_mods: `-0.02426`  ·  n_top_tier: `0.97143`  ·  corrupted: `0.04273`  ·  n_sockets: `-0.12531`  ·  quality: `-0.00118`

| stat_id | coef |
|---|---|
| `explicit.stat_472520716@T2` | -1.05333 |
| `explicit.stat_803737631@T1` | -1.04341 |
| `explicit.stat_2901986750@T1` | -1.03778 |
| `explicit.stat_472520716@T1` | -1.02708 |
| `explicit.stat_1050105434@T2` | -1.02144 |
| `explicit.stat_3917489142@T2` | -1.00996 |
| `explicit.stat_2866361420@T2` | -1.00964 |
| `explicit.stat_587431675@T2` | -1.00775 |
| `explicit.stat_803737631@T2` | -1.00725 |
| `explicit.stat_3489782002@T2` | -1.00195 |
| `explicit.stat_2974417149@T1` | -0.99817 |
| `explicit.stat_2974417149@T2` | -0.99793 |

### accessory.belt — n=34045, R²=-0.6294

intercept: `6.3099`  ·  log_price: True  ·  ilvl: `-0.05275`  ·  n_mods: `-0.41273`  ·  n_top_tier: `1.13324`  ·  corrupted: `0.80641`  ·  n_sockets: `-0.77605`

| stat_id | coef |
|---|---|
| `explicit.stat_1389754388@T1` | -1.81356 |
| `explicit.stat_2881298780@T1` | -1.64014 |
| `explicit.stat_3299347043@T1` | -1.57719 |
| `explicit.stat_644456512@T1` | -1.51312 |
| `explicit.stat_3299347043@T2` | -1.41998 |
| `explicit.stat_1389754388@T2` | -1.37731 |
| `explicit.stat_809229260@T2` | -1.35123 |
| `explicit.stat_51994685@T1` | -1.33127 |
| `explicit.stat_809229260@T1` | -1.30534 |
| `explicit.stat_4080418644@T2` | -1.25987 |
| `explicit.stat_2923486259@T1` | -1.25520 |
| `explicit.stat_4220027924@T2` | -1.25238 |

### armour.chest — n=33685, R²=-1.223

intercept: `4.1327`  ·  log_price: True  ·  ilvl: `-0.04911`  ·  n_mods: `-0.08466`  ·  n_top_tier: `0.57021`  ·  corrupted: `0.24906`  ·  n_sockets: `0.11738`  ·  quality: `0.04289`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 2.02921 |
| `explicit.stat_3484657501@T1` | -0.89426 |
| `explicit.stat_986397080@T2` | -0.88659 |
| `explicit.stat_4080418644@T1` | -0.78326 |
| `explicit.stat_986397080@T1` | -0.77397 |
| `explicit.stat_1999113824@T1` | -0.73132 |
| `explicit.stat_1692879867@T2` | -0.72111 |
| `explicit.stat_2923486259@T2` | -0.71697 |
| `explicit.stat_124859000@T2` | -0.70997 |
| `explicit.stat_4080418644@T2` | -0.70788 |
| `explicit.stat_2451402625@T2` | -0.68825 |
| `explicit.stat_3981240776@T1` | 0.67907 |

### armour.helmet — n=32773, R²=-1.0141

intercept: `3.9790`  ·  log_price: True  ·  ilvl: `-0.04936`  ·  n_mods: `-0.10857`  ·  n_top_tier: `0.44844`  ·  corrupted: `0.74094`  ·  n_sockets: `0.17436`  ·  quality: `0.04200`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.17296 |
| `explicit.stat_3917489142@T2` | -1.01518 |
| `explicit.stat_1999113824@T1` | -0.85167 |
| `explicit.stat_53045048@T2` | -0.81700 |
| `explicit.stat_3261801346@T1` | -0.72966 |
| `explicit.stat_3321629045@T2` | -0.71689 |
| `explicit.stat_1999113824@T2` | -0.70171 |
| `explicit.stat_2162097452@T2` | -0.58935 |
| `explicit.stat_1050105434@T2` | -0.57913 |
| `explicit.stat_803737631@T2` | -0.57471 |
| `explicit.stat_1263695895@T1` | -0.57204 |
| `explicit.stat_3917489142@T1` | -0.54944 |

### armour.boots — n=30677, R²=-1.5552

intercept: `3.9448`  ·  log_price: True  ·  ilvl: `-0.04811`  ·  n_mods: `-0.03550`  ·  n_top_tier: `0.71102`  ·  corrupted: `0.12064`  ·  n_sockets: `0.05695`  ·  quality: `0.03222`

| stat_id | coef |
|---|---|
| `crafted.stat_3917489142@T1` | 1.65480 |
| `explicit.stat_2250533757@T1` | 1.44058 |
| `explicit.stat_2339757871@T1` | -1.16648 |
| `explicit.stat_3299347043@T1` | -0.95743 |
| `explicit.stat_3917489142@T2` | -0.89441 |
| `explicit.stat_2923486259@T2` | -0.86484 |
| `explicit.stat_53045048@T1` | -0.81652 |
| `explicit.stat_1062208444@T2` | -0.80901 |
| `explicit.stat_2160282525@T1` | -0.80579 |
| `explicit.stat_1999113824@T2` | -0.77985 |
| `explicit.stat_4052037485@T2` | -0.77394 |
| `explicit.stat_1874553720@T1` | -0.77356 |

### armour.gloves — n=29895, R²=-1.3596

intercept: `3.9651`  ·  log_price: True  ·  ilvl: `-0.05183`  ·  n_mods: `-0.03483`  ·  n_top_tier: `0.50407`  ·  corrupted: `0.09534`  ·  n_sockets: `0.12397`  ·  quality: `0.04550`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 4.81852 |
| `rune.stat_201332984` | -2.88098 |
| `explicit.stat_3484657501@T2` | -0.90347 |
| `explicit.stat_9187492@T1` | 0.88270 |
| `explicit.stat_3484657501@T1` | -0.85200 |
| `explicit.stat_3321629045@T2` | -0.82806 |
| `explicit.stat_1671376347@T1` | 0.75349 |
| `explicit.stat_803737631@T2` | -0.75304 |
| `explicit.stat_2923486259@T1` | -0.72803 |
| `explicit.stat_4052037485@T1` | -0.68504 |
| `explicit.stat_9187492@T2` | -0.64270 |
| `explicit.stat_3917489142@T2` | -0.63043 |

### weapon.wand — n=19029, R²=-2.246

intercept: `3.5880`  ·  log_price: True  ·  ilvl: `-0.04430`  ·  n_mods: `-0.01530`  ·  n_top_tier: `0.67723`  ·  corrupted: `0.04044`  ·  n_sockets: `0.03426`  ·  quality: `0.00268`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 2.66747 |
| `rune.stat_124131830` | -2.61327 |
| `explicit.stat_2254480358@T1` | 2.20691 |
| `explicit.stat_4226189338@T1` | 2.05848 |
| `explicit.stat_591105508@T1` | 1.69559 |
| `explicit.stat_124131830@T1` | 1.60767 |
| `explicit.stat_736967255@T2` | 1.53923 |
| `crafted.stat_124131830` | 1.14859 |
| `explicit.stat_2254480358@T2` | 0.85648 |
| `explicit.stat_1263695895@T2` | -0.81108 |
| `explicit.stat_1263695895@T1` | -0.77224 |
| `explicit.stat_737908626@T1` | -0.76232 |

### weapon.bow — n=15285, R²=-1.8608

intercept: `3.6640`  ·  log_price: True  ·  ilvl: `-0.04318`  ·  n_mods: `-0.06794`  ·  n_top_tier: `0.56402`  ·  corrupted: `-0.02861`  ·  n_sockets: `0.02091`  ·  quality: `0.03346`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -1.99530 |
| `explicit.stat_1202301673@T1` | 1.55890 |
| `crafted.stat_3035140377` | 1.46177 |
| `desecrated.stat_666077204@T1` | 1.44107 |
| `explicit.stat_2463230181@T2` | -1.14305 |
| `explicit.stat_1263695895@T1` | -0.88016 |
| `explicit.stat_1263695895@T2` | -0.84947 |
| `explicit.stat_1509134228@T1` | -0.74333 |
| `explicit.stat_518292764@T2` | -0.72610 |
| `explicit.stat_3695891184@T2` | -0.70876 |
| `explicit.stat_2463230181@T1` | -0.70870 |
| `explicit.stat_1940865751@T1` | 0.70091 |

### weapon.crossbow — n=14398, R²=-1.8741

intercept: `3.6949`  ·  log_price: True  ·  ilvl: `-0.04495`  ·  n_mods: `-0.03855`  ·  n_top_tier: `0.78259`  ·  corrupted: `0.02721`  ·  n_sockets: `0.04200`  ·  quality: `0.01299`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.95183 |
| `explicit.stat_2250681686@T2` | -1.45109 |
| `explicit.stat_1202301673@T1` | 1.25984 |
| `explicit.stat_709508406@T1` | 1.24621 |
| `explicit.stat_1980802737` | 1.15565 |
| `explicit.stat_1263695895@T2` | -0.97460 |
| `explicit.stat_2694482655@T1` | -0.91541 |
| `explicit.stat_1509134228@T2` | -0.90615 |
| `explicit.stat_210067635@T2` | -0.90546 |
| `crafted.stat_3035140377` | 0.89030 |
| `explicit.stat_210067635@T1` | -0.88537 |
| `explicit.stat_3695891184@T1` | -0.87085 |

### flask.charm — n=13683, R²=-0.5468

intercept: `0.0215`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00000`  ·  n_top_tier: `2.99556`  ·  corrupted: `1.97458`  ·  quality: `0.00003`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.49089 |
| `explicit.stat_1056492907` | 3.32607 |
| `explicit.stat_828533480@T2` | -2.99558 |
| `explicit.stat_2676834156@T2` | -2.99556 |
| `explicit.stat_2541588185@T2` | -2.99555 |
| `explicit.stat_828533480@T1` | -2.99555 |
| `explicit.stat_1120862500@T2` | -2.99555 |
| `explicit.stat_3196823591@T2` | -2.99555 |
| `explicit.stat_1873752457@T2` | -2.99554 |
| `explicit.stat_388617051@T2` | -2.99554 |
| `explicit.stat_2365392475@T2` | -2.99553 |
| `explicit.stat_1873752457@T1` | -2.99552 |

### weapon.warstaff — n=8998, R²=-0.426

intercept: `-8.9708`  ·  log_price: True  ·  ilvl: `0.12105`  ·  n_mods: `-0.17735`  ·  n_top_tier: `0.51695`  ·  corrupted: `0.24792`  ·  n_sockets: `0.14690`  ·  quality: `0.05830`

| stat_id | coef |
|---|---|
| `explicit.stat_328541901@T1` | -1.06069 |
| `rune.stat_243313994` | 1.04596 |
| `explicit.stat_1037193709@T1` | 0.93638 |
| `explicit.stat_328541901@T2` | -0.83110 |
| `crafted.stat_210067635@T2` | 0.76462 |
| `desecrated.stat_9187492` | 0.69995 |
| `explicit.stat_1037193709@T2` | -0.69322 |
| `desecrated.stat_2231156303@T1` | 0.66944 |
| `desecrated.stat_2527686725@T1` | 0.66944 |
| `explicit.stat_55876295@T2` | -0.59381 |
| `explicit.stat_1940865751@T1` | -0.56844 |
| `explicit.stat_9187492@T1` | 0.55296 |

### weapon.staff — n=8393, R²=-0.437

intercept: `-11.9923`  ·  log_price: True  ·  ilvl: `0.15517`  ·  n_mods: `-0.11467`  ·  n_top_tier: `0.63180`  ·  corrupted: `0.22148`  ·  n_sockets: `0.21979`  ·  quality: `0.03845`

| stat_id | coef |
|---|---|
| `explicit.stat_1545858329@T1` | 1.45833 |
| `explicit.stat_293638271@T2` | -1.15655 |
| `explicit.stat_124131830@T2` | 1.10009 |
| `explicit.stat_4226189338@T1` | 1.03713 |
| `explicit.stat_124131830@T1` | 1.02858 |
| `explicit.stat_4226189338@T2` | 0.96081 |
| `explicit.stat_591105508@T1` | 0.87752 |
| `explicit.stat_1263695895@T2` | -0.82254 |
| `explicit.stat_2505884597@T2` | -0.78199 |
| `explicit.stat_2974417149@T1` | -0.77191 |
| `explicit.stat_3962278098@T2` | 0.73090 |
| `explicit.stat_2768835289@T2` | 0.68126 |

### weapon.sceptre — n=8322, R²=-0.3646

intercept: `-18.1669`  ·  log_price: True  ·  ilvl: `0.23052`  ·  n_mods: `-0.01824`  ·  n_top_tier: `0.30918`  ·  corrupted: `0.50155`  ·  n_sockets: `0.18969`  ·  quality: `0.04457`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.90954 |
| `explicit.stat_2162097452@T2` | 1.70552 |
| `explicit.stat_3057012405@T1` | 1.23331 |
| `explicit.stat_1250712710@T2` | 1.22681 |
| `explicit.stat_1263695895@T1` | -0.73043 |
| `explicit.stat_2347036682@T2` | -0.72599 |
| `explicit.stat_101878827@T1` | 0.68152 |
| `explicit.stat_1263695895@T2` | -0.60843 |
| `explicit.stat_2347036682@T1` | 0.59701 |
| `explicit.stat_289128254@T2` | -0.55286 |
| `explicit.stat_2854751904@T2` | -0.55256 |
| `explicit.stat_1574590649@T1` | -0.52796 |

### weapon.spear — n=6853, R²=-0.4811

intercept: `-9.4246`  ·  log_price: True  ·  ilvl: `0.12803`  ·  n_mods: `-0.07210`  ·  n_top_tier: `0.72155`  ·  corrupted: `-0.06453`  ·  n_sockets: `0.23288`  ·  quality: `0.09126`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.06061 |
| `explicit.stat_1202301673@T1` | 2.05536 |
| `explicit.stat_9187492@T1` | 1.36601 |
| `explicit.stat_1509134228@T1` | 1.29492 |
| `explicit.stat_1037193709@T1` | -1.11430 |
| `explicit.stat_210067635@T1` | 1.08440 |
| `explicit.stat_1263695895@T2` | -1.04375 |
| `crafted.stat_3035140377` | 1.01389 |
| `explicit.stat_55876295@T1` | -0.92068 |
| `explicit.stat_691932474@T1` | -0.83594 |
| `explicit.stat_1940865751@T2` | -0.81651 |
| `desecrated.stat_210067635@T1` | -0.75417 |

### armour.focus — n=5609, R²=-0.4

intercept: `-12.3006`  ·  log_price: True  ·  ilvl: `0.15846`  ·  n_mods: `-0.16104`  ·  n_top_tier: `0.79747`  ·  corrupted: `0.64747`  ·  n_sockets: `0.49552`  ·  quality: `0.07559`

| stat_id | coef |
|---|---|
| `crafted.stat_2974417149@T1` | 5.28150 |
| `crafted.stat_737908626@T2` | 1.59318 |
| `explicit.stat_3962278098@T1` | -1.34852 |
| `explicit.stat_4220027924@T2` | -1.27411 |
| `explicit.stat_2974417149@T2` | -1.06602 |
| `explicit.stat_2231156303@T1` | -1.00967 |
| `explicit.stat_2923486259@T1` | -1.00158 |
| `explicit.stat_2231156303@T2` | -0.95243 |
| `explicit.stat_2339757871@T2` | -0.93541 |
| `explicit.stat_3962278098@T2` | -0.93325 |
| `explicit.stat_737908626@T2` | -0.88675 |
| `explicit.stat_736967255@T2` | -0.86471 |

### armour.quiver — n=5223, R²=-0.3599

intercept: `-13.4966`  ·  log_price: True  ·  ilvl: `0.16476`  ·  n_mods: `-0.11172`  ·  n_top_tier: `0.86431`  ·  corrupted: `0.46957`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.19521 |
| `explicit.stat_2463230181@T1` | 2.14970 |
| `explicit.stat_681332047@T2` | -1.37419 |
| `explicit.stat_4067062424@T1` | -1.25468 |
| `explicit.stat_2321178454@T2` | -1.24641 |
| `explicit.stat_803737631@T2` | -1.12678 |
| `explicit.stat_1573130764@T2` | -1.00070 |
| `explicit.stat_2321178454@T1` | -0.99522 |
| `explicit.stat_1573130764@T1` | -0.99452 |
| `explicit.stat_4067062424@T2` | -0.97942 |
| `explicit.stat_2194114101@T2` | -0.97645 |
| `explicit.stat_681332047@T1` | -0.91900 |

### armour.shield — n=4575, R²=-0.5408

intercept: `-9.4112`  ·  log_price: True  ·  ilvl: `0.12222`  ·  n_mods: `-0.06558`  ·  n_top_tier: `0.47417`  ·  corrupted: `-0.28379`  ·  n_sockets: `0.17812`  ·  quality: `0.06549`

| stat_id | coef |
|---|---|
| `explicit.stat_1301765461@T1` | 1.32623 |
| `explicit.stat_1011760251@T1` | -1.16968 |
| `explicit.stat_3676141501@T1` | 0.96399 |
| `explicit.stat_2481353198@T2` | -0.92566 |
| `explicit.stat_1011760251@T2` | -0.91465 |
| `explicit.stat_2923486259@T2` | -0.84721 |
| `explicit.stat_2481353198@T1` | -0.83930 |
| `explicit.stat_3855016469@T1` | -0.83017 |
| `explicit.stat_3033371881@T2` | -0.79557 |
| `explicit.stat_3484657501@T1` | -0.78258 |
| `explicit.stat_3484657501@T2` | -0.77655 |
| `explicit.stat_3321629045@T2` | -0.70098 |

### weapon.twomace — n=4185, R²=-0.5204

intercept: `-9.4345`  ·  log_price: True  ·  ilvl: `0.12624`  ·  n_mods: `-0.17522`  ·  n_top_tier: `0.37828`  ·  corrupted: `0.10172`  ·  n_sockets: `0.12789`  ·  quality: `0.03910`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -4.27878 |
| `desecrated.stat_1509134228@T1` | 2.93937 |
| `explicit.stat_1037193709@T1` | -1.64176 |
| `crafted.stat_3035140377` | 1.02661 |
| `explicit.stat_3336890334@T1` | -0.97528 |
| `explicit.stat_387439868@T2` | -0.81313 |
| `explicit.stat_1037193709@T2` | -0.78107 |
| `explicit.stat_518292764@T2` | -0.70133 |
| `explicit.stat_3639275092@T1` | -0.66410 |
| `explicit.stat_2694482655@T1` | -0.62848 |
| `explicit.stat_9187492@T1` | -0.60415 |
| `explicit.stat_210067635@T1` | 0.59036 |

## Coverage (listings per base)

- … **Sapphire** — 24872 listings (24833 priced) [0.3–7553463.8 ex]
- … **Emerald** — 24390 listings (24360 priced) [0.3–7553463.8 ex]
- … **Ruby** — 18710 listings (18690 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 9903 listings (9889 priced) [0.2–398912568423.8 ex]
- … **Prismatic Ring** — 8279 listings (8263 priced) [0.2–3985176410.3 ex]
- … **Solar Amulet** — 8016 listings (7998 priced) [1.0–2608914286.6 ex]
- … **Amethyst Ring** — 7900 listings (7893 priced) [0.2–2608914286.6 ex]
- … **Gold Amulet** — 7525 listings (7511 priced) [0.3–39887666593.4 ex]
- … **Stellar Amulet** — 7419 listings (7410 priced) [0.3–91750808.2 ex]
- … **Gold Ring** — 7381 listings (7363 priced) [0.2–91750808.2 ex]
- … **Sapphire Ring** — 6191 listings (6183 priced) [0.2–307202867.9 ex]
- … **Dueling Wand** — 6061 listings (6044 priced) [0.3–4297682211.9 ex]
- … **Topaz Ring** — 5903 listings (5898 priced) [0.3–307202867.9 ex]
- … **Ruby Ring** — 5874 listings (5868 priced) [0.2–91750808.2 ex]
- … **Plate Belt** — 5273 listings (5251 priced) [0.3–398912568423.8 ex]
- … **Lapis Amulet** — 5244 listings (5239 priced) [0.3–19945827.9 ex]
- … **Ancestral Tiara** — 5121 listings (5104 priced) [0.6–398912568423.8 ex]
- … **Amber Amulet** — 5104 listings (5098 priced) [0.3–3985176410.3 ex]
- … **Jade Amulet** — 5102 listings (5094 priced) [0.3–4547453.5 ex]
- … **Unset Ring** — 5072 listings (5059 priced) [0.2–24532814.5 ex]
- … **Bloodstone Amulet** — 4937 listings (4930 priced) [0.3–4275054.0 ex]
- … **Pearl Ring** — 4769 listings (4762 priced) [0.2–275252424.7 ex]
- … **Heavy Belt** — 4726 listings (4719 priced) [0.3–398912568423.8 ex]
- … **Azure Amulet** — 4666 listings (4665 priced) [0.3–123132003.2 ex]
- … **Lunar Amulet** — 4623 listings (4614 priced) [0.3–91750808.2 ex]
