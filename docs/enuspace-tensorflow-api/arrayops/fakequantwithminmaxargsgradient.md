# FakeQuantWithMinMaxArgsGradient {#abs}

---

## tensorflow C++ API {#tensorflow-c-api}

[tensorflow::ops::FakeQuantWithMinMaxArgsGradient](https://www.tensorflow.org/versions/r1.2/api_docs/cc/class/tensorflow/ops/fake-quant-with-min-max-args-gradient.html)

Compute gradients for a [FakeQuantWithMinMaxArgs](https://www.tensorflow.org/versions/r1.2/api_docs/cc/class/tensorflow/ops/fake-quant-with-min-max-args.html#classtensorflow_1_1ops_1_1_fake_quant_with_min_max_args) operation.

---

## Summary {#summary}

Arguments:

* scope: A [Scope](https://www.tensorflow.org/versions/r1.2/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* gradients: Backpropagated gradients above the [FakeQuantWithMinMaxArgs](https://www.tensorflow.org/versions/r1.2/api_docs/cc/class/tensorflow/ops/fake-quant-with-min-max-args.html#classtensorflow_1_1ops_1_1_fake_quant_with_min_max_args) operation.
* inputs: Values passed as inputs to the [FakeQuantWithMinMaxArgs](https://www.tensorflow.org/versions/r1.2/api_docs/cc/class/tensorflow/ops/fake-quant-with-min-max-args.html#classtensorflow_1_1ops_1_1_fake_quant_with_min_max_args) operation.

Returns:

* [`Output`](https://www.tensorflow.org/versions/r1.2/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) : Backpropagated gradients below the [FakeQuantWithMinMaxArgs](https://www.tensorflow.org/versions/r1.2/api_docs/cc/class/tensorflow/ops/fake-quant-with-min-max-args.html#classtensorflow_1_1ops_1_1_fake_quant_with_min_max_args) operation: `gradients * (inputs >= min && inputs <= max)`.

---

## FakeQuantWithMinMaxArgsGradient block {#abs-block}

Source link :[https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_array\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/array_ops/fackquantwithminmaxargsgradients1.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input `inputs`: A Tensor of type `float`.
* Attr `attrs` : An optional attribute value
  * min : An optional float. Defaults to -6.
  * max : An optional float. Defaults to 6.
  * num\_bits : An optional int. Defaults to 8.

Attrs use ex\)

Output:

* output : Output object of FakeQuantWithMinMaxArgsGradient  class object.

Result:

* std::vector\(Tensor\) result\_output : A `Tensor` of type `float`  operation: `gradients * (inputs >= min && inputs <= max)`.
  .

---

## Using Method {#using-method}

![](/assets/array_ops/fackquantwithminmaxargsgradients2.png)※

