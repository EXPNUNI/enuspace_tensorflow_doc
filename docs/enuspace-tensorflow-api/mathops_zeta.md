--- 
layout: default 
title: Zeta 
parent: math_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# Zeta

---

## tensorflow C++ API

[tensorflow::ops::Zeta](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/zeta)

Compute the Hurwitz zeta function \(x, q\).

---

## Summary

The Hurwitz zeta function is defined as:

\(x, q\) = {n=0}^{} \(q + n\)^{-x}

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The z tensor.

Constructor

* Zeta\(const ::tensorflow::Scope & scope, ::tensorflow::Input x, ::tensorflow::Input q\) 

Public attributes

* tensorflow::Output z.

---

## Zeta block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](./assets/math_Zeta_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input x:connect  Input node.
* Input q:connect  Input node.

Return:

* Output z: Output object of Zeta class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](./assets/math_Zeta_Method.png)

