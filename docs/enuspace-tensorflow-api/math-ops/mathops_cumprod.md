--- 
layout: default 
title: Cumprod 
parent: math_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# Cumprod

---

## tensorflow C++ API

[tensorflow::ops::Cumprod](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/cumprod)

Compute the cumulative product of the tensor`x`along`axis.`.

---

## Summary

By default, this op performs an inclusive cumprod, which means that the first element of the input is identical to the first element of the output: \`\`\`prettyprint tf.cumprod\(\[a, b, c\]\) ==&gt; \[a, a \* b, a \* b \* c\] \`\`\`

By setting the`exclusive`kwarg to`True`, an exclusive cumprod is performed instead: \`\`\`prettyprint tf.cumprod\(\[a, b, c\], exclusive=True\) ==&gt; \[1, a, a \* b\] \`\`\`

By setting the`reverse`kwarg to`True`, the cumprod is performed in the opposite direction: \`\`\`prettyprint tf.cumprod\(\[a, b, c\], reverse=True\) ==&gt; \[a \* b \* c, b \* c, c\] \`\``This is more efficient than using separate`tf.reverse\` ops.

The`reverse`and`exclusive`kwargs can also be combined: \`\`\`prettyprint tf.cumprod\(\[a, b, c\], exclusive=True, reverse=True\) ==&gt; \[b \* c, c, 1\] \`\`\`

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The out tensor.

Constructor

* Cumprod\(const ::tensorflow::Scope & scope, ::tensorflow::Input x, ::tensorflow::Input axis, const
  [Cumprod::Attrs](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/cumprod/attrs.html#structtensorflow_1_1ops_1_1_cumprod_1_1_attrs) & attrs\).

Public attributes

* tensorflow::Output out.

---

## Cumprod block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](../assets/math_Cumprod_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input x:connect  Input node.
* Input axis:connect  Input node. ex\) 0 or 1.
* Cumprod ::Attrs attrs:Input attrs  in value. ex\) exclusive\_ = false_; reverse\__ =false;

Return:

* Output out: Output object of Cumprod class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](../assets/math_Cumprod_Method.png)

