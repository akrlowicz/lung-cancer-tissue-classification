# lung-cancer-tissue-classification


LC25000 LUNG AND COLON HISTOPATHOLOGICAL IMAGE DATASET is explored here. The project focus is on lung cancer so no colon tissue images were used. There are three classes for lung images: benign lung tissue, malignant lung adenocarcinoma, malignant lung squamous cell carcinoma. Each class consist of 5000 RGB images with sizes 768 x 768. Dataset can be found in this repository in lung_colon_image_set folder or be downloaded from link https://academictorrents.com/details/7a638ed187a6180fd6e464b3666a6ea0499af4af. To read more about database you can visit: https://arxiv.org/ftp/arxiv/papers/1912/1912.12142.pdf


# Problem approach

Here I want to classify histopathological lung tissue images into benign, malignant adenocarcinoma, malignant squamos cell carcinoma so differentatite between healthy and two type cancers.


I use CNN with 4 hidden layers (3 convolution layers and one fully connected). More details can be found in notebook. 
  - Train accuracy: 0.936
  - Validation accuracy: 0.931
  - Test accuracy: 0.929



Second apporach was to use deeper architecture, so I went a bit extreme and used ResNet50 architecture. Training accuracy significantly improved, but there is high variance here on the other hand.
  
  - Train accuracy: 0.988
  - Validation accuracy: 0.917
  - Test accuracy: 0.916

# Evaluation

  - Accuracy metric
  - Confusion matrix
  - Exploration of model miastakes
  
# Further actions

To make this project better:

First of all - minimize variance in the ResNet50 model with some regularization techniques or change the architecture (build something deep, but not as deep as ResNet50).

Second thing is - detecting cancer images is nice, but much cooler would be to to do instance segmentation of cancerous cells. The shape of the cancerous cells plays a vital role in determining the severity of the cancer.

# Used libraries

- numpy, cv2
- matplotlib, seaborn
- sk-learn, keras

# References 
[1] Borkowski AA, Bui MM, Thomas LB, Wilson CP, DeLand LA, Mastorides SM. Lung and Colon Cancer Histopathological Image Dataset (LC25000). arXiv:1912.12142v1 [eess.IV], 2019
[2] Kaiming He, Xiangyu Zhang, Shaoqing Ren, Jian Sun. Deep Residual Learning for Image Recognition. arXiv:1512.03385v1. 2015
