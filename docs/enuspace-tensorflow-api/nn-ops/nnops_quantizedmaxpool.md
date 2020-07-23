--- 
layout: default 
title: QuantizedMaxPool 
parent: nn_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# QuantizedMaxPool

---

## tensorflow C++ API

[tensorflow::ops::QuantizedMaxPool](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/quantized-max-pool)

Produces the max pool of the input tensor for quantized types.

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* input: The 4D \(batch x rows x cols x depth\) [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) to MaxReduce over.
* min\_input: The float value that the lowest quantized input value represents.
* max\_input: The float value that the highest quantized input value represents.
* ksize: The size of the window for each dimension of the input tensor. The length must be 4 to match the number of dimensions of the input.
* strides: The stride of the sliding window for each dimension of the input tensor. The length must be 4 to match the number of dimensions of the input.
* padding: The type of padding algorithm to use.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)output 
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)min\_output: The float value that the lowest quantized output value represents.
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)max\_output: The float value that the highest quantized output value represents.

---

## QuantizedMaxPool block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_nn.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input filter: connect  Input node.
* Input min\_input: connect  Input node.
* Input max\_input: connect  Input node.
* ArraySlice&lt; int&gt; ksize: input ksize in values. ex\)1,1,1,1
* ArraySlice&lt; int&gt; strides: input ksize in values. ex\)1,3,2,1
* stringpiece padding: input padding in value. ex\)SAME

Return:

* Output output: Output object of QuantizedMaxPool class object.
* Output min\_output: Output object of QuantizedMaxPool class object.
* Output max\_output: Output object of QuantizedMaxPool class object.

Result:

* std::vector\(Tensor\) result\_output  : Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_min\_output  : Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_max\_output  : Returned object of executed result by calling session.

---

## Using Method



