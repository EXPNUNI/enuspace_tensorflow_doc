# StopGradient

---

## tensorflow C++ API {#tensorflow-c-api}

[tensorflow::ops::StopGradient](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/stop-gradient.html)

Stops gradient computation.

---

## Summary {#summary}

When executed in a graph, this op outputs its input tensor as-is.

When building ops to compute gradients, this op prevents the contribution of its inputs to be taken into account. Normally, the gradient generator adds ops to a graph to compute the derivatives of a specified 'loss' by recursively finding out inputs that contributed to its computation. If you insert this op in the graph it inputs are masked from the gradient generator. They are not taken into account for computing gradients.

This is useful any time you want to compute a value with TensorFlow but need to pretend that the value was a constant. Some examples include:

* The EM algorithm where the M-step should not involve backpropagation through the output of the E-step.
* Contrastive divergence training of Boltzmann machines where, when differentiating the energy function, the training must not backpropagate through the graph that generated the samples from the model.
* Adversarial training, where no backprop should happen through the adversarial example generation process.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The output tensor.

---

## StopGradient block {#abs-block}

Source link :[https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_array\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/array_ops/stopgradient1.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* InputList input: A `Tensor`.

Output:

* Output output: Output object of StopGradient class object.

Result:

* std::vector\(Tensor\) `result_output`: A`Tensor`. Has the same type as`input`.

---

## Using Method

※ 

