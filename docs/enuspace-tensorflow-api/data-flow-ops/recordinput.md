# RecordInput

---

## tensorflow C++ API

[tensorflow::ops::RecordInput](https://www.tensorflow.org/api_docs/cc/class/tensorflow/ops/record-input)

Emits randomized records.

---

## Summary

Arguments:

* scope: A Scope object
* file\_pattern: Glob pattern for the data files.

Optional attributes \(see`Attrs`\):

* file\_random\_seed: Random seeds used to produce randomized records.
* file\_shuffle\_shift\_ratio: Shifts the list of files after the list is randomly shuffled.
* file\_buffer\_size: The randomization shuffling buffer.
* file\_parallelism: How many sstables are opened and concurrently iterated over.
* batch\_size: The batch size.

Returns:

* Output : A tensor of shape \[batch\_size\].

Constructor

* RecordInput\(const ::tensorflow::Scope & scope, StringPiece file\_pattern, const RecordInput::Attrs & attrs\)\).

Public attributes

* tensorflow::Output records.

---

## RecordInput block

Source link : [https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf\_data\_flow\_ops.cpp](https://github.com/EXPNUNI/enuSpace-Tensorflow/blob/master/enuSpaceTensorflow/tf_data_flow_ops.cpp)

![](/assets/dataflow_RecordInput_Symbol.png)

Argument:

* Scope scope : A Scope object \(A scope is generated automatically each page. A scope is not connected.\)
* component\_types: Input DataType List in accordance with each input.

* RecordInput::Attrs attrs : input attrs data. ex\) file\_random\_seed\_ = 301; file\_shuffle\_shift\_ratio\_ = 0.0f;file\_buffer\_size\_ = 10000; file\_parallelism\_ = 16; batch\_size\_ = 32;

Return:

* Output records: Output object of RecordInput class object.

Result:

* std::vector\(Tensor\) product\_result : Returned object of executed result by calling session.

---

## Using Method

Need sample data file. 

