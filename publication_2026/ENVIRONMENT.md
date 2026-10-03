# Environment

The publication workflow was run locally under Windows with **Python 3.11.9** and an NVIDIA GeForce RTX 3060 Laptop GPU.

The publication setup notebook specifies the following PyTorch stack when installation is required:

- torch==2.5.1
- torchvision==0.20.1
- torchaudio==2.5.1

Additional Python dependencies used by the publication notebooks include numpy, scipy, pandas, PyYAML, tqdm, soundfile, librosa, pesq, pystoi, jiwer, matplotlib, and tensorboard.

For strict environment preservation, the archival package should be accompanied by a machine-generated environment lock (for example, pip freeze) if available from the original speech_pub_env. The dependency list above is taken from the publication setup notebook and should not be presented as a substitute for a historical lock file.
