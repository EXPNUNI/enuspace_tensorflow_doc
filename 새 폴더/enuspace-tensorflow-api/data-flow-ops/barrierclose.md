# BarrierClose

---

## tensorflow C++ API

[tensorflow::ops::BarrierClose](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/barrier-close)

Closes the given barrier.

---

## Summary

This operation signals that no more new elements will be inserted in the given barrier. Subsequent InsertMany that try to introduce a new key will fail. Subsequent InsertMany operations that just add missing components to already existing elements will continue to succeed. Subsequent TakeMany operations will continue to succeed if sufficient completed elements remain in the barrier. Subsequent TakeMany operations that would block will fail immediately.

Arguments:

* scope: A Scope object
* handle: The handle to a barrier.

Optional attributes \(see`Attrs`\):

* cancel\_pending\_enqueues: If true, all pending enqueue requests that are blocked on the barrier's queue will be canceled. InsertMany will fail, even if no new key is introduced.

Returns:

* the created Operation.

Constructor

* BarrierClose\(const ::tensorflow::Scope & scope, ::tensorflow::Input handle, const BarrierClose::Attrs & attrs\).

Public attributes

* Operation operation.

---

## BarrierClose block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_data\_flow\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_data_flow_ops.cpp)

![](/assets/dataflow_BarrierClose_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input handle : connect Input node.
* BarrierClose::Attrs attrs : Input attrs. ex\\) cancel\_pending\_enqueues\_ = false;

Return:

* Operation operation: Operation operation of BarrierClose class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/dataflow_BarrierClose_Method.png)

