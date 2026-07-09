# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-09T19:56:08+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **387506** (386845 priced in exalted)
- Distinct bases: 967 · distinct mods: 2941 · mod rows: 1841203
- Sold signals: **28419** sold · 206232 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-09T19:43:09+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×19.96** (median |log error| 2.9937)
- Within ±30% of asking price: **18%**
- Skill vs constant-price guess: **+0.04** (> 0 = the mods carry signal)
- Calibration: 78% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.06** · typical error ×58.68 · ±30% 12% · n=56683
- Premium segment (60ex+): skill **+0.07** · typical error ×167.37 · ±30% 0% · n=36351

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 7539 | ×13.64 | 3% | +0.04 | +0.05 |
| accessory.amulet | 7105 | ×54.64 | 21% | +0.02 | +0.03 |
| jewel | 6679 | ×7.98 | 11% | +0.02 | +0.04 |
| accessory.belt | 5620 | ×19.70 | 19% | +0.05 | +0.08 |
| armour.chest | 5411 | ×10.00 | 22% | +0.01 | +0.00 |
| armour.helmet | 5366 | ×15.00 | 21% | +0.01 | +0.02 |
| armour.boots | 4994 | ×11.11 | 20% | +0.01 | +0.04 |
| armour.gloves | 4903 | ×25.54 | 19% | +0.00 | +0.01 |
| other | 4564 | ×10.00 | 34% | +0.13 | +0.36 |
| weapon.wand | 3212 | ×49.27 | 20% | +0.03 | +0.07 |
| weapon.bow | 2591 | ×29.25 | 17% | +0.08 | +0.11 |
| weapon.crossbow | 2440 | ×24.47 | 16% | +0.09 | +0.15 |
| weapon.warstaff | 1345 | ×99.99 | 15% | +0.07 | +0.08 |
| weapon.sceptre | 1234 | ×76.81 | 11% | +0.07 | +0.09 |
| weapon.staff | 1171 | ×77.77 | 13% | +0.05 | +0.07 |
| weapon.spear | 1033 | ×50.00 | 16% | +0.04 | +0.05 |
| armour.focus | 849 | ×52.04 | 13% | +0.09 | +0.14 |
| armour.quiver | 779 | ×61.45 | 13% | +0.02 | +0.09 |
| armour.shield | 687 | ×30.00 | 12% | +0.04 | +0.10 |
| weapon.twomace | 606 | ×23.00 | 14% | +0.05 | +0.11 |
| flask.charm | 547 | ×5.00 | 41% | +0.00 | +0.01 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### other — n=38768, R²=-0.3298

intercept: `1.5723`  ·  log_price: True  ·  ilvl: `0.00049`  ·  n_mods: `0.18347`  ·  n_top_tier: `1.12098`  ·  corrupted: `2.02110`  ·  n_sockets: `-0.00088`  ·  quality: `-0.00010`

| stat_id | coef |
|---|---|
| `implicit.stat_3182714256` | 0.55168 |
| `implicit.stat_718638445` | 0.55165 |
| `implicit.stat_1379411836` | -0.27108 |
| `implicit.stat_4041853756` | 0.21176 |
| `implicit.stat_3879011313` | 0.21174 |
| `explicit.stat_789117908@T1` | -0.20814 |
| `implicit.stat_958696139` | -0.18403 |
| `explicit.stat_3141070085` | 0.16662 |
| `implicit.stat_2901986750` | 0.16416 |
| `explicit.stat_1589917703` | 0.16180 |
| `explicit.stat_2901986750` | 0.14232 |
| `explicit.stat_1050105434@T1` | -0.14185 |

### jewel — n=36361, R²=-0.5939

intercept: `-1.3344`  ·  log_price: True  ·  ilvl: `0.03816`  ·  n_mods: `0.22924`  ·  n_top_tier: `-0.11072`  ·  corrupted: `0.20122`  ·  quality: `0.22211`

