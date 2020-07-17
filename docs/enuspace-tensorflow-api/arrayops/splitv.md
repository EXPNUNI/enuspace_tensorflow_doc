# SplitV

---

## tensorflow C++ API {#tensorflow-c-api}

[tensorflow::ops::SplitV](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/split-v.html)

Splits a tensor into `num_split` tensors along one dimension.

---

## Summary {#summary}

Arguments:

* scope: A [Scope](https://www.tensorflow.org/versions/r1.4/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* value: The tensor to split.
* size\_splits: list containing the sizes of each output tensor along the split dimension. Must sum to the dimension of value along split\_dim. Can contain one -1 indicating that dimension is to be inferred.
* axis: 0-D. The dimension along which to split. Must be in the range `[-rank(value), rank(value))`.

Returns:

* `OutputList`: Tensors whose shape matches that of `value` except along `axis`, where their sizes are `size_splits[i]`.

---

## SplitV block {#abs-block}

Source link :[https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_array\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/array_ops/splitv1.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input axis: 0-D. The dimension along which to split. Must be in the range `[-rank(value), rank(value))`.
* Input value: The tensor to split.
* Int64 num\_split: The number of ways to split. Must evenly divide `value.shape[split_dim]`.

Output:

* OutputList output: Output object of SplitV class object.

Result:

* std::vector\(Tensor\) `result_output`: The output tensor.

---

## Using Method

※ 

