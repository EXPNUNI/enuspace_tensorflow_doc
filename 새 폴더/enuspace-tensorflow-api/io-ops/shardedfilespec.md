# ShardedFilespec

---

## tensorflow C++ API

[tensorflow::ops::ShardedFilespec](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sharded-filespec)

Generate a glob pattern matching all sharded file names.

---

## Summary

Arguments:

* scope: A Scope object

Returns:

* Output : The filename tensor.

Constructor

* ShardedFilespec\(const ::tensorflow::Scope & scope, ::tensorflow::Input basename, :tensorflow::Input num\_shards\).

Public attributes

* tensorflow::Output  filename.

---

## ShardedFilespec block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_i\_o\_\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_io_ops.cpp)

![](/assets/io_ShardedFilespec_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input basename : input prefix with path.
* Input num\_shards: connect input node or input total shard number.

Return:

* Output  filename: Output  filename of ShardedFilespec class object.  

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/io_ShardedFilespec_Method.png)

