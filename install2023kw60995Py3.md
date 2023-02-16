```
(superquadric_parsingPy3) luod@kw60995:~/proteinSimplify/official_py3/superquadric_parsing$ pip install --user -e .
Obtaining file:///home/luod/proteinSimplify/official_py3/superquadric_parsing
  Preparing metadata (setup.py) ... error
  error: subprocess-exited-with-error

  × python setup.py egg_info did not run successfully.
  │ exit code: 1
  ╰─> [6 lines of output]
      Traceback (most recent call last):
        File "<string>", line 2, in <module>
        File "<pip-setuptools-caller>", line 34, in <module>
        File "/home/luod/proteinSimplify/official_py3/superquadric_parsing/setup.py", line 4, in <module>
          from Cython.Build import cythonize
      ModuleNotFoundError: No module named 'Cython'
      [end of output]

  note: This error originates from a subprocess, and is likely not a problem with pip.
error: metadata-generation-failed

× Encountered error while generating package metadata.
╰─> See above for output.

note: This is an issue with the package mentioned above, not pip.
hint: See above for details.
(superquadric_parsingPy3) luod@kw60995:~/proteinSimplify/official_py3/superquadric_parsing$ pip install -r requirements.txt
ERROR: Could not find a version that satisfies the requirement torch==0.4.1 (from versions: 1.11.0, 1.12.0, 1.12.1, 1.13.0, 1.13.1)
ERROR: No matching distribution found for torch==0.4.1


```

comment out `torch` in `requirements.txt` gets `Downloading torch-1.13.1`

Failed to build mayavi

