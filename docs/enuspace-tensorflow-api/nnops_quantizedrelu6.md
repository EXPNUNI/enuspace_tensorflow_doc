--- 
layout: default 
title: QuantizedRelu6 
parent: nn_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# QuantizedRelu6

---

## tensorflow C++ API

[tensorflow::ops::QuantizedRelu6](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/quantized-relu6)

Computes Quantized Rectified Linear 6:`min(max(features, 0), 6)`

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* min\_features: The float value that the lowest quantized value represents.
* max\_features: The float value that the highest quantized value represents.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)activations: Has the same output shape as "features".
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)min\_activations: The float value that the lowest quantized value represents.
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)max\_activations: The float value that the highest quantized value represents.

---

## QuantizedRelu6 block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_nn.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input min\_features: connect  Input node.
* Input max\_features: connect  Input node.
* QuantizedRelu6 ::Attrs attrs:input  QuantizedRelu6 ::Attrs in value. ex\)[out\_type\_](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/quantized-relu-x/attrs#structtensorflow_1_1ops_1_1_quantized_relu_x_1_1_attrs_1a7c41aaf8c42e0a8489da6d78d6f724c3)= DT\_QUINT8;

Return:

* Output activations: Output object of QuantizedRelu6 class object.
* Output min\_activations: Output object of QuantizedRelu6 class object.
* Output max\_activations: Output object of QuantizedRelu6 class object.

Result:

* std::vector\(Tensor\) result\_activations : Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_min\_activations  : Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_max\_activations  : Returned object of executed result by calling session.

---

## Using Method



