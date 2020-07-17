# AddN

---

## tensorflow C++ API

[tensorflow::ops::AddN](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/add-n)

Add all input tensors element wise.

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* inputs:** Must all be the same size and shape.**

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The sum tensor.

Constructor

* AddN\(const ::tensorflow::Scope & scope, ::tensorflow::InputList inputs\).

Public attributes

* tensorflow::Output sum.

---

## AddN block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/math_AddN_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* InputList inputs :connect  InputList node.

Return:

* Output sum : Output object of AddN class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/math_AddN_Method.png)

