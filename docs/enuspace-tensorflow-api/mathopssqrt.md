--- 
layout: default 
title: Sqrt 
parent: math_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# Sqrt

---

## tensorflow C++ API

[tensorflow::ops::Sqrt](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sqrt)

Computes square root of x element-wise.

---

## Summary

I.e. y = {x} = x^{1/2}.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The y tensor.

Constructor

* Sqrt\(const ::tensorflow::Scope & scope, ::tensorflow::Input x\) 

Public attributes

* tensorflow::Output y.

---

## Sqrt block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](./assets/math_Sqrt_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input x : connect  Input node.

Return:

* Output output: Output object of Sqrt class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](./assets/math_Sqrt_Method.png)

