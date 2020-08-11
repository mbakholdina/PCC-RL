# PCC-RL
Reinforcement learning resources for the Performance-oriented Congestion Control
project.

## Overview
This repo contains the gym environment required for training reinforcement
learning models used in the PCC project along with the Python module required to
run RL models in the PCC UDT codebase found at github.com/PCCProject/PCC-Uspace.


## Training
To run training only, go to ./src/gym/, install any missing requirements for
stable\_solve.py and run that script. By default, this should replicate the
model presented in A Reinforcement Learning Perspective on Internet Congestion
Control, ICML 2019.

## Testing Models

To test models in the real world (i.e., sending real packets into the Linux
kernel and out onto a real or emulated network), download and install the PCC
UDT code from github.com/PCCProject/PCC-Uspace. Follow the instructions in that
repo for using congestion control algorithms with Python modules, and see
./src/gym/online/README.md for additional instructions regarding testing or training models in the real world.

## Requirements

- Python3.6
- [Stable-Baselines library dependencies](https://stable-baselines.readthedocs.io/en/master/guide/install.html), OpenMPI is required

Then install project dependencies:

```
pip install gym

# Stable-Baselines supports Tensorflow versions from 1.8.0 to 1.15.0, and does not work on Tensorflow versions 2.0.0 and above
pip install tensorflow==1.14.0

# To install Stable-Baselines with support for all algorithms, including those depending on OpenMPI:
pip install stable-baselines[mpi]
```