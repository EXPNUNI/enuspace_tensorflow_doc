# RandomUniform

---

## tensorflow C++ API

[tensorflow::ops::RandomUniform](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/random-uniform)

Outputs random values from a uniform distribution.

---

## Summary

The generated values follow a uniform distribution in the range `[0, 1)`. The lower bound 0 is included in the range, while the upper bound 1 is excluded.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* shape: The shape of the output tensor.
* dtype: The type of the output.

Optional attributes \(see [`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/random-uniform/attrs.html#structtensorflow_1_1ops_1_1_random_uniform_1_1_attrs)\):

* seed: If either `seed` or `seed2` are set to be non-zero, the random number generator is seeded by the given seed. Otherwise, it is seeded by a random seed.
* seed2: A second seed to avoid seed collision.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)
  : A tensor of the specified shape filled with uniform random values.

---

## RandomUniform block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_random.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

![](/assets/random_op/RandomUniform2.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input shape: connect  Input node.
* DataType dtype: Input DataType in Value. ex\)DT\_DOUBLE;
* RandomUniform::Attrs attrs : Input attrs in value. ex\) seed\_ = 0;seed2\_ = 0;

Return:

* Output output : Output object of RandomUniform class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/random_op/RandomUniform1.jpg)

