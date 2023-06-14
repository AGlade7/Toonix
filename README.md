# Image Cartoonifier 

<img src="https://github.com/AGlade7/Toonix/blob/main/testimage.jpg" alt="Original_Image" width=25% height=25%> &emsp; &emsp; <img src="https://github.com/AGlade7/Toonix/blob/main/Cartoonized_Image.jpg" alt="Cartoonified_Image" width=25% height=25%>  

This Python project demonstrates how to cartoonify an image using popular libraries such as OpenCV, NumPy, and Matplotlib. The script takes an input image, applies a series of image processing techniques, and produces a cartoon-like version of the original image.

## Installation

To run this project, you need to have the following dependencies installed:

- Python (version 3.6 or higher)
- OpenCV (version 2 or higher)
- NumPy (version 1.19.3 or higher)
- Matplotlib (version 3.3.3 or higher)

To install the dependencies, you can use `pip`, the package installer for Python. Open your terminal or command prompt and run the following commands:  

    pip install opencv-python

    pip install numpy

    pip install matplotlib
  

## Usage

1. Clone the repository:
```
git clone https://github.com/AGlade7/Toonix.git
```
2. Navigate to the project directory:

3. Place the image you want to cartoonify in the project directory. Note that the image MUST be named `testimage.jpg`.

4. Open the Jupyter Notebook file in any IDE that supports running the file

5. Run all kernels of `Toonix.ipynb` file using the IDE.

6. The script will generate a cartoonified version of the input image and save it as `Cartoonized_Image.jpg` in the project directory.

## How it Works

The script follows these steps to cartoonify an image:

1. Read the input image using OpenCV.
2. Convert the image from the BGR color space to the RGB color space.
3. Now, the first part is to get the mask of the image, that is,  the edges.
   - Convert the image to grayscale.
   - Apply a median blur to further reduce noise.
   - Use adaptive thresholding to create a binary image. The binary image forms our edges.
4. The second component is the reduced color pallete of the image.
   - Convert image data to a suitable format.
   - Define criteria for K-Means clustering.
   - Apply K-Means clustering to group image pixels.
   - Obtain cluster centers and assign labels to pixels.
   - Reconstruct the image using the cluster centers.
   - Apply bilateral filtering for smoothing. 
5. Apply a bitwise_and operation to combine the binary image with the reduced color pallete image.
6. Save the resulting cartoonified image.
