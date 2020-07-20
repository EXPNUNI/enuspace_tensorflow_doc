# SoftmaxCrossEntropyWithLogits

---

## tensorflow C++ API

[tensorflow::ops::SoftmaxCrossEntropyWithLogits](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/softmax-cross-entropy-with-logits)

Computes softmax cross entropy cost and gradients to backpropagate.

---

## Summary

Inputs are the logits, not probabilities.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* features: batch\_size x num\_classes matrix
* labels: batch\_size x num\_classes matrix The caller must ensure that each batch of labels represents a valid probability distribution.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) loss: Per example loss \(batch\_size vector\).
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) backprop: backpropagated gradients \(batch\_size x num\_classes matrix\).

---

## SoftmaxCrossEntropyWithLogits block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_nn.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

![](/nn-ops/SoftmaxCrossEntropyWithLogits1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input features: connect  Input node.
* Input labels: connect  Input node.

Return:

* Output loss: Output object of SoftmaxCrossEntropyWithLogits  class object.
* Output backprop: Output object of SoftmaxCrossEntropyWithLogits  class object.

Result:

* std::vector\(Tensor\) result\_loss : Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_backprop : Returned object of executed result by calling session.

---

## Using Method

![](/nn-ops/SoftmaxCrossEntropyWithLogits2.jpg)

