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


```bash
(superquadric_parsingPy3) luod@kw60995:~/proteinSimplify/official_py3/superquadric_parsing$ pip install https://github.com/pytorch/vision/archive/refs/tags/v0.1.8.tar.gz
Collecting https://github.com/pytorch/vision/archive/refs/tags/v0.1.8.tar.gz
  Downloading https://github.com/pytorch/vision/archive/refs/tags/v0.1.8.tar.gz
     / 252.1 kB 826.8 kB/s 0:00:00
  Preparing metadata (setup.py) ... done
Requirement already satisfied: numpy in /home/luod/.local/lib/python3.7/site-packages (from torchvision==0.1.8) (1.21.6)
Collecting pillow
  Downloading Pillow-9.4.0-cp37-cp37m-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (3.3 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 3.3/3.3 MB 6.5 MB/s eta 0:00:00
Requirement already satisfied: six in /home/luod/.conda/envs/superquadric_parsingPy3/lib/python3.7/site-packages (from torchvision==0.1.8) (1.16.0)
Requirement already satisfied: torch in /home/luod/.conda/envs/superquadric_parsingPy3/lib/python3.7/site-packages (from torchvision==0.1.8) (0.4.1.post2)
Building wheels for collected packages: torchvision
  Building wheel for torchvision (setup.py) ... done
  Created wheel for torchvision: filename=torchvision-0.1.8-py2.py3-none-any.whl size=33449 sha256=e0cc1e83b227d526ebd01a9ae99b1b222bb7a3f874995fc2dcdf368697efbba6
  Stored in directory: /tmp/pip-ephem-wheel-cache-2mlfh0lu/wheels/0d/ac/38/770c9f4ba9569390b98cb6befce237783062e020ca30f92319
Successfully built torchvision
Installing collected packages: pillow, torchvision
Successfully installed pillow-9.4.0 torchvision-0.1.8

```


