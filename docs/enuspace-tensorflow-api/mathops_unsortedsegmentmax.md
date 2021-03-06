--- 
layout: default 
title: UnsortedSegmentMax 
parent: math_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# UnsortedSegmentMax

---

## tensorflow C++ API

[tensorflow::ops::SegmentMax](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/unsorted-segment-max)

Computes the maximum along segments of a tensor.

---

## Summary

Read the section on segmentation for an explanation of segments.

This operator is similar to the[unsorted segment sum operator](https://www.tensorflow.org/api_docs/cc/api_docs/python/math_ops.md#UnsortedSegmentSum). Instead of computing the sum over segments, it computes the maximum such that:

output\_i = data\_j where max is over`j`such that`segment_ids[j] == i`.

If the maximum is empty for a given segment ID`i`, it outputs the smallest possible value for specific numeric type,`output[i] = numeric_limits::min()`.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* segment\_ids: A 1-D tensor whose rank is equal to the rank of`data`'s first dimension.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): Has same shape as data, except for dimension 0 which has size`num_segments`.

Constructor

* UnsortedSegmentMax\(const ::tensorflow::Scope & scope, ::tensorflow::Input data, ::tensorflow::Input segment\_ids, ::tensorflow::Input num\_segments\) 

Public attributes

* tensorflow::Output output.

---

## UnsortedSegmentMax block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](./assets/math_UnsortedSegmentMax_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input data:connect  Input node.
* Input segment\_ids:connect  Input node.
* Input num\_segments : connect  Input node.

Return:

* Output output: Output object of UnsortedSegmentMax class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](./assets/math_UnsortedSegmentMax_Method.png)

