# SparseTensorDenseAdd

---

## tensorflow C++ API

[tensorflow::ops::SparseTensorDenseAdd](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sparse-tensor-dense-add)

Adds up a`SparseTensor`and a dense[`Tensor`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor), producing a dense[`Tensor`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor).

---

## Summary

This Op does not require`a_indices`be sorted in standard lexicographic order.

Arguments:

* scope: A[Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope)object
* a\_indices: 2-D. The`indices`of the`SparseTensor`, with shape`[nnz, ndims]`.
* a\_values: 1-D. The`values`of the`SparseTensor`, with shape`[nnz]`.
* a\_shape: 1-D. The`shape`of the`SparseTensor`, with shape`[ndims]`.
* b:`ndims`-D[Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor). With shape`a_shape`.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The output tensor.

---

## SparseTensorDenseAdd block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_sparse.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_sparse.cpp)

![](/assets/sparse_op/SparseTensorDenseAdd1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input a\_indices: connect  Input node.
* Input a\_values: connect  Input node.
* Input a\_shape: connect  Input node.
* Input b: connect  Input node.

Return:

* Output output\_indices: Output object of SparseTensorDenseAdd class object.

Result:

* std::vector\(Tensor\) _result_\_output : Returned object of executed result by calling session.

---

## Using Method

## ![](/assets/sparse_op/SparseTensorDenseAdd2.jpg)



