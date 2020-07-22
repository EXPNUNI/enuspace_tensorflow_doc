--- 
layout: default 
title: RefNextIteration 
parent: control_flow_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

## RefNextIteration

---

## tensorflow C++ API {#tensorflow-c-api}

[tensorflow::ops::RefNextIteration](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/ref-next-iteration.html)

Makes its input available to the next iteration.

---

## Summary {#summary}

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* data: The tensor to be made available to the next iteration.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The same tensor as `data`.

---

## RefNextIteration block {#abs-block}

Source link :[https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_control\_flow\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_control_flow_ops.cpp)

![](./assets/tf_control_flow_ops/refnextiteration1.png)![](/assets/control_flow_ops/refnextiteration1.png)

Argument:

* Scope scope: A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input data: The tensor to be made available to the next iteration.

Returns:

* [`Output`](#): The same tensor as `data`.

---

## Using Method {#using-method}



