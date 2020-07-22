--- 
layout: default 
title: FifoQueue 
parent: data_flow_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# FIFOQueue

---

## tensorflow C++ API

[tensorflow::ops::FIFOQueue](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/f-i-f-o-queue)

A queue that produces elements in first-in first-out order.

---

## Summary

Arguments:

* scope: A Scope object
* component\_types: The type of each component in a value.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/f-i-f-o-queue/attrs.html#structtensorflow_1_1ops_1_1_f_i_f_o_queue_1_1_attrs)\):

* shapes: The shape of each component in a value. The length of this attr must be either 0 or the same as the length of component\_types. If the length of this attr is 0, the shapes of queue elements are not constrained, and only one element may be dequeued at a time.
* capacity: The upper bound on the number of elements in this queue. Negative numbers mean no limit.
* container: If non-empty, this queue is placed in the given container. Otherwise, a default container is used.
* shared\_name: If non-empty, this queue will be shared under the given name across multiple sessions.

Returns:

* Output : The handle to the queue.

Constructor

* FIFOQueue\(const ::tensorflow::Scope & scope, const DataTypeSlice & component\_types, const FIFOQueue::Attrs & attrs\).

Public attributes

* tensorflow::Output handle.

---

## FIFOQueue block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_data\_flow\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_data_flow_ops.cpp)

![](../assets/dataflow_FIFOQueue_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* component\_types: Input DataType list accordance with each input.
* FIFOQueue::Attrs attrs : input attrs data. ex\) shapes\_ = \{\}; capacity\_ = -1;container\_ = ""; shared\_name\_ = "";

Return:

* Output handle: Output object of FIFOQueue class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](../assets/dataflow_DynamicPartition_Method.png)

