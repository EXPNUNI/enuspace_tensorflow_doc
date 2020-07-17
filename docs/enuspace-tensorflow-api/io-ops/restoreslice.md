# RestoreSlices

---

## tensorflow C++ API

[tensorflow::ops::RestorSlices](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/restore-slice)

Restores a tensor from checkpoint files.

---

## Summary

This is like[`Restore`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/restore.html#classtensorflow_1_1ops_1_1_restore)except that restored tensor can be listed as filling only a slice of a larger tensor.`shape_and_slice`specifies the shape of the larger tensor and the slice that the restored tensor covers.

The`shape_and_slice`input has the same format as the elements of the`shapes_and_slices`input of the[`SaveSlices`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/save-slices.html#classtensorflow_1_1ops_1_1_save_slices)op.

Arguments:

* scope: A Scope object
* file\_pattern: Must have a single element. The pattern of the files from which we read the tensor.
* tensor\_name: Must have a single element. The name of the tensor to be restored.
* shape\_and\_slice: Scalar. The shapes and slice specifications to use when restoring a tensors.
* dt: The type of the tensor to be restored.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/restore-slice/attrs.html#structtensorflow_1_1ops_1_1_restore_slice_1_1_attrs)\):

* preferred\_shard: Index of file to open first if multiple files match`file_pattern`. See the documentation for[`Restore`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/restore.html#classtensorflow_1_1ops_1_1_restore).

Returns:

* Output : The restored tensor.

Constructor

* RestoreSlice\(const ::tensorflow::Scope & scope, ::tensorflow::Input file\_pattern, ::tensorflow::Input tensor\_name, ::tensorflow::Input shape\_and\_slice, DataType dt, const RestoreSlice::Attrs & attrs\).

Public attributes

* tensorflow::Output tensor 

---

## Restore block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_i\_o\_\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_io_ops.cpp)

![](/assets/io_RestoreSlices_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input file\_pattern: input file\_pattern with path.
* Input tensor\_names: input tensor\_name.
* Restore::Attrs attrs : input attrs. ex\) preferred\_shard\_ = -1;

Return:

* Output  tensor : Output  tensor of Restore class object.  

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/io_SaveSlices_Method.png)

