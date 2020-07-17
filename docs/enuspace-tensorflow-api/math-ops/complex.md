# Complex

---

## tensorflow C++ API

[tensorflow::ops::Complex](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/ceil)

Converts two real numbers to a complex number.

---

## Summary

Given a tensor`real`representing the real part of a complex number, and a tensor`imag`representing the imaginary part of a complex number, this operation returns complex numbers elementwise of the form \(a + bj\), where a represents the`real`part and b represents the`imag`part.

The input tensors`real`and`imag`must have the same shape.

For example:

\`\`\` tensor 'real' is \[2.25, 3.25\]

tensor`imag`is \[4.75, 5.75\]

tf.complex\(real, imag\) ==&gt; \[\[2.25 + 4.75j\], \[3.25 + 5.75j\]\] \`\`\`

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The out tensor.

Constructor

* Complex\(const ::tensorflow::Scope & scope, ::tensorflow::Input real, ::tensorflow::Input imag, const Complex::Attrs attrs\).

Public attributes

* tensorflow::Output out.

---

## Complex block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/math_Complex_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input x:connect  Input node.
* Input y:connect  Input node.
* Complex::Attrs attrs:Input DatType in value. ex\) Tout\_=DT\_COMPLEX64_,  Tout\__=DT\_COMPLEX128

Return:

* Output out : Output object of Complex class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/math_Complex_Method.png)

