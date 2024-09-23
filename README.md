# Django Terran Fixtures

This repository contains fixtures for the `django-terran` application. The fixtures include data for:

- Currencies;
- Countries;
- Administrative divisions of countries;
- Settlements;
- and relationships between them all.

This repository exists so that you can conviniently download prebuilt fixtures as a ZIP file.

## What is Django Terran?

See https://github.com/django-terran/django-terran

## How to use?

Load these fixtures just like any other Django fixture

Load mandatory fixtures with
```
./manage.py loadadata <path/to/fixtures>/mandatory.json
```
or with
```
./manage.py loadadata <path/to/fixtures>/currencies.json
./manage.py loadadata <path/to/fixtures>/countries.json
./manage.py loadadata <path/to/fixtures>/level1areas.json
./manage.py loadadata <path/to/fixtures>/level2areas.json
```

Optional fixtures include files under "settlements" and "settlements_10k" directory.
```
./manage.py loadadata <path/to/fixtures>/settlements/GE.json
```

**DO NOT load optional fixtures from "settlements" if you are not positive you need them.**

These fixtures include every small village.
They are huge, they will add more than 2Gb to your database.
If you need settlements at all start with "settlements_10k" fixtures which include settlements with population more than 10 thousands people.
Load only specific countries from "settlements" and only if required.

So, to sum up, this is a recommended setup:
```bash
./manage.py loaddata <path/to/fixtures>/mandatory.json
```
this is also a recommended setup:
```bash
./manage.py loaddata <path/to/fixtures>/mandatory.json

for FILE in <path/to/fixtures>/settlements_10k/*
do
    ./manage.py loaddata $FILE
done
```
this is a supported, but not a recommended setup:
```bash
./manage.py loaddata <path/to/fixtures>/mandatory.json

for FILE in <path/to/fixtures>/settlements/*
do
    ./manage.py loaddata $FILE
done
```

## How can I help?

See https://github.com/django-terran/django-terran-data

## Statistics (I need to show off or something...)

