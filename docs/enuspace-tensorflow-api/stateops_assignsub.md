--- 
layout: default 
title: AssignSub 
parent: state_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# AssignSub

---

## tensorflow C++ API

[tensorflow::ops::AssignSub](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/assign-sub)

Update 'ref' by subtracting 'value' from it.

---

## Summary

This operation outputs "ref" after the update is done. This makes it easier to chain operations that need to use the reset value.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* ref: Should be from a [`Variable`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/variable.html#classtensorflow_1_1ops_1_1_variable) node.
* value: The value to be subtracted to the variable.

Optional attributes \(see [`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/assign-sub/attrs.html#structtensorflow_1_1ops_1_1_assign_sub_1_1_attrs)\):

* use\_locking: If True, the subtraction will be protected by a lock; otherwise the behavior is undefined, but may exhibit less contention.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): = Same as "ref". Returned as a convenience for operations that want to use the new value after the variable has been updated.

---

## AssignSub block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_state.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_state.cpp)

![](./assets/state_op/AssignSub1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input ref: connect  Input node.
* Input value: connect Input node.
* AssignSub ::Attrs attrs : Input attrs in value. ex\)use\_locking\_ = true;

Return:

* Output output : Output object of AssignSub class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](./assets/state_op/AssignSub2.jpg)

