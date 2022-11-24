# One-Shot-Learning-for-Indian-News-Classification
Implementation of the One-Shot Machine Learning model for fake news classification in Tamil.
> This project was carried out by the JBTTM club at [SSN College of Engineering, Chennai, India](https://www.ssn.edu.in/college-of-engineering/computer-science-and-engineering-department-ssn-institutions/).


### Novelty
<div style="text-align: justify">
Our proposed solution attempts to alleviate the problem of training SOTA NLP classification models like BERT for low-resource langauges. It does so by comparing the word embeddings generated by SOTA NLP models trained on massive amounts of <b>English</b> datasets (or in a more general case, any language other than the langauge in consideration) and tuning the weights of the model accordingly. Once trained on the new language, these new word embeddings can be plugged in with any adaptable SOTA NLP model.
</div>
<br>
<div style="text-align: justify">
To faciliate the above, we used a siamese network with the RoBERTa model our base SOTA NLP model. On top of RoBERTa, we used a pooling layer and three dense layers. This siamese network was trained on just <b>one instance</b> per class of the <a href='https://github.com/AAnirudh07/Fake-News-Headlines-In-Tamil'>Tamil Fake News Dataset</a>. After training, these word embeddings were used to train a random-forest model for fake news classification. 
</div>


### Model Architecture
<div style="text-align: justify">
Our proposed solution for one-shot indian news classification consists of two separate architectures for training and testing. During the training phase, we employ a Siamese Network to construct word-embeddings. This siamese network extracts feature vectors from the RoBERTa autoencoder(AE) and passes it to a mean pooling layer. Following which, the feature vectors are passed through three fully connected layers to finally obtain a vector with 64 features.
</div>

<p align='center'>
  <img src='https://github.com/AAnirudh07/One-Shot-Learning-for-Indian-News-Classification/blob/main/Code/assets/Siamese-Network-Training.png' style='height: 40%'>
</p>
