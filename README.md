# Text-Summarization
Abstractive text summarization using LSTM

### Dataset:
This project uses the Annotated English Gigaword dataset,, which can be found at https://deepai.org/dataset/gigaword#__sid=js0 . The dataset is a parallel corpus formed by pairing the first sentence of an 
article with its headline. It contains 3.8 million training samples, the validation and testing datasets have around 189k and
1951 samples respectively. We have taken 15k examples for validation and testing by sampling randomly from the 189k instances of the original validation data.

### Preprocessing:
We limit the number of words in article and summary to be 75 and 30 respectively. While preparing batch of sentences, we pick maximum length sentence and pad
the other sentences to this maximum length with [PAD] token. Also we use basic tokenization to split sentences into words and map them to their indices. 

### Model:
We try the following model architectures for summarization: 
<li> LSTM based encoder - decoder </li>
<li> LSTM + Greedy Decoding </li>
<li> LSTM + Beam Search </li>
<li> Encoder Attention </li>
<li> Using Pre-Trained GloVe Vectors</li>
