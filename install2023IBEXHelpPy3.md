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
$ python -c "from mayavi import mlab"
$ 
```

Testing `superquadric_parsing` fails, it first says `No module named 'shapely'`. After `mamba install shapely`, it says the following. 

```bash
$ cd scripts
$ git checkout port_py3
$ ./forward_pass.py ../demo/03001627/ /tmp/ --model_tag "dac4af24e2facd7d3000ca4b04fcd6ac" --n_primitives 18 --weight_file ../config/chair_T26AK2FES_model_699 --train_with_bernoulli --use_deformations --use_sq --dataset_type shapenet_v2

Running code on  cpu
Found 1 'ShapeNetV2' models
1.models in total ...
Traceback (most recent call last):
  File "./forward_pass.py", line 272, in <module>
    main(sys.argv[1:])
  File "./forward_pass.py", line 148, in main
    torch.load(args.weight_file, map_location=device)
  File "/home/luod/proteinSimplify/ibexHelpPy3/env/lib/python3.7/site-packages/torch/nn/modules/module.py", line 719, in load_state_dict
    self.__class__.__name__, "\n\t".join(error_msgs)))
RuntimeError: Error(s) in loading state_dict for TulsianiNetwork:
	Missing key(s) in state_dict: "_primitive_layer.layer0._translation_layer.weight", "_primitive_layer.layer0._translation_layer.bias", "_primitive_layer.layer1._rotation_layer.weight", "_primitive_layer.layer1._rotation_layer.bias", "_primitive_layer.layer2._size_layer.weight", "_primitive_layer.layer2._size_layer.bias", "_primitive_layer.layer3._probability_layer.weight", "_primitive_layer.layer3._probability_layer.bias", "_primitive_layer.layer5._tapering_layer.weight", "_primitive_layer.layer5._tapering_layer.bias".
	Unexpected key(s) in state_dict: "_primitive_layer.layer0._size_layer.weight", "_primitive_layer.layer0._size_layer.bias", "_primitive_layer.layer1._translation_layer.weight", "_primitive_layer.layer1._translation_layer.bias", "_primitive_layer.layer2._rotation_layer.weight", "_primitive_layer.layer2._rotation_layer.bias", "_primitive_layer.layer3._tapering_layer.weight", "_primitive_layer.layer3._tapering_layer.bias", "_primitive_layer.layer5._probability_layer.weight", "_primitive_layer.layer5._probability_layer.bias".
```

It is the same error as mentioned in this issue https://github.com/paschalidoud/superquadric_parsing/issues/6#issuecomment-711792505. But no solution was mentioned. 

