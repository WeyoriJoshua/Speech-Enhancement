# Speech Enhancement at Low Signal-to-Noise Ratios

Research code and reproducibility materials for deep-learning single-channel speech enhancement under severe noise and distribution shift.

## Current publication study

The current manuscript is:

**Contextual phase-aware speech enhancement under severe noise and distribution shift: A controlled ablation of signal-to-noise ratio conditioning and adversarial learning**

The study evaluates a controlled A0-A5 model family:

- **A0:** magnitude-only U-Net using the noisy phase.
- **A1:** phase-aware U-Net.
- **A2 / CPA-U-Net:** A1 plus dual-axis time-frequency contextual modeling; this is the principal model.
- **A3:** A2 plus internal SNR estimation and FiLM conditioning.
- **A4:** A3 plus fixed adversarial supervision.
- **A5:** A4 plus estimated-SNR-adaptive adversarial weighting.

The external stress test uses all 2,620 LibriSpeech test-clean utterances mixed with Microsoft DNS Challenge noise at **-20, -15, -10, -5, 0, 5, and 10 dB**, producing **18,340 cases**.

Under the final uniform learned-system OOD protocol, inference is performed using **2.56 s chunks**, **0.64 s overlap**, **1.92 s hop**, and complementary linear crossfade overlap-add.

## Main completed result

A2 / CPA-U-Net is the strongest balanced model in the completed study. Relative to A0 over the full external 18,340-case analysis, A2 improves approximately:

- PESQ: **+0.091**
- STOI: **+0.045**
- ESTOI: **+0.055**
- SI-SDR: **+1.763 dB**
- reference-relative SNR: **+0.905 dB**

The extreme **-20 dB and -15 dB** conditions remain stress/failure regimes and are not presented as uniformly improved.

## Publication reproducibility material

See publication_2026/ for the publication protocol, derived summary results, data-availability notes, environment specification, and release manifest.

A complete archival package containing the exact A0-A5 notebooks, OOD evaluation utilities, selected best checkpoints, and the case-level derived OOD results has been prepared for permanent deposit. The permanent DOI will be added here only after the exact versioned archive is published through an archival repository such as Zenodo.

## Legacy notebooks

Earlier TensorFlow U-Net/GAN experiments remain in the repository for provenance. They are not the complete implementation of the current A0-A5 publication study.

## Third-party datasets

Raw datasets are not redistributed. Obtain and configure local paths for:

- VoiceBank+DEMAND
- LibriSpeech test-clean
- Microsoft DNS Challenge noise corpus

## Citation

See CITATION.cff.

## Corresponding author

Joshua Akowuje Weyori  
Department of Computer Science and Informatics, School of Sciences  
University of Energy and Natural Resources, Sunyani, Ghana  
ORCID: https://orcid.org/0009-0006-1526-6110
