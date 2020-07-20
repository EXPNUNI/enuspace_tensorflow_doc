# StringJoin

---

## tensorflow C++ API

[tensorflow::ops::StringJoin](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/string-join)

Joins the strings in the given list of string tensors into one tensor;.

---

## Summary

with the given separator \(default is an empty separator\).

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* inputs: A list of string tensors. The tensors must all have the same shape, or be scalars. Scalars may be mixed in; these will be broadcast to the shape of non-scalar inputs.

Optional attributes \(see [`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/string-join/attrs.html#structtensorflow_1_1ops_1_1_string_join_1_1_attrs)\):

* separator: string, an optional join separator.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The output tensor.

---

## [StringJoin](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/string-join) block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_string.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_string.cpp)

![](/assets/string_op/StringJoin2.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input inputs: connect  Input node.
* StringJoin::Attrs attrs : Input attrs in value. ex\) separator\_ = ;

Return:

* Output output : Output object of StringJoin class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/string_op/StringJoin1.jpg)

