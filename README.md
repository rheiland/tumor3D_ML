# tumor3D_ML - PhysiCell model of a 3D tumor for the HuBMAP ML team

Compile the code, run the model, and visualize/analyze the output. Assumes you have an appropriate compiler/build toolchain and Python module (fury). This is a modified version of the `cancer_immune` sample project that comes bundled with PhysiCell. The `immune_activation_time` parameter in the `run3.xml` configuration file has been set artificially large so as to never invoke the immune aspect of the model, i.e., the tumor grows without being attacked by the immune cells.

```
make
cancer_immune_3D run3.xml
cd run3
```

![Z=0-slices](/images/day9-12.png)


Assuming you have an appropriate Python distribution installed, you should be able to install Fury via `pip install fury` and then see the following rendering (`python tumor_vis2.py`), where we crop out half of the tumor so we can see the necrotic core. Fury allows for dynamic viewing (rotate, scale, pan): 

![fury rendering](/images/fury_half_tumor1.png)
