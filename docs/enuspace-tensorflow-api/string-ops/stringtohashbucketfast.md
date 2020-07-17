# StringToHashBucketFast

---

## tensorflow C++ API

[tensorflow::ops::StringToHashBucketFast](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/string-to-hash-bucket-fast)

Converts each string in the input [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) to its hash mod by a number of buckets.

---

## Summary

The hash function is deterministic on the content of the string within the process and will never change. However, it is not suitable for cryptography. This function may be used when CPU time is scarce and inputs are trusted or unimportant. There is a risk of adversaries constructing inputs that all hash to the same bucket. To prevent this problem, use a strong hash function with `tf.string_to_hash_bucket_strong`.

Arguments:

* scope: A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object
* input: The strings to assign a hash bucket.
* num\_buckets: The number of buckets.

Returns:

* [`Output`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html#classtensorflow_1_1_output): A [Tensor](https://www.tensorflow.org/api_docs/cc/class/tensorflow/tensor.html#classtensorflow_1_1_tensor) of the same shape as the input `string_tensor`
  .

---

## StringToHashBucketFast block

Source link : [https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_string.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_string.cpp)

![](/assets/string_op/StringToHashBucketFast2.jpg)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input input: connect  Input node.
* num\_buckets : Input num\_buckets in value. 

Return:

* Output output : Output object of StringToHashBucketFast class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/string_op/StringToHashBucketFast1.jpg)

