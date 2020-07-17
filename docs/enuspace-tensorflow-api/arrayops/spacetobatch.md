# SpaceToBatch

---

## tensorflow C++ API {#tensorflow-c-api}

[tensorflow::ops::SpaceToBatch](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/space-to-batch.html)

[SpaceToBatch](https://www.tensorflow.org/versions/r1.4/api_docs/cc/class/tensorflow/ops/space-to-batch.html#classtensorflow_1_1ops_1_1_space_to_batch) for 4-D tensors of type T.

---

## Summary {#summary}

This is a legacy version of the more general[SpaceToBatchND](https://www.tensorflow.org/versions/r1.4/api_docs/cc/class/tensorflow/ops/space-to-batch-n-d.html#classtensorflow_1_1ops_1_1_space_to_batch_n_d).

Zero-pads and then rearranges \(permutes\) blocks of spatial data into batch. More specifically, this op outputs a copy of the input tensor where values from the`height`and`width`dimensions are moved to the`batch`dimension. After the zero-padding, both`height`and`width`of the input must be divisible by the block size.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/versions/r1.4/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object 
* input: 4-D with shape `[batch, height, width, depth]`.
* paddings: 2-D tensor of non-negative integers with shape `[2, 2]` . It specifies the padding of the input with zeros across the spatial dimensions as follows:

  ```
  paddings =[[pad_top, pad_bottom],[pad_left, pad_right]]
  ```

  The effective spatial dimensions of the zero-padded input tensor will be:

  ```
  height_pad = pad_top + height + pad_bottom
  width_pad = pad_left + width + pad_right
  ```

The attr`block_size`must be greater than one. It indicates the block size.

* Non-overlapping blocks of size `block_size x block size` in the height and width dimensions are rearranged into the batch dimension at each location.
* The batch of the output tensor is `batch * block_size * block_size`.
* Both height\_pad and width\_pad must be divisible by block\_size.

The shape of the output will be:

```
[batch*block_size*block_size, height_pad/block_size, width_pad/block_size, depth]
```

Some examples:

\(1\) For the following input of shape`[1, 2, 2, 1]`and block\_size of 2:

\`\`\` x = \[\[\[\[1\], \[2\]\], \[\[3\], \[4\]\]\]\] \`\`\`

The output tensor has shape`[4, 1, 1, 1]`and value:

\`\`\` \[\[\[\[1\]\]\], \[\[\[2\]\]\], \[\[\[3\]\]\], \[\[\[4\]\]\]\] \`\`\`

\(2\) For the following input of shape`[1, 2, 2, 3]`and block\_size of 2:

\`\`\` x = \[\[\[\[1, 2, 3\], \[4, 5, 6\]\], \[\[7, 8, 9\], \[10, 11, 12\]\]\]\] \`\`\`

The output tensor has shape`[4, 1, 1, 3]`and value:

\`\`\` \[\[\[1, 2, 3\]\], \[\[4, 5, 6\]\], \[\[7, 8, 9\]\], \[\[10, 11, 12\]\]\] \`\`\`

\(3\) For the following input of shape`[1, 4, 4, 1]`and block\_size of 2:

\`\`\` x = \[\[\[\[1\], \[2\], \[3\], \[4\]\], \[\[5\], \[6\], \[7\], \[8\]\], \[\[9\], \[10\], \[11\], \[12\]\], \[\[13\], \[14\], \[15\], \[16\]\]\]\] \`\`\`

The output tensor has shape`[4, 2, 2, 1]`and value:

\`\`\` x = \[\[\[\[1\], \[3\]\], \[\[9\], \[11\]\]\], \[\[\[2\], \[4\]\], \[\[10\], \[12\]\]\], \[\[\[5\], \[7\]\], \[\[13\], \[15\]\]\], \[\[\[6\], \[8\]\], \[\[14\], \[16\]\]\]\] \`\`\`

\(4\) For the following input of shape`[2, 2, 4, 1]`and block\_size of 2:

\`\`\` x = \[\[\[\[1\], \[2\], \[3\], \[4\]\], \[\[5\], \[6\], \[7\], \[8\]\]\], \[\[\[9\], \[10\], \[11\], \[12\]\], \[\[13\], \[14\], \[15\], \[16\]\]\]\] \`\`\`

The output tensor has shape`[8, 1, 2, 1]`and value:

\`\`\` x = \[\[\[\[1\], \[3\]\]\], \[\[\[9\], \[11\]\]\], \[\[\[2\], \[4\]\]\], \[\[\[10\], \[12\]\]\], \[\[\[5\], \[7\]\]\], \[\[\[13\], \[15\]\]\], \[\[\[6\], \[8\]\]\], \[\[\[14\], \[16\]\]\]\] \`\`\`

Among others, this operation is useful for reducing atrous convolution into regular convolution.

Returns:

* [`Output`](https://www.tensorflow.org/versions/r1.4/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The output tensor.

---

## SpaceToBatch block {#abs-block}

Source link :[https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_array\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/array_ops/spacetobatch1.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input `input`: 4-D with shape \[batch, height, width, depth\].
* Input `paddings`: 2-D tensor of non-negative integers with shape `[2, 2]` 
* Int64 `block_size`: must be greater than one. It indicates the block size.

Output:

* Output output: Output object of SpaceToBatch class object.

Result:

* std::vector\(Tensor\) `result_output`: The output tensor.

---

## Using Method

![](/assets/array_ops/spacetobatch2.png)  
※ [BatchToSpace](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/batch-to-space.html#classtensorflow_1_1ops_1_1_batch_to_space)와 반대되는 기능을 한다. input을 재정렬하며 input의 마지막 차원은 shape의 크기가 변하지 않는다.

