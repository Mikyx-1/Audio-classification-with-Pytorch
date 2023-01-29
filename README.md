# Audio-classification-with-Pytorch

Link Dataset: https://www.kaggle.com/datasets/chrisfilo/urbansound8k

This repo demonstrates a basic, widely used approach to classify audio signals.

Step1: Build a preprocess data pipeline. 
![image](https://user-images.githubusercontent.com/92131994/215331102-b0d3089c-04c5-41d7-80b3-676d98037f0d.png)

I resampled it to 16Khz and just take 48000 samples(3s) to feed to our model because I think 3s is long enough to recognise 
a sound. And then, I use torchaudio to extract the mel points. You can gain more intuition in this link: https://haythamfayek.com/2016/04/21/speech-processing-for-machine-learning.html

Step2: Visualize some random samples in our dataset (as always)
![image](https://user-images.githubusercontent.com/92131994/215331264-515ebf17-657e-4e02-9185-5a4fb39a62fc.png)

Step3: Build a mini VGG-19 like CNN model(where conv layer sizes gradually get smaller)
![image](https://user-images.githubusercontent.com/92131994/215331378-edf2f7e5-1fbd-4fff-8d1c-545c03496bd0.png)

Step4: Train the model using Adam optimizer and CE Loss. 
P/s: Due to limit computational resources. I'll stop here
![image](https://user-images.githubusercontent.com/92131994/215331424-81f0595f-270e-4f66-a22d-74ca5d14eb36.png)
