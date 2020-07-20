# Sigmoid

---

## tensorflow C++ API

[tensorflow::ops::Sigmoid](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sigmoid)

Computes sigmoid of`x`element-wise.

---

## Summary

Specifically,`y = 1 / (1 + exp(-x))`.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The y tensor.

Constructor

* Sigmoid\(const ::tensorflow::Scope & scope, ::tensorflow::Input x\) 

Public attributes

* tensorflow::Output y.

---

## Sigmoid block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/math_Sigmoid_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input x : connect  Input node.

Return:

* Output output: Output object of Sigmoid class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/math_Sigmoid_Method.png)

