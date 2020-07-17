# SparseAddGrad

---

## tensorflow C++ API

[tensorflow::ops::SparseAddGrad](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sparse-add-grad)

The gradient operator for the [SparseAdd](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sparse-add.html#classtensorflow_1_1ops_1_1_sparse_add) op.

---

## Summary

The [SparseAdd](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sparse-add.html#classtensorflow_1_1ops_1_1_sparse_add) op calculates A + B, where A, B, and the sum are all represented as `SparseTensor` objects. This op takes in the upstream gradient w.r.t. non-empty values of the sum, and outputs the gradients w.r.t. the non-empty values of A and B.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* backprop\_val\_grad: 1-D with shape `[nnz(sum)]`. The gradient with respect to the non-empty values of the sum.
* a\_indices: 2-D. The `indices` of the `SparseTensor` A, size `[nnz(A), ndims]`.
* b\_indices: 2-D. The `indices` of the `SparseTensor` B, size `[nnz(B), ndims]`.
* sum\_indices: 2-D. The `indices` of the sum `SparseTensor`, size `[nnz(sum), ndims]`.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) a\_val\_grad: 1-D with shape `[nnz(A)]`. The gradient with respect to the non-empty values of A.
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) b\_val\_grad: 1-D with shape `[nnz(B)]`. The gradient with respect to the non-empty values of B.

---

## SparseAddGrad block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_sparse.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_sparse.cpp)

![](/assets/sparse_op/SparseAddGrad1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input backprop\_val\_grad: connect  Input node.
* Input a\_indices: connect  Input node.
* Input b\_indices: connect  Input node.
* Input sum\_indices: connect  Input node.

Return:

* Output a\_val\_grad: Output object of SparseAdd class object.
* Output b\_val\_grad: Output object of SparseAdd class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/sparse_op/SparseAddGrad2.jpg)\*SparseAdd 노드 생성방법은 [SparseAdd](https://expnuni.gitbooks.io/enuspacetensorflow/content/sparse-ops/sparseadd.html) 페이지에 기재되어 있음.

