# bert_rus_sentiment
Bert Models for Russian Sentiment Analysis

Trained Bert-BASE models for russian sentiment analysis.
There are PyTorch ([transformers](https://github.com/huggingface/transformers)) and TensorFlow ([deeppavlov](https://github.com/deepmipt/DeepPavlov)) versions available.
Models are available for download from [Google Drive](https://drive.google.com/open?id=1LkaSQWfZTpkG3wpoaPVLFOOIEomFxl1S).

## Used Data
5 dataset was used in this work: [Fun](https://github.com/computational-humor/humor-recognition/tree/master/data), [News](https://www.kaggle.com/c/sentiment-analysis-in-russian/overview), [RuSentiment](https://github.com/Ab1992ao/rusentiment/tree/master/Dataset), [SentiRuEval](http://www.dialog-21.ru/evaluation/2016/sentiment/) and [TwitterMokoron](http://study.mokoron.com).

Firstly, 5 separate models were trained on datasets. After that each model was used to predict probability of label to unseen data, probabilities were summarized using model's F1-score as weights and new labels were applied to data. Dataset with new labels from models' predictions are stated as joined dataset later.

## Models Training
Models were pretrained from [DeepPavlov's Conversational RuBERT](http://docs.deeppavlov.ai/en/master/features/pretrained_vectors.html#bert) on russian sentiment data and after that fine-tuned on joined dataset.

## Examples
The example of models loading and using is availabe in [Use BertClassifier Models for Sentiment Analysis.ipynb](Use BertClassifier Models for Sentiment Analysis.ipynb).

## Updates

### 2020-06-07
DistilBert model is also available to download from [Google Drive](https://drive.google.com/open?id=1LkaSQWfZTpkG3wpoaPVLFOOIEomFxl1S).
