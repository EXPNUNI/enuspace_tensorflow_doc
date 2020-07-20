# Round

---

## tensorflow C++ API

[tensorflow::ops::Round](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/round)

Rounds the values of a tensor to the nearest integer, element-wise.

---

## Summary

Rounds half to even. Also known as bankers rounding. If you want to round according to the current system rounding mode use std::cint.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The y tensor.

Constructor

* Round\(const ::tensorflow::Scope & scope,  ::tensorflow::Input x\).

Public attributes

* tensorflow::Output y.

---

## Round block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/math_Round_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input x:connect  Input node.

Return:

* Output y: Output object of Round class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/math_Round_Method.png)

