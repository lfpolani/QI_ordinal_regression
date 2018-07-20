# QI_ordinal_regression

This repository contains the code of the algorithms presented in the paper "Ordinal Regression using Noisy Pairwise Comparisons for Quetelet Index Range Estimation". 

################################# General ##################################

Caffe models download link: https://drive.google.com/open?id=1hZhhHGpqIYq82tThuTs8vYxheXBnTWoP

The code in this repository is ready to run using two testing images located in the folder: Testing_images. The images are from two athletes who won Gold medals in the 2018 Winter Olympics. Images, weight, and height information for the athletes can be found at: https://www.olympic.org/pyeongchang-2018/results/en/general/athletes.htm

Source code provided here does not include the testing data used for the experiments in the papers. Users need to download the data from the Florida Department of Corrections Database if they want to replicate the exact results of the paper by using the table with the image IDs, which is inside the folder "Complementary_files". 

The images in the folder Testing_images are already preprocessed with face detection and cropping. We used the same algorithm used for face detection and cropping in the paper "Deep Face Recognition" by O. M. Parkhi, A. Vedaldi and A. Zisserman. The code for the algorithm can be downloaded from http://www.robots.ox.ac.uk/~vgg/software/vgg_face/ 

################################# Prerequisites ##################################

ubuntu 14.04

Caffe: https://github.com/BVLC/caffe (with cuda installed)

################################# Folder and File Description ##############################
Files: Code for the algortithms/models used in the paper, both the noisy binary search algorithms and the models used for comparison (see Table 4 in the paper).

  NNBS_AgeNet-based_Mode-I.ipynb: Naive Noisy Binary Search using AgeNet and training Mode I.
  NNBS_AgeNet-based_Mode-II.ipynb: Naive Noisy Binary Search using AgeNet and training Mode II.
  NNBS_VGG-based_Mode-I.ipynb: Naive Noisy Binary Search using VGG and training Mode I.
  INBS_AgeNet-based_Mode-II.ipynb: Interval Noisy Binary Search using AgeNet and training Mode II.

  Handcrafted_feature-based_method.ipynb: Hadncrafted feature-based method used for comparison with the noisy binary search algorithms. 
  Fine-tuned_AgeNet.ipynb: Fine-tuned AgeNet model used for comparison with the noisy binary search algorithms. 
  Fine-tuned_VGG.ipynb: Fine-tuned VGG model used for comparison with the noisy binary search algorithms.
  VGG_regression.ipynb: Fine-tuned regression VGG model used for comparison with the noisy binary search algorithms.

Folders:
  Anchors:
    Images: Folder that contains the images used as anchors
    table_anchors.pkl: Contains a dataframe with the filename of the anhors.

  Deployment_prototxt_files: Contains all the deployment .prototxt files for all the models.

  Testing_images: Contains two testing images to easily run and test the algorithms

  Complementary_files: Contains a dataframe with the DC Numbers of the images used for testing in the submitted paper.
 


# QI_ordinal_regression
