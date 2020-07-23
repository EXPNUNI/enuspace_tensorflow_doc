--- 
layout: default 
title: Relu 
parent: nn_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# Relu

---

## tensorflow C++ API

[tensorflow::ops::Relu](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/relu)

Computes rectified linear:`max(features, 0)`.

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The activations tensor.

---

## Relu block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_nn.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_random.cpp)

![](../assets/nn-ops/Relu1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input features: connect  Input node.

Return:

* Output activations: Output object of Relu class object.

Result:

* std::vector\(Tensor\) result\_activations  : Returned object of executed result by calling session.

---

## Using Method

![](../assets/nn-ops/Relu2.jpg)

