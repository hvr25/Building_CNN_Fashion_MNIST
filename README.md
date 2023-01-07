# Building_CNN_Fashion_MNIST

Fashion-MNIST consists of a training set of 60,000 examples and a test set of 10,000 examples. Each example is a 28x28 grayscale image, associated with a label from 10 classes. 
The classes are:

| Label  | Description |
| ------------- | ------------- |
| 0  | T-shirt/top  |
| 1  | Trouser  |
| 2  | Pullover  |
| 3  | Dress  |
| 4  | Coat  |
| 5  | Sandal  |
| 6 | Shirt |
| 7  | Sneaker |
| 8  | Bag  |
| 9  | Ankle boot  |

### Architecture Structure of CNN

| Layer (type)     |           Output Shape         |    Parameters  |
| ------------- | ------------- | ------------- |
 |conv2d_10 (Conv2D)    |      (None, 26, 26, 32)    |    320       |                                                             
| conv2d_11 (Conv2D)    |      (None, 24, 24, 64)    |    18496     |
|max_pooling2d_5 (MaxPooling 2D) | (None, 12, 12, 64)  |     0         |                                                                                                                        
 |dropout_10 (Dropout)    |   (None, 12, 12, 64)    |    0        |                                                                 
 |flatten_5 (Flatten)     |    (None, 9216)       |       0      |                                                                    
| dense_10 (Dense)         |  (None, 128)        |       1179776    |                                                                
| dropout_11 (Dropout)     |   (None, 128)        |       0          |                                                               
| dense_11 (Dense)        |    (None, 10)         |       1290   |   


Total params: 1,199,882

Trainable params: 1,199,882

Non-trainable params: 0


I have used EarlyStopping as improvement tool for this setup. This is one of the best tools to use for controlling when to stop fitting the model. 
I have configured EarlyStopping to monitor on loss. With this, the training stops when the loss begins to rise.
