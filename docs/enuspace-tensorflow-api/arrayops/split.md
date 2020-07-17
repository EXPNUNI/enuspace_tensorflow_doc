# Split

---

## tensorflow C++ API {#tensorflow-c-api}

[tensorflow::ops::Split](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/split.html)

Splits a tensor into `num_split` tensors along one dimension.

---

## Summary {#summary}

Arguments:

* scope: A [Scope](https://www.tensorflow.org/versions/r1.4/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* axis: 0-D. The dimension along which to split. Must be in the range `[-rank(value), rank(value))`.
* value: The tensor to split.
* num\_split: The number of ways to split. Must evenly divide `value.shape[split_dim]`.

Returns:

* `OutputList`: They are identically shaped tensors, whose shape matches that of `value` except along `axis`, where their sizes are `values.shape[split_dim] / num_split`.

---

## Split block {#abs-block}

Source link :[https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_array\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/array_ops/split1.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input axis: 0-D. The dimension along which to split. Must be in the range `[-rank(value), rank(value))`.
* Input value: The tensor to split.
* Int64 num\_split: The number of ways to split. Must evenly divide `value.shape[split_dim]`.

Output:

* OutputList output: Output object of Split class object.

Result:

* std::vector\(Tensor\) `result_output`: The output tensor.

---

## Using Method

![](/assets/array_ops/split2.png)※ axis의 값에 해당하는 차원을 num\_split의 값만큼 나눈다. 즉 num\_split은 해당하는 차원의 값의 갯수를 나눠서 0으로 떨어지는 값만 넣을 수 있다. \(ex: 해당하는 차원의 값의 갯수가 6개 일 때 num\_split에 올수 있는 수는 1, 2, 3, 6 이다.\)

