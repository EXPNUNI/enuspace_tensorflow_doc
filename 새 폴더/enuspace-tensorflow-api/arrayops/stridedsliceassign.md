# StridedSliceAssign

---

## tensorflow C++ API {#tensorflow-c-api}

[tensorflow::ops::StridedSliceAssign](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/strided-slice-assign.html)

[Assign](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/assign.html#classtensorflow_1_1ops_1_1_assign) `value` to the sliced l-value reference of `ref`.

---

## Summary {#summary}

The values of`value`are assigned to the positions in the variable`ref`that are selected by the slice parameters. The slice parameters`begin,`end`,`strides`, etc. work exactly as in`StridedSlice\`.

NOTE this op currently does not support broadcasting and so`value`'s shape must be exactly the shape produced by the slice of`ref`.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The output\_ref tensor.

---

## StridedSliceAssign block {#abs-block}

Source link :[https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_array\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/array_ops/stridedsliceassign1.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input ref: A `Tensor`.
* Input begin: An `int32` or `int64 Tensor`. \`begin\[k\]\` specifies the offset into the \`k\`th range specification. The exact dimension this corresponds to will be determined by context. Out-of-bounds values will be silently clamped. If the \`k\`th bit of \`begin\_mask\` then \`begin\[k\]\` is ignored and the full range of the appropriate dimension is used instead. Negative values causes indexing to start from the highest element e.g. If \`foo==\[1,2,3\]\` then \`foo\[-1\]==3\`.
* Input end: An `int32` or `int64 Tensor`. \`end\[i\]\` is like \`begin\` with the exception that \`end\_mask\` is used to determine full ranges.
* Input strides: An `int32` or `int64 Tensor`. \`strides\[i\]\` specifies the increment in the \`i\`th specification after extracting a given element. Negative indices will reverse the original order. Out or range values are clamped to \`\[0,dim\[i\]\) if slice\[i\]&gt;0 `or` \[-1,dim\[i\]-1\] if slice\[i\] &lt; 0\`
* Input value: A `Tensor` . Assign to ref.
* StridedSlice::Attrs attrs:
  * begin\_mask: a bitmask where a bit i being 1 means to ignore the begin value and instead use the largest interval possible. At runtime begin\[i\] will be replaced with `[0, n-1) if` stride\[i\] &gt; 0 `or`\[-1, n-1\] `if` stride\[i\] &lt; 0
  * end\_mask: analogous to begin\_mask
  * shrink\_axis\_mask: a bitmask where bit i implies that the i th specification should shrink the dimensionality. begin and end must imply a slice of size 1 in the dimension. For example in python one might do foo\[:, 3, :\] which would result in shrink\_axis\_mask being 2.
  * ellipsis\_mask: a bitmask where bit i being 1 means the i\`th position is actually an ellipsis. One bit at most can be 1. If ellipsis\_mask == 0, then an implicit ellipsis mask of 1 &lt;&lt; \(m+1\) is provided. This means that foo\[3:5\] == foo\[3:5, ...\]. An ellipsis implicitly creates as many range specifications as necessary to fully specify the sliced range for every dimension. For example for a 4-dimensional tensor foo the slice foo\[2, ..., 5:8\] implies foo\[2, :, :, 5:8\].
  * new\_axis\_mask: a bitmask where bit i being 1 means the i th specification creates a new shape 1 dimension. For example foo\[:4, tf.newaxis, :2\] would produce a shape \(4, 1, 2\) tensor.

Output:

* Output output: Output object of StridedSliceAssign class object.

Result:

* std::vector\(Tensor\) `result_output`: A `Tensor` the same type as `input`.

---

## Using Method

![](/assets/array_ops/stridedsliceassign2.png)※ value에서 특정한 부분을 잘라내어 ref의 variable에 입력하는 기능을 한다. begin은 각 차원에서 잘라낼 시작지점\(마이너스 값일 경우 reverse시키는것으로 보임\), end는 어디까지 자를것인지 입력한다. strides는 몇 스텝을 이동할 것인지 정한다\(ex: strides가 2일 경우 시작인 1에서 두칸 넘어간 3 그다음은 5 이런식이다.\).

