# A BiLSTM model for Sentiment Classification

### Aim:
To develop a Sentiment Classification model using Deep Recurrent Neural Network (RNN) with Bidirectional LSTM wrapper.

### What is Sentiment Classification?
Sentiment Classification/Analysis is a method of finding and classifying opinions expressed in a piece of text basing on computation technologies, especially in order to find out whether the writer’s behavior towards a specific topic, product, etc. is positive, negative, or neutral.
Sentiments are the reflection of the beliefs, choices and activities of the people.

### Why Sentiment Classification?
With the elevation in the communication technology, a huge number of people from all lineages across the world take part in social networks and express their opinions on a wide range of topics. Now it is a dire need to summarize the data created by people over the social networks and see the insights from them. Besides, in the field of NLP, it has become a topic of enormous interest. Because, it is needed to make smart recommending systems, anticipating the results of political elections, understanding the feedback of people on public events and movements.

### LSTM:
LSTM stands for “Long short-term memory” is an artificial neural network architecture used in the field of deep learning . LSTM networks are well-suited for classifying , processing and making predictions based on time series data .

### BiLSTM:
In unidirectional LSTM information flows from the backward to forward. On the contrary in Bi-directional LSTM information not only flows backward to forward but also forward to backward using two hidden states. Hence Bi-LSTMs understand the context better.

Using bidirectional will run your inputs in two ways, one from past to future and vice-versa  and what differs this approach from unidirectional is that in the LSTM that runs backward you preserve information from the future and using the two hidden states combined you are able in any point in time to preserve information from both past and future. BiLSTMs show very good results as they can understand the context better.
(image)

### Dataset:
The data used for training and testing the model is IMDb movie reviews dataset, which consists of 49,582 movie reviews in English language. Each movie review is labelled as positive or negative.

### Model Definition:
Our BiLSTM model consists of the following layers:
- **Embedding Layer**: It creates word vectors of each word in the word_index and groups words that are related or have similar meaning by analyzing other words around them.
- **Masking layer**: Masking is done to allow the model differentiate between an actual sequence value and padded sequence value.
- **Bidirectional LSTM layer**: To make a decision to keep or throw away data by considering the current input, previous output, and previous memory. 
- **Dense Layer**: Fully connected neural network layer with sigmoid activation.

The optimizer used is **Adam optimizer** and the loss function is **Binary Cross Entropy**.

### Experiments:
Experimented with three different model types within feedback models;
- Simple RNN
- LSTM
- Bi-LSTM 

For each model type, defined a couple of models by adding or removing some layer(s).

### Results and Analysis:
Amongst different experiments, the BiLSTM model consisting of one embedding layer, one masking layer, two BiLSTM wrappers and three dense layers gave the highest test set accuracy of **88.3%**.

The following barplot gives the comparison of different models in terms of test set accuracy:
(image)

### Comparison with other models:
(image)

### Conclusion

BiLSTM model proves to be the best classifier for sentiment classification on this data, compared with other models expeerimented.
