# TruncateDiv

---

## tensorflow C++ API

[tensorflow::ops::TruncateDiv](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/truncate-div)

Returns x / y element-wise for integer types.

---

## Summary

Truncation designates that negative numbers will round fractional quantities toward zero. I.e. -7 / 5 = 1. This matches C semantics but it is different than Python semantics. See[`FloorDiv`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/floor-div.html#classtensorflow_1_1ops_1_1_floor_div)for a division function that matches Python Semantics.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The z tensor.

Constructor

* TruncateDiv\(const ::tensorflow::Scope & scope, ::tensorflow::Input x, ::tensorflow::Input y\).

Public attributes

* tensorflow::Output z.

---

## TruncateDiv block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/math_TruncateDiv_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input x:connect  Input node.
* Input y:connect  Input node.

Return:

* Output z: Output object of TruncateDiv class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/math_TruncateDiv_Method.png)

