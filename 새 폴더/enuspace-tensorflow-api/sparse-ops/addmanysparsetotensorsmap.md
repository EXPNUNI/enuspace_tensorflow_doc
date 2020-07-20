# AddManySparseToTensorsMap

---

## tensorflow C++ API

[tensorflow::ops::AddManySparseToTensorsMap](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/add-many-sparse-to-tensors-map)

[Add](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/add.html#classtensorflow_1_1ops_1_1_add) an `N`-minibatch `SparseTensor` to a `SparseTensorsMap`, return `N` handles.

---

## Summary

A `SparseTensor` of rank `R` is represented by three tensors: `sparse_indices`, `sparse_values`, and `sparse_shape`, where

`sparse_indices.shape[1] == sparse_shape.shape[0] == R`

An `N`-minibatch of `SparseTensor` objects is represented as a `SparseTensor` having a first `sparse_indices` column taking values between `[0, N)`, where the minibatch size `N == sparse_shape[0]`.

The input `SparseTensor` must have rank `R` greater than 1, and the first dimension is treated as the minibatch dimension. Elements of the `SparseTensor` must be sorted in increasing order of this first dimension. The stored `SparseTensor` objects pointed to by each row of the output `sparse_handles` will have rank `R-1`.

The `SparseTensor` values can then be read out as part of a minibatch by passing the given keys as vector elements to [`TakeManySparseFromTensorsMap`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/take-many-sparse-from-tensors-map.html#classtensorflow_1_1ops_1_1_take_many_sparse_from_tensors_map). To ensure the correct `SparseTensorsMap` is accessed, ensure that the same `container` and `shared_name` are passed to that Op. If no `shared_name` is provided here, instead use the name of the [Operation](https://www.tensorflow.org/api_docs/cc/class/tensorflow/operation.html#classtensorflow_1_1_operation) created by calling [`AddManySparseToTensorsMap`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/add-many-sparse-to-tensors-map.html#classtensorflow_1_1ops_1_1_add_many_sparse_to_tensors_map) as the `shared_name` passed to [`TakeManySparseFromTensorsMap`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/take-many-sparse-from-tensors-map.html#classtensorflow_1_1ops_1_1_take_many_sparse_from_tensors_map). Ensure the Operations are colocated.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* sparse\_indices: 2-D. The `indices` of the minibatch `SparseTensor`. 
  `sparse_indices[:, 0]` must be ordered values in `[0, N)`.
* sparse\_values: 1-D. The `values` of the minibatch `SparseTensor`.
* sparse\_shape: 1-D. The `shape` of the minibatch `SparseTensor`. The minibatch size `N == sparse_shape[0]`
  .

Optional attributes \(see [`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/add-many-sparse-to-tensors-map/attrs.html#structtensorflow_1_1ops_1_1_add_many_sparse_to_tensors_map_1_1_attrs)\):

* container: The container name for the `SparseTensorsMap` created by this op.
* shared\_name: The shared name for the `SparseTensorsMap` created by this op. If blank, the new [Operation](https://www.tensorflow.org/api_docs/cc/class/tensorflow/operation.html#classtensorflow_1_1_operation)'s unique name is used.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): 1-D. The handles of the `SparseTensor` now stored in the `SparseTensorsMap`. [Shape](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/shape.html#classtensorflow_1_1ops_1_1_shape): `[N]`.

---

## AddManySparseToTensorsMap block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_sparse.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_sparse.cpp)

![](/assets/sparse_op/AddManySparseToTensorsMap1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input sparse\_indices: connect  Input node.
* Input sparse\_values: connect Input node.
* Input sparse\_shape: connect Input node.
* AddManySparseToTensorsMap::Attrs attrs : Input attrs in value. ex\) container\_= ;shared\_name\_= ;

Return:

* Output output : Output object of AddManySparseToTensorsMap class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/sparse_op/AddManySparseToTensorsMap2.jpg)

