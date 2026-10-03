# PLOS ONE publication reproducibility material

This directory documents the completed experiments supporting the manuscript **“Contextual phase-aware speech enhancement under severe noise and distribution shift: A controlled ablation of signal-to-noise ratio conditioning and adversarial learning.”**

## Completed experimental chain

| System | Change relative to previous stage | Role |
|---|---|---|
| A0 | Magnitude-mask U-Net; noisy phase | Core baseline |
| A1 | Phase-aware reconstruction | Phase package test |
| A2 / CPA-U-Net | Dual-axis time-frequency context | Principal model |
| A3 | Internal SNR estimator + FiLM | Conditioning diagnostic |
| A4 | Fixed conditional adversarial objective | Fixed-GAN diagnostic |
| A5 | SNR-adaptive adversarial weight | Adaptive-GAN diagnostic |

## External evaluation

The frozen external stress test contains 2,620 LibriSpeech test-clean utterances at seven target SNRs (-20 to +10 dB), for 18,340 paired cases. DNS Challenge noise is used as the external noise corpus. This is a deterministic stress test, not the official DNS Challenge evaluation recipe.

Learned systems use a common chunked inference protocol:

- sampling rate: 16 kHz
- chunk: 2.56 s / 40,960 samples
- overlap: 0.64 s / 10,240 samples
- hop: 1.92 s
- reconstruction: complementary linear crossfade overlap-add

## Files

- VOICEBANK_A0_A5_SUMMARY.csv - in-domain seed-42 summary for A0-A5.
- OOD_SUMMARY_BY_TARGET_SNR.csv - external mean/SD results by system and target SNR.
- PAIRED_STATS_ALL_SNRS.csv - selected full-range paired comparisons.
- SNR_ESTIMATOR_DIAGNOSTICS.csv - A3-A5 SNR-estimator calibration under distribution shift.
- CHECKPOINT_RUNTIME_AUDIT.csv - checkpoint epochs, parameter counts, and median RTF.
- REPRODUCIBILITY_AUDIT.json - case counts, manifest hash, per-system hashes, and realized-SNR audit.
- ENVIRONMENT.md - execution environment and package requirements.
- DATA_AVAILABILITY.md - public-data and archival-release statement.
- RELEASE_MANIFEST.md - exact prepared archival package identifier.

## Important scope note

The later Oracle-SNR, matched-strength A4M control, three-seed extension, ASR WER, DNSMOS, and contemporary external-baseline experiments are follow-on work and are **not** represented as completed results in the current manuscript.
