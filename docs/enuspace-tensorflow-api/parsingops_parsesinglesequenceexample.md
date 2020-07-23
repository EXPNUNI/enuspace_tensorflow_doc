--- 
layout: default 
title: ParseSingleSequenceExample 
parent: parsing_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# ParseSingleSequenceExample

---

## tensorflow C++ API

[tensorflow::ops::ParseSingleSequenceExample](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/parse-single-sequence-example)

Transforms a scalar brain.SequenceExample proto \(as strings\) into typed tensors.

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* serialized: A scalar containing a binary serialized SequenceExample proto.
* feature\_list\_dense\_missing\_assumed\_empty: A vector listing the FeatureList keys which may be missing from the SequenceExample. If the associated FeatureList is missing, it is treated as empty. By default, any FeatureList not listed in this vector must exist in the SequenceExample.
* context\_sparse\_keys: A list of Ncontext\_sparse string Tensors \(scalars\). The keys expected in the Examples' features associated with context\_sparse values.
* context\_dense\_keys: A list of Ncontext\_dense string Tensors \(scalars\). The keys expected in the SequenceExamples' context features associated with dense values.
* feature\_list\_sparse\_keys: A list of Nfeature\_list\_sparse string Tensors \(scalars\). The keys expected in the FeatureLists associated with sparse values.
* feature\_list\_dense\_keys: A list of Nfeature\_list\_dense string Tensors \(scalars\). The keys expected in the SequenceExamples' feature\_lists associated with lists of dense values.
* context\_dense\_defaults: A list of Ncontext\_dense Tensors \(some may be empty\). context\_dense\_defaults\[j\] provides default values when the SequenceExample's context map lacks context\_dense\_key\[j\]. If an empty [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) is provided for context\_dense\_defaults\[j\], then the Feature context\_dense\_keys\[j\] is required. The input type is inferred from context\_dense\_defaults\[j\], even when it's empty. If context\_dense\_defaults\[j\] is not empty, its shape must match context\_dense\_shapes\[j\].
* debug\_name: A scalar containing the name of the serialized proto. May contain, for example, table key \(descriptive\) name for the corresponding serialized proto. This is purely useful for debugging purposes, and the presence of values here has no effect on the output. May also be an empty scalar if no name is available.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/parse-single-sequence-example/attrs.html#structtensorflow_1_1ops_1_1_parse_single_sequence_example_1_1_attrs)\):

* context\_sparse\_types: A list of Ncontext\_sparse types; the data types of data in each context Feature given in context\_sparse\_keys. Currently the [ParseSingleSequenceExample](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/parse-single-sequence-example.html#classtensorflow_1_1ops_1_1_parse_single_sequence_example) supports DT\_FLOAT \(FloatList\), DT\_INT64 \(Int64List\), and DT\_STRING \(BytesList\).
* context\_dense\_shapes: A list of Ncontext\_dense shapes; the shapes of data in each context Feature given in context\_dense\_keys. The number of elements in the Feature corresponding to context\_dense\_key\[j\] must always equal context\_dense\_shapes\[j\].NumEntries\(\). The shape of context\_dense\_values\[j\] will match context\_dense\_shapes\[j\].
* feature\_list\_sparse\_types: A list of Nfeature\_list\_sparse types; the data types of data in each FeatureList given in feature\_list\_sparse\_keys. Currently the [ParseSingleSequenceExample](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/parse-single-sequence-example.html#classtensorflow_1_1ops_1_1_parse_single_sequence_example) supports DT\_FLOAT \(FloatList\), DT\_INT64 \(Int64List\), and DT\_STRING \(BytesList\).
* feature\_list\_dense\_shapes: A list of Nfeature\_list\_dense shapes; the shapes of data in each FeatureList given in feature\_list\_dense\_keys. The shape of each Feature in the FeatureList corresponding to feature\_list\_dense\_key\[j\] must always equal feature\_list\_dense\_shapes\[j\].NumEntries\(\).

Returns:

* `OutputList`context\_sparse\_indices
* `OutputList`context\_sparse\_values
* `OutputList`context\_sparse\_shapes
* `OutputList`context\_dense\_values
* `OutputList`feature\_list\_sparse\_indices
* `OutputList`feature\_list\_sparse\_values
* `OutputList`feature\_list\_sparse\_shapes
* `OutputList`feature\_list\_dense\_values

---

## ParseSingleSequenceExample block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_parsing\_op.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input serialized: connect  Input node.
* Input feature\_list\_dense\_missing\_assumed\_empty: connect  Input node.
* InputList context\_sparse\_keys: connect  Input node.
* InputList context\_dense\_keys: connect  Input node.
* InputList feature\_list\_sparse\_keys: connect  Input node.
* InputList feature\_list\_dense\_keys: connect  Input node.
* InputList context\_dense\_defaults: connect  Input node.
* Input debug\_name: connect  Input node.
* ParseSingleSequenceExample::Attrs attrs : input Attrs in  values ex\)context\_sparse\_types\_ = {};feature\_list\_dense\_types\_ = {};context\_dense\_shapes\_ = {};feature\_list\_sparse\_types\_ = {};feature\_list\_dense\_shapes\_ = {};

Return:

* OutputList context\_sparse\_indices : Output object of ParseSingleSequenceExample  class object.
* OutputList context\_sparse\_values : Output object of ParseSingleSequenceExample  class object.
* OutputList context\_sparse\_shapes : Output object of ParseSingleSequenceExample  class object.
* OutputList context\_dense\_values : Output object of ParseSingleSequenceExample  class object.
* OutputList feature\_list\_sparse\_indices : Output object of ParseSingleSequenceExample  class object.
* OutputList feature\_list\_sparse\_values : Output object of ParseSingleSequenceExample  class object.
* OutputList feature\_list\_sparse\_shapes : Output object of ParseSingleSequenceExample  class object.
* OutputList feature\_list\_dense\_values : Output object of ParseSingleSequenceExample  class object.

Result:

* std::vector\(Tensor\) result\_context\_sparse\_indices: Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_context\_sparse\_values: Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_context\_sparse\_shapes : Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_context\_dense\_values: Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_feature\_list\_sparse\_indices: Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_feature\_list\_sparse\_values: Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_feature\_list\_sparse\_shapes: Returned object of executed result by calling session.
* std::vector\(Tensor\) result\_feature\_list\_dense\_values: Returned object of executed result by calling session.

---

## Using Method



