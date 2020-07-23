--- 
layout: default 
title: ApplyCenteredRMSProp 
parent: training_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# ApplyCenteredRMSProp

---

## tensorflow C++ API

[tensorflow::ops::ApplyCenteredRMSProp](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/apply-centered-r-m-s-prop)

Update '\*var' according to the centered RMSProp algorithm.

---

## Summary

The centered RMSProp algorithm uses an estimate of the centered second moment \(i.e., the variance\) for normalization, as opposed to regular RMSProp, which uses the \(uncentered\) second moment. This often helps with training, but is slightly more expensive in terms of computation and memory.

Note that in dense implementation of this algorithm, mg, ms, and mom will update even if the grad is zero, but in this sparse implementation, mg, ms, and mom will not update in iterations during which the grad is zero.

mean\_square = decay \* mean\_square + \(1-decay\) \* gradient \*\* 2 mean\_grad = decay \* mean\_grad + \(1-decay\) \* gradient

Delta = learning\_rate \* gradient / sqrt\(mean\_square + epsilon - mean\_grad \*\* 2\)

mg &lt;- rho \* mg\_{t-1} + \(1-rho\) \* grad ms &lt;- rho \* ms\_{t-1} + \(1-rho\) \* grad \* grad mom &lt;- momentum \* mom\_{t-1} + lr \* grad / sqrt\(ms - mg \* mg + epsilon\) var &lt;- var - mom

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* var: Should be from a Variable\(\).
* mg: Should be from a Variable\(\).
* ms: Should be from a Variable\(\).
* mom: Should be from a Variable\(\).
* lr: Scaling factor. Must be a scalar.
* rho: Decay rate. Must be a scalar.
* epsilon: Ridge term. Must be a scalar.
* grad: The gradient.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/apply-centered-r-m-s-prop/attrs.html#structtensorflow_1_1ops_1_1_apply_centered_r_m_s_prop_1_1_attrs)\):

* use\_locking: If`True`, updating of the var, mg, ms, and mom tensors is protected by a lock; otherwise the behavior is undefined, but may exhibit less contention.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): Same as "var".

---

## ApplyCenteredRMSProp block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_training.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_string.cpp)

![](./assets/training/ApplyCenteredRMSProp1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input var: connect  Input node.
* Input mg: connect  Input node.
* Input ms: connect  Input node.
* Input mom: connect  Input node.
* Input lr: connect  Input node.
* Input rho: connect  Input node.
* Input momentum: connect  Input node.
* Input epsilon: connect  Input node.
* Input grad: connect  Input node.
* ApplyCenteredRMSProp ::Attrs attrs : Input attrs in value. ex\) use\_locking\_ = false;

Return:

* Output output : Output object of ApplyCenteredRMSProp class object.

Result:

* std::vector\(Tensor\) result\_output : Returned object of executed result by calling session.

---

## Using Method

![](./assets/training/ApplyCenteredRMSProp2.jpg)

