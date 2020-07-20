# ApplyProximalGradientDescent

---

## tensorflow C++ API

[tensorflow::ops::ApplyProximalGradientDescent](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/apply-proximal-gradient-descent)

Update '\*var' as FOBOS algorithm with fixed learning rate.

---

## Summary

prox\_v = var - alpha \* delta var = sign\(prox\_v\)/\(1+alpha\*l2\) \* max{\|prox\_v\|-alpha\*l1,0}

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* var: Should be from a Variable\(\).
* alpha: Scaling factor. Must be a scalar.
* l1: L1 regularization. Must be a scalar.
* l2: L2 regularization. Must be a scalar.
* delta: The change.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/apply-proximal-gradient-descent/attrs.html#structtensorflow_1_1ops_1_1_apply_proximal_gradient_descent_1_1_attrs)\):

* use\_locking: If True, the subtraction will be protected by a lock; otherwise the behavior is undefined, but may exhibit less contention.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): Same as "var".

---

## ApplyProximalGradientDescent block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_training.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_string.cpp)

![](/assets/training/ApplyProximalGradientDescent1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input var: connect  Input node.
* Input alpha: connect  Input node.
* Input l1: connect  Input node.
* Input l2: connect  Input node.
* Input delta: connect  Input node.
* ApplyProximalGradientDescent ::Attrs attrs : Input attrs in value. ex\) use\_locking\_ = false;

Return:

* Output output : Output object of ApplyProximalGradientDescent class object.

Result:

* std::vector\(Tensor\) result\_output : Returned object of executed result by calling session.

---

## Using Method

![](/assets/training/ApplyProximalGradientDescent2.jpg)

