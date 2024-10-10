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

## What is mean by Image Type
- Binary Image (1 bit gray scale), consist of values 0 for black and 1 for white. This is useful in black and white document scanning.
- Grayscale Image, represented by 2D array where each value varying from 0-255 ranging from black to white.
- Color Image, represented by 3D array, including multiple channels typically RGB.Each channel is a grayscale representing the intensity level of that color. One example of this Image Modes is RGB where the 3 channels representing Red, Green, and Blue with the value ranging from 0 to 255.

## Color Image Mode
An image mode determines the number of colors that can be displayed in an image and can also affect the file size of the image. Image modes represent the color space or the number of channels in an image. Some image modes include:
1. **RGB (Red, Green, Blue)**, most common for digital images, each channel represent Red, Green, and Blue.
2. **RGBA (Red, Green, Blue)**, most common for digital images, each channel represent Red, Green, and Blue.
3. **CMYK (Cyan, Magenta, Yellow, Key/Black)** , used in color printing it represent four of that color.
4. **Indexed (AKA Palette) Color**, uses a color pallete to represent the image. each pixel's color is an index into the palette.
5. **HSV (Hue, Saturation, Value)**, HSV is often used in computer vision and image processing tasks because it separates information from brightness, making certain operations more intuitive

## Convert Image Modes
To change the mode of an image, mode of the image defines tthe type and depth of a pixel in the image.
### Common Image Modes in Pillow
1. "1" (1-bit pixel, black and white, stored with one pixel per byte)
- Purpose: Creating binary images
- Application: Document scanning, simple graphics

2. "L" (8-bit pixels, grayscale)
- Purpose: For grayscale images where each pixel is represented by a single byte
- Application: Image processing tasks where color is not important, reducing image size.

3. "P" (8-bit pixels, mapped to any other mode using a color pallete)
- Purpose: For image with limited number of colors, up to 256
- ApplicationL Svaing storage space in image files, GIF images.

4. "RGB" (3x8-bit pixels, true color)
- Purpose: For standard true-color images with red, green, and blue channels.
- ApplicationL Most common for displaying images in full color.

5. "RGBA" (4x8-bit pixels, true color with transparency mask)
- Purpose: For true color with alpha for transparency.
- Application: Web graphics, icon, images with varying transparency.

6. "CMYK" (4x8-bit pixels, color separation)
- Purpose: For color printing.
- Application: Preparing images for printing processes.