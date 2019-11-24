Assignment - 2
------------------------------------------------------------------------------------------------------------------------------
A. Logs:

Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 10s 172us/step - loss: 0.3830 - acc: 0.9278 - val_loss: 0.0852 - val_acc: 0.9826
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 6s 92us/step - loss: 0.1078 - acc: 0.9805 - val_loss: 0.0586 - val_acc: 0.9878
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 6s 92us/step - loss: 0.0744 - acc: 0.9846 - val_loss: 0.0390 - val_acc: 0.9909
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 5s 90us/step - loss: 0.0593 - acc: 0.9866 - val_loss: 0.0335 - val_acc: 0.9918
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 5s 90us/step - loss: 0.0519 - acc: 0.9883 - val_loss: 0.0283 - val_acc: 0.9920
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 5s 90us/step - loss: 0.0440 - acc: 0.9895 - val_loss: 0.0305 - val_acc: 0.9916
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 5s 89us/step - loss: 0.0416 - acc: 0.9899 - val_loss: 0.0273 - val_acc: 0.9922
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 5s 89us/step - loss: 0.0379 - acc: 0.9905 - val_loss: 0.0232 - val_acc: 0.9936
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 5s 89us/step - loss: 0.0343 - acc: 0.9913 - val_loss: 0.0260 - val_acc: 0.9926
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 5s 89us/step - loss: 0.0321 - acc: 0.9919 - val_loss: 0.0244 - val_acc: 0.9934
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 5s 90us/step - loss: 0.0311 - acc: 0.9916 - val_loss: 0.0210 - val_acc: 0.9946
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 5s 91us/step - loss: 0.0302 - acc: 0.9922 - val_loss: 0.0228 - val_acc: 0.9936
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 5s 89us/step - loss: 0.0283 - acc: 0.9924 - val_loss: 0.0206 - val_acc: 0.9942
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 5s 90us/step - loss: 0.0273 - acc: 0.9924 - val_loss: 0.0196 - val_acc: 0.9945
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 5s 89us/step - loss: 0.0269 - acc: 0.9928 - val_loss: 0.0185 - val_acc: 0.9946
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 5s 90us/step - loss: 0.0250 - acc: 0.9931 - val_loss: 0.0185 - val_acc: 0.9952
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 5s 89us/step - loss: 0.0249 - acc: 0.9930 - val_loss: 0.0175 - val_acc: 0.9952
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 5s 89us/step - loss: 0.0233 - acc: 0.9937 - val_loss: 0.0194 - val_acc: 0.9949
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 5s 89us/step - loss: 0.0223 - acc: 0.9939 - val_loss: 0.0179 - val_acc: 0.9943
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 5s 91us/step - loss: 0.0222 - acc: 0.9937 - val_loss: 0.0186 - val_acc: 0.9945
[0.01860527147529647, 0.9945]

B. Score:
Score:    99.45%

C. Strategy:

a. To reduce the parameter count below 15000: This is achieved by reducing numer of channels from 32 to 16 in Layer 2 in First Conv Block.

b. To achieve the accuracy of 99.45 or above : By reducing number of parameters as mentioned in a section C-A and increasing dropout to 0.2, better performance in terms of accuracy and training time is achieved.

c. With GlobalAveragePooling in place of flatten, accuracy is slightly increasd to 99.46(refer solution 2)

------------------------------------------------------------------------------------------------------------------------------
Assignment - 1
------------------------------------------------------------------------------------------------------------------------------

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


