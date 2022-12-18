# PageView-Widget


import 'package:flutter/material.dart';

void main() {
  runApp(MaterialApp(
    home: MyApp(),
  ));
}

class MyApp extends StatefulWidget {
  @override
  State<MyApp> createState() => _MyAppState();
}

class _MyAppState extends State<MyApp> {
  var currentPage = 0;

  @override
  Widget build(BuildContext context) {
    return Scaffold(
        appBar: AppBar(
          title: Text('PageView widget'),
        ),
        body: PageView(
          pageSnapping: false,
          scrollDirection: Axis.vertical,
          onPageChanged: (index) {
            setState(() {
              currentPage = index;
            });
          },
          //reverse: true,
          physics: BouncingScrollPhysics(),
          children: [
            Column(
              mainAxisAlignment: MainAxisAlignment.center,
              children: [
                Image.asset(
                  'lib/asset/a1.jpg',
                  height: 500,
                  width: 300,
                ),
                Text(
                    'My name is suraj \n  I am study in a Geentanjali Group of college in\n rojkot Gujarat'),
              ],
            ),
            Column(
              mainAxisAlignment: MainAxisAlignment.center,
              children: [
                Image.asset(
                  'lib/asset/a4.jpg',
                  height: 500,
                  width: 300,
                ),
                Text(
                    'My name is suraj \n  I am study in a Geentanjali Group of college in\n rojkot Gujarat'),
              ],
            ),
            Column(
              mainAxisAlignment: MainAxisAlignment.center,
              children: [
                Image.asset(
                  'lib/asset/a6.jpg',
                  height: 500,
                  width: 300,
                ),
                Text(
                    'My name is suraj \n  I am study in a Geentanjali Group of college in\n rojkot Gujarat'),
              ],
            )
          ],
        ));
  }
}
