# Mesh Total Generalized Variation for Denoising [[paper](https://ieeexplore.ieee.org/document/9453151)]

<p align='center'>
<img src='images/figure1.png' width='850'/>
</p>

<!-- ![figure 1. Comparison of denoising result](images/figure1.png) -->

 by [Zheng Liu](https://labzhengliu.github.io/), Yanlei Li, [Weina Wang](https://www.researchgate.net/profile/Weina-Wang-6), [Ligang Liu](http://staff.ustc.edu.cn/~lgliu/), and [Renjie Chen](http://staff.ustc.edu.cn/~renjiec/)(Corresponding author)

## :bulb: Introduction
MeshTGV is an efficient numerical framework to discretize TGV over triangular meshes.
Based on this discretization, a vectorial TGV regularization model is proposed to restore the face normal field. Then, we introduce an efficient and effective algorithm to solve the optimization problem.

<p align='center'>
<img src='images/figure2.png' width='850'/>
</p>

## :wrench: Usage

### clone this repository, you will get :
   
   ```c++
   MeshTGV
    │
    │── data                  [//comparison data used in our paper]
    │     │—— CAD
    │     │── Kinect
    │     │── NonCAD
    │
    │—— MeshTGV-1.2.0.exe     [//executable file to run our algorithm]
    │—— README.md
   ```

### run MeshTGV:

1. **double click the executable file.**

2. **load a mesh file (.obj):**
   
   `Menu` &#8594; `Model` &#8594; `Load Mesh` &#8594; `Choose your noisy mesh`

3. **open the MeshTGV algorithm panel:**

   `Menu` &#8594; `Denoising` &#8594; `MeshTGV`

4. **set parameters then click the `Run` button.**

5. **get output:**

   - *Visualization output* : showed in the mainwindow.
   - *Norm result output* : automaticlly saved in the same folder with the input Noisy Mesh.
   - *Mesh result output* : You need to save the Mesh result manually :
   `Menu` &#8594; `Model` &#8594; `Save`

### about data :
   There are four files in each model's folder. For example, in Block's folder :

   ```c++
    data                  [//comparison data used in our paper]
      │—— CAD
      │    │—— Block
      │    │    │—— groundtruth.obj
      │    │    │—— noisy.obj
      │    │    │—— tgv_filtered_normals-aad=xxx.txt
      │    │    │—— tgv_result_mesh.obj
      │    │—— ...
      │
      │── Kinect
      │── NonCAD
   ```
   
   - `groundtruth.obj` : 
   The GroundTruth data of model.

   - `noisy.obj` : 
   The Noise data of model.

   - `tgv_filtered_normals-aad=xxx.txt` : 
   The result normals saved **after** MeshTGV Normal Filtering **but before** Vertex Updating. 
   "aad=xxx" in the filename means the Average Angle Deviation(θ) of the result normals is "xxx".

   - `tgv_result_mesh.obj` : 
   The result mesh saved **after** MeshTGV Normal Filtering **and** Vertex Updating.
   
### about parameters:
   Please see Section ```6.1 Parameters Setting``` in our [paper](https://ieeexplore.ieee.org/document/9453151) for more details of parameters.

## :link: Citation
If you find this work helpful please consider citing it:
```
@article{Liu2021MeshTGV,
  title={Mesh Total Generalized Variation for Denoising},
  author={Liu, Zheng and Li, Yanlei and Wang, Weina and Liu, Ligang and Chen, Renjie},
  journal={IEEE Transactions on Visualization and Computer Graphics},
  year={2021},
  doi={10.1109/TVCG.2021.3088118},
}
```