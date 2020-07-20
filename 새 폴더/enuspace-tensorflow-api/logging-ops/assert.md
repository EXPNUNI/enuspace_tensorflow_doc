# Assert

---

## tensorflow C++ API

[tensorflow::ops::Assert](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/assert)

Asserts that the given condition is true.

---

## Summary

If`condition`evaluates to false, print the list of tensors in`data`.`summarize`determines how many entries of the tensors to print.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* condition: The condition to evaluate.
* data: The tensors to print out when condition is false.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/assert/attrs.html#structtensorflow_1_1ops_1_1_assert_1_1_attrs)\):

* summarize: [Print](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/print.html#classtensorflow_1_1ops_1_1_print) this many entries of each tensor.

Returns:

* the created[`Operation`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/operation.html#classtensorflow_1_1_operation)

---

## Assert block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_logging\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_logging_ops.cpp)![](/assets/logging_ops/loggin_ops_assert_symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input condition : connect  condition node \(true or false\).
* InputList data : connect  data node \(InputList\).
* Assert::Attrs attrs : Set attribute property.

Return:

* Operation operation : Operation object of Assert class object.

Result:

* std::vector&lt;Tensor&gt; result\_operation : operation not update value.

---

## Using Method

Condition 의 값이 FALSE인경우, 입력된 데이터의 메세지의 값을 출력하며, TRUE의 값인 경우에는 메세지를 출력하지 않음. ![](/assets/loggping_ops/logging_ops_assert_method.png)

