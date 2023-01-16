![](https://github.com/adbr-dev/calculator/actions/workflows/dart.yml/badge.svg)


Only plus and minus one is provided. This package is a good example for beginners to add package dependencies to their project.


![](https://velog.velcdn.com/images/adbr/post/1958e383-bc8e-40b1-8f5d-61ec0c9915f7/image.gif)

</br>

# Usage
To use this plugin, add `calculator` as a dependency in your pubspec.yaml file.

```yaml
dependencies:
  flutter:
    sdk: flutter

  calculator: 0.0.1
```

### Example

```dart
import 'package:calculator/calculator.dart';

...

class _MyHomePageState extends State<MyHomePage> {
  int _counter = 0;

  void _incrementCounter() {
    _counter = Calculator.plusOne(_counter);
    setState(() {});
  }

  void _decrementCounter() {
    _counter = Calculator.minusOne(_counter);
    setState(() {});
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text(widget.title),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            const Text(
              'You have pushed the button this many times:',
            ),
            Text(
              '$_counter',
              style: Theme.of(context).textTheme.headline4,
            ),
          ],
        ),
      ),
      floatingActionButton: Column(
        mainAxisAlignment: MainAxisAlignment.end,
        children: [
          FloatingActionButton(
            onPressed: _decrementCounter,
            tooltip: 'Decrement',
            child: const Icon(Icons.remove),
          ),
          const SizedBox(height: 10),
          FloatingActionButton(
            onPressed: _incrementCounter,
            tooltip: 'Increment',
            child: const Icon(Icons.add),
          ),
        ],
      ),
    );
  }
}

```
