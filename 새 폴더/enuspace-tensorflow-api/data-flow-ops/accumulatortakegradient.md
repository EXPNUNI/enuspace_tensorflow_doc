# AccumulatorTakeGradient

---

## tensorflow C++ API

[tensorflow::ops::AccumulatorTakeGradient](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/accumulator-take-gradient)

Extracts the average gradient in the given ConditionalAccumulator.

---

## Summary

The op blocks until sufficient \(i.e., more than num\_required\) gradients have been accumulated. If the accumulator has already aggregated more than num\_required gradients, it returns the average of the accumulated gradients. Also automatically increments the recorded global\_step in the accumulator by 1, and resets the aggregate to 0.

Arguments:

* scope: A Scope object
* handle: The handle to an accumulator.
* num\_required: Number of gradients required before we return an aggregate.
* dtype: The data type of accumulated gradients. Needs to correspond to the type of the accumulator.

Returns:

* Output : The average of the accumulated gradients.

Constructor

* AccumulatorTakeGradient\(const ::tensorflow::Scope & scope, ::tensorflow::Input handle, ::tensorflow::Input num\_required, DataType dtype\).

Public attributes

* tensorflow::Output average.

---

## AccumulatorTakeGradient block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_data\_flow\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_data_flow_ops.cpp)

![](/assets/dataflow_AccumulatorTakeGradient_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* Input handle: connect Input node.
* Input num\_required: connect Input node.
* DataType dtype : connect Input node.

Return:

* Output average.: Output operation of AccumulatorTakeGradient object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

![](/assets/dataflow_AccumulatorTakeGradient_Method.png)