```
Collecting torchvision==0.1.8
  Using cached torchvision-0.1.8-py2.py3-none-any.whl (37 kB)
Collecting progress==1.4
  Using cached progress-1.4.tar.gz (5.4 kB)
  Preparing metadata (setup.py) ... done
Collecting trimesh==2.38.42
  Using cached trimesh-2.38.42.tar.gz (328 kB)
  Preparing metadata (setup.py) ... done
Requirement already satisfied: numpy in /home/luod/.local/lib/python3.10/site-packages (from -r requirements.txt (line 6)) (1.23.2)
Requirement already satisfied: scikit-learn in /home/luod/.local/lib/python3.10/site-packages (from -r requirements.txt (line 7)) (1.1.2)
Collecting Cython
  Downloading Cython-0.29.33-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.manylinux_2_24_x86_64.whl (1.9 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.9/1.9 MB 4.6 MB/s eta 0:00:00
Requirement already satisfied: Pillow in /home/luod/.local/lib/python3.10/site-packages (from -r requirements.txt (line 9)) (9.2.0)
Collecting pyquaternion
  Downloading pyquaternion-0.9.9-py3-none-any.whl (14 kB)
Collecting backports.functools_lru_cache
  Using cached backports.functools_lru_cache-1.6.4-py2.py3-none-any.whl (5.9 kB)
Collecting sympy
  Downloading sympy-1.11.1-py3-none-any.whl (6.5 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 6.5/6.5 MB 34.2 MB/s eta 0:00:00
Requirement already satisfied: matplotlib in /home/luod/.local/lib/python3.10/site-packages (from -r requirements.txt (line 15)) (3.5.3)
Collecting seaborn
  Downloading seaborn-0.12.2-py3-none-any.whl (293 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 293.3/293.3 kB 54.3 MB/s eta 0:00:00
Collecting mayavi
  Downloading mayavi-4.8.1.tar.gz (20.6 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 20.6/20.6 MB 30.3 MB/s eta 0:00:00
  Installing build dependencies ... done
  Getting requirements to build wheel ... done
  Preparing metadata (pyproject.toml) ... done
Collecting torch
  Downloading torch-1.13.1-cp310-cp310-manylinux1_x86_64.whl (887.5 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 887.5/887.5 MB 1.6 MB/s eta 0:00:00
Requirement already satisfied: six in /home/luod/.local/lib/python3.10/site-packages (from torchvision==0.1.8->-r requirements.txt (line 2)) (1.16.0)
Requirement already satisfied: scipy in /home/luod/.local/lib/python3.10/site-packages (from trimesh==2.38.42->-r requirements.txt (line 4)) (1.9.0)
Collecting networkx
  Downloading networkx-3.0-py3-none-any.whl (2.0 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 2.0/2.0 MB 1.8 MB/s eta 0:00:00
Requirement already satisfied: threadpoolctl>=2.0.0 in /home/luod/.local/lib/python3.10/site-packages (from scikit-learn->-r requirements.txt (line 7)) (3.1.0)
Requirement already satisfied: joblib>=1.0.0 in /home/luod/.local/lib/python3.10/site-packages (from scikit-learn->-r requirements.txt (line 7)) (1.1.0)
Collecting mpmath>=0.19
  Downloading mpmath-1.2.1-py3-none-any.whl (532 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 532.6/532.6 kB 1.9 MB/s eta 0:00:00
Requirement already satisfied: kiwisolver>=1.0.1 in /home/luod/.local/lib/python3.10/site-packages (from matplotlib->-r requirements.txt (line 15)) (1.4.4)
Requirement already satisfied: cycler>=0.10 in /home/luod/.local/lib/python3.10/site-packages (from matplotlib->-r requirements.txt (line 15)) (0.11.0)
Requirement already satisfied: packaging>=20.0 in /home/luod/.local/lib/python3.10/site-packages (from matplotlib->-r requirements.txt (line 15)) (21.3)
Requirement already satisfied: pyparsing>=2.2.1 in /home/luod/.local/lib/python3.10/site-packages (from matplotlib->-r requirements.txt (line 15)) (3.0.9)
Requirement already satisfied: python-dateutil>=2.7 in /home/luod/.local/lib/python3.10/site-packages (from matplotlib->-r requirements.txt (line 15)) (2.8.2)
Requirement already satisfied: fonttools>=4.22.0 in /home/luod/.local/lib/python3.10/site-packages (from matplotlib->-r requirements.txt (line 15)) (4.36.0)
Collecting pandas>=0.25
  Downloading pandas-1.5.3-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (12.1 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 12.1/12.1 MB 2.3 MB/s eta 0:00:00
Collecting pygments
  Downloading Pygments-2.14.0-py3-none-any.whl (1.1 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.1/1.1 MB 2.8 MB/s eta 0:00:00
Collecting traits>=6.0.0
  Downloading traits-6.4.1-cp310-cp310-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (5.1 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 5.1/5.1 MB 3.4 MB/s eta 0:00:00
Collecting envisage
  Downloading envisage-6.1.1-py3-none-any.whl (281 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 281.9/281.9 kB 4.8 MB/s eta 0:00:00
Collecting vtk
  Using cached vtk-9.2.6-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (79.3 MB)
Collecting traitsui>=7.0.0
  Downloading traitsui-7.4.3-py3-none-any.whl (1.5 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.5/1.5 MB 4.4 MB/s eta 0:00:00
Collecting pyface>=6.1.1
  Downloading pyface-7.4.4-py3-none-any.whl (1.3 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.3/1.3 MB 4.8 MB/s eta 0:00:00
Collecting apptools
  Downloading apptools-5.2.0-py3-none-any.whl (229 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 229.2/229.2 kB 5.6 MB/s eta 0:00:00
Collecting pytz>=2020.1
  Using cached pytz-2022.7.1-py2.py3-none-any.whl (499 kB)
Collecting configobj
  Downloading configobj-5.0.8-py2.py3-none-any.whl (36 kB)
Requirement already satisfied: setuptools in /home/luod/.conda/envs/superquadric_parsingPy3/lib/python3.10/site-packages (from envisage->mayavi->-r requirements.txt (line 17)) (65.6.3)
Collecting nvidia-cudnn-cu11==8.5.0.96
  Downloading nvidia_cudnn_cu11-8.5.0.96-2-py3-none-manylinux1_x86_64.whl (557.1 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 557.1/557.1 MB 4.0 MB/s eta 0:00:00
Collecting typing-extensions
  Downloading typing_extensions-4.5.0-py3-none-any.whl (27 kB)
Collecting nvidia-cublas-cu11==11.10.3.66
  Downloading nvidia_cublas_cu11-11.10.3.66-py3-none-manylinux1_x86_64.whl (317.1 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 317.1/317.1 MB 2.7 MB/s eta 0:00:00
Collecting nvidia-cuda-runtime-cu11==11.7.99
  Downloading nvidia_cuda_runtime_cu11-11.7.99-py3-none-manylinux1_x86_64.whl (849 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 849.3/849.3 kB 3.7 MB/s eta 0:00:00
Collecting nvidia-cuda-nvrtc-cu11==11.7.99
  Downloading nvidia_cuda_nvrtc_cu11-11.7.99-2-py3-none-manylinux1_x86_64.whl (21.0 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 21.0/21.0 MB 3.2 MB/s eta 0:00:00
Requirement already satisfied: wheel in /home/luod/.conda/envs/superquadric_parsingPy3/lib/python3.10/site-packages (from nvidia-cublas-cu11==11.10.3.66->torch->torchvision==0.1.8->-r requirements.txt (line 2)) (0.37.1)
WARNING: The candidate selected for download or install is a yanked version: 'torchvision' candidate (version 0.1.8 at https://files.pythonhosted.org/packages/8c/52/33d739bcc547f22c522def535a8da7e6e5a0f6b98594717f519b5cb1a4e1/torchvision-0.1.8-py2.py3-none-any.whl (from https://pypi.org/simple/torchvision/))
Reason for being yanked: So that users won't accidentally install this when using python 3.11
Building wheels for collected packages: progress, trimesh, mayavi
  Building wheel for progress (setup.py) ... done
  Created wheel for progress: filename=progress-1.4-py3-none-any.whl size=8828 sha256=13c1f64d93d6586db8101907a80551396535f8d90582b2edc812bece28d7050a
  Stored in directory: /home/luod/.cache/pip/wheels/48/8e/ee/ce019b7c5e132f659e9c1a1d290ea4cfd9d10547509de8cb9f
  Building wheel for trimesh (setup.py) ... done
  Created wheel for trimesh: filename=trimesh-2.38.42-py3-none-any.whl size=377862 sha256=5e125dc1c1115b5112c8828e64d1e0332cbf2c13c055ef190be5289ee58417e1
  Stored in directory: /home/luod/.cache/pip/wheels/63/c5/7c/243a9e098d32f342722f0eb9b70019af918515033abaafcf7b
  Building wheel for mayavi (pyproject.toml) ... error
  error: subprocess-exited-with-error

  × Building wheel for mayavi (pyproject.toml) did not run successfully.
  │ exit code: -11
  ╰─> [39 lines of output]
      running bdist_wheel
      running build
      Building tvtk_classes.zip
      ----------------------------------------------------------------------
      Deleting possibly old TVTK classes
      Building TVTK classes... Fatal Python error: Segmentation fault

      Current thread 0x000014eac89d6200 (most recent call first):
        File "/tmp/pip-install-o62y0ki1/mayavi_7b9542bc25774f8bb6fb2703d058e03b/tvtk/vtk_parser.py", line 711 in _find_get_set_methods
        File "/tmp/pip-install-o62y0ki1/mayavi_7b9542bc25774f8bb6fb2703d058e03b/tvtk/vtk_parser.py", line 491 in _organize_methods
        File "/tmp/pip-install-o62y0ki1/mayavi_7b9542bc25774f8bb6fb2703d058e03b/tvtk/vtk_parser.py", line 157 in parse
        File "/tmp/pip-install-o62y0ki1/mayavi_7b9542bc25774f8bb6fb2703d058e03b/tvtk/wrapper_gen.py", line 341 in _gen_methods
        File "/tmp/pip-install-o62y0ki1/mayavi_7b9542bc25774f8bb6fb2703d058e03b/tvtk/wrapper_gen.py", line 242 in generate_code
        File "/tmp/pip-install-o62y0ki1/mayavi_7b9542bc25774f8bb6fb2703d058e03b/tvtk/code_gen.py", line 235 in _write_wrapper_class
        File "/tmp/pip-install-o62y0ki1/mayavi_7b9542bc25774f8bb6fb2703d058e03b/tvtk/code_gen.py", line 142 in generate_code
        File "/tmp/pip-install-o62y0ki1/mayavi_7b9542bc25774f8bb6fb2703d058e03b/tvtk/setup.py", line 98 in gen_tvtk_classes_zip
        File "<string>", line 273 in build_tvtk_classes_zip
        File "<string>", line 287 in run
        File "/tmp/pip-build-env-94v50hn3/overlay/lib/python3.10/site-packages/setuptools/_distutils/dist.py", line 988 in run_command
        File "/tmp/pip-build-env-94v50hn3/overlay/lib/python3.10/site-packages/setuptools/dist.py", line 1221 in run_command
        File "/tmp/pip-build-env-94v50hn3/overlay/lib/python3.10/site-packages/setuptools/_distutils/cmd.py", line 318 in run_command
        File "/tmp/pip-build-env-94v50hn3/overlay/lib/python3.10/site-packages/wheel/bdist_wheel.py", line 325 in run
        File "/tmp/pip-build-env-94v50hn3/overlay/lib/python3.10/site-packages/setuptools/_distutils/dist.py", line 988 in run_command
        File "/tmp/pip-build-env-94v50hn3/overlay/lib/python3.10/site-packages/setuptools/dist.py", line 1221 in run_command
        File "/tmp/pip-build-env-94v50hn3/overlay/lib/python3.10/site-packages/setuptools/_distutils/dist.py", line 969 in run_commands
        File "/tmp/pip-build-env-94v50hn3/overlay/lib/python3.10/site-packages/setuptools/_distutils/core.py", line 201 in run_commands
        File "/tmp/pip-build-env-94v50hn3/overlay/lib/python3.10/site-packages/setuptools/_distutils/core.py", line 185 in setup
        File "/tmp/pip-build-env-94v50hn3/overlay/lib/python3.10/site-packages/setuptools/__init__.py", line 108 in setup
        File "/tmp/pip-build-env-94v50hn3/overlay/lib/python3.10/site-packages/numpy/distutils/core.py", line 169 in setup
        File "<string>", line 432 in <module>
        File "/tmp/pip-build-env-94v50hn3/overlay/lib/python3.10/site-packages/setuptools/build_meta.py", line 335 in run_setup
        File "/tmp/pip-build-env-94v50hn3/overlay/lib/python3.10/site-packages/setuptools/build_meta.py", line 484 in run_setup
        File "/tmp/pip-build-env-94v50hn3/overlay/lib/python3.10/site-packages/setuptools/build_meta.py", line 398 in _build_with_temp_dir
        File "/tmp/pip-build-env-94v50hn3/overlay/lib/python3.10/site-packages/setuptools/build_meta.py", line 413 in build_wheel
        File "/home/luod/.conda/envs/superquadric_parsingPy3/lib/python3.10/site-packages/pip/_vendor/pep517/in_process/_in_process.py", line 249 in build_wheel
        File "/home/luod/.conda/envs/superquadric_parsingPy3/lib/python3.10/site-packages/pip/_vendor/pep517/in_process/_in_process.py", line 333 in main
        File "/home/luod/.conda/envs/superquadric_parsingPy3/lib/python3.10/site-packages/pip/_vendor/pep517/in_process/_in_process.py", line 351 in <module>

      Extension modules: numpy.core._multiarray_umath, numpy.core._multiarray_tests, numpy.linalg.lapack_lite, numpy.linalg._umath_linalg, numpy.fft._pocketfft_internal, numpy.random._common, numpy.random.bit_generator, numpy.random._bounded_integers, numpy.random._mt19937, numpy.random.mtrand, numpy.random._philox, numpy.random._pcg64, numpy.random._sfc64, numpy.random._generator, vtkmodules.vtkCommonCore, vtkmodules.vtkWebCore, vtkmodules.vtkCommonMath, vtkmodules.vtkCommonTransforms, vtkmodules.vtkCommonDataModel, vtkmodules.vtkCommonExecutionModel, vtkmodules.vtkIOCore, vtkmodules.vtkImagingCore, vtkmodules.vtkIOImage, vtkmodules.vtkIOXMLParser, vtkmodules.vtkIOXML, vtkmodules.vtkCommonMisc, vtkmodules.vtkFiltersCore, vtkmodules.vtkRenderingCore, vtkmodules.vtkRenderingContext2D, vtkmodules.vtkRenderingFreeType, vtkmodules.vtkRenderingSceneGraph, vtkmodules.vtkRenderingVtkJS, vtkmodules.vtkIOExport, vtkmodules.vtkWebGLExporter, vtkmodules.vtkInteractionStyle, vtkmodules.vtkFiltersGeneral, vtkmodules.vtkFiltersSources, vtkmodules.vtkInteractionWidgets, vtkmodules.vtkViewsCore, vtkmodules.vtkViewsInfovis, vtkmodules.vtkCommonComputationalGeometry, vtkmodules.vtkCommonSystem, vtkmodules.vtkIOLegacy, vtkmodules.vtkDomainsChemistry, vtkmodules.vtkRenderingHyperTreeGrid, vtkmodules.vtkRenderingUI, vtkmodules.vtkRenderingOpenGL2, vtkmodules.vtkRenderingContextOpenGL2, vtkmodules.vtkRenderingVolume, vtkmodules.vtkImagingMath, vtkmodules.vtkRenderingVolumeOpenGL2, vtkmodules.vtkViewsContext2D, vtkmodules.vtkTestingRendering, vtkmodules.vtkRenderingVolumeAMR, vtkmodules.vtkPythonContext2D, vtkmodules.vtkRenderingParallel, vtkmodules.vtkRenderingVR, vtkmodules.vtkRenderingMatplotlib, vtkmodules.vtkRenderingLabel, vtkmodules.vtkRenderingLOD, vtkmodules.vtkRenderingLICOpenGL2, vtkmodules.vtkRenderingImage, vtkmodules.vtkRenderingExternal, vtkmodules.vtkIOXdmf2, vtkmodules.vtkIOVeraOut, vtkmodules.vtkIOVPIC, vtkmodules.vtkIOTecplotTable, vtkmodules.vtkIOTRUCHAS, vtkmodules.vtkIOSegY, vtkmodules.vtkIOParallelXML, vtkmodules.vtkIOLSDyna, vtkmodules.vtkIOParallelLSDyna, vtkmodules.vtkIOExodus, vtkmodules.vtkIOParallelExodus, vtkmodules.vtkIOPLY, vtkmodules.vtkIOPIO, vtkmodules.vtkIOMovie, vtkmodules.vtkIOOggTheora, vtkmodules.vtkIOOMF, vtkmodules.vtkIONetCDF, vtkmodules.vtkIOMotionFX, vtkmodules.vtkIOGeometry, vtkmodules.vtkIOParallel, vtkmodules.vtkIOMINC, vtkmodules.vtkIOInfovis, vtkmodules.vtkIOImport, vtkmodules.vtkParallelCore, vtkmodules.vtkIOIOSS, vtkmodules.vtkIOH5part, vtkmodules.vtkIOH5Rage, vtkmodules.vtkIOGeoJSON, vtkmodules.vtkIOVideo, vtkmodules.vtkIOExportPDF, vtkmodules.vtkRenderingGL2PSOpenGL2, vtkmodules.vtkIOExportGL2PS, vtkmodules.vtkIOEnSight, vtkmodules.vtkIOCityGML, vtkmodules.vtkIOChemistry, vtkmodules.vtkIOCesium3DTiles, vtkmodules.vtkIOCONVERGECFD, vtkmodules.vtkIOHDF, vtkmodules.vtkIOCGNSReader, vtkmodules.vtkIOAsynchronous, vtkmodules.vtkIOAMR, vtkmodules.vtkInteractionImage, vtkmodules.vtkImagingStencil, vtkmodules.vtkImagingStatistics, vtkmodules.vtkImagingGeneral, vtkmodules.vtkImagingOpenGL2, vtkmodules.vtkImagingMorphological, vtkmodules.vtkImagingFourier, vtkmodules.vtkIOSQL, vtkmodules.vtkCommonColor, vtkmodules.vtkImagingSources, vtkmodules.vtkInfovisCore, vtkmodules.vtkGeovisCore, vtkmodules.vtkInfovisLayout, vtkmodules.vtkRenderingAnnotation, vtkmodules.vtkImagingHybrid, vtkmodules.vtkImagingColor, vtkmodules.vtkFiltersTopology, vtkmodules.vtkFiltersSelection, vtkmodules.vtkFiltersSMP, vtkmodules.vtkFiltersPython, vtkmodules.vtkFiltersProgrammable, vtkmodules.vtkFiltersModeling, vtkmodules.vtkFiltersPoints, vtkmodules.vtkFiltersVerdict, vtkmodules.vtkFiltersStatistics, vtkmodules.vtkFiltersParallelStatistics, vtkmodules.vtkFiltersImaging, vtkmodules.vtkFiltersExtraction, vtkmodules.vtkFiltersGeometry, vtkmodules.vtkFiltersHybrid, vtkmodules.vtkFiltersTexture, vtkmodules.vtkFiltersParallel, vtkmodules.vtkFiltersParallelImaging, vtkmodules.vtkFiltersParallelDIY2, vtkmodules.vtkFiltersGeneric, vtkmodules.vtkFiltersFlowPaths, vtkmodules.vtkFiltersAMR, vtkmodules.vtkDomainsChemistryOpenGL2, vtkmodules.vtkFiltersHyperTree, vtkmodules.vtkCommonPython, vtkmodules.vtkChartsCore, vtkmodules.vtkAcceleratorsVTKmCore, vtkmodules.vtkAcceleratorsVTKmDataModel, vtkmodules.vtkAcceleratorsVTKmFilters (total: 148)
      [end of output]

  note: This error originates from a subprocess, and is likely not a problem with pip.
  ERROR: Failed building wheel for mayavi
Successfully built progress trimesh
Failed to build mayavi
ERROR: Could not build wheels for mayavi, which is required to install pyproject.toml-based projects
```


