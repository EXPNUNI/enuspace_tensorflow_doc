# SparseMatMul

---

## tensorflow C++ API

[tensorflow::ops::SparseMatMul](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/sparse-mat-mul)

[Multiply](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/multiply.html#classtensorflow_1_1ops_1_1_multiply) matrix "a" by matrix "b".

---

## Summary

The inputs must be two-dimensional matrices and the inner dimension of "a" must match the outer dimension of "b". This op is optimized for the case where at least one of "a" or "b" is sparse. The breakeven for using this versus a dense matrix multiply on one platform was 30% zero values in the sparse matrix.

The gradient computation of this operation will only take advantage of sparsity in the input gradient when that gradient comes from a [Relu](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/relu.html#classtensorflow_1_1ops_1_1_relu).

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* a : float or bfloat16
* b : float or bfloat16

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): The product tensor.

Constructor

* SparseMatMul\(const ::tensorflow::Scope & scope, ::tensorflow::Input a, ::tensorflow::Input b, const MatMul::Attrs & attrs\) 

Public attributes

* tensorflow::Output product

---

## SparseMatMul block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_math.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_math.cpp)

![](/assets/math_SparseMatMul_Symbol.png)

Argument:

* Scope scope : A Scope object\(A scope is generated automatically each page. A scope is not connected.\).
* Input a : connect  Input node.
* Input b : connect  Input node.
* SparseMatMul::Attrs attrs : Input attrs in value. ex\) transpose\_a\_ = false;transpose\_b\_ = false;a\_is\_sparse\_ = false;b\_is\_sparse\_ = false;

Return:

* Output product : Output object of SparseMatMul class object. 

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/math_SparseMatMul_Method.png)

