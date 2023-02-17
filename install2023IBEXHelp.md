```bash
git clone https://github.com/paschalidoud/superquadric_parsing.git
export ENV_PREFIX=$PWD/env

mamba create -p $ENV_PREFIX 

conda activate $ENV_PREFIX

mamba install python=2.7 mayavi=4.5.0

mamba install apptools=4.5.0 pytorch=0.4.1 cuda90 traitsui==6.1.1 pyface=6.1.1 scikit-learn cython matplotlib=2.2.4 seaborn pillow -c pytorch -c conda-forge

cat requirements.txt

pyquaternion
torchvision==0.1.8
progress==1.4
trimesh==2.38.42
backports.functools_lru_cache
sympy


python -m pip install -r requirements.txt


edit the setup.py to make the torch version match (from 0.4.1 -> 0.4.1.post2 )


python -m pip install --user -e .

python -c "from mayavi import mlab"

```
