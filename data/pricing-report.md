# POE2 Rare Pricing — Runes of Aldur

_Generated 2026-07-23T01:14:22+00:00 by POE2-Scanner 0.1.0._

## Dataset
- Rare listings: **751995** (749572 priced in exalted)
- Distinct bases: 1003 · distinct mods: 3355 · mod rows: 3552520
- Sold signals: **23984** sold · 428257 censored (left the sample window, fate unknown)
- Observed: 2026-07-01T20:49:02+00:00 → 2026-07-23T01:01:41+00:00

## Prediction accuracy (holdout backtest)

Newest ~20% of each group held out (split at scan boundaries, relist duplicates dropped); equation fitted on the rest predicts them.

- Typical error: **×22.59** (median |log error| 3.1175)
- Within ±30% of asking price: **18%**
- Skill vs constant-price guess: **+0.08** (> 0 = the mods carry signal)
- Calibration: 79% of actuals above prediction (target ≈ 75%)
- Premium segment (5ex+): skill **+0.13** · typical error ×62.92 · ±30% 5% · n=109198
- Premium segment (60ex+): skill **+0.13** · typical error ×329.74 · ±30% 0% · n=72434

| group | n_test | ×err | ±30% | skill | gbm |
|---|---|---|---|---|---|
| accessory.ring | 16224 | ×44.38 | 21% | +0.04 | +0.06 |
| jewel | 15772 | ×55.19 | 21% | +0.02 | +0.03 |
| accessory.amulet | 14532 | ×24.15 | 16% | +0.04 | +0.04 |
| accessory.belt | 10222 | ×24.19 | 17% | +0.06 | +0.09 |
| armour.chest | 9936 | ×16.49 | 21% | +0.08 | +0.11 |
| armour.helmet | 9701 | ×26.21 | 18% | +0.08 | +0.11 |
| armour.boots | 8916 | ×22.78 | 17% | +0.11 | +0.13 |
| armour.gloves | 8802 | ×31.72 | 13% | +0.09 | +0.11 |
| other | 8690 | ×1.78 | 44% | +0.13 | +0.18 |
| weapon.wand | 5127 | ×35.69 | 13% | +0.12 | +0.13 |
| weapon.bow | 4041 | ×23.23 | 12% | +0.17 | +0.18 |
| weapon.crossbow | 3765 | ×24.22 | 12% | +0.13 | +0.18 |
| weapon.warstaff | 2653 | ×13.62 | 7% | +0.15 | +0.16 |
| weapon.staff | 2554 | ×15.83 | 6% | +0.13 | +0.14 |
| weapon.sceptre | 2510 | ×17.10 | 5% | +0.07 | +0.07 |
| weapon.spear | 1993 | ×12.73 | 6% | +0.12 | +0.15 |
| armour.focus | 1655 | ×13.85 | 6% | +0.10 | +0.12 |
| armour.quiver | 1568 | ×18.32 | 7% | +0.12 | +0.13 |
| armour.shield | 1279 | ×7.68 | 8% | +0.10 | +0.11 |
| flask.charm | 1272 | ×10.00 | 27% | +0.03 | +0.03 |
| weapon.twomace | 1178 | ×8.95 | 6% | +0.09 | +0.10 |

## Fitted price equations

Consumer evaluates: `price_exalted = exp(intercept + Σ coef[stat_id] × mod_value)` (when `log_price` is true).

_Grouped by **category**._

### jewel — n=86899, R²=-1.9134

intercept: `-0.0559`  ·  log_price: True  ·  ilvl: `0.00069`  ·  n_mods: `0.98636`  ·  n_top_tier: `-0.88556`  ·  corrupted: `1.11913`  ·  quality: `-0.06937`

| stat_id | coef |
|---|---|
| `explicit.stat_3485067555@T1` | 3.60249 |
| `explicit.stat_1604736568@T1` | -1.98009 |
| `explicit.stat_1604736568` | 1.89164 |
| `explicit.stat_274716455@T1` | -1.29999 |
| `explicit.stat_3556824919@T1` | 1.04053 |
| `explicit.stat_2194114101@T1` | -0.67880 |
| `explicit.stat_681332047@T1` | -0.53039 |
| `explicit.stat_3714003708@T1` | 0.47793 |
| `explicit.stat_2023107756@T1` | -0.38331 |
| `explicit.stat_3174700878@T1` | 0.31816 |
| `explicit.stat_2023107756` | 0.28325 |
| `explicit.stat_587431675@T1` | -0.26598 |

