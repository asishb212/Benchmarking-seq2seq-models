# Benchmarking Seq2Seq Models

 The project employs a variety of neural network architec-tures to construct a chatbot capable of engaging in stylized conversations reminiscent of popular movie dialogues. To accomplish this, a sequence-to-sequence model is trained on the comprehensive Cornell Movie-Dialogs Corpus dataset. This sequential nature of the task is accomplished by employing an architecture with two main components: an encoder and a decoder. 
	
  The encoder takes an input sequence and transforms it into a fixed-length vector representation called a context vector or latent space representation. This is done to cap-ture the semantic and contextual information of the input sequence. The decoder then takes the context vector gener-ated by the encoder and generates an output. The output is relevant and meaningful given the input. The best perform-ing sequence transduction models typically connected the encoder and decoders through an attention mechanism, un-til Vaswani et al. proposed to dispense with recurrence and convolutions entirely in a multi-layered self-attention feed-forward neural network, the Transformer. 

	
  We have built and trained models for a set of six recur-rent neural networks (RNN) which were created by combin-ing different types of RNN layers, including Vanilla RNN, GRU, and LSTM, with two attention mecha-nism–Luong and Bahdanau. We have also built a self-attention Seq2Seq Transformer.

	
  For the six RNNs, we have used wandb, an online weights and biases platform, to optimize for hyper-parameters such as learning rate, clip, decoder learning ratio, type of optimizer, and the teacher forcing ratio. We au-tomated the task of training the models for 15 epochs under all the allowed permutations of the hyper-parameters and selected the ones with the lowest loss as the optimal set. The loss is calculated through a blank function assuming blank. The optimal RNN models were then tested and benchmarked along with the transformer on their testing and validation loss and accuracy, along with an evaluation of performance on the same input sentences.

# Repository structure
 
```
Notebooks
   |-- Bahdanau_LSTM.ipnyb
   |-- Bahdanau_GRU.ipnyb
   |-- Bahdanau_RNN.ipnyb
   |-- Luong_LSTM.ipnyb
   |-- Luong_GRU.ipnyb
   |-- Luong_RNN.ipnyb
   |-- Transformer.ipnyb
 ```
 
# Instructions to run
 
## Requirements

```
!pip install -r requirements.txt
```

## Training

```
Run Bahdanau_LSTM.ipnyb for Bahdanau attention and LSTM architecture
Run Bahdanau_GRU.ipnyb for Bahdanau attention and GRU architecture
Run Bahdanau_RNN.ipnyb for Bahdanau attention and RNN architecture
Run Luong_LSTM.ipnyb for Bahdanau attention and LSTM architecture
Run Luong_GRU.ipnyb for Bahdanau attention and GRU architecture
Run Luong_RNN.ipnyb for Bahdanau attention and RNN architecture
```
 