| stat_id | coef |
|---|---|
| `explicit.stat_3292710273` | -0.18613 |
| `explicit.stat_1604736568` | 0.13595 |
| `explicit.stat_2709367754` | 0.12617 |
| `explicit.stat_1459321413` | -0.12512 |
| `explicit.stat_4236566306` | -0.10040 |
| `explicit.stat_2174054121` | -0.09640 |
| `explicit.stat_1135928777` | -0.08877 |
| `explicit.stat_1062710370` | -0.07984 |
| `explicit.stat_1444556985` | -0.07570 |
| `explicit.stat_318953428` | -0.06868 |
| `explicit.stat_918325986` | -0.06529 |
| `explicit.stat_2866361420` | -0.05765 |

### accessory.ring — n=34513, R²=-1.2048

intercept: `3.9169`  ·  log_price: True  ·  ilvl: `-0.04297`  ·  n_mods: `0.00469`  ·  n_top_tier: `0.01628`  ·  corrupted: `1.03327`  ·  n_sockets: `0.85519`  ·  quality: `0.01061`

| stat_id | coef |
|---|---|
| `implicit.stat_2748665614` | -0.36981 |
| `implicit.stat_3182714256` | 0.36492 |
| `implicit.stat_718638445` | -0.36492 |
| `implicit.stat_958696139` | -0.35335 |
| `implicit.stat_3032590688` | -0.22188 |
| `explicit.stat_4080418644@T2` | 0.11446 |
| `explicit.stat_3917489142@T1` | 0.09361 |
| `explicit.stat_1967040409` | 0.09185 |
| `explicit.stat_3917489142@T2` | -0.08875 |
| `explicit.stat_328541901@T1` | 0.08358 |
| `explicit.stat_1050105434@T2` | -0.07881 |
| `explicit.stat_328541901@T2` | -0.07582 |

### accessory.amulet — n=32369, R²=-2.1461

intercept: `4.2310`  ·  log_price: True  ·  ilvl: `-0.05139`  ·  n_mods: `-0.02376`  ·  n_top_tier: `0.00246`  ·  corrupted: `0.18232`  ·  n_sockets: `1.60466`  ·  quality: `-0.00349`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830` | 1.17200 |
| `explicit.stat_9187492` | 0.68857 |
| `pseudo.total_chaos_res` | 0.19457 |
| `explicit.stat_2923486259` | -0.19203 |
| `implicit.stat_2901986750` | 0.14028 |
| `explicit.stat_3981240776@T2` | 0.10252 |
| `explicit.stat_1202301673` | 0.09482 |
| `implicit.stat_718638445` | 0.06988 |
| `explicit.stat_3981240776@T1` | 0.05469 |
| `implicit.stat_3182714256` | 0.04677 |
| `explicit.stat_3917489142@T2` | -0.04418 |
| `explicit.stat_2106365538@T1` | -0.03679 |

### accessory.belt — n=25606, R²=-1.5256

intercept: `4.1857`  ·  log_price: True  ·  ilvl: `-0.04916`  ·  n_mods: `-0.04029`  ·  n_top_tier: `0.01888`  ·  corrupted: `1.19144`  ·  n_sockets: `-0.07035`

| stat_id | coef |
|---|---|
| `implicit.stat_731781020` | -0.15236 |
| `pseudo.total_chaos_res` | 0.09877 |
| `explicit.stat_2639966148` | 0.08757 |
| `explicit.stat_2923486259` | -0.08606 |
| `explicit.stat_174664100` | 0.07240 |
| `pseudo.total_ele_res>=80` | 0.07099 |
| `explicit.stat_3811191316` | 0.05239 |
| `explicit.stat_3372524247@T1` | 0.04721 |
| `explicit.stat_1389754388@T1` | -0.04543 |
| `explicit.stat_809229260@T2` | -0.04427 |
| `explicit.stat_3585532255@T1` | 0.04162 |
| `explicit.stat_51994685@T1` | -0.04032 |

### armour.chest — n=25336, R²=-0.2728

intercept: `2.3028`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.00105`  ·  corrupted: `0.00022`  ·  n_sockets: `0.00000`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 0.05747 |
| `desecrated.stat_4220027924` | -0.04039 |
| `pseudo.total_ele_res` | 0.03801 |
| `implicit.stat_3372524247` | -0.03801 |
| `implicit.stat_1671376347` | -0.03801 |
| `desecrated.stat_3372524247` | -0.03801 |
| `explicit.stat_1671376347` | -0.03801 |
| `implicit.stat_4220027924` | -0.03801 |
| `explicit.stat_3372524247` | -0.03801 |
| `explicit.stat_4220027924` | -0.03801 |
| `rune.stat_1671376347` | -0.03801 |
| `rune.stat_4220027924` | -0.03801 |

