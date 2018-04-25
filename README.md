# GANMM
GANMM code for paper **Mixture of GANs for Clustering** (IJCAI 2018)

## Requirement
- python 3.5
- tensorflow
- numpy
- sklearn
- argparse
- pickle

## Files

- GANMM.py  implements the algorihtm
- main.py   is the demo that uses GANMM to cluster some data sets as in the paper
- Data      contains data sets
- nets      network structure
- tflib     tensorflow components

## Run Demo
- To run experiment on mnist data set, just running:
```bash
# mnist raw data
python main.py mnist

# mnist preprocessed by stacked auto-encoder
python main.py sae_mnist
```
GPU version of TensorFlow is recommended for mnist data set. Tensorflow (CPU) may not support `data_format="NCHW"` in Conv2DBackpropFilter operate.

- Two UCI-dataset:
```bash
# Image Segmentation data set
python main.py seg

# Artificial Characters data set
python main.py chara
```
- On different data scale:
```bash
python main.py seg --scale 0.5
```
