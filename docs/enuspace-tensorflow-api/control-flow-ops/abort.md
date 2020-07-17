# Abort {#abs}

---

## tensorflow C++ API {#tensorflow-c-api}

[tensorflow::ops::Abort](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/abort.html)

Raise a exception to abort the process when called.

---

## Summary {#summary}

If exit\_without\_error is true, the process will exit normally, otherwise it will exit with a SIGABORT signal.

Returns nothing but an exception.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Optional attributes \(see [`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/abort/attrs.html#structtensorflow_1_1ops_1_1_abort_1_1_attrs)\):

* error\_msg: A string which is the message associated with the exception.

Returns:

* the created [`Operation`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/operation.html#classtensorflow_1_1_operation)

---

## Abort block {#abs-block}

Source link :[https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_control\_flow\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_control_flow_ops.cpp)

![](/assets/tf_control_flow_ops/abort1.png)![](/assets/control_flow_ops/abort1.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Abort::Attr `attrs`: 2 attr option, 
  * error\_msg\_: A string which is the message associated with the exception.
  * exit\_without\_error\_: A boolean value. If true  exit without error. false will exit with an error message.

Return:

* Operation operation : the created Operation

---

## Using Method {#using-method}

※ 이 함수를 사용하면 텐서플로우 dll만 종료되는 것이 아닌 텐서플로우 dll을 실행하고 있던 프로그램까지 종료 명령이 가게되므로 텐서플로우만 단독으로 사용할 때 쓰도록 해야한다.

