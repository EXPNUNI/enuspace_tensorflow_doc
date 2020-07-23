--- 
layout: default 
title: ApplyAdagrad 
parent: training_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# ApplyAdagrad

---

## tensorflow C++ API

[tensorflow::ops::ApplyAdagrad](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/apply-adagrad)

Update '\*var' according to the adagrad scheme.

---

## Summary

accum += grad \* grad var -= lr \* grad \* \(1 / sqrt\(accum\)\)

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* var: Should be from a Variable\(\).
* accum: Should be from a Variable\(\).
* lr: Scaling factor. Must be a scalar.
* grad: The gradient.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/apply-adagrad/attrs.html#structtensorflow_1_1ops_1_1_apply_adagrad_1_1_attrs)\):

* use\_locking: If `True`, updating of the var and accum tensors will be protected by a lock; otherwise the behavior is undefined, but may exhibit less contention.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): Same as "var".

---

## ApplyAdagrad block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_training.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_string.cpp)

![](./assets/training/ApplyAdagrad1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input var: connect  Input node.
* Input accum: connect  Input node.
* Input lr: connect  Input node.
* Input grad: connect  Input node.
* ApplyAdagrad ::Attrs attrs : Input attrs in value. ex\) use\_locking\_ = false;

Return:

* Output output : Output object of ApplyAdagrad class object.

Result:

* std::vector\(Tensor\) result\_output : Returned object of executed result by calling session.

---

## Using Method

![](./assets/training/ApplyAdagrad2.jpg)![](/assets/training/ApplyAdagrad3.jpg)

