# DecodeGif

---

## tensorflow C++ API

[tensorflow::ops::DecodeGif](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/decode-gif)

Decode the first frame of a GIF-encoded image to a uint8 tensor.

---

## Summary

GIF with frame or transparency compression are not supported convert animated GIF from compressed to uncompressed by:

```
convert $src.gif -coalesce $dst.gif
```

This op also supports decoding JPEGs and PNGs, though it is cleaner to use`tf.image.decode_image`.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* contents: 0-D. The GIF-encoded image.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): 4-D with shape`[num_frames, height, width, 3]`. RGB order

Constructor

* DecodeGif\(const ::tensorflow::Scope & scope, ::tensorflow::Input contents\) .

Public attributes

* tensorflow::Output image.

---

## DecodeGif block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_image\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_image_ops.cpp)

![](/assets/image_DecodeGif_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* contents : connect  Input node.

Return:

* Output image: Output object of DecodeGif class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/image_DecodeGif_Method.png)

