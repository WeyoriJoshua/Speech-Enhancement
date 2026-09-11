A1 PHASE-AWARE CONTROLLED ABLATION

Project root:
D:\PAPERS\SPEECH\low_snr_speech_enhancement

Run after A0 has been frozen.

Order:
1. 04_A1_PhaseAware_UNet_Training.ipynb
2. 05_A1_PhaseAware_Evaluation.ipynb
3. 06_A0_vs_A1_Comparison.ipynb

Kernel:
Python 3 (speech_pub_env)

A1 keeps the A0 U-Net backbone, data manifests, STFT configuration,
optimizer settings, batch size, seed, and early stopping protocol.
It adds only explicit phase estimation and the corresponding
phase-aware supervision.

Output root:
D:\PAPERS\SPEECH\low_snr_speech_enhancement\outputs\a1_phaseaware
