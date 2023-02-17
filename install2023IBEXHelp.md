```bash
git clone https://github.com/paschalidoud/superquadric_parsing.git
export ENV_PREFIX=$PWD/env
mamba create -p $ENV_PREFIX 
conda activate $ENV_PREFIX
mamba install python=2.7 mayavi=4.5.0 traitsui==6.1.1 pyface=6.1.1 -c conda-forge
```

Testing `mayavi` fails

<details><summary>Click to open</summary>
<p>

```bash
$ python -c "from mayavi import mlab"
Traceback (most recent call last):
  File "<string>", line 1, in <module>
  File "/home/luod/proteinSimplify/ibexHelpPy2_2/env/lib/python2.7/site-packages/mayavi/mlab.py", line 27, in <module>
    from mayavi.tools.camera import view, roll, yaw, pitch, move
  File "/home/luod/proteinSimplify/ibexHelpPy2_2/env/lib/python2.7/site-packages/mayavi/tools/camera.py", line 25, in <module>
    from .engine_manager import get_engine
  File "/home/luod/proteinSimplify/ibexHelpPy2_2/env/lib/python2.7/site-packages/mayavi/tools/engine_manager.py", line 14, in <module>
    from mayavi.core.engine import Engine
  File "/home/luod/proteinSimplify/ibexHelpPy2_2/env/lib/python2.7/site-packages/mayavi/core/engine.py", line 12, in <module>
    import vtk
  File "/home/luod/proteinSimplify/ibexHelpPy2_2/env/lib/python2.7/site-packages/vtk/__init__.py", line 112, in <module>
    from .vtkIOParallel import *
  File "/home/luod/proteinSimplify/ibexHelpPy2_2/env/lib/python2.7/site-packages/vtk/vtkIOParallel.py", line 9, in <module>
    from vtkIOParallelPython import *
ImportError: No module named vtkIOParallelPython
________________________________________________________________________________
Do you have vtk and its Python bindings installed properly?
```

I do have `/home/luod/proteinSimplify/ibexHelpPy2_2/env/lib/python2.7/site-packages/vtk`, so according to this [hint](https://stackoverflow.com/a/956889)
```bash
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/home/luod/proteinSimplify/ibexHelpPy2_2/env/lib/python2.7/site-packages

$ python -c "from mayavi import mlab"
Traceback (most recent call last):
  File "<string>", line 1, in <module>
  File "/home/luod/proteinSimplify/ibexHelpPy2_2/env/lib/python2.7/site-packages/mayavi/mlab.py", line 27, in <module>
    from mayavi.tools.camera import view, roll, yaw, pitch, move
  File "/home/luod/proteinSimplify/ibexHelpPy2_2/env/lib/python2.7/site-packages/mayavi/tools/camera.py", line 25, in <module>
    from .engine_manager import get_engine
  File "/home/luod/proteinSimplify/ibexHelpPy2_2/env/lib/python2.7/site-packages/mayavi/tools/engine_manager.py", line 14, in <module>
    from mayavi.core.engine import Engine
  File "/home/luod/proteinSimplify/ibexHelpPy2_2/env/lib/python2.7/site-packages/mayavi/core/engine.py", line 12, in <module>
    import vtk
  File "/home/luod/proteinSimplify/ibexHelpPy2_2/env/lib/python2.7/site-packages/vtk/__init__.py", line 112, in <module>
    from .vtkIOParallel import *
  File "/home/luod/proteinSimplify/ibexHelpPy2_2/env/lib/python2.7/site-packages/vtk/vtkIOParallel.py", line 9, in <module>
    from vtkIOParallelPython import *
ImportError: libjsoncpp.so.0: cannot open shared object file: No such file or directory
________________________________________________________________________________
Do you have vtk and its Python bindings installed properly?
```

According to [this](https://github.com/conda-forge/vtk-feedstock/issues/46#issuecomment-343494640), and [this](https://mfix.netl.doe.gov/forum/t/cannot-open-vtk-output-file/2862/31)

</p>
</details>

These two package versions solve the above error (I must have done something else that I forgot to log, the following two only, cannot solve the above error...)
```bash
mamba install jsoncpp=1.8.3 
mamba install apptools=4.5
```



```bash
mamba install pytorch=0.4.1 cuda90 scikit-learn cython matplotlib=2.2.4 seaborn pillow -c pytorch -c conda-forge
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

Testing `superquadric_parsing` succeeds!

