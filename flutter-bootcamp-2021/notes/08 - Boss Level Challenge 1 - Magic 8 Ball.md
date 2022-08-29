# 08 - Boss Level Challenge 1 - Magic 8 Ball

Project Link: https://github.com/MuaazShoaib/magic_8_ball

```
// In main.dart

// 08 - Boss Level Challenge 1 - Magic 8 Ball

import 'package:flutter/material.dart';
import 'dart:math';

void main() {
  runApp(
    MaterialApp(
      home: BallPage(),
    ),
  );
}

class BallPage extends StatelessWidget {
  const BallPage({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.blue,
      appBar: AppBar(
        title: Text('Ask Me Anything'),
        backgroundColor: Colors.blue.shade900,
      ),
      body: Ball(),
    );
  }
}

class Ball extends StatefulWidget {
  const Ball({Key? key}) : super(key: key);

  @override
  State<Ball> createState() => _BallState();
}

class _BallState extends State<Ball> {
  int ballNumber = 1;

  @override
  Widget build(BuildContext context) {
    return Container(
      child: Center(
        child: FlatButton(
            onPressed: () {
              setState(() {
                ballNumber = Random().nextInt(4) + 1;
              });
            },
            child: Image.asset('images/ball$ballNumber.png')),
      ),
    );
  }
}
```
