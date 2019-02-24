# Tensorflow Issues

### Tensorflow `sess.run` runs slower and slower

Perhaps because of constantly adding more nodes to the graph, like:

```
pi = self.sess.run(tf.squeeze(tf.nn.softmax(self.pi)), feed_dict={self.s_: ob})
```

Move the defination of `softmax` and `squeeze` out of the loop will fix this.

reference: https://github.com/tensorflow/tensorflow/issues/1439

---

### `tf.squared_difference` runs extremely slow.

Perhaps because of the dimensions are not exactly the same, like `x` is `(None, 1)` and `y` is `(None,)`. 
This leads to unwilling automatic boardcasting.

---
