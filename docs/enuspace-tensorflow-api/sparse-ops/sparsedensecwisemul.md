# SparseDenseCwiseMul

---

## tensorflow C++ API

[tensorflow::ops::SparseDenseCwiseMul](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sparse-dense-cwise-mul)

Component-wise multiplies a SparseTensor by a dense [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor).

---

## Summary

The output locations corresponding to the implicitly zero elements in the sparse tensor will be zero \(i.e., will not take up storage space\), regardless of the contents of the dense tensor \(even if it's +/-INF and that INF\*0 == NaN\).

Limitation: this Op only broadcasts the dense side to the sparse side, but not the other direction.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* sp\_indices: 2-D. `N x R` matrix with the indices of non-empty values in a SparseTensor, possibly not in canonical ordering.
* sp\_values: 1-D. `N` non-empty values corresponding to `sp_indices`.
* sp\_shape: 1-D. [Shape](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/shape.html#classtensorflow_1_1ops_1_1_shape) of the input SparseTensor.
* dense: `R`-D. The dense [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) operand.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): 1-D. The `N` values that are operated on.

---

## SparseDenseCwiseMul block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_sparse.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_sparse.cpp)

![](/assets/sparse_op/SparseDenseCwiseMul1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input sp\_indices: connect  Input node.
* Input sp\_values: connect  Input node.
* Input sp\_shape: connect  Input node.
* Input dense: connect  Input node.

Return:

* Output output: Output object of SparseDenseCwiseMul class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/sparse_op/SparseDenseCwiseMul2.jpg)

