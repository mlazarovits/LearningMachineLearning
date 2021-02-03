---
title: "2/2/21: Competition Details"
---
Hey everyone!

For those of you who showed up to the meeting today, this will just be review, but here is the overview of LML's coding competition!

We will be using the fasion dataset from Tensorflow, and I will paste code below to access this data, assuming you have Tensorflow installed on your computer. The only restriction we're placing on you is that your network can only have Dense layers, as a CNN will always have an accuracy of 100% with this dataset. I have attached the notebooks from Chris's talk today, and I STRONGLY recommend you take a look at it, as he has a lot of examples that may inspire you. 

When you feel that you have trained your network to a satisfactory degree, save it to a file and send it to Margaret and me. The team with the best F1 score wins. An example of how to do this was covered in Chris's talk, but really, it's as simple as inputting this line of code: model.save("file_name.h5"). The Jupyter notebook from his talk can be found [here](../../../assets/SpringKickoff21/NeuralNetworks.ipynb).

The deadline for submitting these is Friday (2/5) at Noon CST. The winning team will be announced during our meeting later that day.

Good luck everyone! I'm excited to see what you all come up with.

Best,
Jackson


Here is the code, as promised:
(x_train, y_train), (x_test, y_test) = tf.keras.datasets.fashion_mnist.load_data()

x_train = x_train.reshape(60000, 784)
x_test = x_test.reshape(10000, 784)
x_train = x_train.astype('float32')
x_test = x_test.astype('float32')

y_train = tf.keras.utils.to_categorical(y_train, 10)
y_test = tf.keras.utils.to_categorical(y_test, 10)