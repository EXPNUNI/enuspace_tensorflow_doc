# Add

---

## tensorflow C++ API

[tensorflow::ops::Add](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/add)

Returns x + y element-wise.

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The z tensor.

Constructor

* Add\(const ::tensorflow::Scope & scope, ::tensorflow::Input x, ::tensorflow::Input y\).

Public attributes

* tensorflow::Output z.

---

## Add block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/math_Add_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input x :connect  Input node.
* Input y :connect  Input node.

Return:

* Output z : Output object of Add class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

Using example\) double 

![](/assets/math_Add_Method.png)

Using example\) string 

![](/assets/math_Add_Method1.png)

