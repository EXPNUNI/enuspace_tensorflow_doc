# BarrierIncompleteSize

---

## tensorflow C++ API

[tensorflow::ops::BarrierIncompleteSize](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/barrier-incomplete-size)

Computes the number of incomplete elements in the given barrier.

---

## Summary

Arguments:

* scope: A Scope object
* handle: The handle to a barrier.

Returns:

* Output : The number of incomplete elements \(i.e. those with some of their value components not set\) in the barrier.

Constructor

* BarrierIncompleteSize\(const ::tensorflow::Scope & scope, ::tensorflow::Input handle\).

Public attributes

* tensorflow::Output size.

---

## BarrierIncompleteSize block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_data\_flow\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_data_flow_ops.cpp)

![](/assets/dataflow_BarrierIncompleteSize_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input handle : connect Input node.

Return:

* Output  size: Output object of BarrierIncompleteSize class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/dataflow_BarrierIncompleteSize_Method.png)

