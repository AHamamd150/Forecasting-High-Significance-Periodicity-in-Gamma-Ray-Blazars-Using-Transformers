# Forecasting-High-Significance-Periodicity-in-Gamma-Ray-Blazars-Using-Transformers
## Authors: $$\textcolor{blue}{\text{Mohamed Hashad, Amr El-Zant and Ahmed Hamad}}$$ 

<img width="569" height="582" alt="Screenshot 2025-10-01 at 5 03 37 PM" src="https://github.com/user-attachments/assets/91bf4c5b-8db8-4f5f-af67-990d2540a28b" />



## Prerequisites

Before you begin, ensure you have git installed on your machine to clone this repository. If git is not installed, you can download it from [Git's official site](https://git-scm.com/downloads).

## Installation

Follow these steps to set up your environment and start analyzing the Higgs boson's CP structure.

### Step 1: Clone the Repository

Clone this repository to your local machine using the following command:

```bash
git https://github.com/AHamamd150/Forecasting-High-Significance-Periodicity-in-Gamma-Ray-Blazars-Using-Transformers.git
```

### Step 2: Install Conda

If you do not have Miniconda or Anaconda installed, download and install it from [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/individual) respectively.

### Step 3: Set Up Your Environment

This project relies on several dependencies listed in `environment.yml`, including libraries such as NumPy, Pandas, Matplotlib, tqdm, h5py, scikit-learn, PyTorch, PyTorch Geometric, PyTorch Lightning, and Torchmetrics.

To install all dependencies at once and create a Conda environment named `higgscp`, run the following command in your terminal:

```bash
conda env create -f environment.yml
```

### Step 4: Activate the Environment
```bash
conda activate higgscp
```

##  Get started
To traint the Transformer network.
```bash
python main.py fit --config config/config_Transformer.yaml
```
To traint the Graph Attention network.
```bash
python main.py fit --config config/config_GAT.yaml
```

For testing the network one need to retore the weigths and the configuration file from the best epoch results as 

```bash
python main.py test -c checkpoints/version_0/config.yaml --ckpt_path checkpoints/version_0/checkpoints/best_checkpoint.ckpt
```


