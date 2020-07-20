# Multinomial

---

## tensorflow C++ API

[tensorflow::ops::Multinomial](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/multinomial)

Draws samples from a multinomial distribution.

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

* logits: 2-D [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) with shape`[batch_size, num_classes]`. Each slice`[i, :]`  
  represents the unnormalized log probabilities for all classes.

* num\_samples: 0-D. Number of independent samples to draw for each row slice.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/multinomial/attrs)\):

* seed: If either seed or seed2 is set to be non-zero, the internal random number generator is seeded by the given seed. Otherwise, a random seed is used.
* seed2: A second seed to avoid seed collision.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): 2-D [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) with shape`[batch_size, num_samples]`. Each slice `[i, :]`
  contains the drawn class labels with range`[0, num_classes)`
  .

---

## Multinomial block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_random.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

![](/assets/random_op/multinomal1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input logits : connect  Input node.
* Input num\_samples : connect Input node.
* Multinomial ::Attrs attrs : Input attrs in value. ex\) seed\_ = 0;seed2\_ = 0;

Return:

* Output output : Output object of Multinomial class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/random_op/multinomal2.jpg)

