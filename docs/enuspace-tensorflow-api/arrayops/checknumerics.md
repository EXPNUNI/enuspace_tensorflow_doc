# CheckNumerics

[tensorflow::ops::CheckNumerics](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/check-numerics.html)

Checks a tensor for NaN and Inf values.

---

## Summary {#summary}

When run, reports an `InvalidArgument` error if `tensor` has any values that are not a number \(NaN\) or infinity \(Inf\). Otherwise, passes`tensor`as-is.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object 
* message: Prefix of the error message.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) : The output tensor.

---

## CheckNumerics block {#abs-block}

Source link :[https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_array\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/array_ops/checknumerics1.png)

Argument:

* Scope `scope` : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input `tensor` : A tensor.
* StringPiece message: Prefix of the error message.

Return:

* Output output : Output object of CheckNumerics class object. 

Result:

* std::vector\(Tensor\) result\_output : The output tensor.

---

## Using Method {#using-method}

![](/assets/array_ops/checknumerics2.png)※ NaN과 Inf를 검출 하는데 쓰이는 기능이다.

