--- 
layout: default 
title: ParseExample 
parent: parsing_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# ParseExample

---

## tensorflow C++ API

[tensorflow::ops::ParseExample](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/parse-example)

Transforms a vector of brain.Example protos \(as strings\) into typed tensors.

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object.
* serialized: A vector containing a batch of binary serialized Example protos.
* names: A vector containing the names of the serialized protos. May contain, for example, table key \(descriptive\) names for the corresponding serialized protos. These are purely useful for debugging purposes, and the presence of values here has no effect on the output. May also be an empty vector if no names are available. If non-empty, this vector must be the same length as "serialized".

* sparse\_keys: A list of Nsparse string Tensors \(scalars\). The keys expected in the Examples' features associated with sparse values.

* dense\_keys: A list of Ndense string Tensors \(scalars\). The keys expected in the Examples' features associated with dense values.

* dense\_defaults: A list of Ndense Tensors \(some may be empty\). dense\_defaults\[j\] provides default values when the example's feature\_map lacks dense\_key\[j\]. If an empty [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) is provided for dense\_defaults\[j\], then the Feature dense\_keys\[j\] is required. The input type is inferred from dense\_defaults\[j\], even when it's empty. If dense\_defaults\[j\] is not empty, and dense\_shapes\[j\] is fully defined, then the shape of dense\_defaults\[j\] must match that of dense\_shapes\[j\]. If dense\_shapes\[j\] has an undefined major dimension \(variable strides dense feature\), dense\_defaults\[j\] must contain a single element: the padding element.

* sparse\_types: A list of Nsparse types; the data types of data in each Feature given in sparse\_keys. Currently the [arseExample](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/parse-example.html#classtensorflow_1_1ops_1_1_parse_example) supports DT\_FLOAT \(FloatList\), DT\_INT64 \(Int64List\), and DT\_STRING \(BytesList\).
* dense\_shapes: A list of Ndense shapes; the shapes of data in each Feature given in dense\_keys. The number of elements in the Feature corresponding to dense\_key\[j\] must always equal dense\_shapes\[j\].NumEntries\(\). If dense\_shapes\[j\] == \(D0, D1, ..., DN\) then the shape of output [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) dense\_values\[j\] will be \(\|serialized\|, D0, D1, ..., DN\): The dense outputs are just the inputs row-stacked by batch. This works for dense\_shapes\[j\] = \(-1, D1, ..., DN\). In this case the shape of the output
  [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) dense\_values\[j\] will be \(\|serialized\|, M, D1, .., DN\), where M is the maximum number of blocks of elements of length D1 \* .... \* DN, across all minibatch entries in the input.
  [Any](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/any.html#classtensorflow_1_1ops_1_1_any) minibatch entry with less than M blocks of elements of length D1 \* ... \* DN will be padded with the corresponding default\_value scalar element along the second dimension.

Returns:

* `OutputList`sparse\_indices
* `OutputList`sparse\_values
* `OutputList`sparse\_shapes
* `OutputList`dense\_values

---

## ParseExample block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_parsing\_op.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input serialized: connect  Input node.
* Input names: connect  Input node.
* InputList sparse\_keys: connect  Input node.
* InputList dense\_keys: connect  Input node.
* InputList dense\_defaults: connect  Input node.
* DataTypeSlice sparse\_types: input DataTypeSlice in values.
* ArraySlice&lt; PartialTensorShape &gt; dense\_shapes: input ArraySlice&lt; PartialTensorShape &gt; in values.

Return:

* Output sparse\_indices : Output object of ParseExample  class object.
* Output sparse\_values : Output object of ParseExample  class object.
* Output sparse\_shapes : Output object of ParseExample  class object.
* Output dense\_values : Output object of ParseExample  class object.

Result:

* std::vector\(Tensor\) result\_sparse\_indices: Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_sparse\_values: Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_sparse\_shapes : Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_dense\_values: Returned object of executed result by calling session.

---

## Using Method



