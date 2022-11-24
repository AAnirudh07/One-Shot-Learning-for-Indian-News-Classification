# One-Shot-Learning-for-Indian-News-Classification
Implementation of the One-Shot Machine Learning model for fake news classification in Tamil.
> This project was carried out by the JBTTM club at [SSN College of Engineering, Chennai, India](https://www.ssn.edu.in/college-of-engineering/computer-science-and-engineering-department-ssn-institutions/).


### Novelty



### Model Architecture
<div style="text-align: justify">
Our proposed solution for one-shot indian news classification consists of two separate architectures for training and testing. During the training phase, we employ a Siamese Network to construct word-embeddings. This siamese network extracts feature vectors from the RoBERTa autoencoder(AE) and passes it to a mean pooling layer. Following which, the feature vectors are passed through three fully connected layers to finally obtain a vector with 64 features.
</div>

<p align='center'>
  <img src='https://github.com/AAnirudh07/One-Shot-Learning-for-Indian-News-Classification/blob/main/Code/assets/Siamese-Network-Training.png' style='height: 40%'>
</p>
