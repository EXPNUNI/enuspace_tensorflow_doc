--- 
layout: default 
title: TensorArraySize 
parent: data_flow_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# TensorArraySize

---

## tensorflow C++ API

[tensorflow::ops::TensorArraySize](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/tensor-array-size)

Get the current size of the TensorArray.

---

## Summary

Arguments:

* scope: A Scope object
* handle: The handle to a queue.
* flow\_in: A float scalar that enforces proper chaining of operations.

Returns:

* Output : The current size of the TensorArray.

Constructor

* TensorArraySize\(const ::tensorflow::Scope & scope, ::tensorflow::Input handle, ::tensorflow::Input flow\_in\).

Public attributes

* tensorflow::Output size.

---

## TensorArraySize block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_data\_flow\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_data_flow_ops.cpp)

![](./assets/dataflow_TensorArraySize_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input handle : connect Input node.
* flow\_in : connect Input node or input float value.

Return:

* Output  size: Output object of TensorArraySize class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](./assets/dataflow_TensorArrayGather_Method.png)

