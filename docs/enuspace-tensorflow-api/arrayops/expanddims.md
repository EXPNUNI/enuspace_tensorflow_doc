# ExpandDims {#abs}

---

## tensorflow C++ API {#tensorflow-c-api}

[tensorflow::ops::ExpandDims](https://www.tensorflow.org/versions/r1.2/api_docs/cc/class/tensorflow/ops/expand-dims.html)

Inserts a dimension of 1 into a tensor's shape.

---

## Summary {#summary}

Given a tensor`input`, this operation inserts a dimension of 1 at the dimension index`axis`of`input`'s shape. The dimension index`axis`starts at zero; if you specify a negative number for`axis`it is counted backward from the end.

This operation is useful if you want to add a batch dimension to a single element. For example, if you have a single image of shape`[height, width, channels]`, you can make it a batch of 1 image with`expand_dims(image, 0)`, which will make the shape`[1, height, width, channels]`.

Other examples:

\`\`\` 't' is a tensor of shape \[2\]

shape\(expand\_dims\(t, 0\)\) ==&gt; \[1, 2\] shape\(expand\_dims\(t, 1\)\) ==&gt; \[2, 1\] shape\(expand\_dims\(t, -1\)\) ==&gt; \[2, 1\]

't2' is a tensor of shape \[2, 3, 5\]

shape\(expand\_dims\(t2, 0\)\) ==&gt; \[1, 2, 3, 5\] shape\(expand\_dims\(t2, 2\)\) ==&gt; \[2, 3, 1, 5\] shape\(expand\_dims\(t2, 3\)\) ==&gt; \[2, 3, 5, 1\] \`\`\`

This operation requires that:

`-1-input.dims() <= dim <= input.dims()`

This operation is related to`squeeze()`, which removes dimensions of size 1.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/versions/r1.2/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* axis: 0-D \(scalar\). Specifies the dimension index at which to expand the shape of `input`

Returns:

* [`Output`](https://www.tensorflow.org/versions/r1.2/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): Contains the same data as `input`, but its shape has an additional dimension of size 1 added.

---

## ExpandDims block {#abs-block}

Source link :[https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_array\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/array_ops/expanddims1.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input `input`: A N-D `Tensor` .
* Input axis : 0-D \(scalar\). Specifies the dimension index at which to expand the shape of `input`.

Return:

* Output output : Output object of ExpandDims class object. 

Result:

* std::vector\(Tensor\) result\_output : A `Tensor`with the same data as `input`, but its shape has an additional dimension of size 1 added.

---

## Using Method {#using-method}

![](/assets/array_ops/expanddims2.png)※ 차원을 증가 시킨다.



