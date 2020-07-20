# BatchMatMul

---

## tensorflow C++ API

[tensorflow::ops::BatchMatMul](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/batch-mat-mul)

Multiplies slices of two tensors in batches.

---

## Summary

Multiplies all slices of[`Tensor`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor)`x`and`y`\(each slice can be viewed as an element of a batch\), and arranges the individual results in a single output tensor of the same batch size. Each of the individual slices can optionally be adjointed \(to adjoint a matrix means to transpose and conjugate it\) before multiplication by setting the`adj_x`or`adj_y`flag to`True`, which are by default`False`.

The input tensors`x`and`y`are 2-D or higher with shape`[..., r_x, c_x]`and`[..., r_y, c_y]`.

The output tensor is 2-D or higher with shape`[..., r_o, c_o]`, where:

```
r_o = c_x if adj_x else r_x
c_o = r_y if adj_y else c_y
```

It is computed as:

```
output
[...,:,:]= matrix(x[...,:,:])* matrix(y[...,:,:])
```

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object

* x: 2-D or higher with shape`[..., r_x, c_x]`.

* y: 2-D or higher with shape`[..., r_y, c_y]`

Optional attributes \(see[`Attrs`](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/batch-mat-mul/attrs.html#structtensorflow_1_1ops_1_1_batch_mat_mul_1_1_attrs)\):

* adj\_x: If`True`, adjoint the slices of`x`. Defaults to`False`.
* adj\_y: If`True`, adjoint the slices of`y`. Defaults to`False`.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): 3-D or higher with shape`[..., r_o, c_o]`

Constructor

* BatchMatMul\(const ::tensorflow::Scope & scope, ::tensorflow::Input y, ::tensorflow::Input x,const [BatchMatMul::Attrs](https://www.tensorflow.org/api_docs/cc/struct/tensorflow/ops/batch-mat-mul/attrs.html#structtensorflow_1_1ops_1_1_batch_mat_mul_1_1_attrs) &
   attrs\).

Public attributes

* tensorflow::Output z.

---

## BatchMatMul block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/math_BatchMatMul_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input y :connect  Input node.
* Input x :connect  Input node.
* BatchMatMul::Attrs attrs : Input  attrs value. ex\) adj\_x\_=false;adj\_y\_=false;

Return:

* Output z : Output object of BatchMatMul class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

adj\_x\_ = false;adj\_y\_ = false;

![](/assets/math_BatchMatMul_Method.png)

