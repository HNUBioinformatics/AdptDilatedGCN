AdptDilatedGCN: Protein-Ligand Binding Affinity Prediction Based on Multi-Scale Interaction Fusion Mechanism and Dilated GCN.

The data needed for training and prediction of AdptDilatedGCN and AdptDilatedGCN-Sta are available at  
https://pan.baidu.com/s/1q5_K3huRGYy-UVSkrhJyZQ?pwd=2024 to download, and the data needed for both models are the same. 
Unzip the downloaded data and place it in the data directory of our  model. 
The weights of our model are publicly available and placed in the “model” directory,  and the predicted results are placed in the “result” directory. 
If you want to get the raw data you can visit  http://www.pdbbind-cn.org/ download it yourself.

Here are the steps to repeat.

1. The download model code can be obtained through the following command or downloaded directly through “code” on github:
git clone https://github.com/HNUBioinformatics/AdptDilatedGCN.git
cd AdptDilatedGCN
cd AdptDilatedGCN-Sta

2. Run AdptDilatedGCN and AdPTdilatedGCN-sta to create related environments. We have given the script for creating the environment, 
which can be created with one click through the following commands (the name of the environment script for both models is environment_gpu.yml) :
conda env create -f environment_gpu.yml
conda activate AdptDilatedGCN

3. The commands for retraining the model are as follows:
cd ./src/
python train.py

4. Use the model to predict the following commands:
cd ./src/
python predict2013.py
python predict2016.py

In order to facilitate the effective reproduction of our model results, we debug and encapsulate the code. 
The prediction and training using pycharm only need to run the predict2013.py, predict2016.py and train.
py files with one click. The model's prediction results and training weights are saved in the result and Model directories, respectively.