### accessory.ring — n=74197, R²=-2.0208

intercept: `3.2211`  ·  log_price: True  ·  ilvl: `-0.04051`  ·  n_mods: `0.00139`  ·  n_top_tier: `0.95340`  ·  corrupted: `-0.00030`  ·  n_sockets: `2.21624`  ·  quality: `0.00051`

| stat_id | coef |
|---|---|
| `explicit.stat_1573130764@T1` | -1.00698 |
| `explicit.stat_1263695895@T2` | -0.99394 |
| `explicit.stat_1573130764@T2` | -0.98160 |
| `explicit.stat_1263695895@T1` | -0.97975 |
| `explicit.stat_4080418644@T1` | -0.97623 |
| `explicit.stat_2891184298@T1` | -0.97313 |
| `explicit.stat_3917489142@T2` | -0.97208 |
| `explicit.stat_2923486259@T2` | -0.97125 |
| `explicit.stat_2901986750@T2` | -0.96869 |
| `explicit.stat_1671376347@T2` | -0.96721 |
| `explicit.stat_3695891184@T1` | -0.96719 |
| `explicit.stat_2144192055@T1` | -0.96712 |

### other — n=71607, R²=-0.6831

intercept: `1.6092`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.08514`  ·  n_top_tier: `0.26144`  ·  corrupted: `-0.00001`  ·  n_sockets: `-0.00004`  ·  quality: `-0.00000`

| stat_id | coef |
|---|---|
| `explicit.stat_1050105434@T1` | -0.40254 |
| `implicit.stat_718638445` | 0.25545 |
| `implicit.stat_3182714256` | 0.25544 |
| `explicit.stat_3299347043@T1` | -0.24268 |
| `implicit.stat_2219129443` | 0.22173 |
| `explicit.stat_3917489142@T1` | -0.18459 |
| `explicit.stat_2974417149@T1` | 0.13862 |
| `implicit.stat_958696139` | -0.08512 |
| `explicit.stat_789117908@T1` | -0.06270 |
| `implicit.stat_1416292992` | -0.05676 |
| `explicit.stat_736967255@T1` | -0.04272 |
| `implicit.stat_3879011313` | 0.04159 |

### accessory.amulet — n=66459, R²=-2.0808

intercept: `3.0322`  ·  log_price: True  ·  ilvl: `-0.04007`  ·  n_mods: `-0.00129`  ·  n_top_tier: `0.96615`  ·  corrupted: `0.09331`  ·  n_sockets: `-0.07686`  ·  quality: `0.06790`

| stat_id | coef |
|---|---|
| `explicit.stat_3299347043@T2` | -1.64784 |
| `explicit.stat_3299347043@T1` | -1.57612 |
| `explicit.stat_4080418644@T1` | -1.09223 |
| `explicit.stat_2866361420@T1` | -1.08867 |
| `explicit.stat_2974417149@T1` | -1.07773 |
| `explicit.stat_2901986750@T1` | -1.06721 |
| `explicit.stat_2866361420@T2` | -1.05458 |
| `explicit.stat_803737631@T1` | -1.05426 |
| `explicit.stat_2974417149@T2` | -1.04439 |
| `explicit.stat_1050105434@T1` | -1.03631 |
| `explicit.stat_4080418644@T2` | -1.02762 |
| `explicit.stat_1202301673@T2` | -1.02469 |

### accessory.belt — n=46850, R²=-1.6443

intercept: `4.5352`  ·  log_price: True  ·  ilvl: `-0.05492`  ·  n_mods: `-0.02898`  ·  n_top_tier: `0.75362`  ·  corrupted: `1.09814`  ·  n_sockets: `1.59722`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | 1.25813 |
| `explicit.stat_3299347043@T2` | -0.81756 |
| `explicit.stat_2881298780@T1` | -0.79197 |
| `explicit.stat_51994685@T1` | -0.78325 |
| `explicit.stat_915769802@T1` | -0.78013 |
| `explicit.stat_809229260@T2` | -0.77643 |
| `explicit.stat_1570770415@T2` | -0.77374 |
| `explicit.stat_3299347043@T1` | -0.76796 |
| `explicit.stat_3325883026@T1` | -0.76387 |
| `explicit.stat_3585532255@T2` | -0.75870 |
| `explicit.stat_4080418644@T2` | -0.75363 |
| `explicit.stat_3372524247@T2` | -0.75067 |

### armour.chest — n=46470, R²=-1.7673

intercept: `3.3871`  ·  log_price: True  ·  ilvl: `-0.04146`  ·  n_mods: `-0.01838`  ·  n_top_tier: `0.38886`  ·  corrupted: `0.28317`  ·  n_sockets: `0.03385`  ·  quality: `0.07431`

| stat_id | coef |
|---|---|
| `implicit.stat_2251279027` | 1.96317 |
| `explicit.stat_3981240776@T1` | 0.53002 |
| `explicit.stat_986397080@T2` | -0.45209 |
| `explicit.stat_4080418644@T2` | -0.43915 |
| `explicit.stat_986397080@T1` | -0.43085 |
| `explicit.stat_3484657501@T1` | -0.42592 |
| `explicit.stat_4080418644@T1` | -0.42263 |
| `explicit.stat_2451402625@T2` | -0.41790 |
| `explicit.stat_1692879867@T2` | -0.41777 |
| `explicit.stat_915769802@T2` | -0.41550 |
| `explicit.stat_915769802@T1` | -0.41542 |
| `explicit.stat_1999113824@T1` | -0.41403 |

### armour.helmet — n=45194, R²=-1.7481

intercept: `3.3347`  ·  log_price: True  ·  ilvl: `-0.04182`  ·  n_mods: `-0.02358`  ·  n_top_tier: `0.52965`  ·  corrupted: `0.61617`  ·  n_sockets: `0.06911`  ·  quality: `0.07302`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -3.81278 |
| `explicit.stat_1263695895@T1` | -0.83162 |
| `explicit.stat_3917489142@T2` | -0.72115 |
| `explicit.stat_2162097452@T2` | -0.67501 |
| `explicit.stat_3917489142@T1` | -0.66139 |
| `explicit.stat_4052037485@T2` | -0.63179 |
| `explicit.stat_4015621042@T2` | -0.61977 |
| `explicit.stat_1263695895@T2` | -0.60828 |
| `explicit.stat_4052037485@T1` | -0.59899 |
| `explicit.stat_3321629045@T2` | -0.58199 |
| `explicit.stat_803737631@T1` | -0.57672 |
| `explicit.stat_1999113824@T1` | -0.57576 |

### armour.boots — n=41656, R²=-1.648

intercept: `3.8102`  ·  log_price: True  ·  ilvl: `-0.04669`  ·  n_mods: `-0.04004`  ·  n_top_tier: `0.44051`  ·  corrupted: `0.09865`  ·  n_sockets: `0.06783`  ·  quality: `0.07205`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | -2.82340 |
| `explicit.stat_2250533757@T1` | 1.73210 |
| `crafted.stat_3917489142@T1` | 1.38076 |
| `explicit.stat_3299347043@T1` | -0.64171 |
| `explicit.stat_2923486259@T2` | -0.56463 |
| `explicit.stat_2923486259@T1` | 0.51881 |
| `explicit.stat_2160282525@T1` | -0.50440 |
| `explicit.stat_3917489142@T2` | -0.50277 |
| `explicit.stat_1062208444@T2` | -0.50180 |
| `explicit.stat_1671376347@T2` | -0.50102 |
| `explicit.stat_1874553720@T1` | -0.49584 |
| `explicit.stat_328541901@T2` | -0.49360 |

### armour.gloves — n=40670, R²=-1.6573

intercept: `3.8340`  ·  log_price: True  ·  ilvl: `-0.05010`  ·  n_mods: `-0.01129`  ·  n_top_tier: `0.73673`  ·  corrupted: `-0.04505`  ·  n_sockets: `0.18985`  ·  quality: `0.05789`

| stat_id | coef |
|---|---|
| `explicit.stat_2339757871@T1` | 1.38906 |
| `rune.stat_201332984` | 1.10729 |
| `explicit.stat_2923486259@T1` | -1.07684 |
| `explicit.stat_4052037485@T1` | -1.05229 |
| `explicit.stat_4052037485@T2` | -1.00615 |
| `explicit.stat_2923486259@T2` | -0.95405 |
| `explicit.stat_4015621042@T2` | -0.93497 |
| `explicit.stat_3321629045@T2` | -0.93095 |
| `explicit.stat_3917489142@T2` | -0.90179 |
| `explicit.stat_9187492@T2` | -0.88782 |
| `explicit.stat_3484657501@T1` | -0.88310 |
| `explicit.stat_803737631@T1` | -0.87796 |

### weapon.wand — n=23793, R²=-1.8744

intercept: `3.8802`  ·  log_price: True  ·  ilvl: `-0.04791`  ·  n_mods: `-0.06859`  ·  n_top_tier: `0.67622`  ·  corrupted: `0.22649`  ·  n_sockets: `0.02679`  ·  quality: `0.03130`

| stat_id | coef |
|---|---|
| `rune.stat_124131830` | -4.25764 |
| `explicit.stat_2254480358@T1` | 2.64524 |
| `explicit.stat_1545858329@T1` | 2.61316 |
| `explicit.stat_124131830@T1` | 1.90766 |
| `explicit.stat_591105508@T1` | 1.79910 |
| `explicit.stat_4226189338@T1` | 1.74483 |
| `crafted.stat_124131830` | 1.23139 |
| `explicit.stat_2254480358@T2` | 1.15378 |
| `explicit.stat_1263695895@T2` | -1.03051 |
| `explicit.stat_1600707273@T1` | 1.01378 |
| `explicit.stat_473429811@T1` | -0.93632 |
| `explicit.stat_473429811@T2` | -0.92447 |

### flask.charm — n=21147, R²=-0.6724

intercept: `0.1066`  ·  log_price: True  ·  ilvl: `0.00000`  ·  n_mods: `0.00001`  ·  n_top_tier: `0.69287`  ·  corrupted: `1.53950`  ·  quality: `0.01712`

| stat_id | coef |
|---|---|
| `explicit.stat_618665892` | 4.59574 |
| `explicit.stat_1056492907` | 2.54434 |
| `explicit.stat_3246948616` | 2.29595 |
| `explicit.stat_2541588185@T1` | 1.56524 |
| `explicit.stat_2365392475@T1` | 0.91667 |
| `explicit.stat_1120862500@T1` | 0.91574 |
| `explicit.stat_2676834156@T1` | 0.90483 |
| `explicit.stat_828533480@T2` | -0.69290 |
| `explicit.stat_1120862500@T2` | -0.69288 |
| `explicit.stat_1873752457@T2` | -0.69287 |
| `explicit.stat_2541588185@T2` | -0.69286 |
| `explicit.stat_388617051@T2` | -0.69286 |

### weapon.bow — n=18997, R²=-1.7886

intercept: `3.8355`  ·  log_price: True  ·  ilvl: `-0.04535`  ·  n_mods: `-0.09770`  ·  n_top_tier: `0.76908`  ·  corrupted: `0.54993`  ·  n_sockets: `0.03645`  ·  quality: `0.02927`

| stat_id | coef |
|---|---|
| `desecrated.stat_666077204@T1` | 5.92391 |
| `desecrated.stat_210067635@T1` | -1.51341 |
| `explicit.stat_1263695895@T1` | -1.39207 |
| `crafted.stat_210067635@T2` | -1.28463 |
| `explicit.stat_1263695895@T2` | -1.24318 |
| `crafted.stat_3035140377` | 1.22053 |
| `explicit.stat_2463230181@T2` | -1.06399 |
| `explicit.stat_3695891184@T1` | -0.99951 |
| `explicit.stat_1509134228@T1` | -0.99438 |
| `explicit.stat_210067635@T2` | -0.96838 |
| `explicit.stat_1368271171@T1` | -0.91371 |
| `explicit.stat_1368271171@T2` | -0.88744 |

### weapon.crossbow — n=17787, R²=-1.6368

intercept: `4.0265`  ·  log_price: True  ·  ilvl: `-0.04681`  ·  n_mods: `-0.11719`  ·  n_top_tier: `0.28067`  ·  corrupted: `-0.00930`  ·  n_sockets: `0.09926`  ·  quality: `0.01574`

| stat_id | coef |
|---|---|
| `explicit.stat_1980802737@T2` | -1.70098 |
| `explicit.stat_1980802737` | 1.47804 |
| `explicit.stat_1202301673@T1` | 1.40105 |
| `explicit.stat_2250681686@T2` | -1.22065 |
| `explicit.stat_1509134228@T1` | 1.13519 |
| `explicit.stat_2250681686` | 1.04720 |
| `explicit.stat_709508406@T1` | 0.96122 |
| `crafted.stat_3035140377` | 0.87953 |
| `rune.stat_731403740` | 0.65523 |
| `explicit.stat_210067635@T2` | -0.56991 |
| `explicit.stat_3336890334@T2` | -0.53813 |
| `explicit.stat_3695891184@T1` | -0.52385 |

### weapon.warstaff — n=12655, R²=-0.3317

intercept: `-10.3893`  ·  log_price: True  ·  ilvl: `0.14180`  ·  n_mods: `-0.23799`  ·  n_top_tier: `0.50061`  ·  corrupted: `0.38196`  ·  n_sockets: `0.12790`  ·  quality: `0.05414`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | 1.03624 |
| `explicit.stat_210067635@T1` | -0.88179 |
| `explicit.stat_328541901@T1` | -0.85948 |
| `explicit.stat_328541901@T2` | -0.83913 |
| `desecrated.stat_9187492` | 0.81259 |
| `explicit.stat_1037193709@T2` | -0.75465 |
| `explicit.stat_821021828@T2` | -0.73254 |
| `desecrated.stat_473429811@T1` | -0.72570 |
| `desecrated.stat_3291658075@T1` | -0.72570 |
| `explicit.stat_1940865751@T1` | -0.69918 |
| `rune.stat_243313994` | 0.65926 |
| `explicit.stat_1940865751@T2` | -0.64907 |

### weapon.staff — n=12054, R²=-0.3464

intercept: `-16.9110`  ·  log_price: True  ·  ilvl: `0.21825`  ·  n_mods: `-0.12674`  ·  n_top_tier: `0.50794`  ·  corrupted: `0.82358`  ·  n_sockets: `0.18991`  ·  quality: `0.03499`

| stat_id | coef |
|---|---|
| `explicit.stat_591105508@T1` | 1.95234 |
| `explicit.stat_4226189338@T1` | 1.67915 |
| `explicit.stat_124131830@T1` | 1.60538 |
| `explicit.stat_1600707273@T1` | 1.53975 |
| `rune.stat_124131830` | 1.21799 |
| `explicit.stat_1545858329@T1` | 1.16232 |
| `explicit.stat_473429811@T2` | -0.85356 |
| `explicit.stat_591105508@T2` | 0.72299 |
| `explicit.stat_3962278098@T2` | 0.70438 |
| `explicit.stat_2768835289@T2` | -0.66450 |
| `explicit.stat_3015669065@T2` | -0.65966 |
| `explicit.stat_293638271@T2` | -0.64506 |

### weapon.sceptre — n=11700, R²=-0.3288

intercept: `-21.8681`  ·  log_price: True  ·  ilvl: `0.27920`  ·  n_mods: `-0.04960`  ·  n_top_tier: `0.18991`  ·  corrupted: `0.26483`  ·  n_sockets: `0.20920`  ·  quality: `0.03464`

| stat_id | coef |
|---|---|
| `explicit.stat_2162097452@T1` | 2.54285 |
| `explicit.stat_2162097452@T2` | 1.01199 |
| `explicit.stat_4080418644@T2` | -0.95958 |
| `explicit.stat_1798257884@T2` | 0.88443 |
| `explicit.stat_3057012405@T1` | 0.81399 |
| `explicit.stat_4080418644@T1` | -0.58072 |
| `explicit.stat_101878827@T1` | 0.55546 |
| `explicit.stat_2854751904@T2` | -0.55347 |
| `explicit.stat_849987426@T1` | 0.48955 |
| `explicit.stat_1574590649@T2` | -0.42168 |
| `explicit.stat_2347036682@T2` | -0.41090 |
| `explicit.stat_1050105434@T1` | 0.39944 |

### weapon.spear — n=9526, R²=-0.3738

intercept: `-14.6493`  ·  log_price: True  ·  ilvl: `0.19779`  ·  n_mods: `-0.16079`  ·  n_top_tier: `0.57109`  ·  corrupted: `-0.50276`  ·  n_sockets: `0.21945`  ·  quality: `0.06574`

| stat_id | coef |
|---|---|
| `crafted.stat_210067635@T2` | -3.63021 |
| `explicit.stat_1037193709@T1` | -1.39381 |
| `desecrated.stat_666077204@T1` | -1.29867 |
| `desecrated.stat_210067635@T1` | -1.14495 |
| `crafted.stat_3035140377` | 1.12294 |
| `explicit.stat_9187492@T2` | -1.04825 |
| `explicit.stat_4080418644@T2` | -1.02308 |
| `explicit.stat_4080418644@T1` | -0.99622 |
| `explicit.stat_748522257@T2` | -0.92112 |
| `explicit.stat_1940865751@T2` | -0.90983 |
| `explicit.stat_3336890334@T2` | -0.89643 |
| `explicit.stat_1202301673@T1` | 0.83755 |

### armour.focus — n=7791, R²=-0.3303

intercept: `-16.3497`  ·  log_price: True  ·  ilvl: `0.20854`  ·  n_mods: `-0.18071`  ·  n_top_tier: `1.00290`  ·  corrupted: `0.04726`  ·  n_sockets: `0.44962`  ·  quality: `0.02261`

| stat_id | coef |
|---|---|
| `explicit.stat_2923486259@T1` | -1.68088 |
| `explicit.stat_4220027924@T1` | -1.48926 |
| `crafted.stat_737908626@T2` | 1.41555 |
| `explicit.stat_3962278098@T2` | -1.34782 |
| `explicit.stat_2231156303@T1` | -1.28375 |
| `crafted.stat_2974417149@T1` | 1.24690 |
| `explicit.stat_2923486259@T2` | -1.24149 |
| `explicit.stat_2339757871@T2` | -1.22902 |
| `explicit.stat_2768835289@T1` | -1.21680 |
| `explicit.stat_3291658075@T2` | -1.16319 |
| `explicit.stat_2231156303@T2` | -1.16207 |
| `explicit.stat_4220027924@T2` | -1.13228 |

### armour.quiver — n=7254, R²=-0.2651

intercept: `-18.2562`  ·  log_price: True  ·  ilvl: `0.22062`  ·  n_mods: `-0.04644`  ·  n_top_tier: `0.60942`  ·  corrupted: `1.01303`

| stat_id | coef |
|---|---|
| `desecrated.stat_3932115504@T1` | 5.25664 |
| `explicit.stat_681332047@T2` | -1.27339 |
| `explicit.stat_681332047@T1` | -1.10123 |
| `explicit.stat_1573130764@T2` | -0.90350 |
| `explicit.stat_2194114101@T2` | -0.80250 |
| `explicit.stat_1573130764@T1` | -0.75162 |
| `explicit.stat_2463230181@T1` | 0.67459 |
| `explicit.stat_2321178454@T2` | -0.64835 |
| `explicit.stat_4067062424@T1` | -0.61824 |
| `explicit.stat_4067062424@T2` | -0.59494 |
| `explicit.stat_803737631@T1` | -0.53700 |
| `explicit.stat_3714003708@T2` | -0.53102 |

### armour.shield — n=6240, R²=-0.4009

intercept: `-13.1322`  ·  log_price: True  ·  ilvl: `0.17761`  ·  n_mods: `-0.17149`  ·  n_top_tier: `0.61000`  ·  corrupted: `-0.61522`  ·  n_sockets: `0.34763`  ·  quality: `0.04419`

| stat_id | coef |
|---|---|
| `explicit.stat_4095671657@T1` | -1.63368 |
| `explicit.stat_3855016469@T1` | -1.51187 |
| `explicit.stat_4095671657@T2` | -1.33604 |
| `explicit.stat_2923486259@T1` | -1.22605 |
| `explicit.stat_328541901@T1` | -1.17625 |
| `explicit.stat_1011760251@T1` | -1.15519 |
| `explicit.stat_2901986750@T1` | -1.15227 |
| `explicit.stat_3033371881@T2` | -1.09683 |
| `explicit.stat_4052037485@T1` | -0.93552 |
| `explicit.stat_3321629045@T2` | -0.90410 |
| `explicit.stat_3484657501@T2` | -0.89694 |
| `explicit.stat_2901986750@T2` | -0.88748 |

### weapon.twomace — n=5688, R²=-0.4354

intercept: `-11.0747`  ·  log_price: True  ·  ilvl: `0.15155`  ·  n_mods: `-0.21967`  ·  n_top_tier: `0.40598`  ·  corrupted: `0.83783`  ·  n_sockets: `0.17339`  ·  quality: `0.06190`

| stat_id | coef |
|---|---|
| `desecrated.stat_210067635@T1` | -5.81999 |
| `desecrated.stat_1509134228@T1` | 2.79674 |
| `explicit.stat_1037193709@T1` | -1.41164 |
| `explicit.stat_3336890334@T1` | -1.15721 |
| `explicit.stat_1263695895@T2` | -1.08634 |
| `explicit.stat_9187492@T1` | -1.06871 |
| `explicit.stat_2694482655@T1` | 0.84770 |
| `explicit.stat_210067635@T1` | -0.75566 |
| `explicit.stat_518292764@T2` | -0.65386 |
| `explicit.stat_821021828@T1` | -0.59965 |
| `explicit.stat_3695891184@T2` | -0.57038 |
| `explicit.stat_709508406@T1` | 0.54701 |

## Coverage (listings per base)

- … **Sapphire** — 39906 listings (39839 priced) [0.3–39887666593.4 ex]
- … **Emerald** — 38792 listings (38739 priced) [0.3–39887666593.4 ex]
- … **Ruby** — 29727 listings (29695 priced) [0.3–3985176410.3 ex]
- … **Utility Belt** — 13375 listings (13355 priced) [0.2–398916549611043.2 ex]
- … **Prismatic Ring** — 12404 listings (12377 priced) [0.2–398916549611043.2 ex]
- … **Solar Amulet** — 12060 listings (12034 priced) [0.3–3985176410.3 ex]
- … **Amethyst Ring** — 11915 listings (11900 priced) [0.2–398916545621877.7 ex]
- … **Gold Amulet** — 11192 listings (11165 priced) [0.3–39887666593.4 ex]
- … **Gold Ring** — 11154 listings (11131 priced) [0.2–3985176410.3 ex]
- … **Stellar Amulet** — 10551 listings (10538 priced) [0.3–398916549611043.2 ex]
- … **Sapphire Ring** — 9233 listings (9218 priced) [0.2–398916549611043.2 ex]
- … **Topaz Ring** — 8904 listings (8893 priced) [0.3–398916549611043.2 ex]
- … **Ruby Ring** — 8807 listings (8797 priced) [0.2–3985176410.3 ex]
- … **Dueling Wand** — 7705 listings (7681 priced) [0.3–398916553600208.8 ex]
- … **Unset Ring** — 7636 listings (7614 priced) [0.2–39887666593.4 ex]
- … **Lapis Amulet** — 7592 listings (7584 priced) [0.3–398916549611043.2 ex]
- … **Jade Amulet** — 7553 listings (7537 priced) [0.3–398916545621877.7 ex]
- … **Amber Amulet** — 7487 listings (7478 priced) [0.3–3985176410.3 ex]
- … **Pearl Ring** — 7378 listings (7369 priced) [0.2–398916549611043.2 ex]
- … **Plate Belt** — 7325 listings (7293 priced) [0.3–398916553600208.8 ex]
- … **Ancestral Tiara** — 7267 listings (7234 priced) [0.3–398912568423.8 ex]
- … **Bloodstone Amulet** — 7237 listings (7225 priced) [0.3–4275054.0 ex]
- … **Azure Amulet** — 6907 listings (6903 priced) [0.3–3985176410.3 ex]
- … **Lunar Amulet** — 6841 listings (6826 priced) [0.3–398916549611043.2 ex]
- … **Heavy Belt** — 6450 listings (6434 priced) [0.3–398916553600208.8 ex]
