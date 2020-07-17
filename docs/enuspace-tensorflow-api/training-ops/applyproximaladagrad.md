# ApplyProximalAdagrad

---

## tensorflow C++ API

[tensorflow::ops::ApplyProximalAdagrad](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/apply-proximal-adagrad)

Update '\*var' and '\*accum' according to FOBOS with Adagrad learning rate.

---

## Summary

accum += grad \* grad prox\_v = var - lr \* grad \* \(1 / sqrt\(accum\)\) var = sign\(prox\_v\)/\(1+lr\*l2\) \* max{\|prox\_v\|-lr\*l1,0}

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* var: Should be from a Variable\(\).
* accum: Should be from a Variable\(\).
* lr: Scaling factor. Must be a scalar.
* l1: L1 regularization. Must be a scalar.
* l2: L2 regularization. Must be a scalar.
* grad: The gradient.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/apply-proximal-adagrad/attrs.html#structtensorflow_1_1ops_1_1_apply_proximal_adagrad_1_1_attrs)\):

* use\_locking: If True, updating of the var and accum tensors will be protected by a lock; otherwise the behavior is undefined, but may exhibit less contention.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) : Same as "var".

---

## ApplyProximalAdagrad block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_training.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_string.cpp)

![](/assets/training/ApplyProximalAdagrad1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input var: connect  Input node.
* Input accum: connect  Input node.
* Input lr: connect  Input node.
* Input l1: connect  Input node.
* Input l2: connect  Input node.
* Input grad: connect  Input node.
* ApplyProximalAdagrad ::Attrs attrs : Input attrs in value. ex\) use\_locking\_ = false;

Return:

* Output output : Output object of ApplyProximalAdagrad class object.

Result:

* std::vector\(Tensor\) result\_output : Returned object of executed result by calling session.

---

## Using Method

![](/assets/training/ApplyProximalAdagrad2.jpg)

