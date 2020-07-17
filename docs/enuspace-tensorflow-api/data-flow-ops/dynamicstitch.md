# DynamicStitch

---

## tensorflow C++ API

[tensorflow::ops::DynamicStitch](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/dynamic-stitch)

Interleave the values from the`data`tensors into a single tensor.

---

## Summary

Builds a merged tensor such that

\`\`\`python merged\[indices\[m\]\[i, ..., j\], ...\] = data\[m\]\[i, ..., j, ...\] \`\`\`

For example, if each`indices[m]`is scalar or vector, we have

\`\`\`python Scalar indices:

merged\[indices\[m\], ...\] = data\[m\]\[...\]

Vector indices:

merged\[indices\[m\]\[i\], ...\] = data\[m\]\[i, ...\] \`\`\`

Each`data[i].shape`must start with the corresponding`indices[i].shape`, and the rest of`data[i].shape`must be constant w.r.t.`i`. That is, we must have`data[i].shape = indices[i].shape + constant`. In terms of this`constant`, the output shape is

```
merged.shape =[max(indices)]+ constant
```

Values are merged in order, so if an index appears in both`indices[m][i]`and`indices[n][j]`for`(m,i) < (n,j)`the slice`data[n][j]`will appear in the merged result.

For example:

\`\`\`python indices\[0\] = 6 indices\[1\] = \[4, 1\] indices\[2\] = \[\[5, 2\], \[0, 3\]\] data\[0\] = \[61, 62\] data\[1\] = \[\[41, 42\], \[11, 12\]\] data\[2\] = \[\[\[51, 52\], \[21, 22\]\], \[\[1, 2\], \[31, 32\]\]\] merged = \[\[1, 2\], \[11, 12\], \[21, 22\], \[31, 32\], \[41, 42\], \[51, 52\], \[61, 62\]\] \`\`\`

This method can be used to merge partitions created by`dynamic_partition`as illustrated on the following example:

\`\`\`python Apply function \(increments x\_i\) on elements for which a certain condition

apply \(x\_i != -1 in this example\).

x=tf.constant\(\[0.1, -1., 5.2, 4.3, -1., 7.4\]\) condition\_mask=tf.not\_equal\(x,tf.constant\(-1.\)\) partitioned\_data = tf.dynamic\_partition\( x, tf.cast\(condition\_mask, tf.int32\) , 2\) partitioned\_data\[1\] = partitioned\_data\[1\] + 1.0 condition\_indices = tf.dynamic\_partition\( tf.range\(tf.shape\(x\)\[0\]\), tf.cast\(condition\_mask, tf.int32\) , 2\) x = tf.dynamic\_stitch\(condition\_indices, partitioned\_data\) Here x=\[1.1, -1., 6.2, 5.3, -1, 8.4\], the -1. values remain

unchanged.

\`\`\`

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* Output : The merged tensor.

Constructor

* DynamicStitch\(const ::tensorflow::Scope & scope, ::tensorflow::InputList indices, ::tensorflow::InputList data\).

Public attributes

* tensorflow::Output merged

---

## DynamicStitch block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_data\_flow\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_data_flow_ops.cpp)

![](/assets/dataflow_DynamicStitch_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* indices : connect  Input node or input data.
* data: connect  Input node.

Return:

* Output merged: Output object of DynamicStitch class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/dataflow_DynamicStitch_Method.png)

