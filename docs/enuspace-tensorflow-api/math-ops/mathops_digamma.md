--- 
layout: default 
title: Digamma 
parent: math_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# Digamma

---

## tensorflow C++ API

[tensorflow::ops::Digamma](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/digamma)

Computes Psi, the derivative of [Lgamma](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/lgamma.html#classtensorflow_1_1ops_1_1_lgamma)\(the log of the absolute value of.`Gamma(x)`\), element-wise.

---

## Summary

![](../assets/math_Digamma_Summary.png)

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The y tensor.

Constructor

* Digamma\(const ::tensorflow::Scope & scope, ::tensorflow::Input x\).

Public attributes

* tensorflow::Output y.

---

## Digamma block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](../assets/math_Digamma_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input x:connect  Input node.

Return:

* Output y: Output object of Digamma class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](../assets/math_Digamma_Method.png)

