# StringToNumber

---

## tensorflow C++ API

[tensorflow::ops::StringToNumber](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/string-to-number)

Converts each string in the input [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) to the specified numeric type.

---

## Summary

\(Note that int32 overflow results in an error while float overflow results in a rounded value.\)

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/string-to-number/attrs.html#structtensorflow_1_1ops_1_1_string_to_number_1_1_attrs)\):

* out\_type: The numeric type to interpret each string in `string_tensor`as.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) : A [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) of the same shape as the input `string_tensor`.

---

## StringToNumber block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_parsing\_op.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

![](/assets/parsing/StringToNumber1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input string\_tensor: connect  Input node.
* StringToNumber::Attrs  attrs: Input Attrs in value.

Return:

* Output output : Output object of ParseTensor class object.

Result:

* std::vector\(Tensor\) _result\_output_ : Returned object of executed result by calling session.

---

## Using Method

![](/assets/parsing/StringToNumber2.jpg)

