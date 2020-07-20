# L2Loss

---

## tensorflow C++ API

[tensorflow::ops::L2Loss](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/l2-loss)

L2 Loss.

---

## Summary

Computes half the L2 norm of a tensor without the`sqrt`:

```
output = sum(t **2)/2
```

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* t: Typically 2-D, but may have any dimensions.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): 0-D.

---

## L2Loss block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_nn.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

![](/nn-ops/L2Loss1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input t: connect  Input node.

Return:

* Output output: Output object of L2Loss class object.

Result:

* std::vector\(Tensor\) result\_output  : Returned object of executed result by calling session.

---

## Using Method

![](/nn-ops/L2Loss2.jpg)

