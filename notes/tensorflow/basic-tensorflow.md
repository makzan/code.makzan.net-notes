---
title: Basic TensorFlow Setup
tags:
  - Python
  - Machine Learning
  - TensorFlow
emoji: 🤖
created: 2021-07-21
modified: 2021-07-21
---

The example code was originally from [DeepLearning.ai](https://www.deeplearning.ai/program/tensorflow-developer-professional-certificate/). It shows the very basic setup to get started using TensorFlow.

```python
import tensorflow as tf
import numpy as np

xs = np.array([1.0,2,3,4,5,6])
ys = np.array([1,1.5,2,2.5,3,3.5])

model = tf.keras.Sequential([
  tf.keras.layers.Dense(units=1, input_shape=[1])
])

model.compile(optimizer='sgd', loss='mean_squared_error')
model.fit(xs, ys, epochs=500)

print(model.predict([7.0]))
```