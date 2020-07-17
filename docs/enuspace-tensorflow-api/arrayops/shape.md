# Shape {#abs}

---

## tensorflow C++ API {#tensorflow-c-api}

[tensorflow::ops::Shape](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/shape.html)

Returns the shape of a tensor.

---

## Summary {#summary}

This operation returns a 1-D integer tensor representing the shape of`input`.

For example:

\`\`\` 't' is \[\[\[1, 1, 1\], \[2, 2, 2\]\], \[\[3, 3, 3\], \[4, 4, 4\]\]\]

shape\(t\) ==&gt; \[2, 2, 3\] \`\`\`

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The output tensor.

---

## Shape block {#abs-block}

Source link :[https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_array\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/array_ops/shape1.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input input: Any tensor.
* Shape::Attrs attrs
  * out\_type: The type of output tensor.

Output:

* Output output: Output object of Shape class object.

Result:

* std::vector\(Tensor\) `result_output`: The output tensor.

---

## Using Method

![](/assets/array_ops/shape2.png)※ input으로 들어온 tensor의 shape를 뽑아낸다.

