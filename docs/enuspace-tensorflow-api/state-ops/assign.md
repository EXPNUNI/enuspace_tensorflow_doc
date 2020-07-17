# Assign

---

## tensorflow C++ API

[tensorflow::ops::Assign](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/assign)

Update 'ref' by assigning 'value' to it.

---

## Summary

This operation outputs "ref" after the assignment is done. This makes it easier to chain operations that need to use the reset value.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* ref: Should be from a [`Variable`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/variable.html#classtensorflow_1_1ops_1_1_variable) node. May be uninitialized.
* value: The value to be assigned to the variable.

Optional attributes \(see [`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/assign/attrs.html#structtensorflow_1_1ops_1_1_assign_1_1_attrs)\):

* validate\_shape: If true, the operation will validate that the shape of 'value' matches the shape of the [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) being assigned to. If false, 'ref' will take on the shape of 'value'.
* use\_locking: If True, the assignment will be protected by a lock; otherwise the behavior is undefined, but may exhibit less contention.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): = Same as "ref". Returned as a convenience for operations that want to use the new value after the variable has been reset.

---

## Assign block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_state.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_state.cpp)

![](/assets/state_op/Assign1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input ref: connect  Input node.
* Input value: connect Input node.
* Assign ::Attrs attrs : Input attrs in value. ex\) validate\_shape\_ = true;use\_locking\_ = true;

Return:

* Output output : Output object of Assign class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/state_op/Assign2.jpg)

