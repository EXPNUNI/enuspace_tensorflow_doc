# SparseTensorDenseMatMul

---

## tensorflow C++ API

[tensorflow::ops::SparseTensorDenseMatMul](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sparse-tensor-dense-mat-mul)

[Multiply](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/multiply.html#classtensorflow_1_1ops_1_1_multiply) SparseTensor \(of rank 2\) "A" by dense matrix "B".

---

## Summary

No validity checking is performed on the indices of A. However, the following input format is recommended for optimal behavior:

if adjoint\_a == false: A should be sorted in lexicographically increasing order. Use[SparseReorder](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sparse-reorder.html#classtensorflow_1_1ops_1_1_sparse_reorder)if you're not sure. if adjoint\_a == true: A should be sorted in order of increasing dimension 1 \(i.e., "column major" order instead of "row major" order\).

Arguments:

* scope: A[Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* a\_indices: 2-D. The`indices`of the`SparseTensor`, size`[nnz, 2]`Matrix.
* a\_values: 1-D. The`values`of the`SparseTensor`, size`[nnz]`Vector.
* a\_shape: 1-D. The`shape`of the`SparseTensor`, size`[2]`Vector.
* b: 2-D. A dense Matrix.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/sparse-tensor-dense-mat-mul/attrs.html#structtensorflow_1_1ops_1_1_sparse_tensor_dense_mat_mul_1_1_attrs)\):

* adjoint\_a: Use the adjoint of A in the matrix multiply. If A is complex, this is transpose\(conj\(A\)\). Otherwise it's transpose\(A\).
* adjoint\_b: Use the adjoint of B in the matrix multiply. If B is complex, this is transpose\(conj\(B\)\). Otherwise it's transpose\(B\).

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The product tensor.

---

## SparseTensorDenseMatMul block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_sparse.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_sparse.cpp)

![](/assets/sparse_op/SparseTensorDenseMatMul1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input a\_indices: connect  Input node.
* Input a\_values: connect  Input node.
* Input a\_shape: connect  Input node.
* Input b: connect  Input node.

Return:

* Ouput output\_indices: Output object of SparseTensorDenseAdd class object.

Result:

* std::vector\(Tensor\) _result_\_output : Returned object of executed result by calling session.

---

## Using Method

## ![](/assets/sparse_op/SparseTensorDenseMatMul2.jpg)



