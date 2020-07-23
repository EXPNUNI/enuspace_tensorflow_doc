--- 
layout: default 
title: ScatterUpdate 
parent: state_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# ScatterUpdate

---

## tensorflow C++ API

[tensorflow::ops::ScatterUpdate](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/scatter-update)

Applies sparse updates to a variable reference.

---

## Summary

This operation computes

\`\`\`python Scalar indices

ref\[indices, ...\] = updates\[...\]

Vector indices \(for each i\)

ref\[indices\[i\], ...\] = updates\[i, ...\]

High rank indices \(for each i, ..., j\)

ref\[indices\[i, ..., j\], ...\] = updates\[i, ..., j, ...\] \`\`\`

This operation outputs `ref` after the update is done. This makes it easier to chain operations that need to use the reset value.

If values in `ref` is to be updated more than once, because there are duplicate entries in `indices`, the order at which the updates happen for each value is undefined.

Requires `updates.shape = indices.shape + ref.shape[1:]`.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* ref: Should be from a [`Variable`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/variable.html#classtensorflow_1_1ops_1_1_variable) node.
* indices: A tensor of indices into the first dimension of `ref`.
* updates: A tensor of updated values to store in `ref`.

Optional attributes \(see [`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/scatter-update/attrs.html#structtensorflow_1_1ops_1_1_scatter_update_1_1_attrs)\):

* use\_locking: If True, the assignment will be protected by a lock; otherwise the behavior is undefined, but may exhibit less contention.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): = Same as `ref`. Returned as a convenience for operations that want to use the updated values after the update is done.

---

## ScatterUpdate block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_state.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_state.cpp)

![](./assets/state_op/ScatterUpdate1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input ref: connect  Input node.
* Input indices: connect Input node.
* Input updates: connect Input node.
* ScatterUpdate::Attrs attrs : Input attrs in value. ex\)use\_locking\_ = true;

Return:

* Output output : Output object of ScatterUpdate class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](./assets/state_op/ScatterUpdate2.jpg)

\*Assign에 연결된 ClientSession은 Assign값을 확인하기 위해 작성된 temp입니다. ClientSession은 처리순서가 있으므로 테스트시 생성을 마지막에 작성하여 사용합니다

