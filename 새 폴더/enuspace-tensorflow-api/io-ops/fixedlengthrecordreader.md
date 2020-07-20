# FixedLengthRecordReader

---

## tensorflow C++ API

[tensorflow::ops::FixedLengthRecordReader](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/fixed-length-record-reader)

A Reader that outputs fixed-length records from a file.

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* record\_bytes: Number of bytes in the record.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/fixed-length-record-reader/attrs.html#structtensorflow_1_1ops_1_1_fixed_length_record_reader_1_1_attrs)\):

* header\_bytes: Number of bytes in the header, defaults to 0.
* footer\_bytes: Number of bytes in the footer, defaults to 0.
* hop\_bytes: Number of bytes to hop before each read. Default of 0 means using record\_bytes.
* container: If non-empty, this reader is placed in the given container. Otherwise, a default container is used.
* shared\_name: If non-empty, this reader is named in the given bucket with this shared\_name. Otherwise, the node name is used instead.
* encoding: The type of encoding for the file. Currently ZLIB and GZIP are supported. Defaults to none.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The handle to reference the Reader.

Constructor

* FixedLengthRecordReader\(const ::tensorflow::Scope & scope, int64 record\_bytes, const FixedLengthRecordReader::Attrs & attrs\) .

Public attributes

* tensorflow::Output reader\_handle.

---

## FixedLengthRecordReader block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_io\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_io_ops.cpp)

![](/assets/io_FixedLengthRecordReader_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input record\_bytes : connect  Input node or input record bytes in int.
* FixedLengthRecordReader::Attrs attrs : input option value. ex\) header\_bytes\_ = 0;footer\_bytes\_ = 0;hop\_bytes\_ = 0;container\_ = "";shared\_name\_ = "";encoding\_ = "";

Return:

* Output reader\_handle : Output object of FixedLengthRecordReader class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/io_FixedLengthRecordReader_Method.png)

