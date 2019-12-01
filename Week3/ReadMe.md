# Final Validation accuracy for Base Network   82.43

# Final Validation accuracy for Assignment Network    82.29

# Your model definition (model.add... ) with output channel size and receptive field

modelNew = Sequential()

modelNew.add(SeparableConv2D(48, 3, 3, border_mode='same', input_shape=(32, 32, 3)))  # output(32,32,48) R.F(3,3),K.size(3,3,1)
modelNew.add(BatchNormalization()) 
modelNew.add(Activation('relu')) 

modelNew.add(SeparableConv2D(48, 3, 3)) # output(30,30,48) R.F(5,5),K.size(3,3,1)
modelNew.add(BatchNormalization())
modelNew.add(Activation('relu'))

modelNew.add(MaxPooling2D(pool_size=(2, 2))) # output(15,15,48) R.F(10,10)
modelNew.add(Dropout(0.2))

modelNew.add(SeparableConv2D(96, 3, 3, border_mode='same')) # output(15,15,96) R.F(12,12),K.size(3,3,1)
modelNew.add(BatchNormalization())
modelNew.add(Activation('relu'))

modelNew.add(SeparableConv2D(96, 3, 3)) # output(13,13,96) R.F(14,14),K.size(3,3,1)
modelNew.add(BatchNormalization())
modelNew.add(Activation('relu'))

modelNew.add(MaxPooling2D(pool_size=(2, 2))) # output(6,6,96) R.F(28,28)
modelNew.add(Dropout(0.2))

modelNew.add(SeparableConv2D(192, 3, 3, border_mode='same')) # output(6,6,192) R.F(30,30),K.size(3,3,1)
modelNew.add(BatchNormalization())
modelNew.add(Activation('relu'))

modelNew.add(SeparableConv2D(192, 3, 3)) # output(4,4,192) R.F(32,32),K.size(3,3,1)
modelNew.add(BatchNormalization())
modelNew.add(Activation('relu'))

modelNew.add(MaxPooling2D(pool_size=(2, 2))) # output(2,2,192) R.F(64,64),K.size(3,3,1)
modelNew.add(Dropout(0.2))

modelNew.add(SeparableConv2D(num_classes, 4, border_mode='same')) 

modelNew.add(GlobalAveragePooling2D())
modelNew.add(Activation('softmax')) 

# Compile the modelNew
modelNew.compile(loss='categorical_crossentropy', optimizer='adam', metrics=['accuracy'])
modelNew.summary()

Parameters details:

Total params: 84,277
Trainable params: 82,933
Non-trainable params: 1,344

Your 50 epoch logs

