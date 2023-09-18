#  <div align="center"> Image-Captioning-Bot </div>

# About
Image Captioning Bot, as the name suggests will predict the caption for any image provided to it on the basis of the trained dataset. Generate word after another, uses Deep Learning to generate words.

# Tech Stack Used

<ul>
<li>Numpy</li>
<li>Pandas</li>
<li>cv2</li>
<li>Matplotlib</li>
<li>Keras</li>
<li>Re</li>
<li>NLTK</li>
<li>string</li>
<li>json</li>
<li>time</li>
<li>pickle</li>
<li>Tensorflow</li>
<li>collections</li>
<li>Resnet50</li>
</ul>

# Model Structure

<a href="https://www.tensorflow.org/api_docs/python/tf/keras/applications/resnet50/ResNet50">Resnet50</a> pre-trained model is used on images first to generate 2048 output size which will be further feed to created model

<pre>
(Image)                                (NLP)
Input (2048)                          Input (30)
  |                                      |
  |                                      |
Dropout (0.3)                        Embedding (input_dim=2574, ouput_dim=50)
  |                                      |
  |                                      |
Dense (256)                           Dropout (0.3)
  |                                      |
  |                                      |
  |                                     LSTM (256)
  |________________       _______________|
                   |     |
                   |     |
                   Add (256 x 2)
                     |
                     |
                   Dense (256)
                     |
                     |
                   Dense (2574)
                  (output)
</pre>

# Examples
![image](https://user-images.githubusercontent.com/100359818/234405487-67210edf-b676-4ae8-8739-7cd4bb6ce7fe.png)

<u>Caption: </u> two dogs are running on beach

# External Links
Refer to this <a href="https://drive.google.com/drive/folders/1_EGQUGSUCucaYd0hOMmsmuygZLqIVmKn?usp=share_link">Link</a> for the dataset and trained models data!

