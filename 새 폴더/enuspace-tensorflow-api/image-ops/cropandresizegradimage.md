# CropAndResizeGradImage

---

## tensorflow C++ API

[tensorflow::ops::CropAndResizeGradImage](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/crop-and-resize-grad-image)

Computes the gradient of the crop\_and\_resize op wrt the input image tensor.

---

## Summary

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* grads: A 4-D tensor of shape \[num\_boxes, crop\_height, crop\_width, depth\].
* boxes: A 2-D tensor of shape`[num_boxes, 4]`. The`i`-th row of the tensor specifies the coordinates of a box in the
  `box_ind[i]`image and is specified in normalized coordinates`[y1, x1, y2, x2]`. A normalized coordinate value of
  `y`is mapped to the image coordinate at`y * (image_height - 1)`, so as the`[0, 1]`interval of normalized image height is mapped to`[0, image_height - 1]`in image height coordinates. We do allow`y1`&gt;`y2`, in which case the sampled crop is an up-down flipped version of the original image. The width dimension is treated similarly. Normalized coordinates outside the
  `[0, 1]`range are allowed.
* box\_ind: A 1-D tensor of shap`[num_boxes]`with int32 values in`[0, batch)`. The value of`box_ind[i]`specifies the image that the`i`-th box refers to.crop\_size: A 1-D tensor of 2 elements,`size = [crop_height, crop_width]`.[All](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/all.html#classtensorflow_1_1ops_1_1_all) cropped image patches are resized to this size. The aspect ratio of the image content is not preserved. Both`crop_height`and`crop_width`need to be positive.
* image\_size: A 1-D tensor with value \[batch, image\_height, image\_width, depth\] containing the original image size. Both image\_height and image\_width need to be positive.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/crop-and-resize/attrs.html#structtensorflow_1_1ops_1_1_crop_and_resize_1_1_attrs)\):

* method: A string specifying the interpolation method. Only 'bilinear' is supported for now.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): A 4-D tensor of shape \[batch, image\_height, image\_width, depth\].

Constructor

* CropAndResizeGradImage\(const ::tensorflow::Scope & scope, ::tensorflow::Input grads, ::tensorflow::Input boxes, ::tensorflow::Input box\_ind, ::tensorflow::Input image\_size, DataType T, const CropAndResizeGradImage::Attrs & attrs\) 
  .

Public attributes

* tensorflow::Output output.

---

## CropAndResizeGradImage block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_image\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_image_ops.cpp)

![](/assets/image_CropAndResizeGradImage_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* grads : connect  Input node.
* boxes : connect Input node or input float value.
* box\_ind : connect Input node or input int32 value. 
* image\_size : connect  Input node or input int32 value. 
* CropAndResizeGradImage::Attrs  attrs : input attrs. ex\) method\_ = "bilinear";

Return:

* Output output: Output object of CropAndResizeGradImage object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/image_CropAndResizeGradImage_Method.png)