```
pip install https://github.com/KieranWynn/pyquaternion/archive/refs/tags/v0.9.5.tar.gz https://github.com/mikedh/trimesh/archive/refs/tags/2.38.42.tar.gz

(superquadric_parsingPy3) luod@kw60995:~/proteinSimplify/official_py3/superquadric_parsing$ cat requirements.txt
# torch==0.4.1
# torchvision==0.1.8
progress==1.4
# trimesh==2.38.42

numpy
scikit-learn
Cython
Pillow
# pyquaternion
backports.functools_lru_cache
sympy

# Visualization
matplotlib
seaborn
mayavi

conda install --file requirements.txt

    apptools-5.1.0             |     pyhd3eb1b0_0         123 KB
    backports-1.1              |     pyhd3eb1b0_0           4 KB
    backports.functools_lru_cache-1.6.4|     pyhd3eb1b0_0           9 KB
    bottleneck-1.3.5           |   py37h7deecbd_0         115 KB
    brotli-1.0.9               |       h5eee18b_7          18 KB
    brotli-bin-1.0.9           |       h5eee18b_7          19 KB
    c-ares-1.18.1              |       h7f8727e_0         114 KB
    configobj-5.0.6            |   py37h06a4308_1         289 KB
    curl-7.87.0                |       h5eee18b_0          88 KB
    cycler-0.11.0              |     pyhd3eb1b0_0          12 KB
    cython-0.29.32             |   py37h6a678d5_0         1.9 MB
    envisage-6.0.1             |     pyhd3eb1b0_0         167 KB
    expat-2.4.9                |       h6a678d5_0         156 KB
    flit-core-3.6.0            |     pyhd3eb1b0_0          42 KB
    fontconfig-2.14.1          |       h52c9d5c_1         281 KB
    freetype-2.12.1            |       h4a9f257_0         626 KB
    future-0.18.2              |           py37_1         631 KB
    giflib-5.2.1               |       h5eee18b_1          75 KB
    glib-2.69.1                |       he621ea3_2         1.9 MB
    gmp-6.2.1                  |       h295c915_3         544 KB
    gmpy2-2.1.2                |   py37heeb90bb_0         188 KB
    hdf4-4.2.13                |       h3ca952b_2         714 KB
    hdf5-1.10.4                |       hb1b8bf9_0         3.9 MB
    joblib-1.1.1               |   py37h06a4308_0         379 KB
    jpeg-9e                    |       h7f8727e_0         240 KB
    jsoncpp-1.9.4              |       hff7bd54_2         150 KB
    kiwisolver-1.4.4           |   py37h6a678d5_0          74 KB
    krb5-1.19.4                |       h568e23c_0         1.3 MB
    libbrotlicommon-1.0.9      |       h5eee18b_7          70 KB
    libbrotlidec-1.0.9         |       h5eee18b_7          31 KB
    libbrotlienc-1.0.9         |       h5eee18b_7         264 KB
    libcurl-7.87.0             |       h91b91d3_0         373 KB
    libedit-3.1.20221030       |       h5eee18b_0         181 KB
    libev-4.33                 |       h7f8727e_1         111 KB
    libnetcdf-4.6.1            |       h11d0813_2         833 KB
    libnghttp2-1.46.0          |       hce63b2e_0         680 KB
    libogg-1.3.5               |       h27cfd23_1         199 KB
    libssh2-1.10.0             |       h8f2d780_0         274 KB
    libtheora-1.1.1            |       h7f8727e_3         338 KB
    libtiff-4.1.0              |       h2733197_0         447 KB
    libvorbis-1.3.7            |       h7b6447c_0         398 KB
    libwebp-1.2.4              |       h11a3e52_0          79 KB
    libwebp-base-1.2.4         |       h5eee18b_0         347 KB
    libxcb-1.15                |       h7f8727e_0         505 KB
    libxml2-2.9.14             |       h74e7548_0         718 KB
    lz4-c-1.8.1.2              |       h14c3975_0         130 KB
    matplotlib-3.5.3           |   py37h06a4308_0           7 KB
    matplotlib-base-3.5.3      |   py37hf590b9c_0         6.4 MB
    mayavi-4.7.1               |   py37h94891b3_2        12.6 MB
    mpc-1.1.0                  |       h10f8cd9_1          90 KB
    mpfr-4.0.2                 |       hb69a4c5_1         487 KB
    mpmath-1.2.1               |   py37h06a4308_0         775 KB
    numexpr-2.8.4              |   py37he184ba9_0         133 KB
    packaging-22.0             |   py37h06a4308_0          68 KB
    pandas-1.3.5               |   py37h8c16a72_0         9.3 MB
    pillow-9.3.0               |   py37hace64e9_1         719 KB
    progress-1.4               |           py37_0          13 KB
    pyface-7.3.0               |   py37h06a4308_1         1.1 MB
    pygments-2.11.2            |     pyhd3eb1b0_0         759 KB
    pyparsing-3.0.9            |   py37h06a4308_0         150 KB
    pyqt-5.9.2                 |   py37h05f1152_2         4.5 MB
    pytz-2022.7                |   py37h06a4308_0         207 KB
    scikit-learn-1.0.2         |   py37h51133e4_1         5.5 MB
    scipy-1.7.3                |   py37hc147768_0        16.4 MB
    seaborn-0.12.2             |   py37h06a4308_0         488 KB
    sip-4.19.8                 |   py37hf484d3e_0         274 KB
    sympy-1.10.1               |   py37h06a4308_0         9.3 MB
    tbb-2021.6.0               |       hdb19cb5_1         1.6 MB
    threadpoolctl-2.2.0        |     pyh0d69192_0          16 KB
    tornado-6.2                |   py37h5eee18b_0         584 KB
    traits-6.2.0               |   py37h27cfd23_0         4.9 MB
    traitsui-7.2.1             |     pyhd3eb1b0_0         854 KB
    typing_extensions-4.4.0    |   py37h06a4308_0          45 KB
    vtk-8.2.0                  | py37haa4764d_200        28.4 MB
    zstd-1.3.7                 |       h0b5b093_0         401 KB
    
```


