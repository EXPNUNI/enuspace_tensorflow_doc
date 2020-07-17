# TakeManySparseFromTensorsMap

---

## tensorflow C++ API

[tensorflow::ops::TakeManySparseFromTensorsMap](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/take-many-sparse-from-tensors-map/attrs)

Read`SparseTensors`from a`SparseTensorsMap`and concatenate them.

---

## Summary

The input`sparse_handles`must be an`int64`matrix of shape`[N, 1]`where`N`is the minibatch size and the rows correspond to the output handles of[`AddSparseToTensorsMap`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/add-sparse-to-tensors-map.html#classtensorflow_1_1ops_1_1_add_sparse_to_tensors_map)or[`AddManySparseToTensorsMap`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/add-many-sparse-to-tensors-map.html#classtensorflow_1_1ops_1_1_add_many_sparse_to_tensors_map). The ranks of the original`SparseTensor`objects that went into the given input ops must all match. When the final`SparseTensor`is created, it has rank one higher than the ranks of the incoming`SparseTensor`objects \(they have been concatenated along a new row dimension on the left\).

The output`SparseTensor`object's shape values for all dimensions but the first are the max across the input`SparseTensor`objects' shape values for the corresponding dimensions. Its first shape value is`N`, the minibatch size.

The input`SparseTensor`objects' indices are assumed ordered in standard lexicographic order. If this is not the case, after this step run[`SparseReorder`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sparse-reorder.html#classtensorflow_1_1ops_1_1_sparse_reorder)to restore index ordering.

For example, if the handles represent an input, which is a`[2, 3]`matrix representing two original`SparseTensor`objects:

\`\`\` index = \[ 0\] \[10\] \[20\] values = \[1, 2, 3\] shape = \[50\] \`\`\`

and

\`\`\` index = \[ 2\] \[10\] values = \[4, 5\] shape = \[30\] \`\`\`

then the final`SparseTensor`will be:

\`\`\` index = \[0 0\] \[0 10\] \[0 20\] \[1 2\] \[1 10\] values = \[1, 2, 3, 4, 5\] shape = \[2 50\] \`\`\`

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope)object
* sparse\_handles: 1-D, The`N`serialized`SparseTensor`objects.[Shape](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/shape.html#classtensorflow_1_1ops_1_1_shape):`[N]`.
* dtype: The`dtype`of the`SparseTensor`objects stored in the`SparseTensorsMap`.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/take-many-sparse-from-tensors-map/attrs.html#structtensorflow_1_1ops_1_1_take_many_sparse_from_tensors_map_1_1_attrs)\):

* container: The container name for the`SparseTensorsMap`read by this op.
* shared\_name: The shared name for the`SparseTensorsMap`read by this op. It should not be blank; rather the`shared_name`
  or unique[Operation](https://www.tensorflow.org/api_docs/cc/class/tensorflow/operation.html#classtensorflow_1_1_operation) name of the Op that created the original`SparseTensorsMap`should be used.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)sparse\_indices: 2-D. The`indices`of the minibatch`SparseTensor`.
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)sparse\_values: 1-D. The`values`of the minibatch`SparseTensor`.
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)sparse\_shape: 1-D. The`shape`of the minibatch`SparseTensor`.

---

## TakeManySparseFromTensorsMap block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_sparse.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_sparse.cpp)

![](/assets/sparse_op/TakeManySparseFromTensorsMap1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input sparse\_handles: connect  Input node.
* Input output\_shape: connect  Input node.
* Datatype dtype : Input DataType in value ex\)DT\_FLOAT;
* TakeManySparseFromTensorsMap ::Attrs attrs : Input attrs in value. ex\) container\_ =;shared\_name\_ =AB;

Return:

* Output  sparse\_indices: Output object of TakeManySparseFromTensorsMap class object.
* Output  sparse\_values: Output object of TakeManySparseFromTensorsMap class object.
* Output  sparse\_shape: Output object of TakeManySparseFromTensorsMap class object.

Result:

* std::vector\(Tensor\) _result_\_sparse\_indices : Returned object of executed result by calling session.
* std::vector\(Tensor\) _result_\_sparse\_values : Returned object of executed result by calling session.
* std::vector\(Tensor\) _result_\_output\_shape : Returned object of executed result by calling session.

---

## Using Method

## ![](/assets/sparse_op/TakeManySparseFromTensorsMap2.jpg)



