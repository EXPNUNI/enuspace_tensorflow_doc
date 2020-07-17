# Conj

---

## tensorflow C++ API

[tensorflow::ops::Conj](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/conj)

Returns the complex conjugate of a complex number.

---

## Summary

Given a tensor`input`of complex numbers, this operation returns a tensor of complex numbers that are the complex conjugate of each element in`input`. The complex numbers in`input`must be of the form \(a + bj\), whereais the real part andbis the imaginary part.

The complex conjugate returned by this operation is of the form \(a - bj\).

For example:

\`\`\` tensor 'input' is \[-2.25 + 4.75j, 3.25 + 5.75j\]

tf.conj\(input\) ==&gt; \[-2.25 - 4.75j, 3.25 - 5.75j\] \`\`\`

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The output tensor.

Constructor

* Conj\(const ::tensorflow::Scope & scope, ::tensorflow::Input input\).

Public attributes

* tensorflow::Output output.

---

## Conj block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/math_Conj_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input input:connect  Input node.

Return:

* Output output : Output object of Conj class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/math_Conj_Method.png)

