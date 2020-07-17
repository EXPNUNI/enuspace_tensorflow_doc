# Scope {#abs}

---

## tensorflow C++ API {#tensorflow-c-api}

[tensorflow::Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html)

A [`Scope`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object represents a set of related TensorFlow ops that have the same properties such as a common name prefix.

---

## Summary {#summary}

A [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object is a container for TensorFlow Op properties. Op constructors get a [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object as a mandatory first argument and the constructed op acquires the properties in the object.

A simple example:

```
using namespace ops;

Scope root =Scope::NewRootScope();
auto c1 =Const(root,{{1,1}});
num = {{41},{1}}
auto m =MatMul(root, c1, num);
GraphDef gdef;
Status s = root.ToGraphDef(&gdef);
if(!s.ok()){...}
```

[Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) hierarchy:

The [Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) class provides various With&lt;&gt; functions that create a new scope. The new scope typically has one property changed while other properties are inherited from the parent scope. NewSubScope\(name\) method appends`name`to the prefix of names for ops created within the scope, and [WithOpName\(\)](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope_1a726021aa3104fec02353e8713f1e5b63) changes the suffix which otherwise defaults to the type of the op.

Name examples:

```
Scope root =Scope::NewRootScope();
Scope linear = root.NewSubScope("linear");
// W will be named "linear/W"
auto W =Variable(linear.WithOpName("W"),
                 {2,2}, DT_FLOAT);
// b will be named "linear/b"
auto b =Variable(linear.WithOpName("b"),{2}, DT_FLOAT);
auto x =Const(linear,{...}); // name: "linear/Const"
auto m =MatMul(linear, x, W); // name: "linear/MatMul"
auto r =BiasAdd(linear, m, b); // name: "linear/BiasAdd"
```

[Scope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) lifetime:

A new scope is created by calling [Scope::NewRootScope](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope_1a2bd1e548f919654da8f57402f844326c). This creates some resources that are shared by all the child scopes that inherit from this scope, directly or transitively. For instance, a new scope creates a new Graph object to which operations are added when the new scope or its children are used by an Op constructor. The new scope also has a [Status](https://www.tensorflow.org/api_docs/cc/class/tensorflow/status.html#classtensorflow_1_1_status) object which will be used to indicate errors by Op-constructor functions called on any child scope. The Op-constructor functions have to check the scope's status by calling the ok\(\) method before proceeding to construct the op.

Thread safety:

A [`Scope`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object is NOT thread-safe. Threads cannot concurrently call op-constructor functions on the same [`Scope`](https://www.tensorflow.org/api_docs/cc/class/tensorflow/scope.html#classtensorflow_1_1_scope) object.

---

## Scope block {#abs-block}

Source link :[https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf\_core.cpp](https://github.com/EXPNUNI/enuSpaceTensorflow/blob/master/enuSpaceTensorflow/tf_core.cpp)

Argument: There is no scope block. The picture file is a scope.

