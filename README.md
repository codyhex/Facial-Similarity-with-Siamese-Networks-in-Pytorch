# Facial Similarity with Siamese Networks in Pytorch
You can read the accompanying article at https://hackernoon.com/one-shot-learning-with-siamese-networks-in-pytorch-8ddaab10340e

The goal is to teach a siamese network to be able to distinguish pairs of images. 
This project uses pytorch. 

Any dataset can be used. Each class must be in its own folder. This is the same structure that PyTorch's own image folder dataset uses.

### Converting pgm files (if you decide to use the AT&T dataset) to png
1. Install imagemagick 
2. Go to root directory of the images
3. Run `find -name "*pgm" | xargs -I {} convert {} {}.png`



## Installing the right version of PyTorch 
This project is updated to be compatible with pytorch 0.4.0


You can find other project requirements in `requirements.txt` , which you can install using `pip install -r requirements.txt`

#### This project requires python3.6

## How to install from fresh
# create conda env
conda create -n pytorch python=3.6

# activate the created environment
conda activate pytorch

# install numpy
conda install numpy

# install torch
conda install torchvision -c anaconda pytorch-gpu
or use this
conda install torchvision pytorch cuda100 -c pytorch

# test gpu install
python -c 'import torch; print(torch.rand(2,3).cuda())'

# for install jupyter & matplotlib in this env 
conda install nb_conda
conda install matplotlib
