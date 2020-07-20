# OnesLike {#abs}

---

## tensorflow C++ API {#tensorflow-c-api}

[tensorflow::ops::OnesLike](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/ones-like.html)

Returns a tensor of ones with the same shape and type as x.

---

## Summary {#summary}

Creates a tensor with all elements set to 1.

Given a single tensor \(`tensor`\), this operation returns a tensor of the same type and shape as`tensor`with all elements set to 1. Optionally, you can specify a new type \(`dtype`\) for the returned tensor.

For example\(python\):

```
# 'tensor' is [[1, 2, 3], [4, 5, 6]]


tf.ones_like(tensor)==>[[1,1,1],[1,1,1]]
```

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* x: a tensor of type T.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) : a tensor of the same shape and type as x but filled with ones.

---

## OnesLike block {#abs-block}

Source link :[https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_array\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/array_ops/oneslike1.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input x: a tensor of type T.

Output:

* Output y: Output object of OnesLike class object.

Result:

* std::vector\(Tensor\) `result_y`: A `Tensor` . The same shape and type as x but filled with ones.

---

## Using Method

![](/assets/array_ops/oneslike2.png)