| Country | Currencies | Level 1<br/>Administrative<br/>Divisions | Level 2<br/>Administrative<br/>Divisions | Settlements | Settlements 10K+ |
| :-- | --: | --: | --: | --: | --: |
| AD, Andorra | 4 | 7 | - | 68 | 1 |
| AE, United Arab Emirates | 1 | 7 | - | 506 | 10 |
| AF, Afghanistan | 2 | 34 | - | 4507 | 33 |
| AG, Antigua & Barbuda | 1 | 8 | - | 54 | 1 |
| AL, Albania | 2 | 12 | - | 4604 | 30 |
| AM, Armenia | 3 | 11 | - | 1044 | 27 |
| AO, Angola | 4 | 18 | - | 4192 | 51 |
| AR, Argentina | 5 | 24 | - | 7864 | 562 |
| AT, Austria | 2 | 9 | - | 21660 | 67 |
| AU, Australia | 1 | 8 | - | 8034 | 135 |
| AZ, Azerbaijan | 4 | 70 | 8 | 4138 | 95 |
| BA, Bosnia & Herzegovina | 6 | 3 | - | 8772 | 38 |
| BB, Barbados | 2 | 11 | - | 319 | 1 |
| BD, Bangladesh | 3 | 8 | 64 | 4159 | 71 |
| BE, Belgium | 3 | 3 | 10 | 5992 | 259 |
| BF, Burkina Faso | 1 | 13 | 45 | 15301 | 58 |
| BG, Bulgaria | 4 | 28 | - | 6759 | 79 |
| BH, Bahrain | 1 | 4 | - | 26 | 11 |
| BI, Burundi | 1 | 18 | - | 1869 | 118 |
| BJ, Benin | 1 | 12 | - | 6070 | 49 |
| BN, Brunei | 2 | 4 | - | 148 | 7 |
| BO, Bolivia | 3 | 9 | - | 17421 | 53 |
| BR, Brazil | 7 | 27 | - | 76832 | 3157 |
| BS, Bahamas | 1 | 32 | - | 171 | 2 |
| BT, Bhutan | 2 | 20 | - | 856 | 2 |
| BW, Botswana | 2 | 16 | - | 620 | 19 |
| BY, Belarus | 5 | 7 | - | 21900 | 84 |
| BZ, Belize | 1 | 6 | - | 327 | 6 |
| CA, Canada | 1 | 13 | - | 10998 | 248 |
| CD, Congo - Kinshasa | 3 | 26 | - | 55435 | 24 |
| CF, Central African Republic | 1 | 17 | - | 11137 | 18 |
| CG, Congo - Brazzaville | 1 | 12 | - | 1518 | 20 |
| CH, Switzerland | 1 | 26 | - | 10666 | 143 |
| CI, Côte d’Ivoire | 1 | 14 | - | 12294 | 82 |
| CL, Chile | 2 | 16 | - | 14821 | 138 |
| CM, Cameroon | 1 | 10 | - | 12090 | 27 |
| CN, China | 1 | 34 | - | 437998 | 2652 |
| CO, Colombia | 1 | 33 | - | 14765 | 106 |
| CR, Costa Rica | 1 | 7 | - | 3404 | 108 |
| CU, Cuba | 3 | 16 | - | 6438 | 109 |
| CV, Cape Verde | 2 | 2 | 22 | - | - |
| CY, Cyprus | 2 | 6 | - | 516 | 12 |
| CZ, Czechia | 2 | 14 | 76 | 16121 | 126 |
| DE, Germany | 2 | 16 | - | 84334 | 1318 |
| DJ, Djibouti | 1 | 6 | - | 134 | 6 |
| DK, Denmark | 1 | 5 | - | 8107 | 72 |
| DM, Dominica | 1 | 10 | - | 86 | 1 |
| DO, Dominican Republic | 2 | 10 | 32 | - | - |
| DZ, Algeria | 1 | 48 | - | 12810 | 654 |
| EC, Ecuador | 2 | 24 | - | 16243 | 42 |
| EE, Estonia | 3 | 15 | 79 | 4661 | 15 |
| EG, Egypt | 1 | 27 | - | 1921 | 94 |
| ER, Eritrea | 2 | 6 | - | 482 | 13 |
| ES, Spain | 2 | 19 | 50 | 66551 | 600 |
| ET, Ethiopia | 1 | 12 | - | 8913 | 44 |
| FI, Finland | 2 | 18 | - | 9280 | 94 |
| FJ, Fiji | 1 | 5 | 14 | 677 | 8 |
| FK, Falkland Islands | 1 | - | - | - | - |
| FM, Micronesia | 2 | 4 | - | 58 | - |
| FO, Faroe Islands | 1 | - | - | - | - |
| FR, France | 2 | 18 | 98 | 269354 | 430 |
| GA, Gabon | 1 | 9 | - | 1091 | 7 |
| GB, United Kingdom | 1 | 4 | 216 | 35847 | 530 |
| GD, Grenada | 1 | 7 | - | 138 | - |
| GE, Georgia | 4 | 12 | - | 4355 | 24 |
| GH, Ghana | 2 | 16 | - | 9367 | 45 |
| GI, Gibraltar | 1 | - | - | - | - |
| GL, Greenland | 1 | 5 | - | 153 | 1 |
| GM, Gambia | 1 | 6 | - | 1162 | 7 |
| GN, Guinea | 2 | 8 | 33 | 14133 | 32 |
| GQ, Equatorial Guinea | 2 | 2 | 8 | 1088 | 7 |
| GR, Greece | 2 | 14 | - | 12386 | 79 |
| GT, Guatemala | 1 | 22 | - | 4621 | 61 |
| GW, Guinea-Bissau | 3 | 4 | 8 | 1627 | 3 |
| GY, Guyana | 1 | 10 | - | 909 | 3 |
| HN, Honduras | 1 | 18 | - | 3313 | 39 |
| HR, Croatia | 5 | 21 | - | 19025 | 36 |
| HT, Haiti | 2 | 10 | - | 3953 | 67 |
| HU, Hungary | 1 | 43 | - | 4638 | 140 |
| ID, Indonesia | 1 | 7 | 34 | 94592 | 291 |
| IE, Ireland | 3 | 4 | 26 | 3447 | 77 |
| IL, Israel | 3 | 6 | - | 1222 | 52 |
| IN, India | 1 | 36 | - | 285676 | 1884 |
| IQ, Iraq | 3 | 16 | 3 | 8245 | 67 |
| IR, Iran | 1 | 31 | - | 46520 | 535 |
| IS, Iceland | 3 | 8 | 69 | 119 | 8 |
| IT, Italy | 2 | 20 | 106 | 62995 | 1183 |
| JM, Jamaica | 1 | 14 | - | 1847 | 4 |
| JO, Jordan | 1 | 12 | - | 803 | 16 |
| JP, Japan | 1 | 47 | - | 7552 | 1231 |
| KE, Kenya | 1 | 47 | - | 9288 | 49 |
| KG, Kyrgyzstan | 3 | 9 | - | 1853 | 49 |
| KH, Cambodia | 1 | 25 | - | 1478 | 15 |
| KI, Kiribati | 1 | 3 | - | 133 | 2 |
| KM, Comoros | 1 | 3 | - | 211 | 2 |
| KN, St. Kitts & Nevis | 1 | 2 | 14 | 64 | 1 |
| KP, North Korea | 1 | 12 | - | 5041 | 25 |
| KR, South Korea | 3 | 17 | - | 17063 | 94 |
| KW, Kuwait | 1 | 6 | - | 65 | 32 |
| KZ, Kazakhstan | 1 | 17 | - | - | - |
| LA, Laos | 1 | 18 | - | 7308 | 6 |
| LB, Lebanon | 1 | 8 | - | 1482 | 10 |
| LC, St. Lucia | 1 | 10 | - | 310 | 2 |
| LI, Liechtenstein | 1 | 11 | - | 33 | - |
| LK, Sri Lanka | 1 | 9 | 25 | 6087 | 331 |
| LR, Liberia | 1 | 15 | - | 12894 | 7 |
| LS, Lesotho | 2 | 10 | - | 3982 | 4 |
| LT, Lithuania | 4 | 10 | 60 | 20930 | 33 |
| LU, Luxembourg | 2 | 12 | - | 681 | 5 |
| LV, Latvia | 4 | 43 | - | 5798 | 19 |
| LY, Libya | 1 | 22 | - | 907 | 40 |
| MA, Morocco | 2 | 12 | 75 | 13359 | 168 |
| MC, Monaco | 3 | 17 | - | 1 | 1 |
| MD, Moldova | 2 | 37 | - | 1669 | 42 |
| ME, Montenegro | 3 | 24 | - | 3616 | 12 |
| MG, Madagascar | 2 | 6 | - | 63916 | 77 |
| MH, Marshall Islands | 1 | 2 | 24 | 46 | 2 |
| MK, North Macedonia | 2 | 80 | - | 1733 | 26 |
| ML, Mali | 3 | 11 | - | 26400 | 38 |
| MM, Myanmar (Burma) | 2 | 15 | - | 14215 | 77 |
| MN, Mongolia | 1 | 22 | - | 625 | 24 |
| MR, Mauritania | 3 | 15 | - | 2602 | 19 |
| MT, Malta | 3 | 68 | - | 91 | 17 |
| MU, Mauritius | 1 | 12 | - | 244 | 17 |
| MV, Maldives | 2 | 21 | - | 33 | 3 |
| MW, Malawi | 1 | 3 | 28 | 2279 | 12 |
| MX, Mexico | 2 | 32 | - | 53173 | 837 |
| MY, Malaysia | 1 | 16 | - | 6264 | 130 |
| MZ, Mozambique | 3 | 11 | - | 2343 | 33 |
| NA, Namibia | 2 | 14 | - | 1061 | 17 |
| NE, Niger | 1 | 8 | - | 24554 | 46 |
| NG, Nigeria | 1 | 37 | - | 27868 | 81 |
| NI, Nicaragua | 2 | 17 | - | 6989 | 59 |
| NL, Netherlands | 2 | 15 | - | 6283 | 319 |
| NO, Norway | 2 | 13 | - | 15109 | 37 |
| NP, Nepal | 2 | 12 | 14 | 16902 | 35 |
| NR, Nauru | 1 | 14 | - | 16 | - |
| NZ, New Zealand | 1 | 17 | - | 2034 | 43 |
| OM, Oman | 1 | 11 | - | 2728 | 21 |
| PA, Panama | 2 | 14 | - | 2948 | 22 |
| PE, Peru | 3 | 26 | - | 49879 | 98 |
| PG, Papua New Guinea | 2 | 22 | - | 9552 | 52 |
| PH, Philippines | 1 | 17 | 81 | 40395 | 1754 |
| PK, Pakistan | 2 | 7 | - | 24688 | 332 |
| PL, Poland | 2 | 16 | - | 105293 | 409 |
| PS, Palestinian Territories | 4 | 16 | - | 31 | 11 |
| PT, Portugal | 2 | 20 | - | 18403 | 127 |
| PW, Palau | 1 | 16 | - | 42 | - |
| PY, Paraguay | 1 | 18 | - | 1410 | 68 |
| QA, Qatar | 1 | 8 | - | 45 | 3 |
| RO, Romania | 2 | 42 | - | 13830 | 187 |
| RS, Serbia | 3 | 20 | 12 | 5982 | 75 |
| RU, Russia | 2 | 83 | - | 145065 | 1322 |
| RW, Rwanda | 1 | 5 | - | 2950 | 6 |
| SA, Saudi Arabia | 1 | 13 | - | 6413 | 133 |
| SB, Solomon Islands | 2 | 10 | - | 388 | 1 |
| SC, Seychelles | 1 | 27 | - | 39 | 1 |
| SD, Sudan | 5 | 18 | - | 27198 | 37 |
| SE, Sweden | 1 | 21 | - | 42451 | 136 |
| SG, Singapore | 2 | 5 | - | 6 | 1 |
| SI, Slovenia | 2 | 212 | - | 6634 | 16 |
| SK, Slovakia | 3 | 8 | - | 4552 | 81 |
| SL, Sierra Leone | 3 | 5 | - | 9417 | 9 |
| SM, San Marino | 2 | 9 | - | 273 | 1 |
| SN, Senegal | 1 | 14 | - | 13345 | 38 |
| SO, Somalia | 1 | 18 | - | 16989 | 16 |
| SR, Suriname | 3 | 10 | - | 358 | 3 |
| SS, South Sudan | 2 | 10 | - | 4781 | 14 |
| ST, São Tomé & Príncipe | 2 | 7 | - | 394 | 2 |
| SV, El Salvador | 2 | 14 | - | 1786 | 13 |
| SY, Syria | 1 | 14 | - | 7356 | 117 |
| SZ, Eswatini | 1 | 4 | - | 438 | 4 |
| TD, Chad | 1 | 23 | - | 27443 | 24 |
| TG, Togo | 1 | 5 | - | 2353 | 24 |
| TH, Thailand | 1 | 78 | - | 26761 | 140 |
| TJ, Tajikistan | 3 | 5 | - | 2671 | 46 |
| TL, Timor-Leste | 3 | 13 | - | 2837 | 10 |
| TM, Turkmenistan | 4 | 6 | - | 1246 | 23 |
| TN, Tunisia | 1 | 24 | - | 1383 | 73 |
| TO, Tonga | 1 | 5 | - | 213 | 1 |
| TR, Türkiye | 2 | 81 | - | 46434 | 674 |
| TT, Trinidad & Tobago | 1 | 15 | - | 190 | 6 |
| TV, Tuvalu | 1 | 8 | - | 15 | - |
| TW, Taiwan | 1 | 22 | - | 15750 | 213 |
| TZ, Tanzania | 1 | 31 | - | 12217 | 94 |
| UA, Ukraine | 4 | 27 | - | 29685 | 418 |
| UG, Uganda | 2 | 4 | 135 | 73655 | 37 |
| US, United States | 1 | 51 | - | 138148 | 4007 |
| UY, Uruguay | 2 | 19 | - | 610 | 38 |
| UZ, Uzbekistan | 1 | 14 | - | 7687 | 99 |
| VA, Vatican City | 2 | - | - | - | - |
| VC, St. Vincent & Grenadines | 1 | 6 | - | 70 | 1 |
| VE, Venezuela | 3 | 25 | - | 11495 | 109 |
| VG, British Virgin Islands | 2 | - | - | - | - |
| VN, Vietnam | 2 | 63 | - | 11635 | 97 |
| VU, Vanuatu | 1 | 6 | - | 962 | 2 |
| WS, Samoa | 1 | 11 | - | 164 | 1 |
| XK, Kosovo | 3 | - | - | - | - |
| YE, Yemen | 1 | 22 | - | 69889 | 60 |
| ZA, South Africa | 1 | 9 | - | 2596 | 136 |
| ZM, Zambia | 2 | 10 | - | 1617 | 42 |
| ZW, Zimbabwe | 5 | 10 | - | 637 | 31 |
| Total | 185 | 3543 | 1469 | 3390304 | 33073 |

## Licenses

See https://github.com/django-terran/django-terran-data

## Acknowledgments

See https://github.com/django-terran/django-terran-data