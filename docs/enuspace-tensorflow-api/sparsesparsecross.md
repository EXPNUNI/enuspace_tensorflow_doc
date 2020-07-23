--- 
layout: default 
title: SparseCross 
parent: sparse_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# SparseCross

---

## tensorflow C++ API

[tensorflow::ops::SparseCross](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sparse-cross)

Generates sparse cross from a list of sparse and dense tensors.

---

## Summary

The op takes two lists, one of 2D `SparseTensor` and one of 2D [`Tensor`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor), each representing features of one feature column. It outputs a 2D `SparseTensor` with the batchwise crosses of these features.

For example, if the inputs are

```
inputs[0]: SparseTensor with shape = [2, 2]
//[0, 0]: "a"
//[1, 0]: "b"
//[1, 1]: "c"

inputs[1]: SparseTensor with shape = [2, 1]
//[0, 0]: "d"
//[1, 0]: "e"

inputs[2]: Tensor [["f"], ["g"]]
```

then the output will be

```
shape = [2, 2]
//[0, 0]: "a_X_d_X_f"
//[1, 0]: "b_X_e_X_g"
//[1, 1]: "c_X_e_X_g"
```

if hashed\_output=true then the output will be

```
shape = [2, 2]
            Fingerprint64("f"), FingerprintCat64(
                Fingerprint64("d"), Fingerprint64("a")))
            Fingerprint64("g"), FingerprintCat64(
                Fingerprint64("e"), Fingerprint64("b")))
            Fingerprint64("g"), FingerprintCat64(
                Fingerprint64("e"), Fingerprint64("c")))
```

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* indices: 2-D. Indices of each input `SparseTensor`.
* values: 1-D. values of each `SparseTensor`.
* shapes: 1-D. Shapes of each `SparseTensor`.
* dense\_inputs: 2-D. Columns represented by dense [`Tensor`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor).
* hashed\_output: If true, returns the hash of the cross instead of the string. This will allow us avoiding string manipulations.
* num\_buckets: It is used if hashed\_output is true. output = hashed\_valuenum\_buckets if num\_buckets &gt; 0 else hashed\_value.
* hash\_key: Specify the hash\_key that will be used by the `FingerprintCat64` function to combine the crosses fingerprints.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) output\_indices: 2-D. Indices of the concatenated `SparseTensor`.
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) output\_values: 1-D. Non-empty values of the concatenated or hashed `SparseTensor`.
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) output\_shape: 1-D. [Shape](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/shape.html#classtensorflow_1_1ops_1_1_shape) of the concatenated `SparseTensor`.

---

## SparseCross block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_sparse.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_sparse.cpp)



---

## Using Method



