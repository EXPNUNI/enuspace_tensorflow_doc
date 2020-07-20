# Greater

---

## tensorflow C++ API

[tensorflow::ops::Greater](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/greater)

Returns the truth value of \(x &gt; y\) element-wise.

## Summary

NOTE:[`Greater`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/greater.html#classtensorflow_1_1ops_1_1_greater)supports broadcasting. More about broadcasting [here](http://docs.scipy.org/doc/numpy/user/basics.broadcasting.html)

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The z tensor.

Constructor

* Greater\(const ::tensorflow::Scope & scope, ::tensorflow::Input x, ::tensorflow::Input y\).

Public attributes

* tensorflow::Output z.

---

## Greater block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/math_Greater_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input x:connect  Input node.
* Input y:connect  Input node.

Return:

* Output z: Output object of Greater class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/math_Greater_Method.png)