### armour.helmet — n=24759, R²=-0.3123

intercept: `2.3027`  ·  log_price: True  ·  ilvl: `-0.00000`  ·  n_mods: `-0.00002`  ·  n_top_tier: `0.00158`  ·  corrupted: `1.60933`  ·  n_sockets: `0.00001`  ·  quality: `0.00001`

| stat_id | coef |
|---|---|
| `desecrated.stat_1671376347` | -0.04143 |
| `rune.stat_3523867985` | 0.00894 |
| `pseudo.total_ele_res>=80` | 0.00776 |
| `crafted.stat_3917489142` | 0.00338 |
| `explicit.stat_53045048@T2` | -0.00161 |
| `explicit.stat_3362812763@T2` | -0.00160 |
| `explicit.stat_2451402625@T1` | -0.00160 |
| `explicit.stat_803737631@T2` | -0.00160 |
| `explicit.stat_53045048@T1` | -0.00159 |
| `explicit.stat_4080418644@T2` | -0.00159 |
| `explicit.stat_3917489142@T2` | -0.00159 |
| `explicit.stat_4080418644@T1` | -0.00159 |

### armour.boots — n=23235, R²=-0.3431

intercept: `2.3341`  ·  log_price: True  ·  ilvl: `-0.00058`  ·  n_mods: `-0.00413`  ·  n_top_tier: `0.00483`  ·  corrupted: `0.01475`  ·  n_sockets: `0.00098`  ·  quality: `0.00033`

| stat_id | coef |
|---|---|
| `rune.stat_232299587` | 0.16297 |
| `crafted.stat_3917489142` | 0.10754 |
| `pseudo.total_chaos_res` | 0.09525 |
| `explicit.stat_2923486259` | -0.09455 |
| `explicit.stat_2250533757@T1` | 0.01792 |
| `explicit.stat_1062208444@T2` | -0.01263 |
| `desecrated.stat_2250533757@T2` | -0.01136 |
| `explicit.stat_1999113824@T1` | -0.00942 |
| `explicit.stat_1999113824@T2` | -0.00809 |
| `explicit.stat_2923486259@T2` | -0.00785 |
| `explicit.stat_3261801346@T2` | -0.00722 |
| `explicit.stat_1671376347@T2` | -0.00690 |

### armour.gloves — n=22609, R²=-0.3941

intercept: `2.3810`  ·  log_price: True  ·  ilvl: `-0.00245`  ·  n_mods: `-0.01292`  ·  n_top_tier: `0.01107`  ·  corrupted: `0.06053`  ·  n_sockets: `0.01206`  ·  quality: `0.00281`

