# CropAndResize

---

## tensorflow C++ API

[tensorflow::ops::CropAndResize](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/crop-and-resize)

Extracts crops from the input image tensor and bilinearly resizes them \(possibly with aspect ratio change\) to a common output size specified by`crop_size`.

---

## Summary

This is more general than the`crop_to_bounding_box`op which extracts a fixed size slice from the input image and does not allow resizing or aspect ratio change.

Returns a tensor with`crops`from the input`image`at positions defined at the bounding box locations in`boxes`. The cropped boxes are all resized \(with bilinear interpolation\) to a fixed`size = [crop_height, crop_width]`. The result is a 4-D tensor`[num_boxes, crop_height, crop_width, depth]`.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* image: A 4-D tensor of shape`[batch, image_height, image_width, depth]`. Both`image_height`and`image_width`need to be positive.
* boxes: A 2-D tensor of shape`[num_boxes, 4]`. The`i`-th row of the tensor specifies the coordinates of a box in the
  `box_ind[i]`image and is specified in normalized coordinates`[y1, x1, y2, x2]`. A normalized coordinate value of
  `y`is mapped to the image coordinate at`y * (image_height - 1)`, so as the`[0, 1]`interval of normalized image height is mapped to`[0, image_height - 1]`in image height coordinates. We do allow`y1`&gt;`y2`, in which case the sampled crop is an up-down flipped version of the original image. The width dimension is treated similarly. Normalized coordinates outside the
  `[0, 1]`range are allowed, in which case we use`extrapolation_value`to extrapolate the input image values.
* box\_ind: A 1-D tensor of shap`[num_boxes]`with int32 values in`[0, batch)`. The value of`box_ind[i]`specifies the image that the`i`-th box refers to.crop\_size: A 1-D tensor of 2 elements,`size = [crop_height, crop_width]`.[All](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/all.html#classtensorflow_1_1ops_1_1_all) cropped image patches are resized to this size. The aspect ratio of the image content is not preserved. Both`crop_height`and`crop_width`need to be positive.
* crop\_size: A 1-D tensor of 2 elements, size = \[crop\_height, crop\_width\]. All cropped image patches are resized to this size. The aspect ratio of the image content is not preserved. Both crop\_height and crop\_width need to be positive.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/crop-and-resize/attrs.html#structtensorflow_1_1ops_1_1_crop_and_resize_1_1_attrs)\):

* method: A string specifying the interpolation method. Only 'bilinear' is supported for now.
* extrapolation\_value: Value used for extrapolation, when applicable.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): A 4-D tensor of shape`[num_boxes, crop_height, crop_width, depth]`.

Constructor

* CropAndResize\(const ::tensorflow::Scope & scope, ::tensorflow::Input image, ::tensorflow::Input boxes, ::tensorflow::Input box\_ind, ::tensorflow::Input crop\_size, const CropAndResize::Attrs & attrs\) .

Public attributes

* tensorflow::Output crops.

---

## CropAndResize block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_image\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_image_ops.cpp)

![](/assets/image_CropAndResize_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* image : connect  Input node.
* boxes : connect Input node or input float value.
* box\_ind : connect Input node or input int32 value. 
* crop\_size : connect Input node or input int32 value.
* CropAndResize::Attrs  attrs : input attrs. ex\) method\_ = "bilinear";extrapolation\_value\_ = 0.0f;

Return:

* Output crops: Output object of CropAndResize class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/image_CropAndResize_Method.png)

