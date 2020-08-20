
## Table of Contents (Optional)

- [Data collection](#Data_collection)
- [Understanding the data](#Understanding_data)
- [Data Cleaning](#Data_Cleaning)
- [Loading the training batch](#Loading_batch)
- [Model Architecture](#Model_Architecture)

---


## Installation
### from conda
- `conda install -c anaconda tensorflow-gpu` 
### from pip
- `pip install tensorflow-gpu` 

## Data_collection
- <a href="https://s3.amazonaws.com/video.udacity-data.com/topher/2018/November/5be7eb6f_processed-celeba-small/processed-celeba-small.zip" target="_blank">Data Set</a> .

---

## Understanding_data
- Since the project's main focus is on building the GANs, we've done some of the pre-processing for you.
- Each of the CelebA images has been cropped to remove parts of the image that don't include a face, then resized down to 64x64x3 NumPy images. 
- This pre-processed dataset is a smaller subset of the very large CelebA data.

## Data_Cleaning
- We are using transform function to resize and crop the image into 32x32 pixel
- batch size is also 32 and make a dataloder after that
- we rescale the image from -1 to 1

## Loading_batch
- Now we check our images of 1 bacth by calling iter method which gives generator of 1 batch
- by calling the imshow function we can see our batch images

### Model Architecture
##  Generator
- The goal is to get the generator to create fake images that are convincing enough to trick the discriminator into thinking that they're real. 
- the generator has to craft a coloured photo that's realistic-looking enough for the discriminator to believe it's a genuine photo like the ones it's seen in the training data

##  discriminator 
- the generator is terrible and the discriminator can easily tell it has done a bad job.
- Over time, however, with more training, the generator manages to fool the discriminator. 

## now after writing the both the method its time for training and generates some image and check the loss of both the model and see how well they perform
