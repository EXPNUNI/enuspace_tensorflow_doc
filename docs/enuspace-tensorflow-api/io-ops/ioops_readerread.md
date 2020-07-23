--- 
layout: default 
title: ReaderRead 
parent: io_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# ReaderRead

---

## tensorflow C++ API

[tensorflow::ops::ReaderRead](https://www.tensorflow.org/versions/r1.3/api_docs/cc/class/tensorflow/ops/reader-read)

Returns the next record \(key, value pair\) produced by a Reader.

---

## Summary

Will dequeue from the input queue if necessary \(e.g. when the Reader needs to start reading from a new file since it has finished with the previous file\).

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* reader\_handle: Handle to a Reader.
* queue\_handle: Handle to a Queue, with string work items.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): key: A scalar.
* [`Output`](https://www.gitbook.com/book/expnuni/enuspacetensorflow/edit#): value: A scalar.

Constructor

* ReaderRead\(const ::tensorflow::Scope & scope, ::tensorflow::Input reader\_handle, ::tensorflow::Input queue\_handle\) .

Public attributes

* tensorflow::Output key.
* tensorflow::Output value.

---

## ReaderRead block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_io\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_io_ops.cpp)

![](../assets/io_ReaderRead_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input reader\_handle : connect  Input node.
* Input queue\_handle : connect  Input node.

Return:

* Output reader\_handle : Output object of ReaderRead class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](../assets/io_FixedLengthRecordReader_Method.png)