| stat_id | coef |
|---|---|
| `rune.stat_201332984` | 0.46739 |
| `desecrated.stat_4067062424` | 0.10186 |
| `desecrated.stat_3032590688` | 0.09646 |
| `explicit.stat_9187492` | 0.04216 |
| `rune.stat_789117908` | -0.03959 |
| `explicit.stat_3484657501@T2` | -0.02708 |
| `rune.stat_2418344131` | 0.02337 |
| `desecrated.stat_3299347043` | 0.02251 |
| `explicit.stat_9187492@T2` | -0.02227 |
| `explicit.stat_803737631@T2` | -0.02185 |
| `explicit.stat_53045048@T2` | 0.01815 |
| `explicit.stat_1573130764@T1` | -0.01558 |

### weapon.wand — n=14995, R²=-2.4014

intercept: `3.5918`  ·  log_price: True  ·  ilvl: `-0.04471`  ·  n_mods: `-0.02047`  ·  n_top_tier: `0.02390`  ·  corrupted: `-0.02889`  ·  n_sockets: `0.03877`  ·  quality: `0.01180`

| stat_id | coef |
|---|---|
| `crafted.stat_124131830` | 0.83330 |
| `rune.stat_124131830` | 0.56551 |
| `explicit.stat_4226189338` | 0.19525 |
| `desecrated.stat_2505884597` | 0.10009 |
| `explicit.stat_1600707273` | 0.08316 |
| `explicit.stat_4226189338@T1` | 0.06785 |
| `explicit.stat_1545858329@T1` | 0.05821 |
| `explicit.stat_2254480358@T1` | 0.04709 |
| `desecrated.stat_3278136794` | 0.04552 |
| `explicit.stat_591105508@T1` | 0.04360 |
| `rune.stat_3990135792` | -0.04305 |
| `explicit.stat_1545858329` | 0.04007 |

### weapon.bow — n=12210, R²=-1.9518

intercept: `3.3205`  ·  log_price: True  ·  ilvl: `-0.04080`  ·  n_mods: `-0.01992`  ·  n_top_tier: `0.02594`  ·  corrupted: `0.29184`  ·  n_sockets: `0.00930`  ·  quality: `0.01853`

| stat_id | coef |
|---|---|
| `rune.stat_3885405204` | -1.84060 |
| `crafted.stat_3035140377` | 1.53520 |
| `crafted.stat_518292764` | 0.42776 |
| `desecrated.stat_1202301673` | 0.37531 |
| `explicit.stat_1202301673` | 0.31504 |
| `desecrated.stat_518292764` | 0.22038 |
| `rune.stat_1509134228` | 0.14385 |
| `rune.stat_1631975646` | 0.11163 |
| `rune.stat_1039491398` | -0.11073 |
| `crafted.stat_210067635` | 0.08959 |
| `explicit.stat_518292764` | 0.08031 |
| `rune.stat_1037193709` | 0.07295 |

### weapon.crossbow — n=11476, R²=-1.7475

intercept: `3.2989`  ·  log_price: True  ·  ilvl: `-0.04075`  ·  n_mods: `-0.02363`  ·  n_top_tier: `0.09819`  ·  corrupted: `-0.00160`  ·  n_sockets: `0.04991`  ·  quality: `0.00416`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 0.96380 |
| `rune.stat_55876295` | 0.80012 |
| `rune.stat_2246411426` | -0.65105 |
| `rune.stat_669069897` | -0.41047 |
| `rune.stat_1586906534` | 0.35746 |
| `rune.stat_1509134228` | 0.29832 |
| `explicit.stat_1202301673` | 0.26478 |
| `rune.stat_1039491398` | -0.22047 |
| `explicit.stat_1202301673@T1` | 0.09811 |
| `implicit.stat_1980802737` | 0.07792 |
| `explicit.stat_1202301673@T2` | -0.06255 |
| `explicit.stat_2250681686` | -0.05831 |

### flask.charm — n=9022, R²=-0.4469

