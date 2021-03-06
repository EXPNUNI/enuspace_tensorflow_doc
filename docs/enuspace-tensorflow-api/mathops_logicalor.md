--- 
layout: default 
title: LogicalOr 
parent: math_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# LogicalOr

---

## tensorflow C++ API

[tensorflow::ops::LogicalOr](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/logical-or)

Returns the truth value of x OR y element-wise.

## Summary

NOTE:[`LogicalOr`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/logical-or.html#classtensorflow_1_1ops_1_1_logical_or)supports broadcasting. More about broadcasting [here](http://docs.scipy.org/doc/numpy/user/basics.broadcasting.html)

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The z tensor.

Constructor

* LogicalOr\(const ::tensorflow::Scope & scope, ::tensorflow::Input x, ::tensorflow::Input y\).

Public attributes

* tensorflow::Output z.

---

## LogicalOr block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](./assets/math_LogicalOr_Symbol_.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input x:connect  Input node.
* Input y:connect  Input node.

Return:

* Output z: Output object of LogicalOr class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](./assets/math_LogicalOr_Method.png)

