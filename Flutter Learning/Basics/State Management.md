> **State Management** refers to the management of the state of an application, which is a way to efficiently manage the state of various UI components and data within an application. Effective state management ensures that the UI reflects the current state of the app correctly and updates efficiently in response to changes.
---
# Common State Management Techniques
1. **setState**
	- The simplest form of state management.
	- Used within a stateful widget to rebuild the widget tree when the state changes.
	```dart
	void _incrementCounter() {
		setState(
			() {
				_counter++;
			}
		);
	}
	```
2.  **InheritedWidget**
	- Used to propagate state down the widget tree.
	- Useful for small to medium-sized applications.
	```dart
	class MyInheritedWidget extends InheritedWidget {
		final int counter;
		MyInheritedWidget({required Widget child, required this.counter}) : super(child: child);    
		static MyInheritedWidget? of(BuildContext context) {     
			return context.dependOnInheritedWidgetOfExactType<MyInheritedWidget>();   
		}    
		@override   
		bool updateShouldNotify(covariant MyInheritedWidget oldWidget) {     
		return oldWidget.counter != counter;   
		} 
	}
	```
3. **Provider**
	- A popular and flexible state management solution.
	- Uses the InheritedWidget internally but provides a more convenient API.
	```dart
	class Counter with ChangeNotifier {
		int _count = 0;    
		int get count => _count;    
		void increment() {     
			_count++;     
			notifyListeners();   
		} 
	}  
	void main() {
		runApp(  
			ChangeNotifierProvider(       
				create: (_) => 
					Counter(),       
					child: MyApp(),     
			),
		); 
	}
	class MyApp extends StatelessWidget {   
		@override   
		Widget build(BuildContext context) {     
			return MaterialApp(       
				home: Scaffold(         
					body: Center(           
						child: Column(             
							mainAxisAlignment: MainAxisAlignment.center,             
							children: [               
								Consumer<Counter>(                
									builder: (context, counter, child) => Text('Counter: ${counter.count}'),
								),   
								ElevatedButton(                 
									onPressed: () => Provider.of<Counter>(context, listen: false).increment(), 
									child: Text('Increment'), 
								),             
							],           
						),         
					),    
				),   
			);   
		} 
	}
	```
4. **Bloc (Business Logic Component)**
    - A more structured approach that separates business logic from UI.
    - Uses streams to manage state changes.
    ```dart
	class CounterBloc {   
		final _counterController = StreamController<int>();   
		int _counter = 0;    
		Stream<int> get counterStream => _counterController.stream;    
		void increment() {     
			_counter++;     
			_counterController.sink.add(_counter);   
		}    
		void dispose() {     
			_counterController.close();   
		} 
	}
	```
5. **Riverpod**
    - A robust and modern state management solution.
    - Provides a more flexible and safer approach than Provider.
	```dart
	final counterProvider = StateProvider<int>((ref) => 0);  
	class MyApp extends ConsumerWidget {   
		@override   
		Widget build(BuildContext context, ScopedReader watch) {     
			final counter = watch(counterProvider).state;      
			return MaterialApp(       
				home: Scaffold(         
					body: Center(           
						child: Column(             
							mainAxisAlignment: MainAxisAlignment.center,             
							children: [               
								Text('Counter: $counter'),               
								ElevatedButton(                 
									onPressed: () => context.read(counterProvider).state++,                 
									child: Text('Increment'),               
								),             
							],          
						),         
					),       
				),     
			);   
		} 
	}
	```