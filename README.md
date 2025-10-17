# Ephys‑Jupyter

A small, reproducible **Jupyter** workflow for extracellular electrophysiology (Neuropixels / SpikeGLX).
It covers **Preprocessing → Sorting (Kilosort4 via SpikeInterface) → Quality metrics → Export to Phy**


## Features

* **Jupyter‑first**: clear notebooks for each step.
* **SpikeGLX‑ready**: reads AP/LFP/NIDQ streams (e.g., `imec0.ap`, `imec0.lf`, `nidq`).
* **One stack**: SpikeInterface for preprocessing & QC; Kilosort4 for sorting; Phy for manual curation.
* **Export that works**: ships Phy files with **binary** so single‑spike waveforms can be viewed.



## Requirements
* Python **3.9+** (Conda recommended)
* **SpikeInterface**, **Phy**
* All packages are exported in the requirements.yml



## What this code does (in plain words)

* **Reads** SpikeGLX AP data.
* **Filters** 300 Hz and applies a **global reference**.
* **Sorts** spikes with **Kilosort4** (via SpikeInterface).
* **Computes** basic quality metrics (presence ratio, amplitude cutoff, ISI violation).
* **Exports** all files needed by **Phy**, **including binary** for per‑spike waveforms.


## Notes

* If Phy shows only average waveforms and says files are missing, make sure you exported with `copy_binary=True` and did not move files.
* Keep versions pinned for reproducibility.


## License

MIT
