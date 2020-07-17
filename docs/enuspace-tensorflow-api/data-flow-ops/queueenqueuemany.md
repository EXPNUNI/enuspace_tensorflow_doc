# QueueEnqueuMany

---

## tensorflow C++ API

[tensorflow::ops::QueueEnqueuMany](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/queue-enqueue)

Enqueues a tuple of one or more tensors in the given queue.

---

## Summary

The components input has k elements, which correspond to the components of tuples stored in the given queue.

N.B. If the queue is full, this operation will block until the given element has been enqueued \(or 'timeout\_ms' elapses, if specified\).

Arguments:

* scope: A Scope object
* handle: The handle to a queue.
* components: One or more tensors from which the enqueued tensors should be taken.

Optional attributes :

* timeout\_ms: If the queue is empty, this operation will block for up to timeout\_ms milliseconds. Note: This option is not supported yet.

Returns:

* the created Operation

Constructor

* QueueEnqueueMany\(const ::tensorflow::Scope & scope, ::tensorflow::Input handle, ::tensorflow::Input n, const DataTypeSlice & component\_types\).

Public attributes

* tensorflow::Operation operation.

---

## QueueEnqueueMany block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_data\_flow\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_data_flow_ops.cpp)

![](/assets/dataflow_QueueEnqueueMany_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* handle : connect  Input node.
* components : connect Input node..
* QueueEnqueueMany::Attrs attrs : input attrs data. ex\) timeout\_ms= -1;

Return:

* Output Operation: Output object of QueueEnqueueMany  class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/dataflow_QueueDequeueMany_Method.png)

