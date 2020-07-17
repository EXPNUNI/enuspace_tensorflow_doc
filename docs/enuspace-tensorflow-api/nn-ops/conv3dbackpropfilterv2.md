# Conv3DBackpropFilterV2

---

## tensorflow C++ API

[tensorflow::ops::Conv3DBackpropFilterV2](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/conv3-d-backprop-filter-v2)

Computes the gradients of 3-D convolution with respect to the filter.

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope)  object
* input:[Shape](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/shape.html#classtensorflow_1_1ops_1_1_shape)`[batch, depth, rows, cols, in_channels]`.
* filter\_sizes: An integer vector representing the tensor shape of`filter`where`filter`is a 5-D`[filter_depth, filter_height, filter_width, in_channels, out_channels]`tensor.
* out\_backprop: Backprop signal of shape`[batch, out_depth, out_rows, out_cols, out_channels]`.
* strides: 1-D tensor of length 5. The stride of the sliding window for each dimension of`input`.  
  Must have`strides[0] = trides[4] = 1.`

* padding: The type of padding algorithm to use.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/conv3-d-backprop-filter-v2/attrs.html#structtensorflow_1_1ops_1_1_conv3_d_backprop_filter_v2_1_1_attrs)\):

* data\_format: The data format of the input and output data. With the default format "NDHWC", the data is stored in the order of: \[batch, in\_depth, in\_height, in\_width, in\_channels\]. Alternatively, the format could be "NCDHW", the data storage order is: \[batch, in\_channels, in\_depth, in\_height, in\_width\].

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The output tensor.

---

## Conv3DBackpropFilterV2 block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_nn.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

![](/nn-ops/Conv3DBackpropFilterV21.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input input: connect  Input node.
* Input filter\_sizes: connect  Input node.
* Input out\_backprop: connect  Input node.
* gtl::ArraySlice&lt; int &gt; strides: Input strides in value ex\)1,2,2,1,1
* StringPiece padding: Input paddingin value ex\)SAME
* Conv3DBackpropFilterV2 ::Attrs attrs : Input attrs in value. ex\) data\_format\_ = NDHWC;

Return:

* Output output : Output object of Conv3DBackpropFilterV2 class object.

Result:

* std::vector\(Tensor\) _result\_output_ : Returned object of executed result by calling session.

---

## Using Method

![](/nn-ops/Conv3DBackpropFilterV22.jpg)

