# RandomShuffle

---

## tensorflow C++ API

[tensorflow::ops::RandomShuffle](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/random-shuffle)

Randomly shuffles a tensor along its first dimension.

---

## Summary

The tensor is shuffled along dimension 0, such that each `value[j]` is mapped to one and only one `output[i]`. For example, a mapping that might occur for a 3x2 tensor is:

\`\`\` \[\[1, 2\], \[\[5, 6\], \[3, 4\], ==&gt; \[1, 2\], \[5, 6\]\] \[3, 4\]\] \`\`\`

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* value: The tensor to be shuffled.

Optional attributes \(see [`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/random-shuffle/attrs.html#structtensorflow_1_1ops_1_1_random_shuffle_1_1_attrs)\):

* seed: If either `seed` or `seed2` are set to be non-zero, the random number generator is seeded by the given seed. Otherwise, it is seeded by a random seed.
* seed2: A second seed to avoid seed collision.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)
  : A tensor of same shape and type as `value`, shuffled along its first dimension.

---

## RandomShuffle block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_random.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input shape: connect  Input node.
* DataType dtype: Input DataType in value. ex\)DT\_DOUBLE;
* RandomShuffle ::Attrs attrs : Input attrs in value. ex\) seed\_ = 0;seed2\_ = 0;

Return:

* Output output : Output object of RandomNormal class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method



