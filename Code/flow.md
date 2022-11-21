1. Collect a set of datasets with the following specifications:

            a. One-Shot: One headline per class (real & fake) along with their corresponding english translation
            b. Three-Shot: One headline per class (real & fake) along with their corresponding english translation
            c. Five-Shot: One headline per class (real & fake) along with their corresponding english translation

2. Perform some basic pre-processing on the mini-corpus:

            a. Stem the english version of the mini-corpus
            b. Apply TF-IDF preprocessing to the native language and english translated version of the sentences 

3. Create a Siamese Network with the folllowing neural network:

            a. Input Layer (restrict input to the top-five words in the corpus)
            b. Four LTSM layers
            c. Three Dense layers

4. Train the siamese network on the few shots

5. Pass the feature vectors from the last dense layer to the BERT model and perform classification (real/fake)