--- 
layout: default 
title: Imag 
parent: math_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# Imag

---

## tensorflow C++ API

[tensorflow::ops::Imag](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/imag)

Returns the imaginary part of a complex number.

---

## Summary

Given a tensor`input`of complex numbers, this operation returns a tensor of type`float`that is the imaginary part of each element in`input`.[All](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/all.html#classtensorflow_1_1ops_1_1_all)elements in`input`must be complex numbers of the form \\(a + bj\\), whereais the real part andbis the imaginary part returned by this operation.

For example:

\`\`\` tensor 'input' is \[-2.25 + 4.75j, 3.25 + 5.75j\]

tf.imag\(input\) ==&gt; \[4.75, 5.75\] \`\`\`

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The output tensor.

Constructor

* Imag\(const ::tensorflow::Scope & scope, ::tensorflow::Input input, const Imag::Attrs & attrs\)

Public attributes

* tensorflow::Output output.

---

## Imag block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](../assets/math_Imag_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input input : connect  Input node.
* Imag::Attrs & attrs : Input DataType. ex\)Tout\_ = DT\_DOUBLE;

Return:

* Output output : Output object of Imag class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method![](../assets/math_Imag_Method.png)



