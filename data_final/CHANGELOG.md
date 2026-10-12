# data_final — changelog

Built 2026-10-09T15:44:30+00:00 by `tools/build_final_dataset.py` from the raw harvest. Rules R1-R6 are stated in the script's header and approved by Charbel (9 Oct 2026).

## Raw data untouched

| | files | bytes | sha256 of all raw files |
|---|---|---|---|
| before the build | 6856 | 7960344706 | `ce502631004ac952eab5bc4d066be63090663cd352452b10d6c74d407ffc8aa8` |
| after the build | 6856 | 7960344706 | `ce502631004ac952eab5bc4d066be63090663cd352452b10d6c74d407ffc8aa8` |

Equal: yes

## Counts

| | problems |
|---|---|
| in the raw harvest | 1369 |
| copied unchanged (weights 1) | 1324 |
| weights only (R3) | 20 |
| re-split (R2) | 22 |
| samples removed (R5) | 2 |
| excluded (R1, R2.4, R5) | 1 |
| with flagged samples (R6) | 27 |
| in data_final | 1368 |

## Excluded

| problem | reason |
|---|---|
| sat-generator-2:XOR-3:n=10:count-high | R1: overall class balance 0.19 < 0.2 (the median-tie rule had only checked TRAIN) |

## Re-split (R2): groups of identical inputs had straddled TRAIN and TEST

| problem | straddling groups | TRAIN/TEST before | after | samples changing side | label flips | median cut before → after | distinct TEST inputs | TEST balance | ambiguous samples |
|---|---|---|---|---|---|---|---|---|---|
| TU-molecules:alchemy_full:n=11:property0 | 2 | 210/90 | 211/89 | 131 | 2 | 0.193213 → 0.193504 | 89 | 0.51 | 2 |
| TU-molecules:alchemy_full:n=11:property1 | 2 | 210/90 | 211/89 | 119 | 8 | 6.595e-05 → 6.62e-05 | 89 | 0.52 | 0 |
| TU-molecules:alchemy_full:n=11:property2 | 2 | 210/90 | 210/90 | 134 | 2 | 0.221254 → 0.221932 | 89 | 0.49 | 2 |
| TU-molecules:alchemy_full:n=11:property3 | 2 | 210/90 | 211/89 | 127 | 9 | -501.318 → -501.262 | 89 | 0.48 | 0 |
| TU-molecules:alchemy_full:n=11:property4 | 2 | 210/90 | 210/90 | 124 | 5 | -0.229146 → -0.229971 | 89 | 0.50 | 2 |
| TU-molecules:alchemy_full:n=11:property6 | 2 | 210/90 | 210/90 | 134 | 3 | 102.991 → 102.722 | 90 | 0.50 | 0 |
| TU-molecules:alchemy_full:n=11:property9 | 2 | 210/90 | 210/90 | 132 | 1 | -0.000449179 → -0.00095788 | 89 | 0.49 | 2 |
| TU-molecules:alchemy_full:n=11:property10 | 2 | 210/90 | 211/89 | 121 | 2 | 2.2928 → 2.31113 | 89 | 0.49 | 2 |
| TU-molecules:alchemy_full:n=11:property11 | 2 | 210/90 | 210/90 | 134 | 11 | 1871.55 → 1843.22 | 90 | 0.50 | 2 |
| TS-archive:EigenWorms:n=6:class 1 vs rest | 11 | 181/78 | 183/76 | 104 | 0 | — | 71 | 0.43 | 0 |
| sat-generator-2:2-SAT:n=4:count-low | 39 | 210/90 | 192/108 | 138 | 0 | 9 → 9 | 59 | 0.40 | 0 |
| sat-generator-2:2-SAT:n=4:count-mid | 1 | 210/90 | 210/90 | 126 | 71 | 3 → 4 | 90 | 0.23 | 0 |
| sat-generator-2:2-SAT:n=5:count-low | 2 | 210/90 | 211/89 | 123 | 63 | 14 → 12 | 89 | 0.56 | 0 |
| sat-generator-2:XOR-3:n=4:satisfiable | 38 | 210/90 | 204/96 | 118 | 0 | — | 55 | 0.50 | 0 |
| sat-generator-2:XOR-3:n=4:count-high | 50 | 210/90 | 221/79 | 109 | 0 | 2 → 2 | 31 | 0.33 | 0 |
| sat-generator-2:XOR-3:n=5:count-high | 2 | 210/90 | 211/89 | 127 | 0 | 2 → 2 | 88 | 0.27 | 0 |
| sat-generator-2:1-IN-3:n=4:satisfiable | 2 | 210/90 | 210/90 | 96 | 0 | — | 89 | 0.56 | 0 |
| sat-generator-2:1-IN-3:n=4:count-mid | 22 | 210/90 | 209/91 | 131 | 0 | 2 → 2 | 67 | 0.34 | 0 |
| sat-generator-2:1-IN-3:n=5:count-mid | 7 | 210/90 | 213/87 | 113 | 0 | 4 → 4 | 85 | 0.34 | 0 |
| sat-generator-2:NAE-3:n=4:count-low | 49 | 210/90 | 202/98 | 134 | 0 | 8 → 8 | 36 | 0.46 | 0 |
| sat-generator-2:NAE-3:n=5:count-low | 2 | 210/90 | 211/89 | 137 | 0 | 14 → 14 | 89 | 0.30 | 0 |
| sat-generator-2:NAE-3:n=6:count-low | 2 | 210/90 | 211/89 | 129 | 58 | 26 → 28 | 89 | 0.31 | 0 |

