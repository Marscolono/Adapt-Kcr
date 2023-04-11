# Adapt-Kcr

Cite:Zutan Li+, Jingya Fang+, Shining Wang, Liangyun Zhang*, Yuanyuan Chen*, Cong Pian*. Adapt-Kcr: A novel deep learning framework for accurate prediction of lysine crotonylation sites based on learning embedding features and attention architecture. Briefings in Bioinformatic, 2022, bbac037. 



Protein lysine crotonylation (Kcr) is an important type of posttranslational modification that is associated with a wide range of biological processes. The identification of Kcr sites is critical to better understanding their functional mechanisms. However, the existing experimental techniques for detecting Kcr sites are cost-ineffective, to a great need for new computational methods to address this problem. We here describe Adapt-Kcr, an advanced deep learning model that utilizes adaptive embedding and is based on a convolutional neural network (CNN) together with a bi-directional long short-term memory network (BLSTM) and attention architecture.


1. File 'Adapt-Kcr' contains scripts for training the model and loading model. The Adaptive_embed_Train_Kcr.py, Adaptive_embed_Train_ST.py are scripts based on Kcr dataset and s/t dataset, respectively. Adaptive_embed_Test_Kcr.py and Adaptive_embed_Test_ST.py were used to predict Kcr sites and S/T phosphorylation sites, respectively.

2. File 'Kcr_Model' contains models trained by adaptive embedding method and CNN-LSTM-Att architecture. checkpoint.pth.tar are final model files based on Kcr sites and S/T sites, respectively.

3. File 'data' contains training and testing data used in this study. 


# Predict For Your Test Data
#Change the parameters of the script according to your own data path

cd to the Adapt-Kcr fold

python Adaptive_embed_Test_Kcr.py


# Train For Your own Data

cd to the Adapt-Kcr fold

python Adaptive_embed_Train_Kcr.py

Note: Due to the randomness of the initial parameters in the process of feature extraction and training of the neural network, the final AUC result will have an error of about 0.001-0.01.

