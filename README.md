## Captionbot - Image Caption Generator Model for Assisted vision people  

**Description :** Image caption generator is a task that involves natural language processing (NLP) concepts to recognize the context of an image and describe them in a natural language like English.Python based project as captionbot for blind or blurred vision people – Learn to Build Image Caption Generator with **CNN & LSTM**.

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
<a href="http://www.youtube.com/watch?feature=player_embedded&v=
" target="_blank"><img src="http://img.youtube.com/vi//0.jpg" 
alt="IMAGE ALT TEXT HERE" width="330" height="236" border="10" /></a>

#### GIF tutorial of working of this model  
dash dash dash------

#### Some Screenshots :    
dash dash dash------

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

> Working of CNN

> Working of LSTM


#### Summary :
We built an image caption generator to create a CNN-RNN model in this Python project. It's important to note that our model is data-driven, so it can't predict words that aren't in its vocabulary. We worked with a tiny dataset of 8000 photos. We need to train production-level models on datasets larger than 100,000 pictures in order to develop better accuracy models.

#### Future Goals :   
Integration with android application and camera.What I do using this model mentioned the steps below :   
_**Steps :**_      
* First of all train ML Model on `Best dataset`(so that it can predict better) and Create `tflite` model using TensorflowLite. 
* After Creating tflite, Build or integrate this `model.tflite` in android studio.
* Front end -> `ImageView`, `TextView`, `select(From Internal)`, `capture(Camera)` and `predict` button in Android Studio.
* Back end -> working Implementation => show output `caption` in `textview` as well as convert this `text to speech` for blind people or blurred vision people.
* Finally Improve Front end of App for Better Visuals(Colorful and splashscreen & Headlines - Caption Bot for Assisted Vision)
* App is ready to `predict`.
