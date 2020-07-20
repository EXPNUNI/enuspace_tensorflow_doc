# Maximum

---

## tensorflow C++ API

[tensorflow::ops::Maximum](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/maximum)

Returns the max of x and y \(i.e.x &gt; y ? x : y\) element-wise.

## Summary

NOTE:[`Maximum`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/maximum.html#classtensorflow_1_1ops_1_1_maximum)supports broadcasting. More about broadcasting [here](http://docs.scipy.org/doc/numpy/user/basics.broadcasting.html)

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The z tensor.

Constructor

* Maximum\(const ::tensorflow::Scope & scope, ::tensorflow::Input x, ::tensorflow::Input y\).

Public attributes

* tensorflow::Output z.

---

## Maximum block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/math_Maximum_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input x:connect  Input node.
* Input y:connect  Input node.

Return:

* Output z: Output object of Maximum class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/math_Maximum_Method.png)

