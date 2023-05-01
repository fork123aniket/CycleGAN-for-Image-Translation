# CycleGAN for Image Translation
This repository aims at developing a ***CycleGAN*** model to translate photos of horses to zebras and vice versa. Here, it is not necessary to provide paired examples in the dataset to ***CycleGAN***, i.e. it does not require examples of photographs before and after the translation in order to train the model. Instead, the model is able to use a collection of photographs from each domain and extract and harness the underlying style of images in the collection in order to perform the translation.
## Requirements
- `numpy`
- `matplotlib`
- `keras`
## Usage
### Data
- The ***horse2zebra*** dataset can be downloaded from the [***CycleGAN webpage***](https://people.eecs.berkeley.edu/~taesung_park/CycleGAN/datasets/horse2zebra.zip). 
- In the dataset, the ***A*** category refers to horse and ***B*** category refers to zebra, and the dataset is comprised of train and test elements. However, the current implementation loads all photographs and use them as a training dataset.
- All photographs are of the same size, i.e. *256 * 256*.
- To prepare the image dataset, considered here, in order to properly train the ***CycleGAN*** model, run `Data.py`
### Training and Testing
- To train and test the ***CycleGAN*** model along with plotting the results, run `Cycle_GAN_to_translate_Images.py`
- To translate multiple images using ad-hoc image translation process with the help of trained ***CycleGAN***, run `Image_Translation_with_Cycle_GAN_Generators.py`
- To translate merely individual images using the trained ***CycleGAN*** model, run `Single_Image_Translation_with_Cycle_GAN_Generators.py`
- All hyperparameters to control training and testing of the ***CycleGAN*** model in single as well as multiple image translation settings are provided in their respective `.py` files.
- The average loss for both generator and discriminator components of the ***CycleGAN*** model for each of the two catagories (***Horse (A)*** and ***Zebra (B)***) are printed after every epoch.
## Output Samples
### Few Examples of Image Dataset
![alt text](https://github.com/fork123aniket/CycleGAN-for-Image-Translation/blob/main/Images/1.PNG)
### Image-to-Image Translation Results
| Horse-to-Zebra Results        | Zebra-to-Horse Results           |
| ------------------------- |:----------------------------:|
| ![alt text](https://github.com/fork123aniket/CycleGAN-for-Image-Translation/blob/main/Images/2.PNG) | ![alt text](https://github.com/fork123aniket/CycleGAN-for-Image-Translation/blob/main/Images/3.PNG) |
### Multiple Images Translation
| Horse-to-Zebra Results        | Zebra-to-Horse Results           |
| ------------------------- |:----------------------------:|
| ![alt text](https://github.com/fork123aniket/CycleGAN-for-Image-Translation/blob/main/Images/4.PNG) | ![alt text](https://github.com/fork123aniket/CycleGAN-for-Image-Translation/blob/main/Images/5.PNG) |
### Single Image Translation
| Real Horse Image        | Generated Zebra Image           |
| ------------------------- |:----------------------------:|
| ![alt text](https://github.com/fork123aniket/CycleGAN-for-Image-Translation/blob/main/Images/6.PNG) | ![alt text](https://github.com/fork123aniket/CycleGAN-for-Image-Translation/blob/main/Images/7.PNG) |
