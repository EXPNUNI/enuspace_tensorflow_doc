# ReaderNumWorkUnitsCompleted

## tensorflow C++ API

[tensorflow::ops::ReaderNumRecordsProduced](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/reader-num-records-produced)

Returns the number of work units this Reader has finished processing.

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* reader\_handle: Handle to a Reader.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The units\_completed tensor.

Constructor

* ReaderNumWorkUnitsCompleted\(const ::tensorflow::Scope & scope, ::tensorflow::Input reader\_handle\).

Public attributes

* tensorflow::Output units\_completed.

---

## ReaderNumWorkUnitsCompleted block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_i\_o\_\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_io_ops.cpp)

![](/assets/io_ReaderNumWorkUnitsCompleted_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input reader\_handle: connect  Input node.

Return:

* Output units\_completed: Output object of ReaderNumWorkUnitsCompleted class object.  

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/io_ReaderNumWorkUnitsCompleted_Method.png)

