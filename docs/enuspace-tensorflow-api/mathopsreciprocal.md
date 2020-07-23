--- 
layout: default 
title: Reciprocal 
parent: math_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# Reciprocal

---

## tensorflow C++ API

[tensorflow::ops::Reciprocal](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/reciprocal)

Computes the reciprocal of x element-wise.

---

## Summary

I.e., y = 1 / x.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The y tensor.

Constructor

* Reciprocal\(const ::tensorflow::Scope & scope,  ::tensorflow::Input x\).

Public attributes

* tensorflow::Output y.

---

## Reciprocal block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](./assets/math_Reciprocal_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input x:connect  Input node.

Return:

* Output y: Output object of Reciprocal class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](./assets/math_Reciprocal_Method.png)

