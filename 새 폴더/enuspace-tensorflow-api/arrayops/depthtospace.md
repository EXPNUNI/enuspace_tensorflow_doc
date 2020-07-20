# DepthToSpace {#abs}

---

## tensorflow C++ API {#tensorflow-c-api}

[tensorflow::ops::DepthToSpace](https://www.tensorflow.org/versions/r1.2/api_docs/cc/class/tensorflow/ops/depth-to-space)

[DepthToSpace](https://www.tensorflow.org/versions/r1.2/api_docs/cc/class/tensorflow/ops/depth-to-space.html#classtensorflow_1_1ops_1_1_depth_to_space) for tensors of type T.

---

## Summary {#summary}

Rearranges data from depth into blocks of spatial data. This is the reverse transformation of[SpaceToDepth](https://www.tensorflow.org/versions/r1.2/api_docs/cc/class/tensorflow/ops/space-to-depth.html#classtensorflow_1_1ops_1_1_space_to_depth). More specifically, this op outputs a copy of the input tensor where values from the`depth`dimension are moved in spatial blocks to the`height`and`width`dimensions. The attr`block_size`indicates the input block size and how the data is moved.

* Chunks of data of size `block_size * block_size` from depth are rearranged into non-overlapping blocks of size `block_size x block_size`
* The width the output tensor is `input_depth * block_size` , whereas the height is `input_height * block_size` .
* The depth of the input tensor must be divisible by `block_size * block_size` .

That is, assuming the input is in the shape:`[batch, height, width, depth]`, the shape of the output will be: `[batch,height*block_size, width*block_size, depth/(block_size*block_size)]`

This operation requires that the input tensor be of rank 4, and that`block_size`be &gt;=1 and that`block_size * block_size`be a divisor of the input depth.

This operation is useful for resizing the activations between convolutions \(but keeping all data\), e.g. instead of pooling. It is also useful for training purely convolutional models.

For example, given this input of shape`[1, 1, 1, 4]`, and a block size of 2:

\`\`\` x = \[\[\[\[1, 2, 3, 4\]\]\]\]\`\`\`

This operation will output a tensor of shape`[1, 2, 2, 1]`:

\`\`\` \[\[\[\[1\], \[2\]\], \[\[3\], \[4\]\]\]\] \`\`\`

Here, the input has a batch of 1 and each batch element has shape`[1, 1, 4]`, the corresponding output will have 2x2 elements and will have a depth of 1 channel \(1 =`4 / (block_size * block_size)`\). The output element shape is`[2, 2, 1]`.

For an input tensor with larger depth, here of shape`[1, 1, 1, 12]`, e.g.

\`\`\` x = \[\[\[\[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12\]\]\]\] \`\`\`

This operation, for block size of 2, will return the following tensor of shape`[1, 2, 2, 3]`

\`\`\` \[\[\[\[1, 2, 3\], \[4, 5, 6\]\], \[\[7, 8, 9\], \[10, 11, 12\]\]\]\]\`\`\`

Similarly, for the following input of shape`[1 2 2 4]`, and a block size of 2:

\`\`\` x = \[\[\[\[1, 2, 3, 4\], \[5, 6, 7, 8\]\], \[\[9, 10, 11, 12\], \[13, 14, 15, 16\]\]\]\] \`\`\`

the operator will return the following tensor of shape`[1 4 4 1]`:

\`\`\` x = \[\[ \[1\], \[2\], \[5\], \[6\]\], \[ \[3\], \[4\], \[7\], \[8\]\], \[ \[9\], \[10\], \[13\], \[14\]\], \[ \[11\], \[12\], \[15\], \[16\]\]\]\`\`\`

Arguments:

* scope: A [Scope](https://www.tensorflow.org/versions/r1.2/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* block\_size: The size of the spatial block, same as in Space2Depth.

Returns:

* [`Output`](https://www.tensorflow.org/versions/r1.2/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) : The output tensor.

---

## DepthToSpace block {#abs-block}

Source link :[https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_array\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/array_ops/depthtospace1.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input input : connect Input or const shape node. \(Rank 4 tensor with shape\)
* Int64 block\_size : The size of the spatial block, same as in Space2Depth

Return:

* Output output : Output object of Dequantize class object. 

Result:

* std::vector\(Tensor\) result\_output : Returned object of executed result by calling session. \(Rank 4 tensor with shape\)

---

## Using Method {#using-method}

##### ![](/assets/array_ops/depthtospace2.png)

※ input의 shape에서 batch가 아닌 depth를 조절하는 기능을 한다. BatchToSpace와 비슷하게 동작하지만 역할은 다르다.

