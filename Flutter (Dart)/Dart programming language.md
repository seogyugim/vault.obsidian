# Hello World

```dart
void main() {
	print('hello world');
}

dart run main.dart
```

# The Var keyword

```dart
void main() {
	// Compiler automatically infers type of value
	var name = 'seogyugim';

	// Declare obviously type of value 
	String strname = 'seogyugim';
}
```

# Dynamic Type

```dart
void main() {
	dynamic name;
	if (name is String) {
		// Compiler already knows type of name
		name.isEmpty;
	}

	// And dart support optional chaining
	name?.isEmpty;
}
```

# Null Safety

```dart
bool isEmpty(String s) => s.length == 0;

void main() {
	// It'll throw NoSuchMethodError
	isEmpty(null);

	// It's not okay
	String name1 = 'seogyugim';
	// Because name2 must be not null
	if (name1 != null) {
		nico.isNotEmpty;
	}

	// It's not okay
	String? name2 = 'seogyugim';
	name = null;
	// Because name could be a null
	name.isNotEmpty
	if (name2 != null) {
		nico.isNotEmpty;
	}

	// It's okay
	String? name = 'seogyugim';
	name = null;
	name?.isNotEmpty;
}
```

# Final

```dart
void main() {
	// As same as val of kotlin, const of javascript
	final name = 'seogyugim';
}
```

# Late Variables

```dart
void main() {
	// We can create variable without data with late keyword
	late final String name;
	late var name2;

	// It will throw Error because it is not definitely assigned
	print(name);
}
```

# Constant Variables

```dart
void main() {
	// compile-time constant
	const name = 'seogyugim';
	// Error
	name = ''

	// OK
	const API_KEY = '123123';
	// Error, because compiler don't know when compile-time.
	const apiRes = fetchApi();
	// OK
	final apiRes = fetchApi();
}
```