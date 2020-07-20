# SparseConcat

---

## tensorflow C++ API

[tensorflow::ops::SparseConcat](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sparse-concat)

Concatenates a list of `SparseTensor` along the specified dimension.

---

## Summary

Concatenation is with respect to the dense versions of these sparse tensors. It is assumed that each input is a `SparseTensor` whose elements are ordered along increasing dimension number.

[All](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/all.html#classtensorflow_1_1ops_1_1_all) inputs' shapes must match, except for the concat dimension. The `indices`, `values`, and `shapes` lists must have the same length.

The output shape is identical to the inputs', except along the concat dimension, where it is the sum of the inputs' sizes along that dimension.

The output elements will be resorted to preserve the sort order along increasing dimension number.

This op runs in `O(M log M)` time, where `M` is the total number of non-empty values across all inputs. This is due to the need for an internal sort in order to concatenate efficiently across an arbitrary dimension.

For example, if `concat_dim = 1` and the inputs are

```
sp_inputs[0]: shape =[2,3]
//[0, 2]: "a"
//[1, 0]: "b"
//[1, 1]: "c"

sp_inputs[1]: shape =[2,4]
//[0, 1]: "d"
//[0, 2]: "e"
```

then the output will be

```
shape =[2,7]
//[0, 2]: "a"
//[0, 4]: "d"
//[0, 5]: "e"
//[1, 0]: "b"
//[1, 1]: "c"
```

Graphically this is equivalent to doing

```
[    a] concat[ d e  ]=[   a   d e  ]
[b c  ]       [      ] [b c         ]
```

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* indices: 2-D. Indices of each input `SparseTensor`.
* values: 1-D. Non-empty values of each `SparseTensor`.
* shapes: 1-D. Shapes of each `SparseTensor`.
* concat\_dim: Dimension to concatenate along. Must be in range \[-rank, rank\), where rank is the number of dimensions in each input `SparseTensor`.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) output\_indices: 2-D. Indices of the concatenated `SparseTensor`.
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) output\_values: 1-D. Non-empty values of the concatenated `SparseTensor`.
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) output\_shape: 1-D. [Shape](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/shape.html#classtensorflow_1_1ops_1_1_shape) of the concatenated `SparseTensor`.

---

## SparseConcat block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_sparse.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_sparse.cpp)

![](/assets/sparse_op/SparseConcat1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* InputList indices: connect  Input node.
* InputList values: connect  Input node.
* InputList shapes: connect  Input node.
* int64 concat\_dim : intput int64 in value.

Return:

* Output output\_indices: Output object of SparseAdd class object.
* Output output\_values: Output object of SparseAdd class object.
* Output output\_shape: Output object of SparseAdd class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/sparse_op/SparseConcat2.jpg)

