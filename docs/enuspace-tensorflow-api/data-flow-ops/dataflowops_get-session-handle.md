--- 
layout: default 
title: GetSessionHandle 
parent: data_flow_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# GetSessionHandle

---

## tensorflow C++ API

[tensorflow::ops::GetSessionHandle](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/get-session-handle)

Store the input tensor in the state of the current session.

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* value: The tensor to be stored.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The handle for the tensor stored in the session state, represented as a string.

---

## GetSessionHandle block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_data\_flow\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_data_flow_ops.cpp)

![](../assets/dataflow_getsessionhandle_symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* value: The tensor to be stored.

Return:

* Output handle: Output object of GetSessionHandle class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

Issue : [https://github.com/tensorflow/tensorflow/issues/12901](https://github.com/tensorflow/tensorflow/issues/12901)

