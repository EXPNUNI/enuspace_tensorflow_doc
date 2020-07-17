# QueueSize

---

## tensorflow C++ API

[tensorflow::ops::QueueSize](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/queue-size)

Computes the number of elements in the given queue.

---

## Summary

Arguments:

* scope: A Scope object
* handle: The handle to a queue.

Returns:

* Output : the number of elements in the given queue.

Constructor

* QueueSize\(const ::tensorflow::Scope & scope, ::tensorflow::Input handle\).

Public attributes

* tensorflow::Output size.

---

## QueueSize block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_data\_flow\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_data_flow_ops.cpp)

![](/assets/dataflow_QueueSize_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input handle : connect Input node.

Return:

* Output  size: Output object of QueueSize class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/dataflow_QueueDequeueMany_Method.png)

