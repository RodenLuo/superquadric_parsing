```bash
git clone https://github.com/paschalidoud/superquadric_parsing.git
export ENV_PREFIX=$PWD/env
mamba create -p $ENV_PREFIX 
conda activate $ENV_PREFIX
mamba install pytorch=0.4.1 cuda90 mayavi traitsui==6.1.1 pyface=6.1.0 scikit-learn cython matplotlib seaborn pillow -c pytorch -c conda-forge
```

Edit the `requirements.txt` file, reduced it to a few libraries that have not been installed 


```bash
$ cat requirements.txt
pyquaternion
torchvision==0.1.8
progress==1.4
trimesh==2.38.42
backports.functools_lru_cache
sympy
```

Edit the `setup.py` to make the torch version match (from 0.4.1 -> 0.4.1.post2 )

```bash
58         "torch==0.4.1",
->
58         "torch==0.4.1.post2",
```

```bash
python -m pip install -r requirements.txt
python -m pip install --user -e .
```

Testing `mayavi` succeeds

```
python -c "from mayavi import mlab"
```


