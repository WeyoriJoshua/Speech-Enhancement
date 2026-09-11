# Speech Enhancement at Low Signal-to-Noise Ratios

Research code for deep-learning speech enhancement, including earlier TensorFlow U-Net/GAN experiments and a reproducible publication workflow for VoiceBank-DEMAND and LibriSpeech evaluation.

## Current notebook workflow

Run the notebooks in numerical order:

1. `00_Environment_Setup_and_Check_v2.ipynb`
2. `01_Data_Manifests_and_LowSNR_Testset_v2.ipynb`
3. `02_A0_UNet_Training_v2.ipynb`
4. `03_A0_Evaluation_v2.ipynb`
5. `04_A1_PhaseAware_UNet_Training.ipynb`
6. `05_A1_PhaseAware_Evaluation.ipynb`
7. `06_A0_vs_A1_Comparison.ipynb`

The A0 workflow provides the baseline magnitude-mask U-Net. The A1 workflow adds phase-aware training and a direct A0-versus-A1 comparison.

## Data

Audio datasets are not committed. Configure local paths for:

- VoiceBank-DEMAND (`DS_10283_2791`)
- LibriSpeech `test-clean`

Do not upload the datasets, virtual environment, or trained checkpoints directly to this repository.

## Status

The notebooks are intended to run locally in VS Code/Jupyter with Python 3.11. Dataset paths must be set before manifest generation and training. This is active research code; metrics should only be reported from completed, verified runs.
