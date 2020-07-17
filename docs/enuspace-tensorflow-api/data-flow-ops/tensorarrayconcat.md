# TensorArrayConcat

---

## tensorflow C++ API

[tensorflow::ops::TensorArrayConcat](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/tensor-array-concat)

Concat the elements from the TensorArray into value.

---

## Summary

Takes`T`elements of shapes

\`\`\` \(n0 x d0 x d1 x ...\), \(n1 x d0 x d1 x ...\), ..., \(n\(T-1\) x d0 x d1 x ...\) \`\`\`

and concatenates them into a Tensor of shape:

`(n0 + n1 + ... + n(T-1) x d0 x d1 x ...)`

All elements must have the same shape \(excepting the first dimension\).

Arguments:

* scope: A Scope object
* handle: The handle to a TensorArray.
* flow\_in: A float scalar that enforces proper chaining of operations.
* dtype: The type of the elem that is returned.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/tensor-array-concat/attrs.html#structtensorflow_1_1ops_1_1_tensor_array_concat_1_1_attrs)\):

* element\_shape\_except0: The expected shape of an element, if known, excluding the first dimension. Used to validate the shapes of TensorArray elements. If this shape is not fully specified, concatenating zero-size TensorArrays is an error.

Returns:

* Output value: All of the elements in the TensorArray , concatenated along the first axis.
* Output lengths: A vector of the row sizes of the original T elements in the value output. In the example above, this would be the values:`(n1, n2, ..., n(T-1))`.

Constructor

* TensorArrayConcat\(const ::tensorflow::Scope & scope, ::tensorflow::Input handle, ::tensorflow::Input flow\_in, DataType dtype, const TensorArrayConcat::Attrs & attrs\).

Public attributes

* tensorflow::Output lengths.
* tensorflow::Output value.

---

## TensorArrayConcat block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_data\_flow\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_data_flow_ops.cpp)

![](/assets/dataflow_TensorArrayConcat_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* handle : connect Input node.
* flow\_in : connect Input node.
* DataType dtype : input datatype. ex\) DT\_DOUBLE
* TensorArrayConcat::Attrs attrs : input attrs array. ex\) element\_shape\_except0\_ ={2}

Return:

* Output value : Output object of TensorArrayConcat class object.
* Output  lengths : Output object of TensorArrayConcat class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/dataflow_TensorArrayConcat_Method.png)

