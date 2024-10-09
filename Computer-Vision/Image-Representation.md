# Image Representation

## What's an Image?
Lets say an image has the resolution of 100 x 200 this would imply our image is represented as grid of pixels, with 100 rows and 200 columns with the total of 100 x 200 = 20,000 pixels in our image.

## Understanding Image Data
When working with digital image in computer vision, it is important to understand how image is structured and  stored. Here are some concepts:
- Image Array: in python it is usually represented in multi-dimensional arrays using libraries like NumPy. Each element in the array corresponds to a pixel value.
- Channel: for color images. Each channel represents the intensity values for one color component. Most formats have three color "channels": Red, Green, and Blue (some of it even has the fourth channel which is alpha that control transparency). For each pixel in an image, there is a value for every channel.
<br>
This is basically representing the data in a three-dimen sional matrix. The width of the matrix is the width of the image, the height of the matrix is the height of the image and the depth of the matrix is the number of channels. When we have an image with 100 x 100 pixels in size, this means the underlying data is a matrix with the dimension 100 x 100 x 3.

## What is mean by Pixel?
The smalles unit for digital image, any point of it is correspond to the intensity of the light photons striking at that point. Each pixel has unique logical address, a sie of eight bits or more depending on the color system gray or color. In a grayscale image, each pixel have value between 0 and 255, where 0 mean "black" and 255 corresponds 'white". The value between 0 and 255 are varying shades og gray.
