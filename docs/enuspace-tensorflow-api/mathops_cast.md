--- 
layout: default 
title: Cast 
parent: math_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# Cast

---

## tensorflow C++ API

[tensorflow::ops::Cast](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/cast)

[Cast](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/cast.html#classtensorflow_1_1ops_1_1_cast) x of type SrcT to y of DstT.

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The y tensor.

Constructor

* Cast\(const ::tensorflow::Scope & scope, ::tensorflow::Input x, DataType DstT\).

Public attributes

* tensorflow::Output y.

---

## Cast block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](./assets/math_Cast_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input x:connect  Input node.
* DataType DstT:Input DatType in value. ex\) DT\_INT32, DT\_INT64, DT\_DOUBLE.

Return:

* Output y : Output object of Cast class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](./assets/math_Cast_Method.png)

