# HSVToRGB

---

## tensorflow C++ API

[tensorflow::ops::HSVToRGB](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/h-s-v-to-r-g-b)

Convert one or more images from HSV to RGB.

---

## Summary

Outputs a tensor of the same shape as the`images`tensor, containing the RGB value of the pixels. The output is only well defined if the value in`images`are in`[0,1]`.

See`rgb_to_hsv`for a description of the HSV encoding.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* images: 1-D or higher rank. HSV data to convert. Last dimension must be size 3.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): `images`converted to RGB.

Constructor

* HSVToRGB\(const ::tensorflow::Scope & scope, ::tensorflow::Input images\).

Public attributes

* tensorflow::Output output.

---

## RGBToHSV block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_image\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_image_ops.cpp)

![](/assets/image_HSVToRGB_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* images : connect  Input node.

Return:

* Output output: Output object of HSVToRGB class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/image_HSVToRGB_Method.png)

Input contents datatype of images  must be float.

