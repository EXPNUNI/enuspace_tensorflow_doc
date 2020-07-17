# FusedBatchNormGrad

---

## tensorflow C++ API

[tensorflow::ops::FusedBatchNormGrad](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/fused-batch-norm-grad)

Gradient for batch normalization.

---

## Summary

Note that the size of 4D Tensors are defined by either "NHWC" or "NCHW". The size of 1D Tensors matches the dimension C of the 4D Tensors.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* y\_backprop: A 4D [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) for the gradient with respect to y.
* x: A 4D [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) for input data.
* scale: A 1D [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) for scaling factor, to scale the normalized x.
* reserve\_space\_1: A 1D [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) for the computed batch mean, to be reused in the gradient computation.
* reserve\_space\_2: A 1D [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) for the computed batch variance \(inverted variance in the cuDNN case\), to be used in the gradient computation.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/fused-batch-norm-grad/attrs.html#structtensorflow_1_1ops_1_1_fused_batch_norm_grad_1_1_attrs)\):

* epsilon: A small float number added to the variance of x.
* data\_format: The data format for y\_backprop, x, x\_backprop. Either "NHWC" \(default\) or "NCHW".
* is\_training: A bool value to indicate the operation is for training \(default\) or inference.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) x\_backprop: A 4D [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) for the gradient with respect to x.
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)scale\_backprop: A 1D [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) for the gradient with respect to scale.
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)offset\_backprop: A 1D [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) for the gradient with respect to offset.
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)reserve\_space\_3: Unused placeholder to match the mean input in [FusedBatchNorm](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/fused-batch-norm.html#classtensorflow_1_1ops_1_1_fused_batch_norm).
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)reserve\_space\_4: Unused placeholder to match the variance input in [FusedBatchNorm](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/fused-batch-norm.html#classtensorflow_1_1ops_1_1_fused_batch_norm) .

---

## FusedBatchNormGrad block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_nn.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input x: connect  Input node.
* Input scale: connect  Input node.
* Input offset: connect  Input node.
* Input mean: connect  Input node.
* Input variance: connect  Input node.
* FusedBatchNorm ::Attrs attrs : Input attrs in value. 
  ex\) pseudo\_random\_ = false;overlapping\_ = false;deterministic\_ = false;seed\_ = 0;seed2\_ = 0;

Return:

* Output y: Output object of FractionalAvgPool class object.
* Output batch\_mean: Output object of FractionalAvgPool class object.
* Output batch\_variance: Output object of FractionalAvgPool class object.
* Output reserve\_space\_1: Output object of FractionalAvgPool class object.
* Output reserve\_space\_2: Output object of FractionalAvgPool class object.

Result:

* std::vector\(Tensor\) result\_y  : Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_batch\_variance  : Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_batch\_mean  : Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_reserve\_space\_1  : Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_reserve\_space\_2 : Returned object of executed result by calling session.

---

## Using Method