```bash
(superquadric_parsingPy3) luod@kw60995:~/proteinSimplify/official_py3/superquadric_parsing$ conda list
# packages in environment at /home/luod/.conda/envs/superquadric_parsingPy3:
#
# Name                    Version                   Build  Channel
_libgcc_mutex             0.1                        main
_openmp_mutex             5.1                       1_gnu
apptools                  5.1.0              pyhd3eb1b0_0
backports                 1.1                pyhd3eb1b0_0
backports.functools_lru_cache 1.6.4              pyhd3eb1b0_0
blas                      1.0                         mkl
bottleneck                1.3.5            py37h7deecbd_0
brotli                    1.0.9                h5eee18b_7
brotli-bin                1.0.9                h5eee18b_7
bzip2                     1.0.8                h7b6447c_0
c-ares                    1.18.1               h7f8727e_0
ca-certificates           2023.01.10           h06a4308_0
certifi                   2022.12.7        py37h06a4308_0
cffi                      1.15.1           py37h5eee18b_3
configobj                 5.0.6            py37h06a4308_1
cuda90                    1.0                  h6433d27_0    pytorch
curl                      7.87.0               h5eee18b_0
cycler                    0.11.0             pyhd3eb1b0_0
cython                    0.29.32          py37h6a678d5_0
dbus                      1.13.18              hb2f20db_0
envisage                  6.0.1              pyhd3eb1b0_0
expat                     2.4.9                h6a678d5_0
flit-core                 3.6.0              pyhd3eb1b0_0
fontconfig                2.14.1               h52c9d5c_1
fonttools                 4.25.0             pyhd3eb1b0_0
freetype                  2.12.1               h4a9f257_0
future                    0.18.2                   py37_1
giflib                    5.2.1                h5eee18b_1
glib                      2.69.1               he621ea3_2
gmp                       6.2.1                h295c915_3
gmpy2                     2.1.2            py37heeb90bb_0
gst-plugins-base          1.14.0               h8213a91_2
gstreamer                 1.14.0               h28cd5cc_2
hdf4                      4.2.13               h3ca952b_2
hdf5                      1.10.4               hb1b8bf9_0
icu                       58.2                 he6710b0_3
intel-openmp              2021.4.0          h06a4308_3561
joblib                    1.1.1            py37h06a4308_0
jpeg                      9e                   h7f8727e_0
jsoncpp                   1.9.4                hff7bd54_2
kiwisolver                1.4.4            py37h6a678d5_0
krb5                      1.19.4               h568e23c_0
lcms2                     2.12                 h3be6417_0
ld_impl_linux-64          2.38                 h1181459_1
libbrotlicommon           1.0.9                h5eee18b_7
libbrotlidec              1.0.9                h5eee18b_7
libbrotlienc              1.0.9                h5eee18b_7
libcurl                   7.87.0               h91b91d3_0
libedit                   3.1.20221030         h5eee18b_0
libev                     4.33                 h7f8727e_1
libffi                    3.4.2                h6a678d5_6
libgcc-ng                 11.2.0               h1234567_1
libgfortran-ng            7.5.0               ha8ba4b0_17
libgfortran4              7.5.0               ha8ba4b0_17
libgomp                   11.2.0               h1234567_1
libnetcdf                 4.6.1                h11d0813_2
libnghttp2                1.46.0               hce63b2e_0
libogg                    1.3.5                h27cfd23_1
libpng                    1.6.37               hbc83047_0
libssh2                   1.10.0               h8f2d780_0
libstdcxx-ng              11.2.0               h1234567_1
libtheora                 1.1.1                h7f8727e_3
libtiff                   4.1.0                h2733197_0
libuuid                   1.41.5               h5eee18b_0
libvorbis                 1.3.7                h7b6447c_0
libwebp                   1.2.4                h11a3e52_0
libwebp-base              1.2.4                h5eee18b_0
libxcb                    1.15                 h7f8727e_0
libxml2                   2.9.14               h74e7548_0
lz4-c                     1.8.1.2              h14c3975_0
matplotlib                3.5.3            py37h06a4308_0
matplotlib-base           3.5.3            py37hf590b9c_0
mayavi                    4.7.1            py37h94891b3_2
mkl                       2021.4.0           h06a4308_640
mkl-service               2.4.0            py37h7f8727e_0
mkl_fft                   1.3.1            py37hd3c417c_0
mkl_random                1.2.2            py37h51133e4_0
mpc                       1.1.0                h10f8cd9_1
mpfr                      4.0.2                hb69a4c5_1
mpmath                    1.2.1            py37h06a4308_0
munkres                   1.1.4                      py_0
ncurses                   6.4                  h6a678d5_0
networkx                  2.6.3                    pypi_0    pypi
ninja                     1.10.2               h06a4308_5
ninja-base                1.10.2               hd09550d_5
numexpr                   2.8.4            py37he184ba9_0
numpy                     1.21.5           py37h6c91a56_3
numpy-base                1.21.5           py37ha15fc14_3
openssl                   1.1.1t               h7f8727e_0
packaging                 22.0             py37h06a4308_0
pandas                    1.3.5            py37h8c16a72_0
pcre                      8.45                 h295c915_0
pillow                    9.4.0                    pypi_0    pypi
pip                       22.3.1           py37h06a4308_0
progress                  1.4                      py37_0
pycparser                 2.21               pyhd3eb1b0_0
pyface                    7.3.0            py37h06a4308_1
pygments                  2.11.2             pyhd3eb1b0_0
pyparsing                 3.0.9            py37h06a4308_0
pyqt                      5.9.2            py37h05f1152_2
pyquaternion              0.9.5                    pypi_0    pypi
python                    3.7.16               h7a1cb2a_0
python-dateutil           2.8.2              pyhd3eb1b0_0
pytorch                   0.4.1           py37_py36_py35_py27__9.0.176_7.1.2_2    pytorch
pytz                      2022.7           py37h06a4308_0
qt                        5.9.7                h5867ecd_1
readline                  8.2                  h5eee18b_0
scikit-learn              1.0.2            py37h51133e4_1
scipy                     1.7.3            py37hc147768_0
seaborn                   0.12.2           py37h06a4308_0
setuptools                65.6.3           py37h06a4308_0
sip                       4.19.8           py37hf484d3e_0
six                       1.16.0             pyhd3eb1b0_1
sqlite                    3.40.1               h5082296_0
sympy                     1.10.1           py37h06a4308_0
tbb                       2021.6.0             hdb19cb5_1
threadpoolctl             2.2.0              pyh0d69192_0
tk                        8.6.12               h1ccaba5_0
torchvision               0.1.8                    pypi_0    pypi
tornado                   6.2              py37h5eee18b_0
traits                    6.2.0            py37h27cfd23_0
traitsui                  7.2.1              pyhd3eb1b0_0
trimesh                   2.38.42                  pypi_0    pypi
typing_extensions         4.4.0            py37h06a4308_0
tzdata                    2022g                h04d1e81_0
vtk                       8.2.0           py37haa4764d_200
wheel                     0.37.1             pyhd3eb1b0_0
xz                        5.2.10               h5eee18b_1
zlib                      1.2.13               h5eee18b_0
zstd                      1.3.7                h0b5b093_0
(superquadric_parsingPy3) luod@kw60995:~/proteinSimplify/official_py3/superquadric_parsing$
(superquadric_parsingPy3) luod@kw60995:~/proteinSimplify/official_py3/superquadric_parsing$
(superquadric_parsingPy3) luod@kw60995:~/proteinSimplify/official_py3/superquadric_parsing$
(superquadric_parsingPy3) luod@kw60995:~/proteinSimplify/official_py3/superquadric_parsing$ pip install --user -e .
Obtaining file:///home/luod/proteinSimplify/official_py3/superquadric_parsing
  Preparing metadata (setup.py) ... done
Requirement already satisfied: numpy in /home/luod/.local/lib/python3.7/site-packages (from learnable-primitives==0.1) (1.21.6)
Requirement already satisfied: scikit-learn in /home/luod/.conda/envs/superquadric_parsingPy3/lib/python3.7/site-packages (from learnable-primitives==0.1) (1.0.2)
Requirement already satisfied: trimesh==2.38.42 in /home/luod/.conda/envs/superquadric_parsingPy3/lib/python3.7/site-packages (from learnable-primitives==0.1) (2.38.42)
ERROR: Could not find a version that satisfies the requirement torch==0.4.1 (from learnable-primitives) (from versions: 1.0.0, 1.0.1, 1.0.1.post2, 1.1.0, 1.2.0, 1.3.0, 1.3.1, 1.4.0, 1.5.0, 1.5.1, 1.6.0, 1.7.0, 1.7.1, 1.8.0, 1.8.1, 1.9.0, 1.9.1, 1.10.0, 1.10.1, 1.10.2, 1.11.0, 1.12.0, 1.12.1, 1.13.0, 1.13.1)
ERROR: No matching distribution found for torch==0.4.1
```
