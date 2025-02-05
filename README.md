# Fine-Tuning-BERT
Fine-Tuning BERT &amp; BERTurk on the Stanford Sentiment Treebank (SST)
Fine-Tuning BERT & BERTurk on the Stanford Sentiment Treebank (SST)
Overview
This project fine-tunes BERT and BERTurk models on the Stanford Sentiment Treebank (SST) dataset.

English SST: Fine-tuning a pre-trained BERT model.
Turkish SST: Fine-tuning a pre-trained BERTurk model.
The models are trained on the respective datasets and evaluated on the test sets to measure performance.

Dataset
English SST:
Train: 8,544 examples
Dev: 1,101 examples
Test: 2,210 examples
Turkish SST:
Train: 32,000 examples
Dev: 8,000 examples
Test: 8,262 examples
Training Details
Model: bert-large-uncased was used for English SST.
Optimizer: AdamW
Epochs: 2
Batch Size: (Specify if needed)
Loss:
Epoch 1: 0.3962
Epoch 2: 0.2620
Evaluation
Test Accuracy: 0.6036
Sample Predictions
Here are some example sentences and model predictions:

Text	Predicted Score (L1)	Predicted Label (L2)
The gorgeously elaborate continuation of "The Lord of the Rings" trilogy...	0.8333	3
Singer/composer Bryan Adams contributes a slew of songs...	0.625	2
Extreme Ops exceeds expectations.	0.7361	2
Good fun, good action, good acting, good dialogue...	0.9027	3
Dramas like this make it human.	0.8055	3
Requirements
Install dependencies using:

bash
Kopyala
Düzenle
pip install -r requirements.txt
Training
To fine-tune the models, run:

bash
Kopyala
Düzenle
python train_bert.py  # For English BERT
python train_berturk.py  # For Turkish BERTurk
Evaluation
After training, evaluate the models on the test set using:

bash
Kopyala
Düzenle
python evaluate.py
Warnings & Notes
Some weights of BertForSequenceClassification were newly initialized and not loaded from the pre-trained model.
Hugging Face authentication warnings may appear, but training and inference are not affected.
Future versions of datasets may require trust_remote_code=True.
License
This project is open-source under the MIT License.

Bu haliyle eğitim detaylarını, test doğruluğunu ve model uyarılarını eklemiş oldun. İstersen batch size, learning rate gibi ayarları da ekleyebilirsin.
