## Captionbot - Image Caption Generator Model for Assisted vision people  

**Description :** Image caption generator is a task that involves natural language processing (NLP) concepts to recognize the context of an image and describe them in a natural language like English.Python based project as captionbot for blind or blurred vision people – Learn to Build Image Caption Generator with **CNN & LSTM**.

> **Libraries Used :**
* **Tensorflow :** It's an open-source library that supports deep learning using Python etc frameworks. 
* **Keras :** It's an open-source Python library that allows to evaluate the deep learning models. 
* **Pillow :** Pillow is a Python Imaging Library (PIL), that adds support for opening, manipulating, and saving images. 
* **Numpy :** To work with arrays, Numpy library is used. 
* **Matplotlib :** Library to create static and animated visualizations in Python framework.
* **Tqdm :** tqdm is a library in Python which is used for creating Progress Meters or Progress Bars.

> **Type of Dataset :** 
* For the image caption generator, we will be using the **Flickr_8K dataset**. There are also other big datasets like **Flickr_30K** and **MSCOCO** dataset but it can take weeks just to train the network so we will be using a small Flickr8k dataset. The advantage of a huge dataset is that we can build better models.

> **About Dataset used for this model**
* Name of dataset : Flickr_8K dataset  
* Source of dataset : [Kaggle](https://www.kaggle.com/datasets/ming666/flicker8k-dataset)
* Description of dataset : Contains 8091 photographs in JPEG format.

> **Direct link to download the Dataset**
* [Flickr_8K dataset](https://github.com/jbrownlee/Datasets/releases/download/Flickr8k/Flickr8k_Dataset.zip)
  * _Contains 8091 photographs in JPEG format._
* [Flickr_8K Text](https://github.com/jbrownlee/Datasets/releases/download/Flickr8k/Flickr8k_text.zip)
  * _The Flickr_8k_text folder contains file Flickr8k.token which is the main file of our dataset that contains image name and their respective captions separated by newline(“\n”)._

### Complete Demo Video Given Below ⬇
##### Click on image
<a href="http://www.youtube.com/watch?feature=player_embedded&v=zp-8_Rjsjjg
" target="_blank"><img src="http://img.youtube.com/vi/zp-8_Rjsjjg/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="365" height="236" border="10" /></a>

#### GIF Tutorial For Working Of This Model  
![Image Caption Generator Model](https://github.com/Nitinkumar3399/My_GIFs/blob/master/ICG-giphy.gif)

> **Steps shown in above GIF or video described as below :**

**1.** Open `Anaconda Prompt`.  
**2.** Go to the `path`, where your all project files or dataset `(both testing and training)` present.  
**3.** Now you need to run python file `testing_caption_generator.py`.  
**4.** Before running you need to give a `path to the input image`.  
**5.** For performing **step 3** and **step 4**, you need to type the following command in anaconda prompt.      
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; `python testing_caption_generator.py -i "Path to the input image"`  
**6.** After typing the command, hit enter `↩`.    
**7.** After few seconds, you will see a **caption START** and **caption END**.      
**8.** your required image caption will be present in between the **START** and **END**.  

#### Some Screenshots :    

![img1](https://user-images.githubusercontent.com/65066519/169573484-befae699-5e84-4a8b-a364-fc73c9384d6c.jpg)
![img5](https://user-images.githubusercontent.com/65066519/169573530-d938e3a7-f4d6-4e99-9a5a-cf4974171266.jpg)
![img6](https://user-images.githubusercontent.com/65066519/169573543-aadedbc3-16b5-44c0-820e-d1b7944e1490.jpg)
![img3](https://user-images.githubusercontent.com/65066519/169573514-d15d4c66-0d61-4de3-b0a1-d10b81af69f6.jpg)
![img2](https://user-images.githubusercontent.com/65066519/169573498-336ca39a-0742-41ba-855b-540d904eeb56.jpg)
![img4](https://user-images.githubusercontent.com/65066519/169573519-64ff5c80-ee64-4d6c-bde7-7dfdd0f15c81.jpg)
![img7](https://user-images.githubusercontent.com/65066519/169573553-65a345b6-6531-4ff9-9648-cc91fee0c408.jpg)


> **Folder Structure :**

* **Downloaded from dataset :**
  * **Flicker8k_Dataset** – Dataset folder which contains 8091 images.
  * **Flickr_8k_text** – Dataset folder which contains text files and captions of images.

* **The below files will be created by us while making the project :**
  * **Models** – It will contain our trained models.
  * **Descriptions.txt** – This text file contains all image names and their captions after preprocessing.
  * **Features.p** – Pickle object that contains an image and their feature vector extracted from the Xception pre-trained CNN model.
  * **Tokenizer.p** – Contains tokens mapped with an index value.
  * **Model.png** – Visual representation of dimensions of our project.
  * **Testing_caption_generator.py** – Python file for generating a caption of any image.
  * **Training_caption_generator.ipynb** – Jupyter notebook in which we train and build our image caption generator.

> **Working of CNN**

![img](https://user-images.githubusercontent.com/65066519/169506429-689826c8-ff10-4306-92c1-e36d2c9a27fd.png)

* Convolutional Neural networks are specialized deep neural networks which can process the data that has input shape like a 2D matrix. Images are easily represented as a 2D matrix and CNN is very useful in working with images.
* CNN is basically used for **image classifications** and identifying if an image is a bird, a plane or Superman, etc.
* It scans images from **left to right** and **top to bottom** to pull out important features from the image and combines the feature to classify images. It can handle the images that have been **translated**, **rotated**, **scaled** and **changes in perspective**.
* In simple word what CNN does is, it extract the feature of image and convert it into **lower dimension** without **loosing** its characteristics.

> **Working of LSTM**

![Lstm](https://user-images.githubusercontent.com/65066519/169509869-7f42a7cf-3a2c-4f1f-ba41-594ed571a6ce.jpg)

* LSTM stands for **Long short term memory**, they are a type of **RNN (recurrent neural network)** which is well suited for **sequence prediction problems**.
* Based on the previous text, we can predict what the next word will be.
* It has proven itself effective from the traditional RNN by overcoming the limitations of RNN which had short term memory. 
* LSTM can carry out relevant information throughout the processing of inputs and with a forget gate, it discards non-relevant information.

So, to make our image caption generator model, we will be **merging these architectures**. It is also called a **CNN-RNN** model.
![model](https://user-images.githubusercontent.com/65066519/169508812-abe069cf-9608-4cad-bcf9-72dcc7938dcd.jpg)

* CNN is used for extracting features from the image. We will use the pre-trained model Xception.
* LSTM will use the information from CNN to help generate a description of the image.

> **Summary** 

We built an image caption generator to create a CNN-RNN model in this Python project. It's important to note that our model is data-driven, so it can't predict words that aren't in its vocabulary. We worked with a tiny dataset of 8000 photos. We need to train production-level models on datasets larger than 100,000 pictures in order to develop better accuracy models.

> **Future Goals**

Integration with android application and camera.What I do using this model mentioned the steps below :   
_**Steps :**_      
* First of all train ML Model on `Best dataset`(so that it can predict better) and Create `tflite` model using TensorflowLite. 
* After Creating tflite, Build or integrate this `model.tflite` in android studio.
* Front end -> `ImageView`, `TextView`, `select(From Internal)`, `capture(Camera)` and `predict` button in Android Studio.
* Back end -> working Implementation => show output `caption` in `textview` as well as convert this `text to speech` for blind people or blurred vision people.
* Finally Improve Front end of App for Better Visuals(Colorful and splashscreen & Headlines - Caption Bot for Assisted Vision)
* App is ready to `predict`.
