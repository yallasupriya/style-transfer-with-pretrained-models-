Overview
   
Style transfer is a technique that takes two images—a content image and a style image—and blends them in such a way that the content image is transformed to appear as if it were painted in the style of the style image. 
This script uses a pretrained model from TensorFlow Hub to perform style transfer.

1)Key Components

TensorFlow and TensorFlow Hub: These libraries provide the tools necessary for deep learning and accessing pretrained models.
Matplotlib: A plotting library used to display images.
Pillow (PIL): A library for image processing.
Steps in the Script
Load and Preprocess Images:

The load_img function reads an image from a given file path, resizes it to a maximum dimension of 512 pixels while maintaining the aspect ratio, and normalizes the pixel values. 
The image is then expanded to include a batch dimension.
This ensures the images are in the correct format for the model.

2)Display Images:

The imshow function is a utility for displaying images using Matplotlib. It handles batch dimensions and optionally adds a title to the image.
The display_images function sets up a plot to display the content and stylized images side-by-side.

3)User Input:

The script prompts the user to enter the file paths for the content and style images.

4)Load Pretrained Model:

The script loads a pretrained style transfer model from TensorFlow Hub. The specific model used here is arbitrary-image-stylization-v1-256, which is capable of applying the style from one image to another.

5)Apply Style Transfer:

The model is applied to the content and style images. The output is the stylized image, which combines the content of the first image with the style of the second.

6)Display Results:

Finally, the display_images function is called to show the original content image and the resulting stylized image.
