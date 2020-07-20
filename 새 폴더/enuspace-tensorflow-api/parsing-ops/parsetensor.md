# ParseTensor

---

## tensorflow C++ API

[tensorflow::ops::ParseTensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/parse-tensor)

Transforms a serialized tensorflow.TensorProto proto into a [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor).

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* serialized: A scalar string containing a serialized TensorProto proto.
* out\_type: The type of the serialized tensor. The provided type must match the type of the serialized tensor and no implicit conversion will take place.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) : A [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) of type `out_type`.

---

## ParseTensor block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_parsing\_op.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input serialized: connect  Input node.
* DataType  out\_type: Input DataType in value.

Return:

* Output output : Output object of ParseTensor class object.

Result:

* std::vector\(Tensor\) _result\_output_ : Returned object of executed result by calling session.

---

## Using Method