## Weights only (R3): duplicates all on one side, split unchanged

| problem | samples | distinct inputs | ambiguous samples |
|---|---|---|---|
| TU-molecules:alchemy_full:n=9:property0 | 300 | 299 | 2 |
| TU-molecules:alchemy_full:n=9:property1 | 300 | 299 | 2 |
| TU-molecules:alchemy_full:n=9:property2 | 300 | 299 | 0 |
| TU-molecules:alchemy_full:n=9:property3 | 300 | 299 | 2 |
| TU-molecules:alchemy_full:n=9:property4 | 300 | 299 | 2 |
| TU-molecules:alchemy_full:n=9:property6 | 300 | 299 | 2 |
| TU-molecules:alchemy_full:n=9:property9 | 300 | 299 | 0 |
| TU-molecules:alchemy_full:n=9:property10 | 300 | 299 | 2 |
| TU-molecules:alchemy_full:n=9:property11 | 300 | 299 | 0 |
| TU-molecules:alchemy_full:n=10:property0 | 300 | 299 | 0 |
| TU-molecules:alchemy_full:n=10:property1 | 300 | 299 | 0 |
| TU-molecules:alchemy_full:n=10:property2 | 300 | 299 | 2 |
| TU-molecules:alchemy_full:n=10:property3 | 300 | 299 | 0 |
| TU-molecules:alchemy_full:n=10:property4 | 300 | 299 | 0 |
| TU-molecules:alchemy_full:n=10:property6 | 300 | 299 | 0 |
| TU-molecules:alchemy_full:n=10:property9 | 300 | 299 | 0 |
| TU-molecules:alchemy_full:n=10:property10 | 300 | 299 | 0 |
| TU-molecules:alchemy_full:n=10:property11 | 300 | 299 | 0 |
| TU-molecules:ZINC_full:n=12:property0 | 300 | 298 | 0 |
| sat-generator-2:1-IN-3:n=7:count-mid | 300 | 298 | 0 |

## Samples removed (R5): Hartree-Fock not converged

| problem | removed samples | label flips | median cut before → after | outcome |
|---|---|---|---|---|
| chem-generator:H2O:n=12:hf_weight | geometry117, geometry118 | 0 | fixed cut | kept |
| chem-generator:H2O:n=12:correlation | geometry117, geometry118 | 1 | 0.211697 → 0.205715 | kept |

## Flagged (R4): fewer than 50 distinct TEST inputs