Epoch 1/50
390/390 [==============================] - 30s 76ms/step - loss: 1.4775 - acc: 0.4613 - val_loss: 1.6336 - val_acc: 0.4440
Epoch 2/50
390/390 [==============================] - 27s 68ms/step - loss: 1.0727 - acc: 0.6180 - val_loss: 1.0009 - val_acc: 0.6494
Epoch 3/50
390/390 [==============================] - 27s 69ms/step - loss: 0.9300 - acc: 0.6714 - val_loss: 0.8905 - val_acc: 0.6911
Epoch 4/50
390/390 [==============================] - 27s 69ms/step - loss: 0.8370 - acc: 0.7050 - val_loss: 0.8442 - val_acc: 0.7012
Epoch 5/50
390/390 [==============================] - 27s 69ms/step - loss: 0.7707 - acc: 0.7267 - val_loss: 0.7895 - val_acc: 0.7256
Epoch 6/50
390/390 [==============================] - 27s 69ms/step - loss: 0.7209 - acc: 0.7467 - val_loss: 0.8734 - val_acc: 0.7073
Epoch 7/50
390/390 [==============================] - 27s 69ms/step - loss: 0.6852 - acc: 0.7594 - val_loss: 0.7331 - val_acc: 0.7467
Epoch 8/50
390/390 [==============================] - 27s 69ms/step - loss: 0.6538 - acc: 0.7697 - val_loss: 0.6939 - val_acc: 0.7579
Epoch 9/50
390/390 [==============================] - 27s 69ms/step - loss: 0.6232 - acc: 0.7807 - val_loss: 0.7576 - val_acc: 0.7483
Epoch 10/50
390/390 [==============================] - 27s 69ms/step - loss: 0.6038 - acc: 0.7871 - val_loss: 0.9084 - val_acc: 0.6995
Epoch 11/50
390/390 [==============================] - 27s 68ms/step - loss: 0.5819 - acc: 0.7960 - val_loss: 0.8364 - val_acc: 0.7222
Epoch 12/50
390/390 [==============================] - 27s 69ms/step - loss: 0.5656 - acc: 0.7997 - val_loss: 0.6569 - val_acc: 0.7725
Epoch 13/50
390/390 [==============================] - 27s 69ms/step - loss: 0.5504 - acc: 0.8052 - val_loss: 0.6245 - val_acc: 0.7908
Epoch 14/50
390/390 [==============================] - 27s 69ms/step - loss: 0.5353 - acc: 0.8092 - val_loss: 0.6225 - val_acc: 0.7861
Epoch 15/50
390/390 [==============================] - 27s 69ms/step - loss: 0.5213 - acc: 0.8162 - val_loss: 0.6312 - val_acc: 0.7840
Epoch 16/50
390/390 [==============================] - 27s 69ms/step - loss: 0.5091 - acc: 0.8196 - val_loss: 0.5794 - val_acc: 0.8055
Epoch 17/50
390/390 [==============================] - 27s 69ms/step - loss: 0.4963 - acc: 0.8235 - val_loss: 0.6400 - val_acc: 0.7832
Epoch 18/50
390/390 [==============================] - 27s 69ms/step - loss: 0.4818 - acc: 0.8283 - val_loss: 0.6412 - val_acc: 0.7821
Epoch 19/50
390/390 [==============================] - 27s 69ms/step - loss: 0.4759 - acc: 0.8313 - val_loss: 0.6901 - val_acc: 0.7676
Epoch 20/50
390/390 [==============================] - 27s 69ms/step - loss: 0.4636 - acc: 0.8369 - val_loss: 0.6418 - val_acc: 0.7891
Epoch 21/50
390/390 [==============================] - 27s 69ms/step - loss: 0.4532 - acc: 0.8409 - val_loss: 0.6862 - val_acc: 0.7795
Epoch 22/50
390/390 [==============================] - 27s 69ms/step - loss: 0.4505 - acc: 0.8410 - val_loss: 0.6034 - val_acc: 0.7904
Epoch 23/50
390/390 [==============================] - 27s 69ms/step - loss: 0.4379 - acc: 0.8470 - val_loss: 0.7449 - val_acc: 0.7685
Epoch 24/50
390/390 [==============================] - 27s 69ms/step - loss: 0.4273 - acc: 0.8482 - val_loss: 0.6025 - val_acc: 0.7965
Epoch 25/50
390/390 [==============================] - 27s 68ms/step - loss: 0.4239 - acc: 0.8492 - val_loss: 0.6000 - val_acc: 0.8045
Epoch 26/50
390/390 [==============================] - 27s 69ms/step - loss: 0.4183 - acc: 0.8520 - val_loss: 0.5848 - val_acc: 0.8051
Epoch 27/50
390/390 [==============================] - 27s 70ms/step - loss: 0.4072 - acc: 0.8545 - val_loss: 0.6453 - val_acc: 0.7937
Epoch 28/50
390/390 [==============================] - 27s 69ms/step - loss: 0.4080 - acc: 0.8552 - val_loss: 0.6125 - val_acc: 0.7990
Epoch 29/50
390/390 [==============================] - 27s 69ms/step - loss: 0.3920 - acc: 0.8595 - val_loss: 0.5894 - val_acc: 0.8128
Epoch 30/50
390/390 [==============================] - 27s 69ms/step - loss: 0.3941 - acc: 0.8598 - val_loss: 0.6021 - val_acc: 0.8111
Epoch 31/50
390/390 [==============================] - 27s 69ms/step - loss: 0.3893 - acc: 0.8602 - val_loss: 0.8240 - val_acc: 0.7530
Epoch 32/50
390/390 [==============================] - 27s 69ms/step - loss: 0.3748 - acc: 0.8659 - val_loss: 0.6220 - val_acc: 0.8013
Epoch 33/50
390/390 [==============================] - 27s 68ms/step - loss: 0.3775 - acc: 0.8641 - val_loss: 0.6057 - val_acc: 0.7983
Epoch 34/50
390/390 [==============================] - 27s 68ms/step - loss: 0.3684 - acc: 0.8686 - val_loss: 0.7795 - val_acc: 0.7713
Epoch 35/50
390/390 [==============================] - 27s 68ms/step - loss: 0.3638 - acc: 0.8680 - val_loss: 0.7751 - val_acc: 0.7686
Epoch 36/50
390/390 [==============================] - 27s 69ms/step - loss: 0.3600 - acc: 0.8699 - val_loss: 0.6179 - val_acc: 0.8018
Epoch 37/50
390/390 [==============================] - 27s 69ms/step - loss: 0.3574 - acc: 0.8723 - val_loss: 0.6140 - val_acc: 0.8036
Epoch 38/50
390/390 [==============================] - 27s 69ms/step - loss: 0.3497 - acc: 0.8752 - val_loss: 0.5724 - val_acc: 0.8166
Epoch 39/50
390/390 [==============================] - 27s 69ms/step - loss: 0.3458 - acc: 0.8744 - val_loss: 0.6103 - val_acc: 0.8103
Epoch 40/50
390/390 [==============================] - 27s 68ms/step - loss: 0.3380 - acc: 0.8779 - val_loss: 0.5911 - val_acc: 0.8092
Epoch 41/50
390/390 [==============================] - 27s 69ms/step - loss: 0.3397 - acc: 0.8773 - val_loss: 0.6687 - val_acc: 0.7880
Epoch 42/50
390/390 [==============================] - 27s 68ms/step - loss: 0.3355 - acc: 0.8782 - val_loss: 0.5819 - val_acc: 0.8181
Epoch 43/50
390/390 [==============================] - 27s 69ms/step - loss: 0.3319 - acc: 0.8800 - val_loss: 0.6382 - val_acc: 0.8005
Epoch 44/50
390/390 [==============================] - 27s 68ms/step - loss: 0.3294 - acc: 0.8809 - val_loss: 0.5627 - val_acc: 0.8227
Epoch 45/50
390/390 [==============================] - 27s 68ms/step - loss: 0.3236 - acc: 0.8843 - val_loss: 0.5870 - val_acc: 0.8187
Epoch 46/50
390/390 [==============================] - 27s 68ms/step - loss: 0.3150 - acc: 0.8862 - val_loss: 0.6159 - val_acc: 0.8043
Epoch 47/50
390/390 [==============================] - 27s 69ms/step - loss: 0.3205 - acc: 0.8867 - val_loss: 0.6127 - val_acc: 0.8004
Epoch 48/50
390/390 [==============================] - 27s 69ms/step - loss: 0.3137 - acc: 0.8873 - val_loss: 0.6162 - val_acc: 0.8175
Epoch 49/50
390/390 [==============================] - 27s 69ms/step - loss: 0.3150 - acc: 0.8854 - val_loss: 0.6120 - val_acc: 0.8134
Epoch 50/50
390/390 [==============================] - 27s 69ms/step - loss: 0.3110 - acc: 0.8883 - val_loss: 0.5947 - val_acc: 0.8229
Model took 1344.41 seconds to train
