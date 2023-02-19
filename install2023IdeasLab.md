## Installation @ 2023 Feb

- 2019 Jul 7 -> trimesh2.38.42 https://github.com/mikedh/trimesh/releases?q=2.38.42&expanded=true

```
conda create -n rodenSQ  -c conda-forge mayavi==4.5.0 python=2.7
conda activate rodenSQ
pip install https://github.com/KieranWynn/pyquaternion/archive/refs/tags/v0.9.5.tar.gz
conda install pytorch==0.4.1 cuda90 -c pytorch
pip install https://github.com/pytorch/vision/archive/refs/tags/v0.1.8.tar.gz
pip install https://github.com/mikedh/trimesh/archive/refs/tags/2.38.42.tar.gz
pip install https://github.com/verigak/progress/archive/refs/tags/1.4.tar.gz
conda install -c anaconda cython
conda install -c anaconda scikit-learn 
# The above step installed numpy 1.16.5
# (Or pip install https://github.com/numpy/numpy/archive/refs/tags/v1.16.5.tar.gz)

# pip install https://github.com/python-pillow/Pillow/archive/refs/tags/6.1.0.tar.gz

pip install https://github.com/sympy/sympy/archive/refs/tags/sympy-1.4.tar.gz
pip install https://github.com/mwaskom/seaborn/archive/refs/tags/v0.9.0.tar.gz
pip install https://github.com/matplotlib/matplotlib/archive/refs/tags/v2.2.3.tar.gz
pip install backports.functools-lru-cache==1.5

# comment out https://github.com/RodenLuo/superquadric_parsing/blob/master/setup.py#L58

# comment out all required packages in setup.py and requirements.txt

conda install traitsui==6.1.1
conda install  -c conda-forge pyface=6.1.0

pip install --user -e .

# Try also Py3 version https://github.com/yishayahu/superquadric_parsing
```
