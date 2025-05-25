
# AI & Sleep — Summer-School 2025  
> Hands-on Workshop · **8** Jupyter Notebooks

Bienvenue ! This README gathers everything you need **before** arriving at the
90-minute workshop. Follow the steps for your operating system and
you’ll be ready to run all notebooks offline — the data are already bundled
inside the repo (`./data/`).

---

## 1 · Fast checklist

| Task | macOS 13 + | Windows 10/11 | Ubuntu 22.04 |
|------|------------|---------------|--------------|
| Install **Anaconda** | `.pkg` | `.exe` | `.sh` |
| Create env `sleep‑ai` & deps | Terminal.app | Anaconda Prompt | Terminal |
| Launch **JupyterLab** | `conda activate … && jupyter lab` | same | same |
| Clone repo | `git clone …` | Git Bash / Desktop | same |

_Total prep time ≈ 15 min._

---

## 2 · Workshop goals

* Load & pre‑process EEG/ECG/EDA  
* Engineer classical features & visualise  
* Train ML models (LogReg, SVM, RF)  
* Compare to a tiny raw‑signal CNN (TF & PyTorch)

---

## 3 · Notebook line‑up

| # | Notebook | Core concept | Time |
|---|----------|--------------|------|
| 01 | 01_Intro.ipynb | PSG loading & band‑power | 12 min |
| 02 | 02_Sleep_Stage_Logreg.ipynb | Logistic Regression | 15 min |
| 03 | 03_KMeans_HRV.ipynb | HRV K‑Means | 12 min |
| 04 | 04_SVM_EDA_Arousal.ipynb | EDA SVM | 15 min |
| 05 | 05_PCA_UMAP_Fusion.ipynb | PCA + UMAP | 12 min |
| 06 | 06_RandomForest_SE.ipynb | Sleep Efficiency RF | 12 min |
| 07a | 07a_Tiny_CNN_TF.ipynb | CNN (TensorFlow) | 15 min |
| 07b | 07b_Tiny_CNN_PT.ipynb | CNN (PyTorch) | 15 min |

---

## 4 · Installation

### 4.1 Install Anaconda

Choose the installer for your OS:

* macOS Apple Silicon 🤍 `Anaconda3‑2025‑MacOS‑arm64.pkg`  
* macOS Intel             `…‑x86_64.pkg`  
* Windows                 `Anaconda3‑2025‑Windows‑x86_64.exe`  
* Ubuntu                  `Anaconda3‑2025‑Linux‑x86_64.sh`

### 4.2 Create the environment

```bash
conda create -n sleep-ai python=3.11 -y
conda activate sleep-ai

conda install numpy pandas scipy scikit-learn matplotlib seaborn -y
pip install mne neurokit2 umap-learn imbalanced-learn

# deep‑learning
pip install tensorflow==2.16        # notebook 07a
pip install torch==2.2 torchinfo    # notebook 07b
```

**Apple Silicon GPU**

```bash
pip install --pre torch --extra-index-url https://download.pytorch.org/whl/nightly/cpu
export PYTORCH_ENABLE_MPS_FALLBACK=1
```

### 4.3 Install JupyterLab

```bash
conda install jupyterlab notebook -y
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
