# GetSessionTensor

---

## tensorflow C++ API

[tensorflow::ops::GetSessionTensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/get-session-tensor)

Get the value of the tensor specified by its handle.

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* handle: The handle for a tensor stored in the session state.
* dtype: The type of the output value.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The tensor for the given handle.

---

## GetSessionTensor block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_data\_flow\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_data_flow_ops.cpp)

![](/assets/dataflow_getsessiontensor_symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* handle: The handle for a tensor stored in the session state.
* dtype: The type of the output value.

Return:

* Output handle: Output object of GetSessionTensor class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

Issue : [https://github.com/tensorflow/tensorflow/issues/12901](https://github.com/tensorflow/tensorflow/issues/12901)

