# Forecasting-High-Significance-Periodicity-in-Gamma-Ray-Blazars-Using-Transformers
## Authors: $$\textcolor{blue}{\text{Mohamed Hashad, Amr El-Zant and Ahmed Hammad}}$$ 

<img width="1205" height="666" alt="Screenshot 2025-10-01 at 5 07 23 PM" src="https://github.com/user-attachments/assets/1c058b25-e7d9-488f-b276-2267e2a6199a" />



## Prerequisites

Before you begin, ensure you have git installed on your machine to clone this repository. If git is not installed, you can download it from [Git's official site](https://git-scm.com/downloads).

## Installation

Follow these steps to set up your environment and start time series forecasting. 

### Step 1: Clone the Repository

Clone this repository to your local machine using the following command:

```bash
git https://github.com/AHamamd150/Forecasting-High-Significance-Periodicity-in-Gamma-Ray-Blazars-Using-Transformers.git
```

### Step 2: Install Conda

If you do not have Miniconda or Anaconda installed, download and install it from [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/individual) respectively.

### Step 3: Set Up Your Environment

This project relies on several dependencies listed in `environment.yml`, including libraries such as NumPy, Pandas, Matplotlib, tqdm, h5py, scikit-learn, PyTorch, PyTorch Geometric, PyTorch Lightning, and Torchmetrics.

To install all dependencies at once and create a Conda environment, run the following command in your terminal:

```bash
conda env create -f environment.yml
```

### Step 4: Activate the Environment
```bash
conda activate Blazars_Forecasting
```

##  Get started
To traint the Transformer network.
```bash
python main.py fit --config config/config.yaml
```

For testing the network one need to retore the weigths and the configuration file from the best epoch results as 

```bash
python main.py test -c checkpoints/version_0/config.yaml --ckpt_path checkpoints/version_0/checkpoints/best_checkpoint.ckpt
```


