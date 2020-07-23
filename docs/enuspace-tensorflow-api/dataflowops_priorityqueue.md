--- 
layout: default 
title: PriorityQueue 
parent: data_flow_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# PriorityQueue

---

## tensorflow C++ API

[tensorflow::ops::PriorityQueue](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/priority-queue)

A queue that produces elements sorted by the first component value.

---

## Summary

Note that the PriorityQueue requires the first component of any element to be a scalar int64, in addition to the other elements declared by component\_types. Therefore calls to Enqueue and EnqueueMany \(resp. Dequeue and DequeueMany\) on a PriorityQueue will all require \(resp. output\) one extra entry in their input \(resp. output\) lists..

Arguments:

* scope: A Scope object
* shapes: The shape of each component in a value. The length of this attr must be either 0 or the same as the length of component\_types. If the length of this attr is 0, the shapes of queue elements are not constrained, and only one element may be dequeued at a time.

Optional attributes \(see`Attrs`\):

* component\_types: The type of each component in a value.
* capacity: The upper bound on the number of elements in this queue. Negative numbers mean no limit.
* container: If non-empty, this queue is placed in the given container. Otherwise, a default container is used.
* shared\_name: If non-empty, this queue will be shared under the given name across multiple sessions.

Returns:

* Output : The handle to the queue.

Constructor

* PriorityQueue\(const ::tensorflow::Scope & scope, const gtl::ArraySlice&lt; PartialTensorShape &gt; & shapes,const PriorityQueue::Attrs & attrs\).

Public attributes

* tensorflow::Output handle.

---

## PriorityQueue block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_data\_flow\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_data_flow_ops.cpp)

![](./assets/dataflow_PriorityQueue_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* shapes: Input tensor shapes.

PriorityQueue ::Attrs attrs : input attrs data. ex\) component\_types_ = DT\_INT32; capacity _= -1;_container = ; shared\_name_ = ;

Return:

* Output handle: Output object of PriorityQueue class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](./assets/dataflow_PriorityQueue_Method.png)

