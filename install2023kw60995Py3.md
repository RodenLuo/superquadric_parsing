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
