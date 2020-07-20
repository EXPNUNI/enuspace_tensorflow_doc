# QueueDequeuMany

---

## tensorflow C++ API

[tensorflow::ops::QueueDequeueMany](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/queue-dequeue-many)

Dequeues n tuples of one or more tensors from the given queue.

---

## Summary

If the queue is closed and there are fewer than`n`elements, then an OutOfRange error is returned.

This operation concatenates queue-element component tensors along the 0th dimension to make a single component tensor.[All](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/all.html#classtensorflow_1_1ops_1_1_all)of the components in the dequeued tuple will have size`n`in the 0th dimension.

This operation has`k`outputs, where`k`is the number of components in the tuples stored in the given queue, and output`i`is the ith component of the dequeued tuple.

N.B. If the queue is empty, this operation will block until`n`elements have been dequeued \(or 'timeout\_ms' elapses, if specified\).

Arguments:

* scope: A Scope object
* handle: The handle to a queue.
* n: The number of tuples to dequeue.
* component\_types: The type of each component in a tuple.

Optional attributes :

* timeout\_ms: If the queue is empty, this operation will block for up to timeout\_ms milliseconds. Note: This option is not supported yet.

Returns:

* OutputList : One or more tensors that were dequeued as a tuple.

Constructor

* QueueDequeueMany\(const ::tensorflow::Scope & scope, ::tensorflow::Input handle, ::tensorflow::Input n, const DataTypeSlice & component\_types\).

Public attributes

* tensorflow::OutputList components.

---

## QueueDequeueMany block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_data\_flow\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_data_flow_ops.cpp)

![](/assets/dataflow_QueueDequeueMany_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* handle : connect  Input node.
* n : connect  Input node or Input int32 number.
* DataTypeSlice  component\_types : Input DataType list accordance with each Queued data.
* QueueDequeueMany::Attrs attrs : input attrs data. ex\) timeout\_ms= -1;

Return:

* OutputList components: Output object of QueueDequeueMany class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/dataflow_QueueDequeueMany_Method.png)

