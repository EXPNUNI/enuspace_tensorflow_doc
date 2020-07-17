# CountUpTo

---

## tensorflow C++ API

[tensorflow::ops::CountUpTo](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/count-up-to)

Increments 'ref' until it reaches 'limit'.

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* ref: Should be from a scalar [`Variable`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/variable.html#classtensorflow_1_1ops_1_1_variable) node.
* limit: If incrementing ref would bring it above limit, instead generates an 'OutOfRange' error.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): A copy of the input before increment. If nothing else modifies the input, the values produced will all be distinct.

---

## CountUpTo block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_state.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_state.cpp)

![](/assets/state_op/CountUpTo1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input ref: connect  Input node.
* int64 limit: connect Input lmit in value ex\)10 =&gt;int64

Return:

* Output output : Output object of CountUpTo class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

## ![](/assets/state_op/CountUpTo2.jpg)



