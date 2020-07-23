--- 
layout: default 
title: Min 
parent: math_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# Min

---

## tensorflow C++ API

[tensorflow::ops::Min](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/min)

Computes the minimum of elements across dimensions of a tensor.

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

* Min\(const ::tensorflow::Scope & scope, ::tensorflow::Input input, ::tensorflow::Input axis, const Mean::Attrs attrs\).

Public attributes

* tensorflow::Output output.

---

## Max block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](./assets/math_Min_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input input:connect  Input node.
* Input axis:connect  Input node.
* Min::Attrs attrs : Input attrs in value. ex\) keep\_dims\_ = false;

Return:

* Output output: Output object of Min class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](./assets/math_Min_Method.png)

