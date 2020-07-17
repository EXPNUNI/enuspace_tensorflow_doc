# InTopK

---

## tensorflow C++ API

[tensorflow::ops::InTopK](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/in-top-k)

Says whether the targets are in the top `K`predictions.

---

## Summary

This outputs a`batch_size`bool array, an entry`out[i]`is`true`if the prediction for the target class is among the top`k`predictions among all predictions for example`i`. Note that the behavior of[`InTopK`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/in-top-k.html#classtensorflow_1_1ops_1_1_in_top_k)differs from the[`TopK`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/top-k.html#classtensorflow_1_1ops_1_1_top_k)op in its handling of ties; if multiple classes have the same prediction value and straddle the top-`k`boundary, all of those classes are considered to be in the top`k`.

More formally, let

\\(predictions\_i\\) be the predictions for all classes for example`i`, \\(targets\_i\\) be the target class for example`i`, \\(out\_i\\) be the output for example`i`,

$$out\_i = predictions\_{i, targets\_i} TopKIncludingTies\(predictions\_i\)$$

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* predictions: A `batch_size`x `classes`tensor.
* targets: A `batch_size`vector of class ids.
* k: Number of top elements to look at for computing precision.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): Computed Precision at`k`as a`bool`[`Tensor`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor).

---

## InTopK block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_nn.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

![](/nn-ops/InTopK1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input predictions: connect  Input node.
* Input targets: connect  Input node.
* int64 k: Input k in value ex\)1

Return:

* Output output: Output object of InTopK class object.

Result:

* std::vector\(Tensor\) result\_precision  : Returned object of executed result by calling session.

---

## Using Method

![](/nn-ops/InTopK2.jpg)

