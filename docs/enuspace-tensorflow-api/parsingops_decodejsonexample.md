--- 
layout: default 
title: DecodeJSONExample 
parent: parsing_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# DecodeJSONExample

---

## tensorflow C++ API

[tensorflow::ops::DecodeJSONExample](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/decode-j-s-o-n-example)

Convert JSON-encoded Example records to binary protocol buffer strings.

---

## Summary

This op translates a tensor containing Example records, encoded using the[standard JSON mapping](https://developers.google.com/protocol-buffers/docs/proto3#json), into a tensor containing the same records encoded as binary protocol buffers. The resulting tensor can then be fed to any of the other Example-parsing ops.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* json\_examples: Each string is a JSON object serialized according to the JSON mapping of the Example proto.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) : Each string is a binary Example protocol buffer corresponding to the respective element of`json_examples`.

---

## DecodeJSONExample block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_parsing\_op.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input json\_examples: connect  Input node.

Return:

* Output binary\_examples : Output object of DecodeCSV class object.

Result:

* std::vector\(Tensor\) _result\_binary\_examples_ : Returned object of executed result by calling session.

---

## Using Method



