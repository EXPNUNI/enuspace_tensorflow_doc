# HistogramSummary

---

## tensorflow C++ API

[tensorflow::ops::HistogramSummary](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/histogram-summary)

Outputs a `Summary `protocol buffer with a histogram.

---

## Summary

The generated[\`Summary\`](https://www.tensorflow.org/code/tensorflow/core/framework/summary.proto)has one summary value containing a histogram for`values`.

This op reports an`InvalidArgument`error if any value is not finite.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* tag: Scalar. Tag to use for the `Summary.Value`.
* values: [Any](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/any.html#classtensorflow_1_1ops_1_1_any) shape. Values to use to build the histogram.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): Scalar. Serialized `Summary `protocol buffer.

---

## HistogramSummary block

Source link :[ https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_logging\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_logging_ops.cpp)

![](/assets/logging_ops/logging_ops_histogramsummary_symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input tag : Input tag name node\(string\).
* Input values : [Any](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/any.html#classtensorflow_1_1ops_1_1_any) shape. Values to use to build the histogram.

Return:

* Output summary : Scalar. Serialized `Summary `protocol buffer.

Result:

* std::vector&lt;Tensor&gt; result\_summary : Returned object of executed result by calling session.

---

## Using Method

![](/assets/logging_ops/logging_ops_histogramsummary_method.png)



