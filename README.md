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
    │—— MeshTGV-1.1.0.exe     [//executable file to run our algorithm]
    │—— README.md
   ```

### About data :
   There are four files in each model's folder. For example, in Block's folder :

   ```
    data                  [//comparison data used in our paper]
      │—— CAD
      │    │—— Block
      │    │    │—— _tgv_filtered_normals-aad=xxx.txt
      │    │    │—— _tgv_result_mesh.obj
      │    │    │—— block-smooth-GroundTruth.obj
      │    │    │—— block-smooth-RandomDirectionNoise0.35.obj
      │    │
      │    │—— ...
      │
      │── ...
      │── ...

   ```

   - `_tgv_filtered_normals-aad=xxx.txt` : 
   Storing the result normals after MeshTGV Normal Filtering **before** Vertex Updating. 
   "aad=xxx" in the filename means the Average Angle Deviation (θ value used in our paper) of the result normals is "xxx".

   - `_tgv_result_mesh.obj` : 
   The result mesh saved after MeshTGV Normal Filtering **and** Vertex Updating.
   
   - `block-smooth-GroundTruth.obj` : 
   The GroundTruth data of Block model.
   - `block-smooth-RandomDirectionNoise0.35.obj` : 
   The Noise data of Block model.

### Run MeshTGV Algorithm:

0. Double click the executable file : "MeshTGV-1.1.0.exe".

1. Load the Noisy Mesh:
   
   Menu -> Model -> LoadMesh -> Choose your noisy mesh

2. Load the GroundTruth Mesh:

   Menu -> Model -> Load GroundTruth Mesh -> Choose your GroundTruth mesh

3. Open MeshTGV algorithm panel:

   Menu -> Denoising -> MeshTGV

4. Set parameters then Click Run button

5. Output: 
   
   - *Visualization output* : showed in the mainwindow.
   - *Quantitative Evaluation output* : showed in the console.
   - *Norm result output* : automaticlly saved in the same folder with the input Noisy Mesh.
   - *Mesh result output* : You need to save the Mesh result manually :
   Menu -> Model -> Save


### About Parameters:

   Coming soon ...