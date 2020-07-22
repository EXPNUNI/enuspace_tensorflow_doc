--- 
layout: default 
title: TensorArrayWrite 
parent: data_flow_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# TensorArrayWrite

---

## tensorflow C++ API

[tensorflow::ops::TensorArrayWrite](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/tensor-array-write)

Push an element onto the tensor\_array.

---

## Summary

Arguments:

* scope: A Scope object
* handle: The handle to a TensorArray.
* index: The position to write to inside the TensorArray.
* value: The tensor to write to the TensorArray.
* flow\_in: A float scalar that enforces proper chaining of operations.

Returns:

* Output : A float scalar that enforces proper chaining of operations.

Constructor

* TensorArrayWrite\(const ::tensorflow::Scope & scope, ::tensorflow::Input handle, ::tensorflow::Input index, ::tensorflow::Input value, ::tensorflow::Input flow\_in\).

Public attributes

* tensorflow::Output flow\_out.

---

## TensorArrayWrite block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_data\_flow\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_data_flow_ops.cpp)

![](../assets/dataflow_TensorArrayWrite_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* handle : connect Input node.
* index : connect Input node or input index number.
* value : connect Input node or input tensor value.
* flow\_in : connect Input node.

Return:

* Output flow\_out: Output object of TensorArrayWrite class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](../assets/dataflow_TensorArray_Method.png)

