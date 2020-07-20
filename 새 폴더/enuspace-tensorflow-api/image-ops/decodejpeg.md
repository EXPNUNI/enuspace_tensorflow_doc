# DecodeJpeg

---

## tensorflow C++ API

[tensorflow::ops::DecodeJpeg](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/decode-jpeg)

Decode a JPEG-encoded image to a uint8 tensor.

---

## Summary

The attr`channels`indicates the desired number of color channels for the decoded image.

Accepted values are:

* 0: Use the number of channels in the JPEG-encoded image.
* 1: output a grayscale image.
* 3: output an RGB image.

If needed, the JPEG-encoded image is transformed to match the requested number of color channels.

The attr`ratio`allows downscaling the image by an integer factor during decoding. Allowed values are: 1, 2, 4, and 8. This is much faster than downscaling the image later.

This op also supports decoding PNGs and non-animated GIFs since the interface is the same, though it is cleaner to use`tf.image.decode_image`.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* contents: 0-D. The JPEG-encoded image.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): 3-D with shape`[height, width, channels]`.

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/decode-jpeg/attrs.html#structtensorflow_1_1ops_1_1_decode_jpeg_1_1_attrs)\):

* channels: Number of color channels for the decoded image.
* ratio: Downscaling ratio.
* fancy\_upscaling: If true use a slower but nicer upscaling of the chroma planes \(yuv420/422 only\).
* try\_recover\_truncated: If true try to recover an image from truncated input.
* acceptable\_fraction: The minimum required fraction of lines before a truncated input is accepted.
* dct\_method: string specifying a hint about the algorithm used for decompression. Defaults to "" which maps to a system-specific default. Currently valid values are \["INTEGER\_FAST", "INTEGER\_ACCURATE"\]. The hint may be ignored \(e.g., the internal jpeg library changes to a version that does not have that specific option.\)

Constructor

* DecodeJpeg\(const ::tensorflow::Scope & scope, ::tensorflow::Input contents, const DecodeJpeg::Attrs & attrs\) .

Public attributes

* tensorflow::Output image.

---

## DecodeJpeg block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_image\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_image_ops.cpp)

![](/assets/image_DecodeJpeg_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* contents : connect  Input node.
* DecodeJpeg::Attrs attrs : input attrs value. ex\) channels\_ = 3;ratio\_ = 1;fancy\_upscaling\_ = true;try\_recover\_truncated\_ = false;acceptable\_fraction\_ = 1.0f;dct\_method\_ = ;

Return:

* Output image : Output object of DecodeJpeg class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/image_DecodeJpeg_Method.png)

