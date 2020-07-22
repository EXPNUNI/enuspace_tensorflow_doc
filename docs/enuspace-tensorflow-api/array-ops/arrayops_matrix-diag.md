--- 
layout: default 
title: MatrixDiag 
parent: array_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# MatrixDiag

---

## tensorflow C++ API {#tensorflow-c-api}

[tensorflow::ops::MatrixDiag](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/matrix-diag.html)

Returns a batched diagonal tensor with a given batched diagonal values.

---

## Summary {#summary}

Given a`diagonal`, this operation returns a tensor with the`diagonal`and everything else padded with zeros. The diagonal is computed as follows:

Assume`diagonal`has`k`dimensions`[I, J, K, ..., N]`, then the output is a tensor of rank`k+1`with dimensions \[I, J, K, ..., N, N\]\` where:

`output[i, j, k, ..., m, n] = 1{m=n} * diagonal[i, j, k, ..., n]`.

For example:

\`\`\` 'diagonal' is \[\[1, 2, 3, 4\], \[5, 6, 7, 8\]\]

and diagonal.shape = \(2, 4\)

tf.matrix\_diag\(diagonal\) ==&gt; \[\[\[1, 0, 0, 0\] \[0, 2, 0, 0\] \[0, 0, 3, 0\] \[0, 0, 0, 4\]\], \[\[5, 0, 0, 0\] \[0, 6, 0, 0\] \[0, 0, 7, 0\] \[0, 0, 0, 8\]\]\]

which has shape \(2, 4, 4\) \`\`\`

Arguments:

* scope: A [Scope](https://www.tensorflow.org/versions/r1.4/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* diagonal: [Rank](https://www.tensorflow.org/versions/r1.4/api_docs/cc/class/tensorflow/ops/rank.html#classtensorflow_1_1ops_1_1_rank) `k`, where `k >= 1`.

Returns:

* [`Output`](https://www.tensorflow.org/versions/r1.4/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): [Rank](https://www.tensorflow.org/versions/r1.4/api_docs/cc/class/tensorflow/ops/rank.html#classtensorflow_1_1ops_1_1_rank) `k+1`, with `output.shape = diagonal.shape + [diagonal.shape[-1]]`.

---

## MatrixDiag block {#abs-block}

Source link :[https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_array\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input diagonal : A 1-D `Tensor` type of `int32`,`int64`\(Must be one integer type\).

Output:

* Output output : Output object of MatrixBandPart class object.

Result:

* std::vector\(Tensor\) `result_output`: A `Tensor`.

---

## Using Method

※ tensorflow 1.3 does not support Windows

