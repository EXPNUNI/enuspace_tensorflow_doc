--- 
layout: default 
title: Igamma 
parent: math_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# Igamma

---

## tensorflow C++ API

[tensorflow::ops::Igamma](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/igamma)

Compute the lower regularized incomplete Gamma function`Q(a, x)`.

---

## Summary

The lower regularized incomplete Gamma function is defined as:

P\(a, x\) = gamma\(a, x\) / Gamma\(a\) = 1 - Q\(a, x\)

where

gamma\(a, x\) = int\_{0}^{x} t^{a-1} exp\(-t\) dt

is the lower incomplete Gamma function.

Note, above`Q(a, x)`\([`Igammac`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/igammac.html#classtensorflow_1_1ops_1_1_igammac)\) is the upper regularized complete Gamma function.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The z tensor.

Constructor

* Igamma\(const ::tensorflow::Scope & scope, ::tensorflow::Input a, ::tensorflow::Input x\).

Public attributes

* tensorflow::Output z.

---

## Igamma block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](../assets/math_Igamma_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input a:connect  Input node.
* Input x:connect  Input node.

Return:

* Output z: Output object of Igamma class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](../assets/math_Igamma_Method.png)

