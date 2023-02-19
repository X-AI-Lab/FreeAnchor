## Installation

### Requirements:
- Python3
- PyTorch 1.7 with CUDA support
- torchvision 0.8.2
- pycocotools
- yacs
- matplotlib
- GCC >= 4.9
- (optional) OpenCV for the webcam demo


### Step-by-step installation

```bash
# first, make sure that your conda is setup properly with the right environment
# for that, check that `which conda`, `which pip` and `which python` points to the
# right path. From a clean conda env, this is what you need to do

conda create --name free_anchor python=3.7
conda activate free_anchor

# this installs the right pip and dependencies for the fresh python
pip install ipython -i https://mirror.baidu.com/pypi/simple

# maskrnn_benchmark and coco api dependencies
pip install ninja yacs cython matplotlib tqdm -i https://mirror.baidu.com/pypi/simple

# pytorch and torchvision
pip install pytorch=1.7 torchvision=0.8.2 -i https://mirror.baidu.com/pypi/simple

# install pycocotools
pip install pycocotools -i https://mirror.baidu.com/pypi/simple

# install FreeAnchor
git clone https://github.com/X-AI-Lab/FreeAnchor.git

# the following will install the lib with
# symbolic links, so that you can modify
# the files if you want and won't need to
# re-build it
cd FreeAnchor
python setup.py build develop

# or if you are on macOS
MACOSX_DEPLOYMENT_TARGET=10.9 CC=clang CXX=clang++ python setup.py build develop
```
