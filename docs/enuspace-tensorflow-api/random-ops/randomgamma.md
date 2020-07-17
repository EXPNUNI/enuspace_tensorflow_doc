# RandomGamma

---

## tensorflow C++ API

[tensorflow::ops::RandomGamma](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/random-gamma)

Outputs random values from the Gamma distribution\(s\) described by alpha.

---

## Summary

This op uses the algorithm by Marsaglia et al. to acquire samples via transformation-rejection from pairs of uniform and normal random variables. See [http://dl.acm.org/citation.cfm?id=358414](http://dl.acm.org/citation.cfm?id=358414)

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* shape: 1-D integer tensor. 
  [Shape](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/shape.html#classtensorflow_1_1ops_1_1_shape) of independent samples to draw from each distribution described by the shape parameters given in alpha.
* alpha: A tensor in which each scalar is a "shape" parameter describing the associated gamma distribution.

Optional attributes \(see [`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/random-gamma/attrs.html#structtensorflow_1_1ops_1_1_random_gamma_1_1_attrs)\):

* seed: If either `seed` or `seed2` are set to be non-zero, the random number generator is seeded by the given seed. Otherwise, it is seeded by a random seed.
* seed2: A second seed to avoid seed collision.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): A tensor with shape `shape + shape(alpha)`. Each slice `[:, ..., :, i0, i1, ...iN]`
   contains the samples drawn for `alpha[i0, i1, ...iN]`. The dtype of the output matches the dtype of alpha.

---

## RandomGamma block

Source link :[ https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_random.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

![](/assets/random_op/RandomGamma1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input shape: connect  Input node.
* Input alpha: connect Input node.
* RandomGamma ::Attrs attrs : Input attrs in value. ex\) seed\_ = 0;seed2\_ = 0;

Return:

* Output output : Output object of RandomGamma class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/random_op/RandomGamma2.jpg)

