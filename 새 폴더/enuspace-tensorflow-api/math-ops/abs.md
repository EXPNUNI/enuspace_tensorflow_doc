# Abs

---

## tensorflow C++ API

[tensorflow::ops::Abs](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/abs)

Computes the absolute value of a tensor.

---

## Summary

Given a tensor`x`, this operation returns a tensor containing the absolute value of each element in`x`. For example, if x is an input element and y is an output element, this operation computes \\(y = \|x\|\\).

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The y tensor.

Constructor

* Abs\(const ::tensorflow::Scope & scope, ::tensorflow::Input x\).

Public attributes

* tensorflow::Output y.

---

## Abs block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/math_Abs_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input x :connect  Input node.

Return:

* Output y : Output object of Abs class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/math_Abs_Method.png)

