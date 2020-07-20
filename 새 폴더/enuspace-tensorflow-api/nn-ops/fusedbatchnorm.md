# FusedBatchNorm

---

## tensorflow C++ API

[tensorflow::ops::FusedBatchNorm](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/fused-batch-norm)

Batch normalization.

---

## Summary

Note that the size of 4D Tensors are defined by either "NHWC" or "NCHW". The size of 1D Tensors matches the dimension C of the 4D Tensors.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* x: A 4D [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) for input data.
* scale: A 1D [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) for scaling factor, to scale the normalized x.
* offset: A 1D [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) for offset, to shift to the normalized x.
* mean: A 1D [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) for population mean. Used for inference only; must be empty for training.
* variance: A 1D [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) for population variance. Used for inference only; must be empty for training.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/fused-batch-norm/attrs.html#structtensorflow_1_1ops_1_1_fused_batch_norm_1_1_attrs)\):

* epsilon: A small float number added to the variance of x.
* data\_format: The data format for x and y. Either "NHWC" \(default\) or "NCHW".
* is\_training: A bool value to indicate the operation is for training \(default\) or inference.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) y: A 4D [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) for output data.
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)batch\_mean: A 1D [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) for the computed batch mean, to be used by TensorFlow to compute the running mean.
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)batch\_variance: A 1D [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) for the computed batch variance, to be used by TensorFlow to compute the running variance.
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)reserve\_space\_1: A 1D [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) for the computed batch mean, to be reused in the gradient computation.
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output)reserve\_space\_2: A 1D [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) for the computed batch variance \(inverted variance in the cuDNN case\), to be used in the gradient computation.

---

## FusedBatchNorm block

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



