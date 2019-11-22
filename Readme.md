Assignment - 2
------------------------------------------------------------------------------------------------------------------------------
A. Logs:

Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 12s 204us/step - loss: 0.4702 - acc: 0.9029 - val_loss: 0.1204 - val_acc: 0.9725
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 6s 99us/step - loss: 0.1369 - acc: 0.9729 - val_loss: 0.0532 - val_acc: 0.9855
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 6s 100us/step - loss: 0.0971 - acc: 0.9788 - val_loss: 0.0509 - val_acc: 0.9868
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 6s 100us/step - loss: 0.0785 - acc: 0.9813 - val_loss: 0.0430 - val_acc: 0.9881
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 6s 100us/step - loss: 0.0693 - acc: 0.9829 - val_loss: 0.0350 - val_acc: 0.9906
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 6s 99us/step - loss: 0.0612 - acc: 0.9845 - val_loss: 0.0294 - val_acc: 0.9917
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 6s 98us/step - loss: 0.0565 - acc: 0.9858 - val_loss: 0.0340 - val_acc: 0.9910
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 6s 99us/step - loss: 0.0523 - acc: 0.9866 - val_loss: 0.0300 - val_acc: 0.9917
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 6s 99us/step - loss: 0.0499 - acc: 0.9867 - val_loss: 0.0368 - val_acc: 0.9897
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 6s 97us/step - loss: 0.0475 - acc: 0.9873 - val_loss: 0.0282 - val_acc: 0.9918
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 6s 98us/step - loss: 0.0463 - acc: 0.9875 - val_loss: 0.0327 - val_acc: 0.9911
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 6s 100us/step - loss: 0.0430 - acc: 0.9878 - val_loss: 0.0240 - val_acc: 0.9926
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 6s 99us/step - loss: 0.0425 - acc: 0.9885 - val_loss: 0.0279 - val_acc: 0.9913
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 6s 98us/step - loss: 0.0409 - acc: 0.9884 - val_loss: 0.0241 - val_acc: 0.9931
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 6s 100us/step - loss: 0.0413 - acc: 0.9886 - val_loss: 0.0237 - val_acc: 0.9933
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 6s 99us/step - loss: 0.0382 - acc: 0.9886 - val_loss: 0.0233 - val_acc: 0.9935
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 6s 100us/step - loss: 0.0374 - acc: 0.9894 - val_loss: 0.0251 - val_acc: 0.9932
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 6s 99us/step - loss: 0.0368 - acc: 0.9897 - val_loss: 0.0229 - val_acc: 0.9938
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 6s 100us/step - loss: 0.0362 - acc: 0.9898 - val_loss: 0.0222 - val_acc: 0.9936
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 6s 99us/step - loss: 0.0356 - acc: 0.9893 - val_loss: 0.0220 - val_acc: 0.9941
<keras.callbacks.History at 0x7fbaa9a22668>

B. Score:
Score:    99.41%

C. Strategy:

a. To reduce the parameter count to 15000: This is achieved by reducing numer of channels from 32 to 16 in Layer 2 in First Conv Block.

b. To achieve the accuracy of 99.4 or above : By reducing number of parameters as mentioned in a section, better performance in terms of accuracy and time is achieved.

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


