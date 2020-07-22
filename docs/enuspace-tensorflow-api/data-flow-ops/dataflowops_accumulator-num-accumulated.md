--- 
layout: default 
title: AccumulatorNumAccumulated 
parent: data_flow_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# AccumulatorNumAccumulated

---

## tensorflow C++ API

[tensorflow::ops::AccumulatorNumAccumulated](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/accumulator-num-accumulated)

Returns the number of gradients aggregated in the given accumulators.

---

## Summary

Arguments:

* scope: A Scope object
* handle: The handle to a accumulator.

Returns:

* Output : The number of gradients aggregated in the given accumulator.

Constructor

* AccumulatorNumAccumulated\(const ::tensorflow::Scope & scope, ::tensorflow::Input handle\).

Public attributes

* tensorflow::Output num\_accumulated.

---

## AccumulatorNumAccumulated block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_data\_flow\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_data_flow_ops.cpp)

![](../assets/dataflow_AccumulatorNumAccumulated_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input handle: connect Input node.

Return:

* Output num\_accumulated: Output object of AccumulatorNumAccumulated object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](../assets/dataflow_AccumulatorNumAccumulated_Method.png)![](/assets/dataflow_AccumulatorNumAccumulated_Method.png)

