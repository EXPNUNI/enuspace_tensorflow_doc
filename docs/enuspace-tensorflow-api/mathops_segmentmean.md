--- 
layout: default 
title: SegmentMean 
parent: math_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# SegmentMean

---

## tensorflow C++ API

[tensorflow::ops::SegmentMean](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/segment-mean)

Computes the mean along segments of a tensor.

---

## Summary

Read the section on segmentation for an explanation of segments.

Computes a tensor such that output\_i = { data\_j}{N} where`mean`is over`j`such that`segment_ids[j] == i`and`N`is the total number of values summed.

If the mean is empty for a given segment ID`i`,`output[i] = 0`.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* segment\_ids: A 1-D tensor whose rank is equal to the rank of data's first dimension. Values should be sorted and can be repeated.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): Has same shape as data, except for dimension 0 which has size`k`, the number of segments.

Constructor

* SegmentMean\(const ::tensorflow::Scope & scope, ::tensorflow::Input data, ::tensorflow::Input segment\_ids\) 

Public attributes

* tensorflow::Output output.

---

## SegmentMean block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](./assets/math_SegmentMean_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input data:connect  Input node.
* Input segment\_ids:connect  Input node.

Return:

* Output output: Output object of SegmentMean class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](./assets/math_SegmentMean_Method.png)

