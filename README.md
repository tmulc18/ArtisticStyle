# ArtisticStyle
Artistic Style implementations from [A Neural Algorithm for Artistic Style](https://arxiv.org/abs/1508.06576)

![styleContent](images/basic2_2.gif)

## Weights
The weights for the pretrained models on Imagenet were taken from Keras and can be found [here](https://github.com/fchollet/deep-learning-models/releases/).  [VGG19](https://github.com/fchollet/deep-learning-models/releases/download/v0.1/vgg19_weights_tf_dim_ordering_tf_kernels_notop.h5)

Make sure the VGG19 no top h5 is in the root directory.

## Style Recontructions
Artistic Style Tensorflow (style).ipynb

![style gif](images/style2.gif)

For whatever level of style you want to generate, assign appropriate loss variable to the loss\_style variable in the graph declaration.  For example, if you want to generate content using conv1\_1, assign loss\_style to loss1.

If you want to create the images of the style reconstuction at the different stages of the networks, makesure to have the Style\<n\> folder in the root directory and uncomment the code in the training cell. 

## Content Recontructions
Artistic Style Tensorflow (content).ipynb

![content gif](images/content4.gif)

For whatever level of content you want to generate, assign appropriate loss variable to the loss\_content variable in the graph declaration.  For example, if you want to generate content using conv1\_1, assign loss\_content to loss1.

If you want to create the images of the style reconstuction at the different stages of the networks, makesure to have the Content\<n\> folder in the root directory and uncomment the code in the training cell. 

## Recreating gifs
To recreate the gifs from [my blog](https://www.hacktilldawn.com) make sure to have the appropriate images in the Content or Style folder and run the Image Stitching notebook with the appropriate folder name.  For example, if you want to generate the gif for content reconstruction at layer 2, change the parameter inside glob.glob in the second cells to say Content2/*.

## Requirements

Install [Anaconda](https://www.continuum.io/downloads) and use the provided env.yml to set up an environment with the required packages by running

`conda env create -f env.yml`

## [Presentation slides](https://drive.google.com/open?id=0B3NC6C-8OM5BeWtBWWx0X250UWM)
