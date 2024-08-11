# Stateful and Stateless Widgets
> Understand the difference between StatefulWidget and StatelessWidget
---
## Stateless Widget
- A **Stateless Widget** is a widget that does not require any mutable state. 
- Once created, it cannot change its appearance or behavior over time. It is essentially static and remains the same throughout its lifetime. 
- Stateless widgets are ideal for displaying static content.
- **Example**:
```dart
import 'package:flutter/material.dart';

class MyStatelessWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Center(
      child: Text('I am a Stateless Widget'),
    );
  }
}
```
## Stateful Widget
- A **Stateful Widget** is a widget that can change its appearance or behavior dynamically based on changes in state. 
- It consists of two classes: the `StatefulWidget` class itself and the `State` class. 
- The `StatefulWidget` class is immutable and can be recreated, while the `State` class holds the mutable state and contains the logic to update the UI.
- **Example**:
```dart
import 'package:flutter/material.dart';

// StatefulWidget class
class MyStatefulWidget extends StatefulWidget {
  @override
  _MyStatefulWidgetState createState() => _MyStatefulWidgetState();
}

// State class
class _MyStatefulWidgetState extends State<MyStatefulWidget> {
  int _counter = 0;

  void _incrementCounter() {
    setState(() {
      _counter++;
    });
  }

  @override
  Widget build(BuildContext context) {
    return Center(
      child: Column(
        mainAxisAlignment: MainAxisAlignment.center,
        children: <Widget>[
          Text('Counter: $_counter'),
          ElevatedButton(
            onPressed: _incrementCounter,
            child: Text('Increment'),
          ),
        ],
      ),
    );
  }
}
```