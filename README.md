# Mesh Total Generalized Variation for Denoising
 by [Zheng Liu](https://labzhengliu.github.io/), Yanlei Li, [Weina Wang](https://www.researchgate.net/profile/Weina-Wang-6), [Ligang Liu](http://staff.ustc.edu.cn/~lgliu/), and [Renjie Chen](http://staff.ustc.edu.cn/~renjiec/)(Corresponding author)


## Introduction
MeshTGV is an efficient numerical framework to discretize TGV over triangular meshes.
Based on this discretization, a vectorial TGV regularization model is proposed to restore the face normal field. Then, we introduce an efficient and effective algorithm to solve the optimization problem.


## How to Use

### Download or Clone this repository, you will get :
   
   ```
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

### About data :
   There are four files in each model's folder. For example, in Block's folder :

   ```
    data                  [//comparison data used in our paper]
      │—— CAD
      │    │—— Block
      │    │    │—— groundtruth.obj
      │    │    │—— noisy.obj
      │    │    │—— tgv_filtered_normals-aad=xxx.txt
      │    │    │—— tgv_result_mesh.obj
      │    │
      │    │—— ...
      │
      │── ...
      │── ...

   ```
   
   - `groundtruth.obj` : 
   The GroundTruth data of model.

   - `noisy.obj` : 
   The Noise data of model.

   - `tgv_filtered_normals-aad=xxx.txt` : 
   Storing the result normals after MeshTGV Normal Filtering **before** Vertex Updating. 
   "aad=xxx" in the filename means the Average Angle Deviation(θ) of the result normals is "xxx".

   - `tgv_result_mesh.obj` : 
   The result mesh saved after MeshTGV Normal Filtering **and** Vertex Updating.
   

### Run MeshTGV Algorithm:

0. Double click the executable file.

1. Load the Noisy Mesh:
   
   `Menu` &#8594; `Model` &#8594; `Load Mesh` &#8594; `Choose your noisy mesh`

2. Open MeshTGV algorithm panel:

   `Menu &#8594; Denoising &#8594; MeshTGV`

3. Set parameters then Click Run button

5. Output: 
   
   - *Visualization output* : showed in the mainwindow.
   - *Norm result output* : automaticlly saved in the same folder with the input Noisy Mesh.
   - *Mesh result output* : You need to save the Mesh result manually :
   `Menu -> Model -> Save`


### About Parameters:

   :soon: Coming soon ...