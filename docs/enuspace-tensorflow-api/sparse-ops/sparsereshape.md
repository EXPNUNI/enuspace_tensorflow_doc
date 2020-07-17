# SparseReshape

---

## tensorflow C++ API

[tensorflow::ops::SparseReshape](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sparse-reshape)

Reshapes a SparseTensor to represent values in a new dense shape.

---

## Summary

This operation has the same semantics as reshape on the represented dense tensor. The `input_indices` are recomputed based on the requested `new_shape`.

If one component of `new_shape` is the special value -1, the size of that dimension is computed so that the total dense size remains constant. At most one component of `new_shape` can be -1. The number of dense elements implied by `new_shape` must be the same as the number of dense elements originally implied by `input_shape`.

Reshaping does not affect the order of values in the SparseTensor.

If the input tensor has rank `R_in` and `N` non-empty values, and `new_shape` has length `R_out`, then `input_indices` has shape `[N, R_in]`, `input_shape` has length `R_in`, `output_indices` has shape `[N, R_out]`, and `output_shape` has length `R_out`.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* input\_indices: 2-D. `N x R_in` matrix with the indices of non-empty values in a SparseTensor.
* input\_shape: 1-D. `R_in` vector with the input SparseTensor's dense shape.
* new\_shape: 1-D. `R_out` vector with the requested new dense shape.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) output\_indices: 2-D. `N x R_out` matrix with the updated indices of non-empty values in the output SparseTensor.
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) output\_shape: 1-D.`R_out` vector with the full dense shape of the output SparseTensor. This is the same as `new_shape` but with any -1 dimensions filled in.

---

## SparseReshape block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_sparse.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_sparse.cpp)

![](/assets/sparse_op/SparseReshape1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input input\_indices: connect  Input node.
* Input input\_shape: connect  Input node.
* Input new\_shape: connect  Input node.

Return:

* Output output: Output object of SparseReshape class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

## ![](/assets/sparse_op/SparseReshape2.jpg)



