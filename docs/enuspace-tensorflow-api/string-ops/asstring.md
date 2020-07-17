# AsString

---

## tensorflow C++ API

[tensorflow::ops::AsString](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/as-string)

Converts each entry in the given tensor to strings.

---

## Summary

Supports many numeric.

types and boolean.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Optional attributes \(see [`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/as-string/attrs.html#structtensorflow_1_1ops_1_1_as_string_1_1_attrs)\):

* precision: The post-decimal precision to use for floating point numbers. Only used if precision &gt; -1.
* scientific: Use scientific notation for floating point numbers.
* shortest: Use shortest representation \(either scientific or standard\) for floating point numbers.
* width: [Pad](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/pad.html#classtensorflow_1_1ops_1_1_pad) pre-decimal numbers to this width. Applies to both floating point and integer numbers. Only used if width &gt; -1.
* fill: The value to pad if width &gt; -1. 
  If empty, pads with spaces. Another typical value is '0'. String cannot be longer than 1 character.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The output tensor.

---

## AsString block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_string.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_string.cpp)

![](/assets/string_op/asString2.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input input: connect  Input node.
* AsString ::Attrs attrs : Input attrs in value. ex\) precision\_= -1;scientific\_= false;shortest\_= false;width\_= -1;fill\_ = ;

Return:

* Output output : Output object of AsString class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/string_op/asString1.jpg)