intercept: `0.0000`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `-0.00000`  ·  n_top_tier: `0.00138`  ·  corrupted: `0.85712`  ·  quality: `0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 5.03907 |
| `explicit.stat_1056492907` | 3.50136 |
| `explicit.stat_2678930256` | 0.02957 |
| `explicit.stat_3138344128` | 0.02061 |
| `explicit.stat_2676834156@T1` | 0.00883 |
| `explicit.stat_2541588185@T1` | 0.00584 |
| `explicit.stat_2676834156@T2` | -0.00140 |
| `explicit.stat_388617051@T2` | -0.00139 |
| `explicit.stat_828533480@T2` | -0.00139 |
| `explicit.stat_1120862500@T2` | -0.00139 |
| `explicit.stat_1873752457@T2` | -0.00138 |
| `explicit.stat_1873752457@T1` | -0.00138 |

### weapon.warstaff — n=6327, R²=-0.6659

intercept: `-0.2249`  ·  log_price: True  ·  ilvl: `0.00305`  ·  n_mods: `-0.00680`  ·  n_top_tier: `0.01008`  ·  corrupted: `0.13564`  ·  n_sockets: `0.00504`  ·  quality: `0.07365`

| stat_id | coef |
|---|---|
| `rune.stat_243313994` | 2.10409 |
| `rune.stat_731403740` | 1.19677 |
| `desecrated.stat_518292764` | 0.54265 |
| `rune.stat_1712188793` | -0.52650 |
| `desecrated.stat_9187492` | 0.52030 |
| `crafted.stat_3035140377` | 0.44573 |
| `rune.stat_1037193709` | 0.28895 |
| `rune.stat_3336890334` | 0.23570 |
| `rune.stat_2430860292` | -0.11545 |
| `rune.stat_1817052494` | -0.11543 |
| `desecrated.stat_669069897` | -0.11371 |
| `desecrated.stat_55876295` | -0.08974 |

### weapon.sceptre — n=5833, R²=-0.5624

intercept: `-8.2702`  ·  log_price: True  ·  ilvl: `0.10240`  ·  n_mods: `-0.04635`  ·  n_top_tier: `0.18554`  ·  corrupted: `1.27245`  ·  n_sockets: `0.23141`  ·  quality: `0.09975`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452` | 0.22932 |
| `explicit.stat_2162097452@T1` | 0.06647 |
| `rune.stat_3984865854` | 0.05788 |
| `desecrated.stat_3057012405` | 0.05706 |
| `rune.stat_1611856026` | 0.05003 |
| `explicit.stat_1050105434@T2` | -0.04483 |
| `explicit.stat_3639275092@T2` | -0.04447 |
| `explicit.stat_1050105434@T1` | 0.04305 |
| `explicit.stat_328541901@T2` | 0.03920 |
| `desecrated.stat_3984865854` | 0.03898 |
| `explicit.stat_2347036682@T2` | -0.03547 |
| `explicit.stat_328541901@T1` | -0.03453 |

### weapon.staff — n=5821, R²=-0.7101

intercept: `-1.2119`  ·  log_price: True  ·  ilvl: `0.01496`  ·  n_mods: `-0.00724`  ·  n_top_tier: `0.03756`  ·  corrupted: `0.10845`  ·  n_sockets: `0.06162`  ·  quality: `0.03364`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | 4.92652 |
| `crafted.stat_124131830` | 0.40839 |
| `rune.stat_731403740` | 0.31695 |
| `explicit.stat_2254480358` | 0.22142 |
| `rune.stat_3990135792` | -0.15645 |
| `rune.stat_2974417149` | 0.09946 |
| `rune.stat_975988108` | -0.07110 |
| `explicit.stat_4226189338` | 0.03038 |
| `desecrated.stat_3278136794` | 0.03030 |
| `explicit.stat_2254480358@T2` | 0.02789 |
| `explicit.stat_2974417149@T1` | -0.02511 |
| `explicit.stat_293638271@T2` | -0.02506 |

### weapon.spear — n=4922, R²=-0.73

