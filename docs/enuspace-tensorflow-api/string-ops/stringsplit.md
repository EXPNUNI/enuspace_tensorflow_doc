# StringSplit

---

## tensorflow C++ API

[tensorflow::ops::StringSplit](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/string-split)

[Split](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/split.html#classtensorflow_1_1ops_1_1_split) elements of `input` based on `delimiter` into a `SparseTensor`.

---

## Summary

Let N be the size of source \(typically N will be the batch size\). [Split](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/split.html#classtensorflow_1_1ops_1_1_split) each element of `input` based on `delimiter` and return a `SparseTensor` containing the splitted tokens. Empty tokens are ignored.

`delimiter` can be empty, or a string of split characters. If `delimiter` is an empty string, each element of `input` is split into individual single-byte character strings, including splitting of UTF-8 multibyte sequences. Otherwise every character of `delimiter` is a potential split point.

For example: N = 2, input\[0\] is 'hello world' and input\[1\] is 'a b c', then the output will be

indices = \[0, 0; 0, 1; 1, 0; 1, 1; 1, 2\] shape = \[2, 3\] values = \['hello', 'world', 'a', 'b', 'c'\]

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* input: 1-D. Strings to split.
* delimiter: 0-D. Delimiter characters \(bytes\), or empty string.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) indices: A dense matrix of int64 representing the indices of the sparse tensor.
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) values: A vector of strings corresponding to the splited values.
* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output) shape: a length-2 vector of int64 representing the shape of the sparse tensor, where the first value is N and the second value is the maximum number of tokens in a single input entry.

---

## StringSplit block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_string.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_string.cpp)

![](/assets/string_op/StringSplit1.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input input: connect  Input node.
* Input delimiter: connect  Input node.

Return:

* Output output : Output object of StringSplit  class in indices  object.
* Output output : Output object of StringSplit  class in values object.
* Output output : Output object of StringSplit  class in shape object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/string_op/StringSplit2.jpg)

