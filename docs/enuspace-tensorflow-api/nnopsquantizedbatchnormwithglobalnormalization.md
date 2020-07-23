--- 
layout: default 
title: QuantizedBatchNormWithGlobalNormalization 
parent: nn_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# QuantizedBatchNormWithGlobalNormalization

---

## tensorflow C++ API

[tensorflow::ops::QuantizedBatchNormWithGlobalNormalization](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/quantized-batch-norm-with-global-normalization)

Quantized Batch normalization.

---

## Summary

This op is deprecated and will be removed in the future. Prefer`tf.nn.batch_normalization`.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* t: A 4D input [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor).
* t\_min: The value represented by the lowest quantized input.
* t\_max: The value represented by the highest quantized input.
* m: A 1D mean [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) with size matching the last dimension of t. This is the first output from tf.nn.moments, or a saved moving average thereof.
* m\_min: The value represented by the lowest quantized mean.
* m\_max: The value represented by the highest quantized mean.
* v: A 1D variance [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) with size matching the last dimension of t. This is the second output from tf.nn.moments, or a saved moving average thereof.
* v\_min: The value represented by the lowest quantized variance.
* v\_max: The value represented by the highest quantized variance.
* beta: A 1D beta [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) with size matching the last dimension of t. An offset to be added to the normalized tensor.
* beta\_min: The value represented by the lowest quantized offset.
* beta\_max: The value represented by the highest quantized offset.
* gamma: A 1D gamma [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) with size matching the last dimension of t. If "scale\_after\_normalization" is true, this tensor will be multiplied with the normalized tensor.
* gamma\_min: The value represented by the lowest quantized gamma.
* gamma\_max: The value represented by the highest quantized gamma.
* variance\_epsilon: A small float number to avoid dividing by 0.
* scale\_after\_normalization: A bool indicating whether the resulted tensor needs to be multiplied with gamma.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)result
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)result\_min
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)result\_max

---

## QuantizedAvgPool block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_nn.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input t: connect  Input node.
* Input t\_min: connect  Input node.
* Input t\_max: connect  Input node.
* Input m: connect  Input node.
* Input m\_min: connect  Input node.
* Input m\_max: connect  Input node.
* Input v: connect  Input node.
* Input v\_min: connect  Input node.
* Input v\_max: connect  Input node.
* Input beta: connect  Input node.
* Input beta\_min: connect  Input node.
* Input beta\_max: connect  Input node.
* Input gamma: connect  Input node.
* Input gamma\_min: connect  Input node.
* Input gamma\_max: connect  Input node.
* DataType out\_type : input DataType in value.
* float variance\_epsilon: input float in value.
* bool scale\_after\_normalization: input bool in value.

Return:

* Output result: Output object of QuantizedAvgPool class object.
* Output result\_min: Output object of QuantizedAvgPool class object.
* Output result\_max: Output object of QuantizedAvgPool class object.

Result:

* std::vector\(Tensor\) result\_result : Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_result\_min  : Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_result\_max  : Returned object of executed result by calling session.

---

## Using Method