intercept: `-0.1724`  ·  log_price: True  ·  ilvl: `0.00223`  ·  n_mods: `-0.00090`  ·  n_top_tier: `0.00677`  ·  corrupted: `0.00036`  ·  n_sockets: `0.00397`  ·  quality: `0.10459`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 0.67912 |
| `crafted.stat_518292764` | 0.62115 |
| `rune.stat_1039491398` | 0.25255 |
| `rune.stat_1509134228` | -0.19832 |
| `crafted.stat_210067635` | 0.14373 |
| `desecrated.stat_210067635` | 0.03764 |
| `explicit.stat_1202301673@T1` | 0.02449 |
| `desecrated.stat_1509134228` | 0.01558 |
| `explicit.stat_1509134228@T1` | 0.01539 |
| `explicit.stat_3336890334@T1` | 0.01456 |
| `explicit.stat_1202301673@T2` | -0.01236 |
| `explicit.stat_210067635@T1` | 0.01218 |

### armour.focus — n=4008, R²=-0.6049

intercept: `-5.4941`  ·  log_price: True  ·  ilvl: `0.06742`  ·  n_mods: `0.00119`  ·  n_top_tier: `0.10387`  ·  corrupted: `0.34007`  ·  n_sockets: `0.18349`  ·  quality: `0.07982`

| stat_id | coef |
|---|---|
| `explicit.stat_124131830` | 0.52073 |
| `desecrated.stat_3393628375` | 0.08054 |
| `rune.stat_3523867985` | 0.05147 |
| `desecrated.stat_274716455` | 0.04652 |
| `crafted.stat_737908626` | 0.04188 |
| `explicit.stat_4220027924@T2` | -0.04117 |
| `crafted.stat_4015621042` | 0.03986 |
| `explicit.stat_1671376347@T1` | 0.03593 |
| `explicit.stat_4052037485@T1` | 0.03230 |
| `explicit.stat_4052037485@T2` | -0.03213 |
| `crafted.stat_2974417149` | 0.03191 |
| `desecrated.stat_378817135` | 0.03043 |

### armour.quiver — n=3784, R²=-0.6244

intercept: `-5.0982`  ·  log_price: True  ·  ilvl: `0.05878`  ·  n_mods: `0.03781`  ·  n_top_tier: `0.08009`  ·  corrupted: `0.70738`

| stat_id | coef |
|---|---|
| `explicit.stat_1202301673` | 0.67156 |
| `desecrated.stat_3932115504` | 0.25465 |
| `desecrated.stat_4067062424` | -0.17808 |
| `desecrated.stat_681332047` | 0.16481 |
| `desecrated.stat_2194114101` | 0.15919 |
| `desecrated.stat_3714003708` | 0.06631 |
| `desecrated.stat_3032590688` | -0.05327 |
| `explicit.stat_1241625305@T1` | 0.04193 |
| `explicit.stat_3759663284@T1` | 0.03797 |
| `explicit.stat_2194114101@T2` | -0.03547 |
| `explicit.stat_681332047@T2` | -0.03500 |
| `explicit.stat_2321178454@T2` | -0.03162 |

### armour.shield — n=3277, R²=-0.6647

intercept: `-0.9786`  ·  log_price: True  ·  ilvl: `0.01223`  ·  n_mods: `-0.00041`  ·  n_top_tier: `0.00860`  ·  corrupted: `0.09638`  ·  n_sockets: `-0.00270`  ·  quality: `0.07840`

| stat_id | coef |
|---|---|
| `explicit.stat_1978899297` | 0.75502 |
| `explicit.stat_2923486259` | -0.14000 |
| `pseudo.total_chaos_res` | 0.13959 |
| `rune.stat_3523867985` | 0.11270 |
| `explicit.stat_4095671657` | 0.07599 |
| `pseudo.total_ele_res>=80` | 0.04361 |
| `explicit.stat_1011760251` | 0.03170 |
| `explicit.stat_1978899297@T2` | -0.01786 |
| `explicit.stat_4220027924@T1` | 0.01529 |
| `explicit.stat_2451402625@T1` | -0.01429 |
| `explicit.stat_3676141501` | 0.01423 |
| `explicit.stat_3372524247@T2` | -0.01221 |

