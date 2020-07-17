# ShapeN {#abs}

---

## tensorflow C++ API {#tensorflow-c-api}

[tensorflow::ops::ShapeN](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/shape-n.html)

Returns shape of tensors.

---

## Summary {#summary}

This operation returns N 1-D integer tensors representing shape of`input[i]s`.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* `OutputList`: The output tensor.

---

## ShapeN block {#abs-block}

Source link :[https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_array\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)



Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input input: Any tensor.

Output:

* Output output: Output object of ShapeN class object.

Result:

* std::vector\(Tensor\) `result_output`: The output tensor.

---

## Using Method

※ input으로 들어온 tensor의 shape를 뽑아낸다.

