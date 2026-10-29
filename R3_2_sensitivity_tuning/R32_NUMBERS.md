# R3.2 numbers for the manuscript and the response letter
_Mode 4; results root: /content/drive/MyDrive/Software_Defects_Revised/R3_2_sensitivity_tuning_

- Test 0, Mode 1: TabNet received no gradient update in some folds of 5 datasets; TabNet mean ROC-AUC 63.48 -> 68.66; deep-tabular gap 7.06 -> 5.33 pp (change -1.73, 95% CI [-2.95, -0.62], Holm p=0.027).
- Test 0, Mode 2: TabNet received no gradient update in some folds of 3 datasets; TabNet mean ROC-AUC 64.63 -> 65.11; deep-tabular gap 6.41 -> 6.25 pp (change -0.16, 95% CI [-1.01, +0.54], Holm p=1.000).
- Test 0, Mode 3: TabNet received no gradient update in some folds of 5 datasets; TabNet mean ROC-AUC 62.81 -> 65.34; deep-tabular gap 7.75 -> 6.91 pp (change -0.84, 95% CI [-1.89, +0.03], Holm p=0.436).
- Test 0, Mode 4: TabNet received no gradient update in some folds of 3 datasets; TabNet mean ROC-AUC 65.44 -> 67.22; deep-tabular gap 5.75 -> 5.15 pp (change -0.59, 95% CI [-1.98, +0.62], Holm p=1.000).
- Test 0, untrained TabNet (mode: datasets): M1: CM1, EQ, KC3, MC2, MW1; M2: EQ, KC3, MC2; M3: CM1, EQ, KC3, MC2, MW1; M4: EQ, KC3, MC2
- Test A, DeepTabular: published Mode-4 gap 5.75 pp; re-run default gap 4.85 pp (TabNet with drop_last=False).
- Test A, Transformer: published Mode-4 gap 2.82 pp; re-run default gap 2.92 pp (TabNet with drop_last=False).
- Test A, DeepTabular, arm default: gap +4.85 pp [+3.23, +6.72], classical better on 16/17, Holm p=<0.001; shift vs default +0.00 pp [+nan, +nan], Holm p=n/a; small datasets +6.40, others +4.21.
- Test A, DeepTabular, arm lr_plateau: gap +2.73 pp [+1.50, +4.28], classical better on 15/17, Holm p=0.002; shift vs default -2.12 pp [-3.33, -1.08], Holm p=0.010; small datasets +2.41, others +2.86.
- Test A, DeepTabular, arm wd_1e-4: gap +4.27 pp [+2.79, +5.84], classical better on 16/17, Holm p=0.001; shift vs default -0.58 pp [-1.18, -0.09], Holm p=1.000; small datasets +4.97, others +3.98.
- Test A, DeepTabular, arm wd_1e-3: gap +4.47 pp [+2.73, +6.56], classical better on 15/17, Holm p=0.001; shift vs default -0.38 pp [-1.01, +0.30], Holm p=1.000; small datasets +6.55, others +3.61.
- Test A, DeepTabular, arm dropout_0.2: gap +4.45 pp [+2.97, +6.12], classical better on 16/17, Holm p=<0.001; shift vs default -0.40 pp [-1.06, +0.24], Holm p=1.000; small datasets +5.67, others +3.94.
- Test A, DeepTabular, arm dropout_0.4: gap +4.31 pp [+2.92, +5.89], classical better on 16/17, Holm p=<0.001; shift vs default -0.54 pp [-1.59, +0.47], Holm p=1.000; small datasets +5.08, others +3.99.
- Test A, DeepTabular, arm patience_15: gap +4.84 pp [+3.30, +6.52], classical better on 16/17, Holm p=<0.001; shift vs default -0.01 pp [-0.60, +0.58], Holm p=1.000; small datasets +6.26, others +4.25.
- Test A, DeepTabular, arm batch_64: gap +4.00 pp [+2.48, +5.86], classical better on 15/17, Holm p=0.001; shift vs default -0.85 pp [-1.74, -0.05], Holm p=1.000; small datasets +6.71, others +2.88.
- Test A, DeepTabular, arm small_data: gap +3.36 pp [+2.05, +4.65], classical better on 14/17, Holm p=0.003; shift vs default -1.49 pp [-3.12, -0.17], Holm p=1.000; small datasets +4.07, others +3.06.
- Test A, DeepTabular, arm best_arm_per_dataset (oracle): gap +1.88 pp [+0.90, +3.04], classical better on 13/17, Holm p=0.013; shift vs default -2.96 pp [-3.93, -2.05], Holm p=<0.001; small datasets +2.74, others +1.53.
- Test A, Transformer, arm default: gap +2.92 pp [+1.43, +4.54], classical better on 15/17, Holm p=0.011; shift vs default +0.00 pp [+nan, +nan], Holm p=n/a; small datasets +4.38, others +2.31.
- Test A, Transformer, arm lr_plateau: gap +2.90 pp [+1.44, +4.48], classical better on 15/17, Holm p=0.011; shift vs default -0.02 pp [-0.08, +0.01], Holm p=1.000; small datasets +4.38, others +2.28.
- Test A, Transformer, arm wd_1e-4: gap +2.81 pp [+1.34, +4.38], classical better on 14/17, Holm p=0.013; shift vs default -0.12 pp [-0.32, +0.05], Holm p=1.000; small datasets +4.51, others +2.10.
- Test A, Transformer, arm wd_1e-3: gap +2.64 pp [+1.20, +4.18], classical better on 13/17, Holm p=0.013; shift vs default -0.28 pp [-0.51, -0.08], Holm p=0.627; small datasets +4.19, others +1.99.
- Test A, Transformer, arm dropout_0.2: gap +2.82 pp [+1.47, +4.32], classical better on 14/17, Holm p=0.007; shift vs default -0.11 pp [-0.35, +0.13], Holm p=1.000; small datasets +4.35, others +2.17.
- Test A, Transformer, arm dropout_0.4: gap +2.58 pp [+1.29, +4.06], classical better on 13/17, Holm p=0.011; shift vs default -0.34 pp [-0.64, -0.03], Holm p=0.140; small datasets +3.94, others +2.01.
- Test A, Transformer, arm patience_15: gap +2.62 pp [+1.55, +3.83], classical better on 15/17, Holm p=0.002; shift vs default -0.30 pp [-1.62, +0.74], Holm p=1.000; small datasets +3.19, others +2.39.
- Test A, Transformer, arm batch_64: gap +2.01 pp [+0.81, +3.44], classical better on 13/17, Holm p=0.013; shift vs default -0.91 pp [-1.99, -0.08], Holm p=1.000; small datasets +2.07, others +1.99.
- Test A, Transformer, arm small_data: gap +2.17 pp [+1.14, +3.28], classical better on 14/17, Holm p=0.008; shift vs default -0.75 pp [-1.95, +0.29], Holm p=1.000; small datasets +2.67, others +1.96.
- Test A, Transformer, arm best_arm_per_dataset (oracle): gap +0.63 pp [-0.41, +1.80], classical better on 9/17, Holm p=0.378; shift vs default -2.29 pp [-3.48, -1.39], Holm p=<0.001; small datasets +0.23, others +0.79.
- Test D, FT-Transformer compact_small_data: FS effect -0.56 pp [-1.58, +0.48], Holm p=0.291; ROC-AUC all features 77.15, FS 76.60.
- Test D, FT-Transformer default: FS effect -2.76 pp [-5.57, -0.46], Holm p=0.080; ROC-AUC all features 75.41, FS 72.65.
- Test D, FT-Transformer difference (compact - default): FS effect +2.20 pp [-0.18, +5.47], Holm p=0.291.

## Outcome per family (pre-specified rules)