### weapon.twomace — n=2950, R²=-0.6467

intercept: `-1.8150`  ·  log_price: True  ·  ilvl: `0.02300`  ·  n_mods: `-0.00313`  ·  n_top_tier: `0.02522`  ·  corrupted: `0.75036`  ·  n_sockets: `0.10364`  ·  quality: `0.05166`

| stat_id | coef |
|---|---|
| `crafted.stat_3035140377` | 0.98712 |
| `crafted.stat_210067635` | 0.08778 |
| `rune.stat_1039491398` | 0.08472 |
| `` | 0.05819 |
| `crafted.stat_1940865751` | 0.04449 |
| `rune.stat_859085781` | -0.03747 |
| `explicit.stat_387439868@T2` | -0.03555 |
| `explicit.stat_387439868@T1` | 0.03518 |
| `explicit.stat_1368271171@T2` | 0.03365 |
| `explicit.stat_791928121@T2` | 0.02415 |
| `rune.stat_1509134228` | -0.02012 |
| `implicit.stat_1503146834` | -0.02000 |

## Coverage (listings per base)

- … **Sapphire** — 17194 listings (17169 priced) [0.4–7553463.8 ex]
- … **Emerald** — 16961 listings (16941 priced) [0.4–7553463.8 ex]
- … **Ruby** — 13040 listings (13028 priced) [0.3–308559482.1 ex]
- … **Utility Belt** — 7426 listings (7419 priced) [0.2–5288620.9 ex]
- … **Prismatic Ring** — 5972 listings (5966 priced) [0.2–24532814.5 ex]
- … **Solar Amulet** — 5828 listings (5818 priced) [1.0–634893788.3 ex]
- … **Amethyst Ring** — 5729 listings (5726 priced) [0.2–4323655.9 ex]
- … **Stellar Amulet** — 5581 listings (5578 priced) [0.3–35690283.3 ex]
- … **Gold Amulet** — 5491 listings (5482 priced) [0.3–4894457.0 ex]
- … **Gold Ring** — 5329 listings (5325 priced) [0.2–24532814.5 ex]
- … **Dueling Wand** — 4738 listings (4728 priced) [0.3–4297682211.9 ex]
- … **Sapphire Ring** — 4471 listings (4466 priced) [0.2–307202867.9 ex]
- … **Topaz Ring** — 4345 listings (4342 priced) [1.0–307202867.9 ex]
- … **Ruby Ring** — 4337 listings (4335 priced) [0.2–37474957.5 ex]
- … **Plate Belt** — 3939 listings (3934 priced) [0.2–5286174.1 ex]
- … **Lapis Amulet** — 3901 listings (3899 priced) [0.2–5286174.1 ex]
- … **Ancestral Tiara** — 3840 listings (3834 priced) [0.6–41469259.3 ex]
- … **Amber Amulet** — 3795 listings (3794 priced) [0.3–124352753.2 ex]
- … **Jade Amulet** — 3776 listings (3773 priced) [0.2–4547453.5 ex]
- … **Unset Ring** — 3684 listings (3683 priced) [0.2–24532814.5 ex]
- … **Obliterator Bow** — 3630 listings (3621 priced) [0.4–42622633798.0 ex]
- … **Heavy Belt** — 3621 listings (3620 priced) [0.2–4877938.3 ex]
- … **Bloodstone Amulet** — 3565 listings (3563 priced) [0.2–4275054.0 ex]
- … **Pearl Ring** — 3452 listings (3450 priced) [0.2–24532814.5 ex]
- … **Azure Amulet** — 3403 listings (3403 priced) [0.2–123132003.2 ex]
