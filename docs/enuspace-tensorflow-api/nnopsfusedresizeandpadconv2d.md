--- 
layout: default 
title: FusedResizeAndPadConv2D 
parent: nn_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# FusedResizeAndPadConv2D

---

## tensorflow C++ API

[tensorflow::ops::FusedResizeAndPadConv2D](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/fused-resize-and-pad-conv2-d)

Performs a resize and padding as a preprocess during a convolution.

---

## Summary

It's often possible to do spatial transformations more efficiently as part of the packing stage of a convolution, so this op allows for an optimized implementation where these stages are fused together. This prevents the need to write out the intermediate results as whole tensors, reducing memory pressure, and we can get some latency gains by merging the transformation calculations. The data\_format attribute for[Conv2D](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/conv2-d.html#classtensorflow_1_1ops_1_1_conv2_d)isn't supported by this op, and defaults to 'NHWC' order. Internally this op uses a single per-graph scratch buffer, which means that it will block if multiple versions are being run in parallel. This is because this operator is primarily an optimization to minimize memory usage.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* input: 4-D with shape `[batch, in_height, in_width, in_channels]`.
* size: A 1-D int32 [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) of 2 elements: `new_height, new_width`. The new size for the images.
* paddings: A two-column matrix specifying the padding sizes. The number of rows must be the same as the rank of `input`.
* filter: 4-D with shape `[filter_height, filter_width, in_channels, out_channels]`.
* strides: 1-D of length 4. The stride of the sliding window for each dimension of `input`. Must be in the same order as the dimension specified with format.
* padding: The type of padding algorithm to use.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/fused-resize-and-pad-conv2-d/attrs.html#structtensorflow_1_1ops_1_1_fused_resize_and_pad_conv2_d_1_1_attrs)\):

* resize\_align\_corners: If true, rescale input by \(new\_height - 1\) / \(height - 1\), which exactly aligns the 4 corners of images and resized images. If false, rescale by new\_height / height. Treat similarly the width dimension.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The output tensor.

---

## FusedResizeAndPadConv2D block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_nn.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

![](./assets/nn-ops/FusedResizeAndPadConv2D1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input input: connect  Input node.
* Input size: connect  Input node.
* Input paddings: connect  Input node.
* Input filter: connect  Input node.
* StringPiece mode: Input mode in value. ex\) REFLECT
* ArraySlice&lt; int&gt; strides\_: Input \_strides in value ex\)1,3,2,1
* StringPiece mode: Input mode in value. ex\) SAME

Return:

* Output output: Output object of FusedPadConv2D class object.

Result:

* std::vector\(Tensor\) result\_output  : Returned object of executed result by calling session.

---

## Using Method

![](./assets/nn-ops/FusedResizeAndPadConv2D2.jpg)