| problem | distinct TEST inputs |
|---|---|
| real-networks:celegans_2019/hermaphrodite_gap_junction:n=12:bipartite | 34 |
| real-networks:arxiv_authors/GrQc:n=11:planar | 30 |
| real-networks:arxiv_authors/GrQc:n=12:planar | 30 |
| real-networks:netscience:n=9:diameter>=3 | 34 |
| real-networks:netscience:n=10:4cycle | 30 |
| real-networks:power:n=12:perfect_matching | 32 |
| real-networks:euroroad:n=12:4cycle | 36 |
| real-networks:openflights:n=10:perfect_matching | 32 |
| real-networks:us_air_traffic:n=8:diameter>=3 | 32 |
| MOABB:BNCI2014_001:n=4:subject 1 session 0train | 44 |
| MOABB:BNCI2014_001:n=4:subject 1 session 1test | 44 |
| MOABB:BNCI2014_001:n=4:subject 2 session 0train | 44 |
| MOABB:BNCI2014_001:n=4:subject 2 session 1test | 44 |
| MOABB:BNCI2014_001:n=4:subject 3 session 0train | 44 |
| MOABB:BNCI2014_001:n=4:subject 3 session 1test | 44 |
| MOABB:BNCI2014_001:n=4:subject 4 session 0train | 44 |
| MOABB:BNCI2014_001:n=4:subject 4 session 1test | 44 |
| MOABB:BNCI2014_001:n=4:subject 5 session 0train | 44 |
| MOABB:BNCI2014_001:n=4:subject 5 session 1test | 44 |
| MOABB:BNCI2014_001:n=4:subject 6 session 0train | 44 |
| MOABB:BNCI2014_001:n=4:subject 6 session 1test | 44 |
| MOABB:BNCI2014_001:n=4:subject 7 session 0train | 44 |
| MOABB:BNCI2014_001:n=4:subject 7 session 1test | 44 |
| MOABB:BNCI2014_001:n=4:subject 8 session 0train | 44 |
| MOABB:BNCI2014_001:n=4:subject 8 session 1test | 44 |
| MOABB:BNCI2014_001:n=4:subject 9 session 0train | 44 |
| MOABB:BNCI2014_001:n=4:subject 9 session 1test | 44 |
| MOABB:BNCI2014_001:n=6:subject 1 session 0train | 44 |
| MOABB:BNCI2014_001:n=6:subject 1 session 1test | 44 |
| MOABB:BNCI2014_001:n=6:subject 2 session 0train | 44 |
| MOABB:BNCI2014_001:n=6:subject 2 session 1test | 44 |
| MOABB:BNCI2014_001:n=6:subject 3 session 0train | 44 |
| MOABB:BNCI2014_001:n=6:subject 3 session 1test | 44 |
| MOABB:BNCI2014_001:n=6:subject 4 session 0train | 44 |
| MOABB:BNCI2014_001:n=6:subject 4 session 1test | 44 |
| MOABB:BNCI2014_001:n=6:subject 5 session 0train | 44 |
| MOABB:BNCI2014_001:n=6:subject 5 session 1test | 44 |
| MOABB:BNCI2014_001:n=6:subject 6 session 0train | 44 |
| MOABB:BNCI2014_001:n=6:subject 6 session 1test | 44 |
| MOABB:BNCI2014_001:n=6:subject 7 session 0train | 44 |
| MOABB:BNCI2014_001:n=6:subject 7 session 1test | 44 |
| MOABB:BNCI2014_001:n=6:subject 8 session 0train | 44 |
| MOABB:BNCI2014_001:n=6:subject 8 session 1test | 44 |
| MOABB:BNCI2014_001:n=6:subject 9 session 0train | 44 |
| MOABB:BNCI2014_001:n=6:subject 9 session 1test | 44 |
| MOABB:BNCI2014_001:n=8:subject 1 session 0train | 44 |
| MOABB:BNCI2014_001:n=8:subject 1 session 1test | 44 |
| MOABB:BNCI2014_001:n=8:subject 2 session 0train | 44 |
| MOABB:BNCI2014_001:n=8:subject 2 session 1test | 44 |
| MOABB:BNCI2014_001:n=8:subject 3 session 0train | 44 |
| MOABB:BNCI2014_001:n=8:subject 3 session 1test | 44 |
| MOABB:BNCI2014_001:n=8:subject 4 session 0train | 44 |
| MOABB:BNCI2014_001:n=8:subject 4 session 1test | 44 |
| MOABB:BNCI2014_001:n=8:subject 5 session 0train | 44 |
| MOABB:BNCI2014_001:n=8:subject 5 session 1test | 44 |
| MOABB:BNCI2014_001:n=8:subject 6 session 0train | 44 |
| MOABB:BNCI2014_001:n=8:subject 6 session 1test | 44 |
| MOABB:BNCI2014_001:n=8:subject 7 session 0train | 44 |
| MOABB:BNCI2014_001:n=8:subject 7 session 1test | 44 |
| MOABB:BNCI2014_001:n=8:subject 8 session 0train | 44 |
| MOABB:BNCI2014_001:n=8:subject 8 session 1test | 44 |
| MOABB:BNCI2014_001:n=8:subject 9 session 0train | 44 |
| MOABB:BNCI2014_001:n=8:subject 9 session 1test | 44 |
| MOABB:BNCI2014_001:n=10:subject 1 session 0train | 44 |
| MOABB:BNCI2014_001:n=10:subject 1 session 1test | 44 |
| MOABB:BNCI2014_001:n=10:subject 2 session 0train | 44 |
| MOABB:BNCI2014_001:n=10:subject 2 session 1test | 44 |
| MOABB:BNCI2014_001:n=10:subject 3 session 0train | 44 |
| MOABB:BNCI2014_001:n=10:subject 3 session 1test | 44 |
| MOABB:BNCI2014_001:n=10:subject 4 session 0train | 44 |
| MOABB:BNCI2014_001:n=10:subject 4 session 1test | 44 |
| MOABB:BNCI2014_001:n=10:subject 5 session 0train | 44 |
| MOABB:BNCI2014_001:n=10:subject 5 session 1test | 44 |
| MOABB:BNCI2014_001:n=10:subject 6 session 0train | 44 |
| MOABB:BNCI2014_001:n=10:subject 6 session 1test | 44 |
| MOABB:BNCI2014_001:n=10:subject 7 session 0train | 44 |
| MOABB:BNCI2014_001:n=10:subject 7 session 1test | 44 |
| MOABB:BNCI2014_001:n=10:subject 8 session 0train | 44 |
| MOABB:BNCI2014_001:n=10:subject 8 session 1test | 44 |
| MOABB:BNCI2014_001:n=10:subject 9 session 0train | 44 |
| MOABB:BNCI2014_001:n=10:subject 9 session 1test | 44 |
| MOABB:BNCI2014_001:n=12:subject 1 session 0train | 44 |
| MOABB:BNCI2014_001:n=12:subject 1 session 1test | 44 |
| MOABB:BNCI2014_001:n=12:subject 2 session 0train | 44 |
| MOABB:BNCI2014_001:n=12:subject 2 session 1test | 44 |
| MOABB:BNCI2014_001:n=12:subject 3 session 0train | 44 |
| MOABB:BNCI2014_001:n=12:subject 3 session 1test | 44 |
| MOABB:BNCI2014_001:n=12:subject 4 session 0train | 44 |
| MOABB:BNCI2014_001:n=12:subject 4 session 1test | 44 |
| MOABB:BNCI2014_001:n=12:subject 5 session 0train | 44 |
| MOABB:BNCI2014_001:n=12:subject 5 session 1test | 44 |
| MOABB:BNCI2014_001:n=12:subject 6 session 0train | 44 |
| MOABB:BNCI2014_001:n=12:subject 6 session 1test | 44 |
| MOABB:BNCI2014_001:n=12:subject 7 session 0train | 44 |
| MOABB:BNCI2014_001:n=12:subject 7 session 1test | 44 |
| MOABB:BNCI2014_001:n=12:subject 8 session 0train | 44 |
| MOABB:BNCI2014_001:n=12:subject 8 session 1test | 44 |
| MOABB:BNCI2014_001:n=12:subject 9 session 0train | 44 |
| MOABB:BNCI2014_001:n=12:subject 9 session 1test | 44 |
| TS-archive:ERing:n=4:class 1 vs rest | 30 |
| TS-archive:ERing:n=4:class 2 vs rest | 30 |
| TS-archive:ERing:n=4:class 3 vs rest | 30 |
| TS-archive:ERing:n=4:class 4 vs rest | 30 |
| TS-archive:ERing:n=4:class 5 vs rest | 30 |
| TS-archive:ERing:n=4:class 6 vs rest | 30 |
| TS-archive:JapaneseVowels:n=12:class 1 vs rest | 36 |
| TS-archive:JapaneseVowels:n=12:class 2 vs rest | 40 |
| TS-archive:JapaneseVowels:n=12:class 4 vs rest | 44 |
| TS-archive:JapaneseVowels:n=12:class 5 vs rest | 36 |
| TS-archive:JapaneseVowels:n=12:class 6 vs rest | 32 |
| TS-archive:JapaneseVowels:n=12:class 7 vs rest | 42 |
| TS-archive:JapaneseVowels:n=12:class 8 vs rest | 48 |
| TS-archive:JapaneseVowels:n=12:class 9 vs rest | 36 |
| sat-generator-2:XOR-3:n=4:count-high | 31 |
| sat-generator-2:NAE-3:n=4:count-low | 36 |
| spin-generator-2:TFIM-open:n=4:h:far | 48 |
| spin-generator-2:TFIM-open:n=5:h:far | 48 |
| spin-generator-2:TFIM-open:n=6:h:far | 48 |
| spin-generator-2:TFIM-open:n=7:h:far | 48 |
| spin-generator-2:TFIM-open:n=8:h:far | 48 |
| spin-generator-2:TFIM-open:n=9:h:far | 48 |
| spin-generator-2:TFIM-open:n=10:h:far | 48 |
| spin-generator-2:TFIM-open:n=11:h:far | 48 |
| spin-generator-2:TFIM-open:n=12:h:far | 48 |
| spin-generator-2:TFIM-open:n=4:h:near | 48 |
| spin-generator-2:TFIM-open:n=5:h:near | 48 |
| spin-generator-2:TFIM-open:n=6:h:near | 48 |
| spin-generator-2:TFIM-open:n=7:h:near | 48 |
| spin-generator-2:TFIM-open:n=8:h:near | 48 |
| spin-generator-2:TFIM-open:n=9:h:near | 48 |
| spin-generator-2:TFIM-open:n=10:h:near | 48 |
| spin-generator-2:TFIM-open:n=11:h:near | 48 |
| spin-generator-2:TFIM-open:n=12:h:near | 48 |
| spin-generator-2:TFIM-periodic:n=4:h:far | 48 |
| spin-generator-2:TFIM-periodic:n=6:h:far | 48 |
| spin-generator-2:TFIM-periodic:n=8:h:far | 48 |
| spin-generator-2:TFIM-periodic:n=10:h:far | 48 |
| spin-generator-2:TFIM-periodic:n=12:h:far | 48 |
| spin-generator-2:TFIM-periodic:n=4:h:near | 48 |
| spin-generator-2:TFIM-periodic:n=6:h:near | 48 |
| spin-generator-2:TFIM-periodic:n=8:h:near | 48 |
| spin-generator-2:TFIM-periodic:n=10:h:near | 48 |
| spin-generator-2:TFIM-periodic:n=12:h:near | 48 |
| spin-generator-2:XXZ-open:n=4:neel:far | 48 |
| spin-generator-2:XXZ-open:n=5:neel:far | 48 |
| spin-generator-2:XXZ-open:n=6:neel:far | 48 |
| spin-generator-2:XXZ-open:n=7:neel:far | 48 |
| spin-generator-2:XXZ-open:n=8:neel:far | 48 |
| spin-generator-2:XXZ-open:n=9:neel:far | 48 |
| spin-generator-2:XXZ-open:n=10:neel:far | 48 |
| spin-generator-2:XXZ-open:n=11:neel:far | 48 |
| spin-generator-2:XXZ-open:n=12:neel:far | 48 |
| spin-generator-2:XXZ-open:n=4:neel:near | 48 |
| spin-generator-2:XXZ-open:n=5:neel:near | 48 |
| spin-generator-2:XXZ-open:n=6:neel:near | 48 |
| spin-generator-2:XXZ-open:n=7:neel:near | 48 |
| spin-generator-2:XXZ-open:n=8:neel:near | 48 |
| spin-generator-2:XXZ-open:n=9:neel:near | 48 |
| spin-generator-2:XXZ-open:n=10:neel:near | 48 |
| spin-generator-2:XXZ-open:n=11:neel:near | 48 |
| spin-generator-2:XXZ-open:n=12:neel:near | 48 |
| spin-generator-2:XXZ-open:n=4:ferro:far | 48 |
| spin-generator-2:XXZ-open:n=5:ferro:far | 48 |
| spin-generator-2:XXZ-open:n=6:ferro:far | 48 |
| spin-generator-2:XXZ-open:n=7:ferro:far | 48 |
| spin-generator-2:XXZ-open:n=8:ferro:far | 48 |
| spin-generator-2:XXZ-open:n=9:ferro:far | 48 |
| spin-generator-2:XXZ-open:n=10:ferro:far | 48 |
| spin-generator-2:XXZ-open:n=11:ferro:far | 48 |
| spin-generator-2:XXZ-open:n=12:ferro:far | 48 |
| spin-generator-2:XXZ-open:n=4:ferro:near | 48 |
| spin-generator-2:XXZ-open:n=5:ferro:near | 48 |
| spin-generator-2:XXZ-open:n=6:ferro:near | 48 |
| spin-generator-2:XXZ-open:n=7:ferro:near | 48 |
| spin-generator-2:XXZ-open:n=8:ferro:near | 48 |
| spin-generator-2:XXZ-open:n=9:ferro:near | 48 |
| spin-generator-2:XXZ-open:n=10:ferro:near | 48 |
| spin-generator-2:XXZ-open:n=11:ferro:near | 48 |
| spin-generator-2:XXZ-open:n=12:ferro:near | 48 |
| spin-generator-2:XXZ-periodic:n=4:neel:far | 48 |
| spin-generator-2:XXZ-periodic:n=6:neel:far | 48 |
| spin-generator-2:XXZ-periodic:n=8:neel:far | 48 |
| spin-generator-2:XXZ-periodic:n=10:neel:far | 48 |
| spin-generator-2:XXZ-periodic:n=12:neel:far | 48 |
| spin-generator-2:XXZ-periodic:n=4:neel:near | 48 |
| spin-generator-2:XXZ-periodic:n=6:neel:near | 48 |
| spin-generator-2:XXZ-periodic:n=8:neel:near | 48 |
| spin-generator-2:XXZ-periodic:n=10:neel:near | 48 |
| spin-generator-2:XXZ-periodic:n=12:neel:near | 48 |
| spin-generator-2:XXZ-periodic:n=4:ferro:far | 48 |
| spin-generator-2:XXZ-periodic:n=6:ferro:far | 48 |
| spin-generator-2:XXZ-periodic:n=8:ferro:far | 48 |
| spin-generator-2:XXZ-periodic:n=10:ferro:far | 48 |
| spin-generator-2:XXZ-periodic:n=12:ferro:far | 48 |
| spin-generator-2:XXZ-periodic:n=4:ferro:near | 48 |
| spin-generator-2:XXZ-periodic:n=6:ferro:near | 48 |
| spin-generator-2:XXZ-periodic:n=8:ferro:near | 48 |
| spin-generator-2:XXZ-periodic:n=10:ferro:near | 48 |
| spin-generator-2:XXZ-periodic:n=12:ferro:near | 48 |
| spin-generator-2:BOND_ALT-open:n=4:dimer:far | 48 |
| spin-generator-2:BOND_ALT-open:n=6:dimer:far | 48 |
| spin-generator-2:BOND_ALT-open:n=8:dimer:far | 48 |
| spin-generator-2:BOND_ALT-open:n=10:dimer:far | 48 |
| spin-generator-2:BOND_ALT-open:n=12:dimer:far | 48 |
| spin-generator-2:BOND_ALT-open:n=4:dimer:near | 48 |
| spin-generator-2:BOND_ALT-open:n=6:dimer:near | 48 |
| spin-generator-2:BOND_ALT-open:n=8:dimer:near | 48 |
| spin-generator-2:BOND_ALT-open:n=10:dimer:near | 48 |
| spin-generator-2:BOND_ALT-open:n=12:dimer:near | 48 |
| spin-generator-2:J1J2-open:n=4:dimerisation:far | 48 |
| spin-generator-2:J1J2-open:n=5:dimerisation:far | 48 |
| spin-generator-2:J1J2-open:n=6:dimerisation:far | 48 |
| spin-generator-2:J1J2-open:n=7:dimerisation:far | 48 |
| spin-generator-2:J1J2-open:n=8:dimerisation:far | 48 |
| spin-generator-2:J1J2-open:n=9:dimerisation:far | 48 |
| spin-generator-2:J1J2-open:n=10:dimerisation:far | 48 |
| spin-generator-2:J1J2-open:n=11:dimerisation:far | 48 |
| spin-generator-2:J1J2-open:n=12:dimerisation:far | 48 |
| spin-generator-2:J1J2-open:n=4:dimerisation:near | 48 |
| spin-generator-2:J1J2-open:n=5:dimerisation:near | 48 |
| spin-generator-2:J1J2-open:n=6:dimerisation:near | 48 |
| spin-generator-2:J1J2-open:n=7:dimerisation:near | 48 |
| spin-generator-2:J1J2-open:n=8:dimerisation:near | 48 |
| spin-generator-2:J1J2-open:n=9:dimerisation:near | 48 |
| spin-generator-2:J1J2-open:n=10:dimerisation:near | 48 |
| spin-generator-2:J1J2-open:n=11:dimerisation:near | 48 |
| spin-generator-2:J1J2-open:n=12:dimerisation:near | 48 |
| spin-generator-2:J1J2-periodic:n=4:dimerisation:far | 48 |
| spin-generator-2:J1J2-periodic:n=6:dimerisation:far | 48 |
| spin-generator-2:J1J2-periodic:n=8:dimerisation:far | 48 |
| spin-generator-2:J1J2-periodic:n=10:dimerisation:far | 48 |
| spin-generator-2:J1J2-periodic:n=12:dimerisation:far | 48 |
| spin-generator-2:J1J2-periodic:n=4:dimerisation:near | 48 |
| spin-generator-2:J1J2-periodic:n=6:dimerisation:near | 48 |
| spin-generator-2:J1J2-periodic:n=8:dimerisation:near | 48 |
| spin-generator-2:J1J2-periodic:n=10:dimerisation:near | 48 |
| spin-generator-2:J1J2-periodic:n=12:dimerisation:near | 48 |
| spin-generator-2:ANNNI-open:n=4:kappa:far | 48 |
| spin-generator-2:ANNNI-open:n=5:kappa:far | 48 |
| spin-generator-2:ANNNI-open:n=6:kappa:far | 48 |
| spin-generator-2:ANNNI-open:n=7:kappa:far | 48 |
| spin-generator-2:ANNNI-open:n=8:kappa:far | 48 |
| spin-generator-2:ANNNI-open:n=9:kappa:far | 48 |
| spin-generator-2:ANNNI-open:n=10:kappa:far | 48 |
| spin-generator-2:ANNNI-open:n=11:kappa:far | 48 |
| spin-generator-2:ANNNI-open:n=12:kappa:far | 48 |
| spin-generator-2:ANNNI-open:n=4:kappa:near | 48 |
| spin-generator-2:ANNNI-open:n=5:kappa:near | 48 |
| spin-generator-2:ANNNI-open:n=6:kappa:near | 48 |
| spin-generator-2:ANNNI-open:n=7:kappa:near | 48 |
| spin-generator-2:ANNNI-open:n=8:kappa:near | 48 |
| spin-generator-2:ANNNI-open:n=9:kappa:near | 48 |
| spin-generator-2:ANNNI-open:n=10:kappa:near | 48 |
| spin-generator-2:ANNNI-open:n=11:kappa:near | 48 |
| spin-generator-2:ANNNI-open:n=12:kappa:near | 48 |
| spin-generator-2:ANNNI-open:n=4:field:far | 48 |
| spin-generator-2:ANNNI-open:n=5:field:far | 48 |
| spin-generator-2:ANNNI-open:n=6:field:far | 48 |
| spin-generator-2:ANNNI-open:n=7:field:far | 48 |
| spin-generator-2:ANNNI-open:n=8:field:far | 48 |
| spin-generator-2:ANNNI-open:n=9:field:far | 48 |
| spin-generator-2:ANNNI-open:n=10:field:far | 48 |
| spin-generator-2:ANNNI-open:n=11:field:far | 48 |
| spin-generator-2:ANNNI-open:n=12:field:far | 48 |
| spin-generator-2:ANNNI-open:n=4:field:near | 48 |
| spin-generator-2:ANNNI-open:n=5:field:near | 48 |
| spin-generator-2:ANNNI-open:n=6:field:near | 48 |
| spin-generator-2:ANNNI-open:n=7:field:near | 48 |
| spin-generator-2:ANNNI-open:n=8:field:near | 48 |
| spin-generator-2:ANNNI-open:n=9:field:near | 48 |
| spin-generator-2:ANNNI-open:n=10:field:near | 48 |
| spin-generator-2:ANNNI-open:n=11:field:near | 48 |
| spin-generator-2:ANNNI-open:n=12:field:near | 48 |
| spin-generator-2:ANNNI-periodic:n=4:kappa:far | 48 |
| spin-generator-2:ANNNI-periodic:n=6:kappa:far | 48 |
| spin-generator-2:ANNNI-periodic:n=8:kappa:far | 48 |
| spin-generator-2:ANNNI-periodic:n=10:kappa:far | 48 |
| spin-generator-2:ANNNI-periodic:n=12:kappa:far | 48 |
| spin-generator-2:ANNNI-periodic:n=4:kappa:near | 48 |
| spin-generator-2:ANNNI-periodic:n=6:kappa:near | 48 |
| spin-generator-2:ANNNI-periodic:n=8:kappa:near | 48 |
| spin-generator-2:ANNNI-periodic:n=10:kappa:near | 48 |
| spin-generator-2:ANNNI-periodic:n=12:kappa:near | 48 |
| spin-generator-2:ANNNI-periodic:n=4:field:far | 48 |
| spin-generator-2:ANNNI-periodic:n=6:field:far | 48 |
| spin-generator-2:ANNNI-periodic:n=8:field:far | 48 |
| spin-generator-2:ANNNI-periodic:n=10:field:far | 48 |
| spin-generator-2:ANNNI-periodic:n=12:field:far | 48 |
| spin-generator-2:ANNNI-periodic:n=4:field:near | 48 |
| spin-generator-2:ANNNI-periodic:n=6:field:near | 48 |
| spin-generator-2:ANNNI-periodic:n=8:field:near | 48 |
| spin-generator-2:ANNNI-periodic:n=10:field:near | 48 |
| spin-generator-2:ANNNI-periodic:n=12:field:near | 48 |
| spin-generator-2:DISORDERED-open:n=4:H:far | 48 |
| spin-generator-2:DISORDERED-open:n=5:H:far | 48 |
| spin-generator-2:DISORDERED-open:n=6:H:far | 48 |
| spin-generator-2:DISORDERED-open:n=7:H:far | 48 |
| spin-generator-2:DISORDERED-open:n=8:H:far | 48 |
| spin-generator-2:DISORDERED-open:n=9:H:far | 48 |
| spin-generator-2:DISORDERED-open:n=10:H:far | 48 |
| spin-generator-2:DISORDERED-open:n=11:H:far | 48 |
| spin-generator-2:DISORDERED-open:n=12:H:far | 48 |
| spin-generator-2:DISORDERED-open:n=4:H:near | 48 |
| spin-generator-2:DISORDERED-open:n=5:H:near | 48 |
| spin-generator-2:DISORDERED-open:n=6:H:near | 48 |
| spin-generator-2:DISORDERED-open:n=7:H:near | 48 |
| spin-generator-2:DISORDERED-open:n=8:H:near | 48 |
| spin-generator-2:DISORDERED-open:n=9:H:near | 48 |
| spin-generator-2:DISORDERED-open:n=10:H:near | 48 |
| spin-generator-2:DISORDERED-open:n=11:H:near | 48 |
| spin-generator-2:DISORDERED-open:n=12:H:near | 48 |
| spin-generator-2:DISORDERED-periodic:n=4:H:far | 48 |
| spin-generator-2:DISORDERED-periodic:n=6:H:far | 48 |
| spin-generator-2:DISORDERED-periodic:n=8:H:far | 48 |
| spin-generator-2:DISORDERED-periodic:n=10:H:far | 48 |
| spin-generator-2:DISORDERED-periodic:n=12:H:far | 48 |
| spin-generator-2:DISORDERED-periodic:n=4:H:near | 48 |
| spin-generator-2:DISORDERED-periodic:n=6:H:near | 48 |
| spin-generator-2:DISORDERED-periodic:n=8:H:near | 48 |
| spin-generator-2:DISORDERED-periodic:n=10:H:near | 48 |
| spin-generator-2:DISORDERED-periodic:n=12:H:near | 48 |
| spin-generator-2:CLUSTER-open:n=4:lambda:far | 48 |
| spin-generator-2:CLUSTER-open:n=5:lambda:far | 48 |
| spin-generator-2:CLUSTER-open:n=6:lambda:far | 48 |
| spin-generator-2:CLUSTER-open:n=7:lambda:far | 48 |
| spin-generator-2:CLUSTER-open:n=8:lambda:far | 48 |
| spin-generator-2:CLUSTER-open:n=9:lambda:far | 48 |
| spin-generator-2:CLUSTER-open:n=10:lambda:far | 48 |
| spin-generator-2:CLUSTER-open:n=11:lambda:far | 48 |
| spin-generator-2:CLUSTER-open:n=12:lambda:far | 48 |
| spin-generator-2:CLUSTER-open:n=4:lambda:near | 48 |
| spin-generator-2:CLUSTER-open:n=5:lambda:near | 48 |
| spin-generator-2:CLUSTER-open:n=6:lambda:near | 48 |
| spin-generator-2:CLUSTER-open:n=7:lambda:near | 48 |
| spin-generator-2:CLUSTER-open:n=8:lambda:near | 48 |
| spin-generator-2:CLUSTER-open:n=9:lambda:near | 48 |
| spin-generator-2:CLUSTER-open:n=10:lambda:near | 48 |
| spin-generator-2:CLUSTER-open:n=11:lambda:near | 48 |
| spin-generator-2:CLUSTER-open:n=12:lambda:near | 48 |
| spin-generator-2:CLUSTER-periodic:n=4:lambda:far | 48 |
| spin-generator-2:CLUSTER-periodic:n=6:lambda:far | 48 |
| spin-generator-2:CLUSTER-periodic:n=8:lambda:far | 48 |
| spin-generator-2:CLUSTER-periodic:n=10:lambda:far | 48 |
| spin-generator-2:CLUSTER-periodic:n=12:lambda:far | 48 |
| spin-generator-2:CLUSTER-periodic:n=4:lambda:near | 48 |
| spin-generator-2:CLUSTER-periodic:n=6:lambda:near | 48 |
| spin-generator-2:CLUSTER-periodic:n=8:lambda:near | 48 |
| spin-generator-2:CLUSTER-periodic:n=10:lambda:near | 48 |
| spin-generator-2:CLUSTER-periodic:n=12:lambda:near | 48 |
| spin-generator-2:XY-open:n=4:h:far | 48 |
| spin-generator-2:XY-open:n=5:h:far | 48 |
| spin-generator-2:XY-open:n=6:h:far | 48 |
| spin-generator-2:XY-open:n=7:h:far | 48 |
| spin-generator-2:XY-open:n=8:h:far | 48 |
| spin-generator-2:XY-open:n=9:h:far | 48 |
| spin-generator-2:XY-open:n=10:h:far | 48 |
| spin-generator-2:XY-open:n=11:h:far | 48 |
| spin-generator-2:XY-open:n=12:h:far | 48 |
| spin-generator-2:XY-open:n=4:h:near | 48 |
| spin-generator-2:XY-open:n=5:h:near | 48 |
| spin-generator-2:XY-open:n=6:h:near | 48 |
| spin-generator-2:XY-open:n=7:h:near | 48 |
| spin-generator-2:XY-open:n=8:h:near | 48 |
| spin-generator-2:XY-open:n=9:h:near | 48 |
| spin-generator-2:XY-open:n=10:h:near | 48 |
| spin-generator-2:XY-open:n=11:h:near | 48 |
| spin-generator-2:XY-open:n=12:h:near | 48 |
| chem-generator:H4-chain:n=8:hf_weight | 48 |
| chem-generator:H6-chain:n=12:hf_weight | 48 |
| chem-generator:H4-rectangle:n=8:hf_weight | 48 |
| chem-generator:LiH:n=12:hf_weight | 48 |
| chem-generator:LiH:n=12:correlation | 48 |
| chem-generator:BeH2:n=12:hf_weight | 48 |
| chem-generator:BeH2:n=12:correlation | 48 |
| chem-generator:H2O:n=12:hf_weight | 47 |
| chem-generator:H2O:n=12:correlation | 48 |

