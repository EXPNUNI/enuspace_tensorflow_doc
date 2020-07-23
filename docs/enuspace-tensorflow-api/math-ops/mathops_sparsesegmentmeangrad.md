--- 
layout: default 
title: SparseSegmentMeanGrad 
parent: math_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# SparseSegmentMeanGrad

---

## tensorflow C++ API

[tensorflow::ops::SparseSegmentMeanGrad](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sparse-segment-mean-grad)

Computes gradients for [SparseSegmentMean](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sparse-segment-mean.html#classtensorflow_1_1ops_1_1_sparse_segment_mean).

---

## Summary

Returns tensor "output" with same shape as grad, except for dimension 0 whose value is output\_dim0.

Arguments:

* scope: A[Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* grad: gradient propagated to the [SparseSegmentMean](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sparse-segment-mean.html#classtensorflow_1_1ops_1_1_sparse_segment_mean) op.
* indices: indices passed to the corresponding [SparseSegmentMean](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sparse-segment-mean.html#classtensorflow_1_1ops_1_1_sparse_segment_mean) op.
* segment\_ids: segment\_ids passed to the corresponding [SparseSegmentMean](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sparse-segment-mean.html#classtensorflow_1_1ops_1_1_sparse_segment_mean) op.
* output\_dim0: dimension 0 of "data" passed to [SparseSegmentMean](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sparse-segment-mean.html#classtensorflow_1_1ops_1_1_sparse_segment_mean) op.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The output tensor.

Constructor

* SparseSegmentMeanGrad\(const ::tensorflow::Scope & scope, ::tensorflow::Input grad, ::tensorflow::Input indices, ::tensorflow::Input segment\_ids, ::tensorflow::Input output\_dim0\) 

Public attributes

* tensorflow::Output output 

---

## SparseSegmentMeanGrad block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](../assets/math_SparseSegmentMeanGrad_Symbol.png)

Argument:

* Scope scope : A Scope object\(A scope is generated automatically each page. A scope is not connected.\).
* Input data : connect  Input node.
* Input indices : connect  Input node.
* Input segment\_ids : connect Input node.
* Input output\_dim0 : connect Input node.

Return:

* Output product : Output object of SparseSegmentMeanGrad class object. 

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](../assets/math_SparseSegmentMeanGrad_Method.png)

