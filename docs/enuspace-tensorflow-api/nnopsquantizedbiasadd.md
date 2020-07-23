--- 
layout: default 
title: QuantizedBiasAdd 
parent: nn_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# QuantizedBiasAdd

---

## tensorflow C++ API

[tensorflow::ops::QuantizedBiasAdd](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/quantized-bias-add)

Adds [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) 'bias' to [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) 'input' for Quantized types.

---

## Summary

Broadcasts the values of bias on dimensions 0..N-2 of 'input'.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* bias: A 1D bias [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) with size matching the last dimension of 'input'.
* min\_input: The float value that the lowest quantized input value represents.
* max\_input: The float value that the highest quantized input value represents.
* min\_bias: The float value that the lowest quantized bias value represents.
* max\_bias: The float value that the highest quantized bias value represents.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)output 
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)min\_out: The float value that the lowest quantized output value represents.
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)max\_out: The float value that the highest quantized output value represents.

---

## QuantizedBiasAdd block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_nn.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input bias: connect  Input node.
* Input min\_input: connect  Input node.
* Input max\_input: connect  Input node.
* Input min\_bias: connect  Input node.
* Input max\_bias: connect  Input node.

Return:

* Output output: Output object of QuantizedBiasAdd class object.
* Output min\_output: Output object of QuantizedBiasAdd class object.
* Output max\_output: Output object of QuantizedBiasAdd class object.

Result:

* std::vector\(Tensor\) result\_output  : Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_min\_output  : Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_max\_output  : Returned object of executed result by calling session.

---

## Using Method



