Score:    99.11%

Write your own definitions for within 20 words.

Convolution: The scanning of input image mutiple times by filter/kernal to get the features from image. 

Filters/Kernels: This helps to extracts features from input image by sliding over the image. The size of kernal is always 
smaller than size of image and calculated using dot product.

Epochs: This is number of time dataset is visited for passing full/batch size of data to network.

1x1 Convolution: The scanning/convolution of input image with 1X1 filter helps to reduce the number of parameters by keeping the height and width same. 64X64X256 image can be decreased to 32 channel output by using 1X1X256X32 filters which gives output 64X64X32.

3x3 Convolution: The scanning/convolution of input image with 3 X 3 filter helps to extract information like vertical and horizontal edges. 3 X 3 which is odd number features extractor are used for maintaining symmetry on all sides and computationally efficient.
3 X 3 contains 9 parameters which mean 9 operations are used.

Feature Maps: This is collection features obtained obtained during convolution(sliding the filter/kernel over the image).

Activation Function: The function  which breaks the linearity to obtain desired(O/P) feature .

Receptive Field: The current scanning/convolved area of the input layer contributing to one pixel of the next layer. Local receptive field is the size of the kernel where Global is entire image.
