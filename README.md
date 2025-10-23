# PPSP Workshops Repository

# AI & Sleep — Summer School 2025  

> Collection of hands-on workshops for sleep and physiological signal processing> Hands-on Workshop · **8** Jupyter Notebooks



This repository contains multiple workshops, each organized in its own branch. Each workshop is self-contained with its own notebooks, data, and specific README.## Workshop Information



---**Event:** [Canadian Sleep Network Summer School 2025](https://reseausommeil.ca/DOC/Programme-EcoleEte-2025.pdf)  

**Date:** June 2025  

## Available Workshops**Duration:** 90 minutes  

**Location:** Québec, Canada  

### 1. Summer School 2025**Language:** English (with French support)

**Branch:** `summer-school-2025`  

**Event:** Canadian Sleep Network Summer School 2025  ---

**Date:** June 2025  

**Location:** Québec, Canada  ## Overview

**Duration:** 90 minutes  

**Topics:** Machine Learning & Deep Learning for Sleep AnalysisBienvenue ! This README gathers everything you need **before** arriving at the

- 8 Jupyter notebooks90-minute workshop. Follow the steps for your operating system and

- EEG/ECG/EDA signal processingyou'll be ready to run all notebooks offline — the data are already bundled

- Classical ML models (LogReg, SVM, RF, K-Means)inside the repo (`./data/`).

- Deep Learning (CNN with TensorFlow & PyTorch)

---

---

## 1 · Fast checklist

## How to Access a Workshop

| Task | macOS 13 + | Windows 10/11 | Ubuntu 22.04 |

To access a specific workshop, checkout its branch:|------|------------|---------------|--------------|

| Install **Anaconda** | `.pkg` | `.exe` | `.sh` |

```bash| Create env `sleep‑ai` & deps | Terminal.app | Anaconda Prompt | Terminal |

# Clone the repository| Launch **JupyterLab** | `conda activate … && jupyter lab` | same | same |

git clone https://github.com/ppsp-team/workshops.git| Clone repo | `git clone …` | Git Bash / Desktop | same |

cd workshops

_Total prep time ≈ 15 min._

# List all available workshops

git branch -a---



# Switch to a specific workshop## 2 · Workshop goals

git checkout summer-school-2025

* Load & pre‑process EEG/ECG/EDA  

# Read the workshop-specific README* Engineer classical features & visualise  

cat README.md* Train ML models (LogReg, SVM, RF)  

```* Compare to a tiny raw‑signal CNN (TF & PyTorch)



------



## Branch Structure## 3 · Notebook line‑up



Each workshop branch contains:| # | Notebook | Core concept | Time |

- **README.md** - Workshop-specific setup and instructions|---|----------|--------------|------|

- **Notebooks/** - Jupyter notebooks (.ipynb files)| 01 | 01_Intro.ipynb | PSG loading & band‑power | 12 min |

- **data/** - Dataset files (when applicable)| 02 | 02_Sleep_Stage_Logreg.ipynb | Logistic Regression | 15 min |

- **requirements.txt** or **environment.yml** - Dependencies| 03 | 03_KMeans_HRV.ipynb | HRV K‑Means | 12 min |

| 04 | 04_SVM_EDA_Arousal.ipynb | EDA SVM | 15 min |

---| 05 | 05_PCA_UMAP_Fusion.ipynb | PCA + UMAP | 12 min |

| 06 | 06_RandomForest_SE.ipynb | Sleep Efficiency RF | 12 min |

## Creating a New Workshop| 07a | 07a_Tiny_CNN_TF.ipynb | CNN (TensorFlow) | 15 min |

| 07b | 07b_Tiny_CNN_PT.ipynb | CNN (PyTorch) | 15 min |

When creating a new workshop:

---

1. Create a new branch from `main`

   ```bash## 4 · Installation

   git checkout main

   git checkout -b workshop-name-YYYY### 4.1 Install Anaconda

   ```

Choose the installer for your OS:

2. Add your workshop materials (notebooks, data, etc.)

* macOS Apple Silicon 🤍 `Anaconda3‑2025‑MacOS‑arm64.pkg`  

3. Create a workshop-specific README with:* macOS Intel             `…‑x86_64.pkg`  

   - Workshop title and date* Windows                 `Anaconda3‑2025‑Windows‑x86_64.exe`  

   - Event context and location* Ubuntu                  `Anaconda3‑2025‑Linux‑x86_64.sh`

   - Setup instructions

   - Learning objectives### 4.2 Create the environment

   - Prerequisites

```bash

4. Commit and push your branchconda create -n sleep-ai python=3.11 -y

   ```bashconda activate sleep-ai

   git add .

   git commit -m "feat: Add [Workshop Name] workshop"conda install numpy pandas scipy scikit-learn matplotlib seaborn -y

   git push origin workshop-name-YYYYpip install mne neurokit2 umap-learn imbalanced-learn

   ```

# deep‑learning

5. Update this main README to list the new workshoppip install tensorflow==2.16        # notebook 07a

pip install torch==2.2 torchinfo    # notebook 07b

---```



## Contact**Apple Silicon GPU**



For questions about any workshop:```bash

- Open an issue on GitHubpip install --pre torch --extra-index-url https://download.pytorch.org/whl/nightly/cpu

- Email: remy.ramadour.hsj @ ssss.gouv.qc.caexport PYTORCH_ENABLE_MPS_FALLBACK=1

```

---

### 4.3 Install JupyterLab

## License

```bash

Each workshop may have its own licensing terms. Check the workshop-specific branch for details.conda install jupyterlab notebook -y

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
