# Dart Reduce Method Error with Empty List

This repository demonstrates a common error encountered when using the `reduce` method in Dart with an empty list. The `reduce` method requires at least one element in the list to perform its operation; otherwise, it throws a `StateError`. This example shows how to handle this scenario gracefully.

## Problem

The `reduce` method in Dart is used to combine elements of a list using a given function. However, if the list is empty, it throws a `StateError`. This can lead to unexpected crashes in your application.

## Solution

To avoid this error, always check if the list is empty before calling `reduce`. You can use a conditional statement or the `isNotEmpty` property to handle empty lists:

```dart
List<int> numbers = [];
int sum;

if (numbers.isNotEmpty) {
  sum = numbers.reduce((a, b) => a + b);
} else {
  sum = 0; // Or any other default value
}
print(sum);
```

This approach allows you to handle the case of an empty list without causing an error.
