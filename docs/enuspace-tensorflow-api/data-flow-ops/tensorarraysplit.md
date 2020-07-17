# TensorArraySplit

---

## tensorflow C++ API

[tensorflow::ops::TensorArraySplit](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/tensor-array-split)

Split the data from the input value into TensorArray elements.

---

## Summary

Assuming that`lengths`takes on values

`(n0, n1, ..., n(T-1))`

and that`value`has shape

`(n0 + n1 + ... + n(T-1) x d0 x d1 x ...)`,

this splits values into a TensorArray with T tensors.

TensorArray index t will be the subtensor of values with starting position

`(n0 + n1 + ... + n(t-1), 0, 0, ...)`

and having size

`nt x d0 x d1 x ...`

Arguments:

* scope: A Scope object
* handle: The handle to a TensorArray.
* value: The concatenated tensor to write to the TensorArray.
* lengths: The vector of lengths, how to split the rows of value into the TensorArray.
* flow\_in: A float scalar that enforces proper chaining of operations.

Returns:

* Output : A float scalar that enforces proper chaining of operations.

Constructor

* TensorArraySplit\(const ::tensorflow::Scope & scope, ::tensorflow::Input handle, ::tensorflow::Input value, ::tensorflow::Input lengths, ::tensorflow::Input flow\_in\).

Public attributes

* tensorflow::Output flow\_out.

---

## TensorArraySplit block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_data\_flow\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_data_flow_ops.cpp)

![](/assets/dataflow_TensorArraySplit_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* handle : connect Input node.
* value : connect Input node or input tensor value.
* lengths : connect Input node or input length number array.
* flow\_in : connect Input node.

Return:

* Output flow\_out: Output object of TensorArraySplit class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/dataflow_TensorArraySplit_Method.png)

