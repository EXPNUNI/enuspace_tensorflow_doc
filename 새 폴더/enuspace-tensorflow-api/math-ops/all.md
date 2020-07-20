# All

---

## tensorflow C++ API

[tensorflow::ops::All](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/all)

Computes the "logical and" of elements across dimensions of a tensor.

---

## Summary

Reduces`input`along the dimensions given in`axis`. Unless`keep_dims`is true, the rank of the tensor is reduced by 1 for each entry in`axis`. If`keep_dims`is true, the reduced dimensions are retained with length 1.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* input: The tensor to reduce.\(Data type must be bool\)
* axis: The dimensions to reduce.\(0:Low axis,1:column axis\)

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/all/attrs.html#structtensorflow_1_1ops_1_1_all_1_1_attrs)\):

* keep_dims_\_: If true, retain reduced dimensions with length 1.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The reduced tensor.

Constructor

* All\(const ::tensorflow::Scope & scope, ::tensorflow::Input input,::tensorflow::Input axis,const All::Attrs & attrs\).

Public attributes

* tensorflow::Output output.

---

## All block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/math_All_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input input : connect  Input node.
* Input axis : connect  Input node.
* All::Attrs attrs : Input  attrs value. ex\) keep_dims_\_=false;

Return:

* Output output : Output object of All class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/math_All_Method.png)

