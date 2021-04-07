# How to customize the selected month cell in Flutter date range picker (SfDateRangePicker)?

In the Flutter date range picker, you can customize the selected cell using the `selectionTextStyle` property of `SfDateRangePicker` in the date picker.
## Step 1: 
Using the `selectionTextStyle` property, you can customize the selected cell. 

```xml
child: SfDateRangePicker(
  view: DateRangePickerView.month,
  selectionShape: DateRangePickerSelectionShape.rectangle,
  selectionTextStyle: TextStyle(
    color: Colors.red,
    decoration: TextDecoration.underline,
  ),
  selectionColor: Colors.amber,
  monthCellStyle: DateRangePickerMonthCellStyle(
    textStyle: TextStyle(fontSize: 15, color: Colors.black),
  ),
),
```

## Step 2:
Please find entire code snippet for the same.

```xml

import 'dart:ui';
import 'package:flutter/cupertino.dart';
import 'package:flutter/material.dart';
import 'package:syncfusion_flutter_datepicker/datepicker.dart';

void main() => runApp(SelectedCellCustomization());

class SelectedCellCustomization extends StatelessWidget {
  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: SelectedCell(),
    );
  }
}

class SelectedCell extends StatefulWidget {
  @override
  _SelectedCellState createState() => _SelectedCellState();
}

class _SelectedCellState extends State<SelectedCell> {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
        body: Card(
      margin: const EdgeInsets.fromLTRB(50, 150, 50, 150),
      child: SfDateRangePicker(
        view: DateRangePickerView.month,
        selectionShape: DateRangePickerSelectionShape.rectangle,
        selectionTextStyle: TextStyle(
            color: Colors.red,
            decoration: TextDecoration.underline,
        ),
        selectionColor: Colors.amber,
        monthCellStyle: DateRangePickerMonthCellStyle(
          textStyle: TextStyle(fontSize: 15, color: Colors.black),
        ),
      ),
    ));
  }
}
```

**[View document in Syncfusion Flutter Knowledge base](https://www.syncfusion.com/kb/11441/how-to-customize-the-selected-month-cell-in-the-flutter-date-range-picker-sfdaterangepicker)**

**Screenshot**

<img alt="seleced cell customization"  src="http://www.syncfusion.com/uploads/user/kb/flut/flut-863/flut-863_img1.png" width="230" height="250" />|