## Flagged samples (R6): kept, listed in each problem's flags.json for a sensitivity check

| problem | samples | uninformative operator | degenerate ground state |
|---|---|---|---|
| TS-archive:LSST:n=6:class 15 vs rest | 494 | 3 | 0 |
| TS-archive:LSST:n=6:class 16 vs rest | 1080 | 11 | 0 |
| TS-archive:LSST:n=6:class 42 vs rest | 1526 | 16 | 0 |
| TS-archive:LSST:n=6:class 52 vs rest | 250 | 4 | 0 |
| TS-archive:LSST:n=6:class 62 vs rest | 612 | 8 | 0 |
| TS-archive:LSST:n=6:class 65 vs rest | 1250 | 53 | 0 |
| TS-archive:LSST:n=6:class 67 vs rest | 272 | 1 | 0 |
| TS-archive:LSST:n=6:class 88 vs rest | 482 | 2 | 0 |
| TS-archive:LSST:n=6:class 90 vs rest | 4924 | 77 | 0 |
| TS-archive:LSST:n=6:class 92 vs rest | 308 | 4 | 0 |
| TS-archive:LSST:n=6:class 95 vs rest | 206 | 4 | 0 |
| TS-archive:RacketSports:n=6:class badminton_clear vs rest | 303 | 73 | 0 |
| TS-archive:RacketSports:n=6:class badminton_smash vs rest | 303 | 73 | 0 |
| TS-archive:RacketSports:n=6:class squash_backhandboast vs rest | 303 | 73 | 0 |
| TS-archive:RacketSports:n=6:class squash_forehandboast vs rest | 303 | 73 | 0 |
| spin-generator-2:BOND_ALT-open:n=12:dimer:far | 160 | 0 | 4 |
| spin-generator-2:ANNNI-periodic:n=12:kappa:far | 160 | 0 | 3 |
| spin-generator-2:CLUSTER-open:n=4:lambda:far | 160 | 0 | 1 |
| spin-generator-2:CLUSTER-open:n=5:lambda:far | 160 | 0 | 1 |
| spin-generator-2:CLUSTER-open:n=6:lambda:far | 160 | 0 | 1 |
| spin-generator-2:CLUSTER-open:n=7:lambda:far | 160 | 0 | 1 |
| spin-generator-2:CLUSTER-open:n=8:lambda:far | 160 | 0 | 2 |
| spin-generator-2:CLUSTER-open:n=9:lambda:far | 160 | 0 | 1 |
| spin-generator-2:CLUSTER-open:n=10:lambda:far | 160 | 0 | 2 |
| spin-generator-2:CLUSTER-open:n=11:lambda:far | 160 | 0 | 4 |
| spin-generator-2:CLUSTER-open:n=12:lambda:far | 160 | 0 | 3 |
| chem-generator:H4-rectangle:n=8:hf_weight | 160 | 0 | 3 |
| **total** | 337930 | 475 | 26 |

All other problems are copied byte for byte from the raw harvest, with a duplicates.json holding weights 1 and a flags.json with empty lists.
