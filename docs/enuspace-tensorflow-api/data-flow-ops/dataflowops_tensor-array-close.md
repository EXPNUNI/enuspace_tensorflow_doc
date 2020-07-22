--- 
layout: default 
title: TensorArrayClose 
parent: data_flow_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# TensorArrayClose

---

## tensorflow C++ API

[tensorflow::ops::TensorArrayClose](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/tensor-array-close)

Delete the TensorArray from its resource container.

---

## Summary

This enables the user to close and release the resource in the middle of a step/run.

Arguments:

* scope: A Scope object
* handle: The handle to a
  TensorArray \(output of TensorArray or TensorArrayGrad \).

Returns:

* the created Operation.

Constructor

* TensorArrayClose\(const ::tensorflow::Scope & scope, ::tensorflow::Input handle\).

Public attributes

* tensorflow::Operation operation.

---

## TensorArrayClose block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_data\_flow\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_data_flow_ops.cpp)

![](../assets/dataflow_TensorArrayClose_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input handle : connect Input node.

Return:

* Operation operation: Output object of TensorArrayClose class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](../assets/dataflow_TensorArrayClose_Method.png)

