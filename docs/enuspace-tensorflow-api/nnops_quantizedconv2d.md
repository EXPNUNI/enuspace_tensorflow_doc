--- 
layout: default 
title: QuantizedConv2D 
parent: nn_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# QuantizedConv2D

---

## tensorflow C++ API

[tensorflow::ops::QuantizedConv2D](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/quantized-conv2-d)

Computes a 2D convolution given quantized 4D input and filter tensors.

---

## Summary

The inputs are quantized tensors where the lowest value represents the real number of the associated minimum, and the highest represents the maximum. This means that you can only interpret the quantized output in the same way, by taking the returned minimum and maximum values into account.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* filter: filter's input\_depth dimension must match input's depth dimensions.
* min\_input: The float value that the lowest quantized input value represents.
* max\_input: The float value that the highest quantized input value represents.
* min\_filter: The float value that the lowest quantized filter value represents.
* max\_filter: The float value that the highest quantized filter value represents.
* strides: The stride of the sliding window for each dimension of the input tensor.
* padding: The type of padding algorithm to use.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)output
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)min\_output: The float value that the lowest quantized output value represents.
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)max\_output: The float value that the highest quantized output value represents.

---

## QuantizedConv2D block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_nn.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input filter: connect  Input node.
* Input min\_input: connect  Input node.
* Input max\_input: connect  Input node.
* Input min\_filter: connect  Input node.
* Input max\_filter: connect  Input node.
* ArraySlice&lt; int&gt; strides: input ksize in values. ex\)1,4,3,2,1
* stringpiece padding: input padding in value. ex\)SAME

Return:

* Output output: Output object of QuantizedConv2D class object.
* Output min\_output: Output object of QuantizedConv2D class object.
* Output max\_output: Output object of QuantizedConv2D class object.

Result:

* std::vector\(Tensor\) result\_output  : Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_min\_output  : Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_max\_output  : Returned object of executed result by calling session.

---

## Using Method



