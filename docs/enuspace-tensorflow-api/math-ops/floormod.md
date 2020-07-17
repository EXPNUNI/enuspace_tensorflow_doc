# FloorMod

---

## tensorflow C++ API

[tensorflow::ops::FloorMod](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/floor-mod)

Returns element-wise remainder of division.

## Summary

When`x < 0`xor`y < 0`is true, this follows Python semantics in that the result here is consistent with a flooring divide. E.g.`floor(x / y) * y + mod(x, y) = x`.

NOTE:[`FloorMod`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/floor-mod.html#classtensorflow_1_1ops_1_1_floor_mod)supports broadcasting. More about broadcasting [here](http://docs.scipy.org/doc/numpy/user/basics.broadcasting.html)

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The z tensor.

Constructor

* FloorMod\(const ::tensorflow::Scope & scope, ::tensorflow::Input x, ::tensorflow::Input y\).

Public attributes

* tensorflow::Output z.

---

## FloorMod block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/math_FloorMod_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input x:connect  Input node.
* Input y:connect  Input node.

Return:

* Output z: Output object of FloorMod class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/math_FloorMod_Method.png)

