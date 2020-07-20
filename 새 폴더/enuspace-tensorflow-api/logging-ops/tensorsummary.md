# TensorSummary

---

## tensorflow C++ API

[tensorflow::ops::TensorSummary](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/tensor-summary)

Outputs a `Summary `protocol buffer with a tensor.

---

## Summary

This op is being phased out in favor of[TensorSummaryV2](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/tensor-summary-v2.html#classtensorflow_1_1ops_1_1_tensor_summary_v2), which lets callers pass a tag as well as a serialized SummaryMetadata proto string that contains plugin-specific data. We will keep this op to maintain backwards compatibility.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* tensor: A tensor to serialize.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/tensor-summary/attrs.html#structtensorflow_1_1ops_1_1_tensor_summary_1_1_attrs)\):

* description: A json-encoded SummaryDescription proto.
* labels: An unused list of strings.
* display\_name: An unused string.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The summary tensor.

---

## TensorSummary block

Source link :[ https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_logging\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_logging_ops.cpp)

![](/assets/logging_ops/logging_ops_tensorsymmary_symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input tensor : Input tensor node.
* TensorSummary::Attrs attrs :optional attributes.

Return:

* Output summary : The summary tensor.

Result:

* std::vector&lt;Tensor&gt; result\_summary : Returned object of executed result by calling session.

---

## Using Method

![](/assets/logging_ops/logging_ops_tensorsummary_method.png)



