# ApproximateEqual

---

## tensorflow C++ API

[tensorflow::ops::ApproximateEqual](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/approximate-equal)

Returns the truth value of abs\(x-y\) &lt; tolerance element-wise

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The z tensor.

Constructor

* ApproximateEqual\(const ::tensorflow::Scope & scope, ::tensorflow::Input x,::tensorflow::Input y,const ApproximateEqual::Attrs & attrs\).

Public attributes

* tensorflow::Output z.

---

## ApproximateEqualblock

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/math_ApproximateEqual_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input x: connect  Input node.
* Input y: connect  Input node.
* ApproximateEqual::Attrs attrs : Input  attrs value. ex\) tolerance\_=1e-05f;

Return:

* Output z: Output object of ApproximateEqual class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/math_ApproximateEqual_Mehod.png)

