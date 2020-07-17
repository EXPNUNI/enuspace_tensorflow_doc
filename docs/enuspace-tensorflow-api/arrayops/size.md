## Size

---

## tensorflow C++ API {#tensorflow-c-api}

[tensorflow::ops::Size](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/size.html)

Returns the size of a tensor.

---

## Summary {#summary}

This operation returns an integer representing the number of elements in`input`.

For example:

\`\`\` 't' is \[\[\[1, 1,, 1\], \[2, 2, 2\]\], \[\[3, 3, 3\], \[4, 4, 4\]\]\]\]

size\(t\) ==&gt; 12 \`\`\`

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The output tensor.

---

## Size block {#abs-block}

Source link :[https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_array\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/array_ops/size1.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input input: Any tensor.
* Size::Attrs attrs
  * out\_type: The type of output tensor.

Output:

* Output output: Output object of Size class object.

Result:

* std::vector\(Tensor\) `result_output`: The number of values in input.

---

## Using Method

![](/assets/array_ops/size2.png)※ input으로 들어온 tensor의 value의 갯수를 알려준다.

