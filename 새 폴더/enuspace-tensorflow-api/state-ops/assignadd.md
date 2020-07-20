# AssignAdd

---

## tensorflow C++ API

[tensorflow::ops::AssignAdd](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/assign-add)

Update 'ref' by adding 'value' to it.

---

## Summary

This operation outputs "ref" after the update is done. This makes it easier to chain operations that need to use the reset value.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* ref: Should be from a [`Variable`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/variable.html#classtensorflow_1_1ops_1_1_variable) node.
* value: The value to be added to the variable.

Optional attributes \(see [`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/assign-add/attrs.html#structtensorflow_1_1ops_1_1_assign_add_1_1_attrs)\):

* use\_locking: If True, the addition will be protected by a lock; otherwise the behavior is undefined, but may exhibit less contention.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): = Same as "ref". Returned as a convenience for operations that want to use the new value after the variable has been updated.

---

## AssignAdd block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_state.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_state.cpp)

![](/assets/state_op/AssignAdd1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input ref: connect  Input node.
* Input value: connect Input node.
* AssignAdd ::Attrs attrs : Input attrs in value. ex\)use\_locking\_ = true;

Return:

* Output output : Output object of AssignAdd  class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/state_op/AssignAdd2.jpg)

