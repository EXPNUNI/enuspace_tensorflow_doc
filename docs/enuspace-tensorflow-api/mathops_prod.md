--- 
layout: default 
title: Prod 
parent: math_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# Prod

---

## tensorflow C++ API

[tensorflow::ops::Prod](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/prod)

Computes the product of elements across dimensions of a tensor.

## Summary

Reduces`input`along the dimensions given in`axis`. Unless`keep_dims`is true, the rank of the tensor is reduced by 1 for each entry in`axis`. If`keep_dims`is true, the reduced dimensions are retained with length 1.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* input: The tensor to reduce.
* axis: The dimensions to reduce.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/max/attrs.html#structtensorflow_1_1ops_1_1_max_1_1_attrs)\):

* keep\_dims: If true, retain reduced dimensions with length 1.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The reduced tensor.

Constructor

* Prod\(const ::tensorflow::Scope & scope, ::tensorflow::Input input, ::tensorflow::Input axis, const Prod::Attrs attrs\).

Public attributes

* tensorflow::Output output.

---

## Prod block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](./assets/math_Prod_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input input:connect  Input node.
* Input axis:connect  Input node.
* Prod::Attrs attrs : Input attrs in value. ex\) keep\_dims\_ = false;

Return:

* Output output: Output object of Prod class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](./assets/math_Prod_Method.png)

