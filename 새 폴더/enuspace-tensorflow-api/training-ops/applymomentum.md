# ApplyMomentum

---

## tensorflow C++ API

[tensorflow::ops::ApplyMomentum](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/apply-momentum)

Update '\*var' according to the momentum scheme.

---

## Summary

accum\_new = accum + grad \* grad linear += grad + \(accum\_new^\(-lr\_power\) - accum^\(-lr\_power\)\) / lr \* var quadratic = 1.0 / \(accum\_new^\(lr\_power\) \* lr\) + 2 \* l2 var = \(sign\(linear\) \* l1 - linear\) / quadratic if \|linear\| &gt; l1 else 0.0 accum = accum\_new

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* var: Should be from a Variable\(\).
* accum: Should be from a Variable\(\).
* linear: Should be from a Variable\(\).
* grad: The gradient.
* lr: Scaling factor. Must be a scalar.
* l1: L1 regulariation. Must be a scalar.
* l2: L2 regulariation. Must be a scalar.
* lr\_power: Scaling factor. Must be a scalar.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/apply-ftrl/attrs.html#structtensorflow_1_1ops_1_1_apply_ftrl_1_1_attrs)\):

* use\_locking: If `True`, updating of the var and accum tensors will be protected by a lock; otherwise the behavior is undefined, but may exhibit less contention.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): Same as "var".

---

## ApplyMomentum block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_training.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_string.cpp)

![](/assets/training/ApplyFtrl1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input var: connect  Input node.
* Input accum: connect  Input node.
* Input linear: connect  Input node.
* Input grad: connect  Input node.
* Input lr: connect  Input node.
* Input l1: connect  Input node.
* Input l2: connect  Input node.
* Input lr\_power: connect  Input node.
* ApplyFtrl ::Attrs attrs : Input attrs in value. ex\) use\_locking\_ = false;

Return:

* Output output : Output object of ApplyMomentum class object.

Result:

* std::vector\(Tensor\) result\_output : Returned object of executed result by calling session.

---

## Using Method

![](/assets/training/ApplyFtrl2.jpg)

