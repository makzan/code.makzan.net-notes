---
title: Basic MNIST Hand-written Digits Classification
tags:
  - Python
  - Machine Learning
  - TensorFlow
emoji: 🤖
created: 2021-07-21
modified: 2021-07-21
---

The example code was originally from [DeepLearning.ai](https://www.deeplearning.ai/program/tensorflow-developer-professional-certificate/). It shows the basic setup to classify hand-written digits.

```python
import tensorflow as tf

# Accuracy callback
class myCallback(tf.keras.callbacks.Callback):
    def on_epoch_end(self, epoch, logs={}):
        if logs.get('acc') > 0.99:
            self.model.stop_training = True


mnist = tf.keras.datasets.mnist
(x_train, y_train),(x_test, y_test) = mnist.load_data()

x_train = x_train/255.0
x_test = x_test/255.0

model = tf.keras.models.Sequential([
    tf.keras.layers.Flatten(),
    tf.keras.layers.Dense(512, activation=tf.nn.relu),
    tf.keras.layers.Dense(10, activation=tf.nn.softmax)    
])

model.compile(optimizer='adam',
              loss='sparse_categorical_crossentropy',
              metrics=['accuracy'])

# model fitting
history = model.fit( x_train, y_train, 
                    epochs=10,
                    callbacks=[myCallback()]


# result
print( history.epoch, history.history['acc'][-1] )
```