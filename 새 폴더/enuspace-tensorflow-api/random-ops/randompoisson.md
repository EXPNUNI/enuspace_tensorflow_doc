# RandomPoisson

---

## tensorflow C++ API

[tensorflow::ops::RandomPoisson](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/random-poisson)

Outputs random values from the Poisson distribution\(s\) described by rate.

---

## Summary

This op uses two algorithms, depending on rate. If rate &gt;= 10, then the algorithm by Hormann is used to acquire samples via transformation-rejection. See [http://www.sciencedirect.com/science/article/pii/0167668793909974](http://www.sciencedirect.com/science/article/pii/0167668793909974).

Otherwise, Knuth's algorithm is used to acquire samples via multiplying uniform random variables. See Donald E. Knuth \(1969\). Seminumerical Algorithms. The Art of Computer Programming, Volume 2. Addison Wesley

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* shape: 1-D integer tensor. 
  [Shape](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/shape.html#classtensorflow_1_1ops_1_1_shape) of independent samples to draw from each distribution described by the shape parameters given in rate.
* rate: A tensor in which each scalar is a "rate" parameter describing the associated poisson distribution.

Optional attributes \(see [`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/random-poisson/attrs.html#structtensorflow_1_1ops_1_1_random_poisson_1_1_attrs)\):

* seed: If either `seed` or `seed2` are set to be non-zero, the random number generator is seeded by the given seed. Otherwise, it is seeded by a random seed.
* seed2: A second seed to avoid seed collision.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)
  : A tensor with shape `shape + shape(rate)`. Each slice `[:, ..., :, i0, i1, ...iN]`
   contains the samples drawn for `rate[i0, i1, ...iN]`
  . The dtype of the output matches the dtype of rate.

---

## RandomPoisson block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_random.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

![](/assets/random_op/RandomPoisson2.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input shape: connect  Input node.
* Input rate: connect  Input node.
* RandomPoisson ::Attrs attrs : Input attrs in value. ex\) seed\_ = 0;seed2\_ = 0;

Return:

* Output output : Output object of RandomPoisson class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/random_op/RandomPoisson1.jpg)

