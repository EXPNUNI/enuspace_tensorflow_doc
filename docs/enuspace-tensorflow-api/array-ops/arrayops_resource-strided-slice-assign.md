--- 
layout: default 
title: ResourceStridedSliceAssign 
parent: array_ops 
grand_parent: enuSpace-Tensorflow API 
last_modified_date: now 
--- 

# ResourceStridedSliceAssign {#abs}

---

## tensorflow C++ API {#tensorflow-c-api}

[tensorflow::ops::ResourceStridedSliceAssign](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/resource-strided-slice-assign.html)

[Assign](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/assign.html#classtensorflow_1_1ops_1_1_assign) `value` to the sliced l-value reference of `ref` .

---

## Summary {#summary}

The values of`value`are assigned to the positions in the variable`ref`that are selected by the slice parameters. The slice parameters`begin,`end`,`strides`, etc. work exactly as in`StridedSlice\`.

NOTE this op currently does not support broadcasting and so`value`'s shape must be exactly the shape produced by the slice of`ref`.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

Returns:

* the created [`Operation`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/operation.html#classtensorflow_1_1_operation)

---

## ResourceStridedSliceAssign block {#abs-block}

Source link :[https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_array\_ops.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)

Output:

* Output `output` : Output object of ResourceStridedSliceAssign class object.

Result:

* std::vector\(Tensor\) `result_output`: 

---

## Using Method



