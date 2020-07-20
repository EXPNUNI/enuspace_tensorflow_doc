# ReduceJoin

---

## tensorflow C++ API

[tensorflow::ops::ReduceJoin](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/reduce-join)

Joins a string [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) across the given dimensions.

---

## Summary

Computes the string join across dimensions in the given string [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) of shape `[d_0, d_1, ..., d_n-1]`. Returns a new [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) created by joining the input strings with the given separator \(default: empty string\). Negative indices are counted backwards from the end, with `-1` being equivalent to `n - 1`.

For example:

\``python`

`tensor`a\` is \[\["a", "b"\], \["c", "d"\]\]

tf.reduce\_join\(a, 0\) ==&gt; \["ac", "bd"\]

tf.reduce\_join\(a, 1\) ==&gt; \["ab", "cd"\]

tf.reduce\_join\(a, -2\) = tf.reduce\_join\(a, 0\) ==&gt; \["ac", "bd"\]

tf.reduce\_join\(a, -1\) = tf.reduce\_join\(a, 1\) ==&gt; \["ab", "cd"\]

tf.reduce\_join\(a, 0, keep\_dims=True\) ==&gt; \[\["ac", "bd"\]\]

tf.reduce\_join\(a, 1, keep\_dims=True\) ==&gt; \[\["ab"\], \["cd"\]\]

tf.reduce\_join\(a, 0, separator="."\) ==&gt; \["a.c", "b.d"\]

tf.reduce\_join\(a, \[0, 1\]\) ==&gt; \["acbd"\] tf.reduce\_join\(a, \[1, 0\]\) ==&gt; \["abcd"\]

tf.reduce\_join\(a, \[\]\) ==&gt; \["abcd"\] \`\`\`

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* inputs: The input to be joined. [All](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/all.html#classtensorflow_1_1ops_1_1_all) reduced indices must have non-zero size.
* reduction\_indices: The dimensions to reduce over. Dimensions are reduced in the order specified. Omitting `reduction_indices` is equivalent to passing `[n-1, n-2, ..., 0]`. Negative indices from `-n` to `-1` are supported.

Optional attributes \(see [`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/reduce-join/attrs.html#structtensorflow_1_1ops_1_1_reduce_join_1_1_attrs)\):

* keep\_dims: If `True`, retain reduced dimensions with length `1`.
* separator: The separator to use when joining.

Returns :

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): Has shape equal to that of the input with reduced dimensions removed or set to `1` depending on `keep_dims`.

---

## ReduceJoin block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_string.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_string.cpp)

![](/assets/ReduceJoin1.jpg)![](/assets/ReduceJoin1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input input: connect  Input node.
* Input reduction\_indices: connect  Input node.
* ReduceJoin::Attrs attrs : Input attrs in value. ex\) keep\_dims\_ = false;separator\_ =;

Return:

* Output output : Output object of ReduceJoin class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/string_op/ReduceJoin2.jpg)

