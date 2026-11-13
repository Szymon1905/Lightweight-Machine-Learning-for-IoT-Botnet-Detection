# Lightweight Machine Learning for IoT Botnet Detection

Research Project at Wrocław University of Science and Technology (PWr).

**Team:** Michał Pawlus, Przemysław Wdowczyk, Szymon Borzdyński.

## Project

We study the trade-off between detection performance and computational cost in IoT botnet detection. We plan to compare logistic regression, a decision tree, a random forest and a small multilayer perceptron using the N-BaIoT dataset.

Research questions:

- How do the models compare in attack recall and false-positive rate?
- How does the amount of training data affect detection performance?
- What trade-offs exist between detection quality and training and prediction time?

## Current progress

TODO add


## Setup on Ubuntu

Create a virtual environment alongside the repository directory. Run these commands from the repository root:

```bash
python3 -m venv ../RPvenv
source ../RPvenv/bin/activate
python -m pip install -r requirements.txt
python -m jupyterlab
```

Open the data audit notebook in JupyterLab and run its cells in order.

## Dataset

Download [N-BaIoT from the UCI Machine Learning Repository](https://doi.org/10.24432/C5RC8J) and extract the device folders into `data/raw/`.

For the Danmini analysis, also extract `gafgyt_attacks.rar` and `mirai_attacks.rar` into their respective subfolders. The expected paths include:

- `data/raw/Danmini_Doorbell/benign_traffic.csv`
- `data/raw/Danmini_Doorbell/gafgyt_attacks/combo.csv`
- `data/raw/Danmini_Doorbell/mirai_attacks/ack.csv`

Set the notebook's `device_dir` variable to the location of the Danmini folder on your computer.

The dataset is excluded from Git through `.gitignore` and must be downloaded separately.

## Related work

- Meidan et al. (2018). [N-BaIoT—Network-Based Detection of IoT Botnet Attacks Using Deep Autoencoders](https://doi.org/10.1109/MPRV.2018.03367731).
- Rey et al. (2022). [Federated learning for malware detection in IoT devices](https://doi.org/10.1016/j.comnet.2021.108693).
- [A lightweight deep learning framework for botnet detecting at the IoT edge](https://doi.org/10.1016/j.cose.2023.103195) (2023).
