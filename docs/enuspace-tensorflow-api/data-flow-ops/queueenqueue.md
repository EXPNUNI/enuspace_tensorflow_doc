# QueueEnqueue

---

## tensorflow C++ API

[tensorflow::ops::QueueEnqueue](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/queue-enqueue)

Enqueues a tuple of one or more tensors in the given queue.

---

## Summary

The components input has k elements, which correspond to the components of tuples stored in the given queue.

N.B. If the queue is full, this operation will block until the given element has been enqueued \(or 'timeout\_ms' elapses, if specified\).

Arguments:

* scope: A Scope object
* handle: The handle to a queue.
* components: The type of each component in a tuple.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/queue-dequeue/attrs.html#structtensorflow_1_1ops_1_1_queue_dequeue_1_1_attrs)\):

* timeout\_ms: If the queue is full, this operation will block for up to timeout\_ms milliseconds. Note: This option is not supported yet.

Returns:

* The created Operation 

Constructor

* QueueEnqueue\(const ::tensorflow::Scope & scope, ::tensorflow::Input handle, ::tensorflow::InputList components, const QueueEnqueue::Attrs & attrs\) .

Public attributes

* tensorflow::Output Operation .

---

## QueueEnqueue block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_data\_flow\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_data_flow_ops.cpp)

![](/assets/dataflow_QueueEnque_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* handle : connect  Input node.
* components: connect  Input node.
* QueueEnqueue::Attrs attrs : input attrs data. ex\) timeout\_ms=-1;

Return:

* Output Operation : There is no output data.

Result:

* std::vector\(Tensor\) product\_result : There is no output data when calling session.

---

## Using Method

![](/assets/dataflow_DynamicPartition_Method.png)

