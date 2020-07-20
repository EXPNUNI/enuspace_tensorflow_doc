# Ceil

---

## tensorflow C++ API

[tensorflow::ops::Ceil](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/ceil)

Returns element-wise smallest integer in not less than x.

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The y tensor.

Constructor

* Ceil\(const ::tensorflow::Scope & scope, ::tensorflow::Input x\).

Public attributes

* tensorflow::Output y.

---

## Ceil block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/math_Ceil_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input x:connect  Input node.

Return:

* Output y : Output object of Ceil class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/math_Ceil_Method.png)

