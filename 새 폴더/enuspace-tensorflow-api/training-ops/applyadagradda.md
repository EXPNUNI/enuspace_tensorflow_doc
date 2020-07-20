# ApplyAdagradDA

---

## tensorflow C++ API

[tensorflow::ops::ApplyAdagradDA](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/apply-adagrad-d-a)

Update '\*var' according to the proximal adagrad scheme.

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* var: Should be from a Variable\(\).
* gradient\_accumulator: Should be from a Variable\(\).
* gradient\_squared\_accumulator: Should be from a Variable\(\).
* grad: The gradient.
* lr: Scaling factor. Must be a scalar.
* l1: L1 regularization. Must be a scalar.
* l2: L2 regularization. Must be a scalar.
* global\_step: Training step number. Must be a scalar.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/apply-adagrad-d-a/attrs.html#structtensorflow_1_1ops_1_1_apply_adagrad_d_a_1_1_attrs)\):

* use\_locking: If True, updating of the var and accum tensors will be protected by a lock; otherwise the behavior is undefined, but may exhibit less contention.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): Same as "var".

---

## ApplyAdagradDA block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_training.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_string.cpp)

![](/assets/training/ApplyAdagradDA1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input var: connect  Input node.
* Input gradient\_accumulator: connect  Input node.
* Input gradient\_squared\_accumulator: connect  Input node.
* Input grad: connect  Input node.
* Input lr: connect  Input node.
* Input l1: connect  Input node.
* Input l2: connect  Input node.
* Input global\_step: connect  Input node.
* ApplyAdagradDA::Attrs attrs : Input attrs in value. ex\) use\_locking\_ = false;

Return:

* Output output : Output object of ApplyAdagradDA class object.

Result:

* std::vector\(Tensor\) result\_output : Returned object of executed result by calling session.

---

## Using Method

![](/assets/training/ApplyAdagradDA2.jpg)

