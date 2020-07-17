# QuantizedMatMul

---

## tensorflow C++ API

[tensorflow::ops::QuantizedMatMul](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/quantized-mat-mul/attrs)

Returns x \* y element-wise, working on quantized buffers.

---

## Summary

\[input\_min, input\_max\] are scalar floats that specify the range for the float interpretation of the 'input' data. For example, if input\_min is -1.0f and input\_max is 1.0f, and we are dealing with quint16 quantized data, then a 0 value in the 16-bit data should be interpreted as -1.0f, and a 65535 means 1.0f.

This operator tries to squeeze as much precision as possible into an output with a lower bit depth by calculating the actual min and max values found in the data. For example, maybe that quint16 input has no values lower than 16,384 and none higher than 49,152. That means only half the range is actually needed, all the float interpretations are between -0.5f and 0.5f, so if we want to compress the data into a quint8 output, we can use that range rather than the theoretical -1.0f to 1.0f that is suggested by the input min and max.

In practice, this is most useful for taking output from operations like [QuantizedMatMul](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/quantized-mat-mul.html#classtensorflow_1_1ops_1_1_quantized_mat_mul) that can produce higher bit-depth outputs than their inputs and may have large potential output ranges, but in practice have a distribution of input values that only uses a small fraction of the possible range. By feeding that output into this operator, we can reduce it from 32 bits down to 8 with minimal loss of accuracy.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* min\_x: The float value that the lowest quantized`x`value represents.
* max\_x: The float value that the highest quantized`x`value represents.
* min\_y: The float value that the lowest quantized`y`value represents.
* max\_y: The float value that the highest quantized`y`value represents.

Output

* output  z
* output  min\_z: The float value that the lowest quantized output value represents.
* output : max\_z: The float value that the highest quantized output value represents.

Constructor

* QuantizedMul\(const ::tensorflow::Scope & scope, ::tensorflow::Input x, ::tensorflow::Input y, ::tensorflow::Input min\_x, ::tensorflow::Input max\_x, ::tensorflow::Input min\_y, ::tensorflow::Input max\_y, const QuantizedMul::Attrs & attrs\)

Public attributes

* tensorflow::Output z.
* tensorflow::Output min\_z.
* tensorflow::Output max\_z.

---

## QuantizedMatMul block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/math_QuantizedMatMul_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input x : connect  Input node.
* Input y : connect  Input node.
* Input min\_x : connect  Input node.
* Input max\_x : connect  Input node.
* Input min\_y : connect  Input node.
* Input max\_y : connect  Input node.
* DataType out\_type:Input DataType. ex\)DT\_QINT8

Return:

* Output output: Output object of QuantizedMatMul class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

tensorflow -&gt; error: No OpKernel was registered to support Op 'QuantizedMatMul' with these attrs.

Registered devices: \[CPU,GPU\], Registered kernels:

&lt;no registered kernels&gt;



