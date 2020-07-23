--- 
layout: default 
title: MaxPoolGradGradWithArgmax 
parent: nn_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# MaxPoolGradGradWithArgmax

---

## tensorflow C++ API

[tensorflow::ops::MaxPoolGradGradWithArgmax](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/max-pool-grad-grad-with-argmax)

Computes second-order gradients of the maxpooling function.

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* input: The original input.
* grad: 4-D with shape`[batch, height, width, channels]`. Gradients w.r.t. the input of`max_pool`.
* argmax: The indices of the maximum values chosen for each output of`max_pool`.
* ksize: The size of the window for each dimension of the input tensor.
* strides: The stride of the sliding window for each dimension of the input tensor.
* padding: The type of padding algorithm to use.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): Gradients of gradients w.r.t. the input of`max_pool`.

---

## MaxPoolGradGradWithArgmax block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_nn.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

![](./assets/nn-ops/MaxPoolGradGradWithArgmax1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input orig\_input: connect  Input node.
* Input grad: connect  Input node.
* Input argmax: connect  Input node.
* ArraySlice&lt; int&gt; ksize: input ksize in values. ex\)1,2,2,2,1
* ArraySlice&lt; int&gt; strides: input ksize in values. ex\)1,4,3,2,1
* stringpiece padding: input padding in value. ex\)SAME

Return:

* Output output: Output object of MaxPoolGradGradWithArgmax  class object.

Result:

* std::vector\(Tensor\) result\_output  : Returned object of executed result by calling session.

---

## Using Method

![](./assets/nn-ops/MaxPoolGradGradWithArgmax2.jpg)

