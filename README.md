# LLM-vs-trad-model-sentiment-analysis
Comparison between an LLM (XLNet) and a traditional neural network (Ensemble of a CNN &amp; a Stacked BiLSTM) for sentiment prediction.

### Findings(XLNet)

![](images_SA_/SA_XLNet.png)

Before the optimisation of the XLNet model, the anticipated train time on a core i7 Intel procesor was greater than 48hours. On the same CPU, the train time was  reduced to 2 hours after optimization. The XLNet model obtained a 95.6% test acurracy and a 27.4% test loss.

### Findings(CNN/Stacked BiLSTM)

![](images_SA_/SA_CNN_STACKEDLSTM.png)

The train time for the proposed CNN-StackedBiLSTM Hybrid model was 2hrs (apprx) on a core i7 intel procesor.It garnered 8.79% test acuracy, 86% Precision and 91%  Recal. 3 optimizers were tested across all 3 models; Adaptive Moment Estimation(Adam),Root Mean Square Propagation (RMSprop), and stochastic gradient descent(SGD) optimizer. The Adam  optimizer yielded the best results across all models. Several numbers of LSTM units were tested on each of the LSTM  models and the optimal values that yielded the best results were adopted as shown in the table above.


### Conclusion

XLNet outperformed LSTM and the hybrid model CNN-BiLSTM in sentiment analysis on IMDB 50k reviews due to its ability to capture bidirectional context information and permutation-based training strategy. Granting, LSTM is a high-performance model, although it has limitations in capturing long-term  dependencies in text sequences and requires a large amount of training data. XLNet is more reliable and flexible as it can be fine-tuned with minimal data, whereas LSTM yields positive outcomes with fewer resources. XLNet is recommended for tasks where computing expense is not a concern, while LSTM is suitable for most sentiment analysis tasks.
