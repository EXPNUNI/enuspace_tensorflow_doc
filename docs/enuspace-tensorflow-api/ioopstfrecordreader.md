--- 
layout: default 
title: TFRecordReader 
parent: io_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# TFRecordReader

---

## tensorflow C++ API

[tensorflow::ops::TFRecordReader](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/t-f-record-reader)

A Reader that outputs the records from a TensorFlow Records file.

---

## Summary

Arguments:

* scope: A Scope object

Optional attributes \(see`Attrs`\):

* container: If non-empty, this reader is placed in the given container. Otherwise, a default container is used.
* shared\_name: If non-empty, this reader is named in the given bucket with this shared\_name. Otherwise, the node name is used instead.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The handle to reference the Reader.

Constructor

* TFRecordReader\(const ::tensorflow::Scope & scope, const TFRecordReader::Attrs & attrs\) .

Public attributes

* tensorflow::Output reader\_handle.

---

## TFRecordReader block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_io\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_io_ops.cpp)

![](./assets/io_TFRecordReader_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)

* TFRecordReader::Attrs attrs : input option value. ex\)     container\_ = ;  shared\_name\_ = ;  compression\_type\_ = ;

Return:

* Output reader\_handle : Output object of TFRecordReader class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

Read Tensorflow Record File Format.

![](./assets/io_TFRecordReader_Method.png)

