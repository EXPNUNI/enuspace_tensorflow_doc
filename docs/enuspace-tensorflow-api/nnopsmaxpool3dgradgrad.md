--- 
layout: default 
title: MaxPool3DGradGrad 
parent: nn_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# MaxPool3DGradGrad

---

## tensorflow C++ API

[tensorflow::ops::MaxPool3DGradGrad](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/max-pool3-d-grad-grad)

Computes second-order gradients of the maxpooling function.

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope)  object
* orig\_input: The original input tensor.
* orig\_output: The original output tensor.
* grad:[Output](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) backprop of shape`[batch, depth, rows, cols, channels]`.
* ksize: 1-D tensor of length 5. The size of the window for each dimension of the input tensor. Must have
  `ksize[0] = ksize[4] = 1`.
* strides: 1-D tensor of length 5. The stride of the sliding window for each dimension of`input`
  . Must have`strides[0] = strides[4] = 1`.
* padding: The type of padding algorithm to use.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/max-pool3-d-grad-grad/attrs.html#structtensorflow_1_1ops_1_1_max_pool3_d_grad_grad_1_1_attrs)\):

* data\_format: The data format of the input and output data. With the default format "NDHWC", the data is stored in the order of: \[batch, in\_depth, in\_height, in\_width, in\_channels\]. Alternatively, the format could be "NCDHW", the data storage order is: \[batch, in\_channels, in\_depth, in\_height, in\_width\].

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): Gradients of gradients w.r.t. the input to`max_pool`.

---

## MaxPool3DGradGrad block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_nn.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

![](./assets/nn-ops/MaxPool3DGradGrad1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input orig\_input: connect  Input node.
* Input orig\_output: connect  Input node.
* Input grad: connect  Input node.
* ArraySlice&lt; int&gt; ksize: input ksize in values. ex\)1,2,2,2,1
* ArraySlice&lt; int&gt; strides: input ksize in values. ex\)1,4,3,2,1
* stringpiece padding: input padding in value. ex\)SAME
* MaxPool3DGradGrad ::Attrs attrs: input attrs in values \)data\_format\_ = NDHWC;

Return:

* Output output: Output object of MaxPool3DGradGrad class object.

Result:

* std::vector\(Tensor\) result\_output  : Returned object of executed result by calling session.

---

## Using Method

![](./assets/nn-ops/MaxPool3DGradGrad2.jpg)

