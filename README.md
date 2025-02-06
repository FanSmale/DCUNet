# DCUNet
Deep learning-based full waveform inversion (DL-FWI) is a high-resolution imaging technique that has attracted significant attention due to its high prediction efficiency and  lack of the need for an initial model.
However, popular methods lack the ability to accurately invert multi-strata model and rock bodies.
In this paper, we propose a new method that emphasizes the recovery of multi-strata and rock within both the network architecture and the loss function.
Regarding the network architecture, deformable convolution is embeded into the first and third scales of the encoder to capture global and local spatial features.     
The attention mechanism is applied before the decoder, allowing the network to focus more on key information such as strata and rock bodies.                             
Specifically, a dimensionality reducer is inserted before the encoder, enabling the model to better handle multi-scale and multi-resolution data.
For the loss function design, we propose an adaptive progressive loss function including structure similarity index measure (SSIM) loss and edge loss.
In the early stages of inversion, SSIM loss dominates the training pocess, allowing the network to optimize global structural similarity.
As the inversion progresses, the weight of edge loss gradually increases, and the network enhances the recovery of detailed information such as strata and rock mass.
Results on OpenFWI and SEG datasets show that our method is superior to state-of-the-art data-driven methods, especially on multiple-strata model and rock bodies.


I. This project includes the code implementation of DC-UNet and the comparative experiment InversionNet, DD-Net70，DD-Net，FCNVMB。 In addition, there are corresponding ablation experiments (C-UNet) and anti noise experiments (D-UNet).

II. Corresponding code files for training and validation methods:
1)model_train.py---------->Training startup file;
2)model_test.py---------->Test startup file;
3)param_config.py---------->Training parameter setting file;
4)path_config.py---------->Path parameter setting file;
5)net---------->Training network structure;
6)func---------->Support files;
