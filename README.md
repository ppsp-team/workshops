# HyPyP – The Hyperscanning Python Pipeline# HyPyP – The Hyperscanning Python Pipeline# PPSP Workshops Repository



> Hands-on Workshop · Practical MEG/EEG 2025



**Event:** [Practical MEG/EEG Conference 2025](https://cuttingeeg.org/practicalmeeg2025/) · [Workshop Page](https://cuttingeeg.org/practicalmeeg2025/bouquet/)  > Hands-on Workshop · Practical MEG/EEG 2025# AI & Sleep — Summer School 2025  

**Instructor:** Guillaume Dumas (Université de Montréal, Canada)  

**Duration:** 1 hour  

**Topics:** Multi-brain hyperscanning analysis with HyPyP (EEG, MEG, fNIRS)

## Workshop Information> Collection of hands-on workshops for sleep and physiological signal processing> Hands-on Workshop · **8** Jupyter Notebooks

This workshop introduces practical computational methods for analyzing data collected simultaneously from multiple participants during social interactions using the open-source HyPyP Python toolbox.



**Event:** [Practical MEG/EEG Conference 2025](https://cuttingeeg.org/practicalmeeg2025/)  

**Workshop Page:** [Bouquet Session](https://cuttingeeg.org/practicalmeeg2025/bouquet/)  

**Instructor:** Guillaume Dumas  This repository contains multiple workshops, each organized in its own branch. Each workshop is self-contained with its own notebooks, data, and specific README.## Workshop Information

**Affiliation:** Université de Montréal, Canada  

**Date:** 2025  

**Duration:** 1 hour  

**Format:** Hands-on workshop with live coding demonstrations---**Event:** [Canadian Sleep Network Summer School 2025](https://reseausommeil.ca/DOC/Programme-EcoleEte-2025.pdf)  



---**Date:** June 2025  



## Overview## Available Workshops**Duration:** 90 minutes  



Discover the potential of hyperscanning analysis with **HyPyP**, an open-source Python toolbox designed specifically for multi-brain neuroscience research (EEG, MEG, & fNIRS). This hands-on workshop will introduce researchers to practical computational methods for analyzing data collected simultaneously from multiple participants during social interactions.**Location:** Québec, Canada  



**Hyperscanning**—the simultaneous recording of brain activity from multiple individuals—represents a paradigm shift in social neuroscience, allowing researchers to move beyond traditional single-brain stimulus-response approaches to study real-time neural dynamics during natural social exchanges between multiple individuals. However, these complex datasets require specialized analytic techniques that conventional neuroimaging software packages do not typically offer.### 1. Summer School 2025**Language:** English (with French support)



---**Branch:** `summer-school-2025`  



## What You Will Learn**Event:** Canadian Sleep Network Summer School 2025  ---



This workshop will provide participants with:**Date:** June 2025  



- **Overview of hyperscanning methodologies** and their analytical challenges**Location:** Québec, Canada  ## Overview

- **Hands-on experience** with HyPyP's core functions for multi-brain data preprocessing

- **Practical implementation** of inter-brain connectivity measures**Duration:** 90 minutes  

- **Visualization techniques** for inter-brain synchrony analysis

- **Statistical approaches** specific to hyperscanning experiments**Topics:** Machine Learning & Deep Learning for Sleep AnalysisBienvenue ! This README gathers everything you need **before** arriving at the



The session will combine brief theoretical explanations with live coding demonstrations using sample datasets in EEG and fNIRS. Participants will work through practical examples illustrating HyPyP's capabilities for capturing neural signatures of social coordination.- 8 Jupyter notebooks90-minute workshop. Follow the steps for your operating system and



---- EEG/ECG/EDA signal processingyou'll be ready to run all notebooks offline — the data are already bundled



## Prerequisites- Classical ML models (LogReg, SVM, RF, K-Means)inside the repo (`./data/`).



### Required- Deep Learning (CNN with TensorFlow & PyTorch)

- **Laptop** with Python installed (Anaconda distribution recommended)

- **Basic knowledge** of Python programming---

- **Basic understanding** of neuroimaging concepts

- **Pre-installation** of HyPyP and dependencies (see below)---



---## 1 · Fast checklist



## Installation Instructions## How to Access a Workshop



### 1. Install Anaconda (if not already installed)| Task | macOS 13 + | Windows 10/11 | Ubuntu 22.04 |



Download and install Anaconda for your operating system:To access a specific workshop, checkout its branch:|------|------------|---------------|--------------|

- **macOS:** [Anaconda3-2025-MacOSX](https://www.anaconda.com/download)

- **Windows:** [Anaconda3-2025-Windows](https://www.anaconda.com/download)| Install **Anaconda** | `.pkg` | `.exe` | `.sh` |

- **Linux:** [Anaconda3-2025-Linux](https://www.anaconda.com/download)

```bash| Create env `sleep‑ai` & deps | Terminal.app | Anaconda Prompt | Terminal |

### 2. Create a dedicated environment

# Clone the repository| Launch **JupyterLab** | `conda activate … && jupyter lab` | same | same |

```bash

# Create environment with Python 3.10git clone https://github.com/ppsp-team/workshops.git| Clone repo | `git clone …` | Git Bash / Desktop | same |

conda create -n hypyp python=3.10 -y

conda activate hypypcd workshops

```

_Total prep time ≈ 15 min._

### 3. Install HyPyP and dependencies

# List all available workshops

```bash

# Core dependenciesgit branch -a---

conda install numpy pandas scipy matplotlib -y

conda install -c conda-forge mne jupyter jupyterlab -y



# Install HyPyP# Switch to a specific workshop## 2 · Workshop goals

pip install hypyp

git checkout summer-school-2025

# Additional useful packages

pip install seaborn scikit-learn* Load & pre‑process EEG/ECG/EDA  

```

# Read the workshop-specific README* Engineer classical features & visualise  

### 4. Verify installation

cat README.md* Train ML models (LogReg, SVM, RF)  

```bash

# Start Python and test import```* Compare to a tiny raw‑signal CNN (TF & PyTorch)

python -c "import hypyp; print(f'HyPyP version: {hypyp.__version__}')"

```



### 5. Launch JupyterLab------



```bash

jupyter lab

```## Branch Structure## 3 · Notebook line‑up



---



## Repository StructureEach workshop branch contains:| # | Notebook | Core concept | Time |



```- **README.md** - Workshop-specific setup and instructions|---|----------|--------------|------|

practicalmeeg-2025/

 ├── notebooks/          # Workshop Jupyter notebooks- **Notebooks/** - Jupyter notebooks (.ipynb files)| 01 | 01_Intro.ipynb | PSG loading & band‑power | 12 min |

 ├── data/              # Sample hyperscanning datasets (EEG/fNIRS)

 ├── examples/          # Code examples and demonstrations- **data/** - Dataset files (when applicable)| 02 | 02_Sleep_Stage_Logreg.ipynb | Logistic Regression | 15 min |

 ├── utils/             # Helper functions

 └── README.md          # This file- **requirements.txt** or **environment.yml** - Dependencies| 03 | 03_KMeans_HRV.ipynb | HRV K‑Means | 12 min |

```

| 04 | 04_SVM_EDA_Arousal.ipynb | EDA SVM | 15 min |

---

---| 05 | 05_PCA_UMAP_Fusion.ipynb | PCA + UMAP | 12 min |

## Sample Dataset

| 06 | 06_RandomForest_SE.ipynb | Sleep Efficiency RF | 12 min |

The workshop will use sample EEG and fNIRS hyperscanning datasets. These will be provided during the workshop or can be accessed from the HyPyP examples repository.

## Creating a New Workshop| 07a | 07a_Tiny_CNN_TF.ipynb | CNN (TensorFlow) | 15 min |

---

| 07b | 07b_Tiny_CNN_PT.ipynb | CNN (PyTorch) | 15 min |

## Key Topics Covered

When creating a new workshop:

### 1. Introduction to Hyperscanning

- Multi-brain recording paradigms---

- Analytical challenges in hyperscanning data

- Overview of HyPyP architecture1. Create a new branch from `main`



### 2. Data Preprocessing   ```bash## 4 · Installation

- Loading multi-participant data

- Synchronization across recordings   git checkout main

- Artifact rejection and cleaning

   git checkout -b workshop-name-YYYY### 4.1 Install Anaconda

### 3. Inter-Brain Connectivity

- Computing inter-brain measures   ```

- Connectivity metrics (PLV, CCorr, etc.)

- Frequency-band specific analysisChoose the installer for your OS:



### 4. Visualization2. Add your workshop materials (notebooks, data, etc.)

- Plotting inter-brain synchrony

- Time-frequency representations* macOS Apple Silicon 🤍 `Anaconda3‑2025‑MacOS‑arm64.pkg`  

- Network visualizations

3. Create a workshop-specific README with:* macOS Intel             `…‑x86_64.pkg`  

### 5. Statistical Analysis

- Permutation testing for hyperscanning   - Workshop title and date* Windows                 `Anaconda3‑2025‑Windows‑x86_64.exe`  

- Cluster-based statistics

- Effect size computation   - Event context and location* Ubuntu                  `Anaconda3‑2025‑Linux‑x86_64.sh`



---   - Setup instructions



## Additional Resources   - Learning objectives### 4.2 Create the environment



- **HyPyP Documentation:** [https://hypyp.readthedocs.io/](https://hypyp.readthedocs.io/)   - Prerequisites

- **GitHub Repository:** [https://github.com/ppsp-team/HyPyP](https://github.com/ppsp-team/HyPyP)

- **Paper:** Dumas, G., et al. (2020). "HyPyP: A Hyperscanning Python Pipeline for inter-brain connectivity analysis." Social Cognitive and Affective Neuroscience.```bash

- **Tutorial Videos:** Available on the HyPyP documentation site

4. Commit and push your branchconda create -n sleep-ai python=3.11 -y

---

   ```bashconda activate sleep-ai

## Troubleshooting

   git add .

| Issue | Solution |

|-------|----------|   git commit -m "feat: Add [Workshop Name] workshop"conda install numpy pandas scipy scikit-learn matplotlib seaborn -y

| `ModuleNotFoundError: hypyp` | Run `pip install hypyp` in your environment |

| MNE import errors | Install with `conda install -c conda-forge mne` |   git push origin workshop-name-YYYYpip install mne neurokit2 umap-learn imbalanced-learn

| Jupyter kernel not found | Run `python -m ipykernel install --user --name hypyp --display-name "Python (hypyp)"` |

| Permission errors on installation | Use `pip install --user hypyp` |   ```

| Dataset loading issues | Ensure MNE is properly installed and datasets are in correct format |

# deep‑learning

---

5. Update this main README to list the new workshoppip install tensorflow==2.16        # notebook 07a

## Getting Help

pip install torch==2.2 torchinfo    # notebook 07b

- **During workshop:** Ask questions in person or via the workshop chat

- **After workshop:** Open issues on [HyPyP GitHub](https://github.com/ppsp-team/HyPyP/issues)---```

- **Email:** guillaume.dumas@umontreal.ca

- **Community:** Join the HyPyP discussions on GitHub



---## Contact**Apple Silicon GPU**



## Citation



If you use HyPyP in your research, please cite:For questions about any workshop:```bash



```- Open an issue on GitHubpip install --pre torch --extra-index-url https://download.pytorch.org/whl/nightly/cpu

Dumas, G., Moreau, Q., Tognoli, E., & Kelso, J. A. S. (2020).

The human dynamic clamp as a paradigm for social interaction.- Email: remy.ramadour.hsj @ ssss.gouv.qc.caexport PYTORCH_ENABLE_MPS_FALLBACK=1

Proceedings of the National Academy of Sciences, 117(30), 17751-17759.

``````



------



## License### 4.3 Install JupyterLab



HyPyP is released under the BSD-3-Clause License. See the [LICENSE](https://github.com/ppsp-team/HyPyP/blob/master/LICENSE) file for details.## License



---```bash



_See you at Practical MEG/EEG 2025 – happy hyperscanning!_ 🧠🧠Each workshop may have its own licensing terms. Check the workshop-specific branch for details.conda install jupyterlab notebook -y


jupyter lab    # opens http://localhost:8888
```

---

## 5 · Repo structure

```
workshops/
 ├─ data/        # contains ST7011J0 EDF files
 ├─ notebooks/   # eight .ipynb notebooks
 ├─ outputs/     # CSVs generated during the lab
 └─ README.md
```

Clone the repo:

```bash
git clone https://github.com/ppsp-team/workshops
cd workshops
```

No extra download — the EDF files are already in `./data/`.

---

## 6 · Optional speed‑ups

| Tip | macOS M‑series | Windows/Linux (NVIDIA) |
|-----|---------------|------------------------|
| TensorFlow GPU | `pip install tensorflow‑metal` | install CUDA 12.4 |
| PyTorch device | `device="mps"` | `device="cuda"` |
| DataLoader workers | `num_workers=4` | `num_workers=4‑8` |
| Mixed precision | `autocast("mps")` | `autocast()` |

---

## 7 · Troubleshooting

| Symptom | Fix |
|---------|-----|
| `ModuleNotFoundError` | `pip install <package>` |
| Kernel not in Jupyter | `python -m ipykernel install --user --name sleep-ai --display-name "Python (sleep-ai)"` |
| Slow PyTorch on Mac | use `mps`, workers, avoid per‑batch `.to(device)` |
| Matplotlib backend error (Win) | `pip install pyqt5` or `%matplotlib inline` |

---

## 8 · Contact

Questions? Open an issue or email **remy.ramadour.hsj @ ssss.gouv.qc.ca**.

_See you at the Summer‑School — happy coding!_
