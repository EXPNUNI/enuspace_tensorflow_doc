## Output

---

## tensorflow C++ API

[tensorflow::Output](https://www.tensorflow.org/api_docs/cc/class/tensorflow/output.html)

Represents a tensor value produced by an [Operation](https://www.tensorflow.org/api_docs/cc/class/tensorflow/operation.html#classtensorflow_1_1_operation).

---

## Public functions

### Output {#output}

```
Output()=default
```

### Output {#output}

```
 Output(
  Node *n
)
```

### Output {#output}

```
 Output(
  Node *n,
  int32 index
)
```

### Output {#output}

```
 Output(
  const Operation & op,
  int32 index
)
```

### hash {#hash}

```
uint64 hash() const
```

### index {#index}

```
int32 index() const
```

### name {#name}

```
string name() const
```

### node {#node}

```
Node * node() const
```

### op {#op}

```
Operation op() const
```

### operator== {#operator}

```
bool operator==(
  const Output & other
) const
```

### type {#type}

```
DataType type() const
```

---

## Output block

Source link :[https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_core.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_core.cpp)

![](/assets/core/output_block.png)

Argument:

* Output `output`: concatenate the output or operation values.
* int32 `index`: default value is 0. When the operation value is connected to the `output` pin.

Output:

* Output `output`: return output type of tensor

---

## UsingMethod

![](/assets/core/output1.png)※ Add 블럭의 output을 Output블럭으로 받아서 clientsession에 넘겨주고, 결과값을 받은 화면

![](/assets/core/output2.png)※ Add블럭의 output을 operation에 연결한뒤 다시 output 블럭에 연결하여 ClientSession에 연결하여 실행한 화면

