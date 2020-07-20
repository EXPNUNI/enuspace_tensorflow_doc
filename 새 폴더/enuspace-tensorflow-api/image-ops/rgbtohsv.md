# RGBToHSV

---

## tensorflow C++ API

[tensorflow::ops::RGBToHSV](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/r-g-b-to-h-s-v)

Converts one or more images from RGB to HSV.

---

## Summary

Outputs a tensor of the same shape as the`images`tensor, containing the HSV value of the pixels. The output is only well defined if the value in`images`are in`[0,1]`.

`output[..., 0]`contains hue,`output[..., 1]`contains saturation, and`output[..., 2]`contains value. [All](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/all.html#classtensorflow_1_1ops_1_1_all) HSV values are in`[0,1]`. A hue of 0 corresponds to pure red, hue 1/3 is pure green, and 2/3 is pure blue.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* images: 1-D or higher rank. RGB data to convert. Last dimension must be size 3.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): `images`converted to HSV.

Constructor

* RGBToHSV\(const ::tensorflow::Scope & scope, ::tensorflow::Input images\).

Public attributes

* tensorflow::Output output.

---

## RGBToHSV block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_image\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_image_ops.cpp)

![](/assets/image_RGBToHSV_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* images : connect  Input node.

Return:

* Output output: Output object of RGBToHSV class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/image_RGBToHSV_Method.png)Input contents datatype of images  must be float.

