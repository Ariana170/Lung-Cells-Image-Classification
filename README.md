# Lung-Cancer-Image-Recognition
Using a neural network, split the images of lung cells into adenocarcinoma, squamous cell carcinoma, or benign.

### Dataset
The dataset is Lung Cancer (Histopathological Images) and contains three main folders:

- Adenocarcinoma: 5000 images
- Benign: 5000 images 
- Squamous cell carcinoma: 5000 images 

### General Approach
Before training, the images were preprocessed to ensure consistency and improve model performance. All images were resized to a fixed dimension of 224x224 pixels, normalized to a [0,1] range, and converted to tensors. Data augmentation techniques such as random rotation, horizontal flipping, and color normalization were applied to increase dataset variability and reduce overfitting. The dataset was then divided into training, validation, and test subsets, each loaded using a PyTorch DataLoader for efficient batch processing.

A Convolutional Neural Network (CNN) model was implemented to extract spatial features from the processed images. The architecture consisted of 4 convolutional layers with ReLU activation and max-pooling layers for downsampling, followed by fully connected layers for classification. In addition, a ResNet-based model was trained to improve accuracy. The use of ResNet allowed the model to achieve higher performance during classification. Both models were trained using "Adam" with "Cross-Entropy Loss" and evaluated based on the metrics: accuracy, precision, and recall.

### Results 
As expected, the better results are yielded using ResNet with an accuracy of 99.5%, while the CNN model only achieved an accuracy of 88.5%. 

### Dataset Sources:
Lung Cancer (Histopathological Images) - https://www.kaggle.com/datasets/rm1000/lung-cancer-histopathological-images/data?select=adenocarcinoma 

### Bibliography:
Borkowski AA, Bui MM, Thomas LB, Wilson CP, DeLand LA, Mastorides SM. Lung and Colon Cancer Histopathological Image Dataset (LC25000). arXiv:1912.12142v1 [eess.IV], 2019
