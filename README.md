**Face and Emotion Detection**
**INTRODUCTION**
This project aims to classify the emotion on a person's face into one of four categories, using deep convolutional neural networks. This repository is an implementation of this research paper and some help from this GitHub repo.
Dataset
The model is trained on the FER-2013 dataset which was published on International Conference on Machine Learning (ICML) available here. This dataset consists of 35887 grayscale, 48x48 sized face images with seven emotions - angry, disgusted, fearful, happy, neutral, sad and surprised.
**Dependencies**
Python 3.6
OpenCV
Tensorflow
Keras.
**Usage**
First clone or downlad this repository then enter the folder: 'cd emotionDetector1'

Now, you can either use this pretrained modelby loading the weights or train your oun custom model: The code is modified in order to use the pretrained model, to use the model use this command: 'python edModel.py'

To train your model, uncomment code at line 18-74 and place your dataset in data/train/ and data/test/ directories. Then use this command 'python edModel.py --mode train' to start training, then 'python edModel.py --mode display'

**Algorithm**
First, we use haar cascade to detect faces in each frame of the webcam feed.
The region of image containing the face is resized to 48x48 and is passed as input to the ConvNet.
The network outputs a list of softmax scores for the seven classes. (we have modified it to give result out of 4 emotions)
The emotion with maximum score is displayed on the screen.
**References**
"Challenges in Representation Learning: A report on three machine learning contests." I Goodfellow, D Erhan, PL Carrier, A Courville, M Mirza, B Hamner, W Cukierski, Y Tang, DH Lee, Y Zhou, C Ramaiah, F Feng, R Li,
X Wang, D Athanasakis, J Shawe-Taylor, M Milakov, J Park, R Ionescu, M Popescu, C Grozea, J Bergstra, J Xie, L Romaszko, B Xu, Z Chuang, and Y. Bengio. arXiv 2013.
