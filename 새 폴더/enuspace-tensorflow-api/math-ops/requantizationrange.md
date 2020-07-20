# RequantizationRange

---

## tensorflow C++ API

[tensorflow::ops::RequantizationRange](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/requantization-range)

Given a quantized tensor described by \(input, input\_min, input\_max\), outputs a.

---

## Summary

range that covers the actual values present in that tensor. This op is typically used to produce the requested\_output\_min and requested\_output\_max for [Requantize](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/requantize.html#classtensorflow_1_1ops_1_1_requantize).

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* input\_min: The float value that the minimum quantized input value represents.
* input\_max: The float value that the maximum quantized input value represents.
* out\_type: The type of the output. Should be a lower bit depth than Tinput.

Output

* Output  output\_min: The computed min output.
* Output  output\_max: The computed max output.

Constructor

* QuantizeDownAndShrinkRange\(const ::tensorflow::Scope & scope, ::tensorflow::Input input, ::tensorflow::Input input\_min, ::tensorflow::Input input\_max, DataType out\_type\) 

Public attributes

* tensorflow::Output output\_min.
* tensorflow::Output output\_max.

---

## RequantizationRange block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/math_RequantizationRange_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\).
* Input input:connect  Input node.
* Input input\_min:connect  Input node.
* Input input\_max:connect  Input node.

Return:

* Output output: Output object of RequantizationRange class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

tensorflow -&gt; error: No OpKernel was registered to support Op 'RequantizationRange' with these attrs.  

 Registered devices: \[CPU,GPU\], Registered kernels:

  &lt;no registered kernels&gt;

 \[\[Node: RequantizationRange = RequantizationRange\[Tinput=DT\_QINT16\]\(Cast, Const\_2, Const\_4\)\]\].

	 



