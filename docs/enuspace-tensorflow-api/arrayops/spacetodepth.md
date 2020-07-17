# SpaceToDepth

---

## tensorflow C++ API {#tensorflow-c-api}

[tensorflow::ops::SpaceToDepth](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/space-to-depth.html)

[SpaceToDepth](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/space-to-depth.html#classtensorflow_1_1ops_1_1_space_to_depth) for tensors of type T.

---

## Summary {#summary}

Rearranges blocks of spatial data, into depth. More specifically, this op outputs a copy of the input tensor where values from the`height`and`width`dimensions are moved to the`depth`dimension. The attr`block_size`indicates the input block size.

* Non-overlapping blocks of size `block_size x block size` are rearranged into depth at each location.
* The depth of the output tensor is `block_size * block_size * input_depth`.
* The Y, X coordinates within each block of the input become the high order component of the output channel index.
* The input tensor's height and width must be divisible by block\_size.

The`data_format`attr specifies the layout of the input and output tensors with the following options: "NHWC":`[ batch, height, width, channels ]`"NCHW":`[ batch, channels, height, width ]`"NCHW\_VECT\_C":`qint8 [ batch, channels / 4, height, width, channels % 4 ]`

It is useful to consider the operation as transforming a 6-D [Tensor](https://www.tensorflow.org/versions/r1.4/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor). e.g. for data\_format = NHWC, Each element in the input tensor can be specified via 6 coordinates, ordered by decreasing memory layout significance as: n,oY,bY,oX,bX,iC \(where n=batch index, oX, oY means X or Y coordinates within the output image, bX, bY means coordinates within the input block, iC means input channels\). The output would be a transpose to the following layout: n,oY,oX,bY,bX,iC

This operation is useful for resizing the activations between convolutions \(but keeping all data\), e.g. instead of pooling. It is also useful for training purely convolutional models.

For example, given an input of shape`[1, 2, 2, 1]`, data\_format = "NHWC" and block\_size = 2:

\`\`\` x = \[\[\[\[1\], \[2\]\], \[\[3\], \[4\]\]\]\] \`\`\`

This operation will output a tensor of shape`[1, 1, 1, 4]`:

\`\`\` \[\[\[\[1, 2, 3, 4\]\]\]\] \`\`\`

Here, the input has a batch of 1 and each batch element has shape`[2, 2, 1]`, the corresponding output will have a single element \(i.e. width and height are both 1\) and will have a depth of 4 channels \(1 \* block\_size \* block\_size\). The output element shape is`[1, 1, 4]`.

For an input tensor with larger depth, here of shape`[1, 2, 2, 3]`, e.g.

\`\`\` x = \[\[\[\[1, 2, 3\], \[4, 5, 6\]\], \[\[7, 8, 9\], \[10, 11, 12\]\]\]\] \`\`\`

This operation, for block\_size of 2, will return the following tensor of shape`[1, 1, 1, 12]`

\`\`\` \[\[\[\[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12\]\]\]\] \`\`\`

Similarly, for the following input of shape`[1 4 4 1]`, and a block size of 2:

\`\`\` x = \[\[\[\[1\], \[2\], \[5\], \[6\]\], \[\[3\], \[4\], \[7\], \[8\]\], \[\[9\], \[10\], \[13\], \[14\]\], \[\[11\], \[12\], \[15\], \[16\]\]\]\] \`\`\`

the operator will return the following tensor of shape`[1 2 2 4]`:

\`\`\` x = \[\[\[\[1, 2, 3, 4\], \[5, 6, 7, 8\]\], \[\[9, 10, 11, 12\], \[13, 14, 15, 16\]\]\]\] \`\`\`

Arguments:

* scope: A [Scope](https://www.tensorflow.org/versions/r1.4/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* block\_size: The size of the spatial block.

Returns:

* [`Output`](https://www.tensorflow.org/versions/r1.4/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The output tensor.

---

## SpaceToDepth block {#abs-block}

Source link :[https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_array\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/array_ops/spacetodepth1.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input `input`: connect Input or const shape node. \(Rank 4 tensor with shape\)
* Int64 `block_size`: 1-D with shape `[M]`, all values must be &gt;= 1.

Output:

* Output output: Output object of SpaceToDepth class object.

Result:

* std::vector\(Tensor\) `result_output`: The output tensor.

---

## Using Method

![](/assets/array_ops/spacetodepth2.png)  
※ [DepthToSpace](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/depth-to-space.html#classtensorflow_1_1ops_1_1_depth_to_space) 의 reverse 기능이며 위의 공식대로 동작한다.

