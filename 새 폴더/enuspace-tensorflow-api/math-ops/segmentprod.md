# SegmentProd

---

## tensorflow C++ API

[tensorflow::ops::SegmentProd](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/segment-prod)

Computes the product along segments of a tensor.

---

## Summary

Read the section on segmentation for an explanation of segments.

Computes a tensor such that output\_i = data\_j where the product is over`j`such that`segment_ids[j] == i`.

If the product is empty for a given segment ID`i`,`output[i] = 1`.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* segment\_ids: A 1-D tensor whose rank is equal to the rank of data's first dimension. Values should be sorted and can be repeated.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): Has same shape as data, except for dimension 0 which has size`k`, the number of segments.

Constructor

* SegmentProd\(const ::tensorflow::Scope & scope, ::tensorflow::Input data, ::tensorflow::Input segment\_ids\) 

Public attributes

* tensorflow::Output output.

---

## SegmentProd block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/math_SegmentProd_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input data:connect  Input node.
* Input segment\_ids:connect  Input node.

Return:

* Output output: Output object of SegmentProd class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/math_SegmentProd_Method.png)

