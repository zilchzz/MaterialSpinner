#MaterialSpinner

[![License](http://img.shields.io/:license-apache-blue.svg?style=flat)]()
[![API](https://img.shields.io/badge/API-14%2B-blue.svg?style=flat)](https://android-arsenal.com/api?level=11)
[![](https://jitpack.io/v/zilchzz/MaterialSpinner.svg)](https://jitpack.io/#zilchzz/MaterialSpinner)

___

<img src="demo.gif" width = "40%" />

Usage
-----

Add it in your root build.gradle at the end of repositories

```groovy
allprojects {
    repositories {
        maven { url 'https://jitpack.io' }
    }
}
```

Add the dependency

```groovy
dependencies {
    implementation 'com.github.zilchzz:MaterialSpinner:1.3.2'
}
```

Add the spinner to your layout XML:

```xml
<com.jaredrummler.materialspinner.MaterialSpinner
    android:id="@+id/spinner"
    app:ms_dropdown_max_height="350dp"
    app:ms_dropdown_text_color="#7c7d7f"
    app:ms_divider_color="#000000"
    app:ms_text_color="#dadadd"
    app:ms_divider_height="0.5dp"
    app:ms_dropdown_height="wrap_content"
    app:ms_background_selector="@drawable/bg_trade_spinner"
    app:ms_background_color="#191b20"
    app:ms_arrow_tint="#696A6D"
    android:layout_width="match_parent"
    android:layout_height="wrap_content" />
```

Add items to the spinner and listen for clicks:

```java
MaterialSpinner spinner = (MaterialSpinner) findViewById(R.id.spinner);
spinner.setItems("Ice Cream Sandwich", "Jelly Bean", "KitKat", "Lollipop", "Marshmallow");
spinner.setOnItemSelectedListener(new MaterialSpinner.OnItemSelectedListener<String>() {

  @Override public void onItemSelected(MaterialSpinner view, int position, long id, String item) {
    Snackbar.make(view, "Clicked " + item, Snackbar.LENGTH_LONG).show();
  }
});
```

You can add attributes to customize the view. Available attributes:

| name                    | type      | info                                                   |
|-------------------------|-----------|--------------------------------------------------------|
| ms_arrow_tint           | color     | sets the color on the drop-down arrow                  |
| ms_hide_arrow           | boolean   | set to true to hide the arrow drawable                 |
| ms_background_color     | color     | set the background color for the spinner and drop-down |
| ms_background_selector  | integer   | set the background resource for the dropdown items     |
| ms_text_color           | color     | set the text color                                     |
| ms_dropdown_max_height  | dimension | set the max height of the drop-down                    |
| ms_dropdown_height      | dimension | set the height of the drop-down                        |
| ms_padding_top          | dimension | set the top padding of the drop-down                   |
| ms_padding_left         | dimension | set the left padding of the drop-down                  |
| ms_padding_bottom       | dimension | set the bottom padding of the drop-down                |
| ms_padding_right        | dimension | set the right padding of the drop-down                 |
| ms_popup_padding_top    | dimension | set the top padding of the drop-down items             |
| ms_popup_padding_left   | dimension | set the left padding of the drop-down items            |
| ms_popup_padding_bottom | dimension | set the bottom padding of the drop-down items          |
| ms_popup_padding_right  | dimension | set the right padding of the drop-down items           |
| ms_divider_height       | dimension | set the height of divider                              |
| ms_divider_color        | color     | set the color of divider                               |
| ms_dropdown_text_color  | color     | set the text color of the drop-down items              |


Acknowledgements
----------------

[Nice Spinner](https://github.com/arcadefire/nice-spinner) by Angelo Marchesin
[MaterialSpinner](https://github.com/jaredrummler/MaterialSpinner) forked from MaterialSpinner by jaredrummler

License
--------

    Copyright (C) 2016 Jared Rummler

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
