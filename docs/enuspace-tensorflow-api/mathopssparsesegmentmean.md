--- 
layout: default 
title: SparseSegmentMean 
parent: math_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# SparseSegmentMean

---

## tensorflow C++ API

[tensorflow::ops::SparseSegmentMean](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sparse-segment-mean)

Computes the mean along sparse segments of a tensor.

---

## Summary

Read the section on segmentation for an explanation of segments.

Like[`SegmentMean`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/segment-mean.html#classtensorflow_1_1ops_1_1_segment_mean), but`segment_ids`can have rank less than`data`'s first dimension, selecting a subset of dimension 0, specified by`indices`.

Arguments:

* scope: A[Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* indices: A 1-D tensor. Has same rank as `segment_ids`.
* segment\_ids: A 1-D tensor. Values should be sorted and can be repeated.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): Has same shape as data, except for dimension 0 which has size`k`, the number of segments.

Constructor

* SparseSegmentMean\(const ::tensorflow::Scope & scope, ::tensorflow::Input data, ::tensorflow::Input indices, ::tensorflow::Input segment\_ids\) 

Public attributes

* tensorflow::Output output

---

## SparseSegmentMean block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](./assets/math_SparseSegmentMean_Symbol.png)

Argument:

* Scope scope : A Scope object\(A scope is generated automatically each page. A scope is not connected.\).
* Input data : connect  Input node.
* Input indices : connect  Input node.
* Input segment\_ids: connect Input node.

Return:

* Output product : Output object of SparseSegmentMean class object. 

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](./assets/math_SparseSegmentMean_Method.png)

