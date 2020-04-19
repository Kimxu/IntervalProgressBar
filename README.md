# IntervalProgressBar

[![Package](https://img.shields.io/static/v1.svg?label=Pub&message=V1.0.1&color=green&style=for-the-badge)](https://pub.dartlang.org/packages/intervalprogressbar)

An interval progress widget for Flutter.

## Preview

<img src="https://raw.githubusercontent.com/stefanJi/IntervalProgressBar/master/doc/intervalprogressbar.png" width=400 alt="demo">

![demo2](./doc/demo2.png)

> v2.0.1 added

## Depend on it

https://pub.dev/packages/intervalprogressbar

Add this to your package's pubspec.yaml file:
```
dependencies:
  intervalprogressbar: ^{last_version}
```

## Features

- Horizontal
- Vertical
- Circle
- Interval Progress
- Colorful

## Getting Started

### Usage

```dart
Widget buildHorizontal() => IntervalProgressBar(
    direction: IntervalProgressDirection.horizontal,
    max: 30,
    progress: 10,
    intervalSize: 2,
    size: Size(400, 10),
    highlightColor: Colors.red,
    defaultColor: Colors.grey,
    intervalColor: Colors.transparent,
    intervalHighlightColor: Colors.transparent,
    reverse: true,
    radius: 0);
```

```dart
Widget buildVertical() => Row(
    mainAxisAlignment: MainAxisAlignment.center,
    children: [10, 29, 18, 27, 16, 15, 24, 3, 20, 10].map<Widget>((i) {
      return Padding(
          padding: EdgeInsets.only(right: 10),
          child: IntervalProgressBar(
              direction: IntervalProgressDirection.vertical,
              max: 30,
              progress: i,
              intervalSize: 2,
              size: Size(12, 200),
              highlightColor: Colors.red,
              defaultColor: Colors.grey,
              intervalColor: Colors.transparent,
              intervalHighlightColor: Colors.transparent,
              reverse: true,
              radius: 0));
    }).toList());
```

```dart
Widget buildCircle() => IntervalProgressBar(
      direction: IntervalProgressDirection.circle,
      max: 30,
      progress: 10,
      intervalSize: 2,
      size: Size(200, 200),
      highlightColor: Colors.red,
      defaultColor: Colors.grey,
      intervalColor: Colors.transparent,
      intervalHighlightColor: Colors.transparent,
      reverse: true,
      radius: 0,
      intervalDegrees: 5,
      strokeWith: 5,
    );
```

### Property

|Property|type|note|
|:---|:---|:---|
|direction|`enum`| ProgressBar's direction, support `vertical` and `horizontal` |
|max|`int`| count of default blocks |
|progress|`int`| count of highlight blocks |
|intervalSize|`int`| size of interval blocks. when `vertical` direction, means *height*, when `horizontal` direction, means *width* |
|size|`Size`| size of this widget |
|highlightColor|`Color`| color of highlight blocks |
|defaultColor|`Color`| color of default blocks |
|intervalColor|`Color`| color of default intervals |
|intervalHighlightColor| `Color`|color of intervals which between highlight blocks |
|reverse|`bool`||
|radius|`int`||
|intervalDegrees|`double`|support for circle progress|
|strokeWith|`int`|support for circle progress|