# EPS210
Evaluating Geospatial Foundation Models for Landslide Detection 

This repository contains the ablation notebook for evaluating Clay v1.5 and hybrid 
U-Net + Clay architectures for pixel-level landslide segmentation on the 
Landslide4Sense benchmark.

## Requirements

- Google Colab (GPU runtime recommended; A100) 
- Google Drive (for storing the dataset, checkpoints, and results)

## Setup

1. Mount your Google Drive in Colab: the notebook will prompt you automatically.
2. Run the dependency installation cells at the top of the notebook. Key packages:
   - `claymodel` (Clay Foundation Model)
   - `peft` (LoRA adapters)
3. The dataset will be downloaded automatically from HuggingFace 
   (`harshinde/LandSlide4Sense`) on first run and cached as a `.tar` on your Drive.
4. Download the Clay v1.5 checkpoint (`clay-v1.5.ckpt`) from the 
   [Clay Foundation Model](https://clay-foundation.github.io/model/) and place it 
   in `MyDrive/EPS210/checkpoints/`.

## Running Experiments

Open `Clay_Abalation_Test_Final_.ipynb` in Colab and run cells sequentially. 
To switch between experiments, change the `ACTIVE_EXP` variable in the experiment 
registry cell to one of the available configurations.

## Results

Checkpoints and evaluation results are saved automatically to `MyDrive/EPS210/`.