```
conda install pytorch==0.4.1 cuda90 -c pytorch

    certifi-2022.12.7          |   py37h06a4308_0         150 KB
    cffi-1.15.1                |   py37h5eee18b_3         240 KB
    cuda90-1.0                 |       h6433d27_0           3 KB  pytorch
    mkl-service-2.4.0          |   py37h7f8727e_0          56 KB
    mkl_fft-1.3.1              |   py37hd3c417c_0         172 KB
    mkl_random-1.2.2           |   py37h51133e4_0         287 KB
    ninja-1.10.2               |       h06a4308_5           8 KB
    ninja-base-1.10.2          |       hd09550d_5         109 KB
    numpy-1.21.5               |   py37h6c91a56_3          10 KB
    numpy-base-1.21.5          |   py37ha15fc14_3         4.8 MB
    pip-22.3.1                 |   py37h06a4308_0         2.7 MB
    pycparser-2.21             |     pyhd3eb1b0_0          94 KB
    python-3.7.16              |       h7a1cb2a_0        44.8 MB
    pytorch-0.4.1              |py37_py36_py35_py27__9.0.176_7.1.2_2       471.7 MB  pytorch
    setuptools-65.6.3          |   py37h06a4308_0         1.1 MB
    six-1.16.0                 |     pyhd3eb1b0_1          18 KB
    
```


