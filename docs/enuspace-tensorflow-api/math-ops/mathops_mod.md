--- 
layout: default 
title: Mod 
parent: math_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# Mod

---

## tensorflow C++ API

[tensorflow::ops::Mod](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/mod)

Returns element-wise remainder of division.

## Summary

This emulates C semantics in that

the result here is consistent with a truncating divide. E.g.`truncate(x / y) * y + truncate_mod(x, y) = x`.

NOTE:[`Mod`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/mod.html#classtensorflow_1_1ops_1_1_mod)supports broadcasting. More about broadcasting [here](http://docs.scipy.org/doc/numpy/user/basics.broadcasting.html)

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The z tensor.

Constructor

* Mod\(const ::tensorflow::Scope & scope, ::tensorflow::Input x, ::tensorflow::Input y\).

Public attributes

* tensorflow::Output z.

---

## Mod block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](../assets/math_Mod_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input x:connect  Input node.
* Input y:connect  Input node.

Return:

* Output z: Output object of Mod class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](../assets/math_Mod_Method.png)

