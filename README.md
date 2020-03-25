# SingleDateAndTimePicker

You can now select a date and a time with only one widget !


<a href="https://goo.gl/WXW8Dc">
  <img alt="Android app on Google Play" src="https://developer.android.com/images/brand/en_app_rgb_wo_45.png" />
</a>



[![screen](https://raw.githubusercontent.com/florent37/SingleDateAndTimePicker/master/media/new_video.gif)](https://www.github.com/florent37/SingleDateAndTimePicker)

# Usage

```java
new SingleDateAndTimePickerDialog.Builder(context)
            //.bottomSheet()
            //.curved()
            //.minutesStep(15)
            //.displayHours(false)
            //.displayMinutes(false)
            //.todayText("aujourd'hui")
            .displayListener(new SingleDateAndTimePickerDialog.DisplayListener() {
                                @Override
                                public void onDisplayed(SingleDateAndTimePicker picker) {
                                     //retrieve the SingleDateAndTimePicker
                                }
                            })
            
            .title("Simple")
            .listener(new SingleDateAndTimePickerDialog.Listener() {
                @Override
                public void onDateSelected(Date date) {
                    
                }
            }).display();
```

## Select 2 dates

[![screen](https://raw.githubusercontent.com/florent37/SingleDateAndTimePicker/master/media/double_small_crop.png)](https://www.github.com/florent37/SingleDateAndTimePicker)

```java
new DoubleDateAndTimePickerDialog.Builder(context)
            //.bottomSheet()
            //.curved()
            //.minutesStep(15)
            .title("Double")
            .tab0Text("Depart")
            .tab1Text("Return")
            .listener(new DoubleDateAndTimePickerDialog.Listener() {
                @Override
                public void onDateSelected(List<Date> dates) {
                
                }
        }).display();
```

## Display days, months and years

[![screen](https://raw.githubusercontent.com/florent37/SingleDateAndTimePicker/master/media/years_crop.png)](https://www.github.com/florent37/SingleDateAndTimePicker)

```java
new SingleDateAndTimePickerDialog.Builder(this)
            .bottomSheet()
            .curved()
            .displayMinutes(false)
            .displayHours(false)
            .displayDays(false)
            .displayMonth(true)
            .displayYears(true)
            .displayDaysOfMonth(true)
            .display();
```

## Include in a layout

[![screen](https://raw.githubusercontent.com/florent37/SingleDateAndTimePicker/master/media/layout_small.png)](https://www.github.com/florent37/SingleDateAndTimePicker)

```xml
<com.github.florent37.singledateandtimepicker.SingleDateAndTimePicker
        android:layout_width="wrap_content"
        android:layout_height="230dp"
        app:picker_curved="true"
        app:picker_cyclic="true"
        app:picker_visibleItemCount="7"
        />
```

# iOS like :P

[![screen](https://raw.githubusercontent.com/florent37/SingleDateAndTimePicker/master/media/ios_simple_crop.png)](https://www.github.com/florent37/SingleDateAndTimePicker)

```java
new SingleDateAndTimePickerDialog.Builder(context)
                                    .bottomSheet()
                                    .curved()
```

[![screen](https://raw.githubusercontent.com/florent37/SingleDateAndTimePicker/master/media/ios_double_crop.png)](https://www.github.com/florent37/SingleDateAndTimePicker)

```java
new DoubleDateAndTimePickerDialog.Builder(context)
                                    .bottomSheet()
                                    .curved()
```

# Customisation

You can change the minutes steps (default : 5min)
```java
new SingleDateAndTimePickerDialog.Builder(context)
            .minutesStep(15)
            .display();
```

And change some colors

[![screen](https://raw.githubusercontent.com/florent37/SingleDateAndTimePicker/master/media/custom_colors.png)](https://www.github.com/florent37/SingleDateAndTimePicker)

```java
new SingleDateAndTimePickerDialog.Builder(context)
            .backgroundColor(Color.BLACK)
            .mainColor(Color.GREEN)
            .titleColor(Color.WHITE)
            .display();
```

# Date range

Force user to select a date between a range

```java
new SingleDateAndTimePickerDialog.Builder(context)
            .defaultDate(defaultDate)
            .minDateRange(minDate)
            .maxDateRange(maxDate)
            .display();
```

Or simply force user to select a future date

```java
new SingleDateAndTimePickerDialog.Builder(context)
            .mustBeOnFuture()
            .display();
```
# DateTime Picker with title
[![screen](https://github.com/pawarlalit29/SingleDateAndTimePicker/blob/master/media/date_picker_with_title.png)](https://github.com/pawarlalit29/SingleDateAndTimePicker)
[![screen](https://github.com/pawarlalit29/SingleDateAndTimePicker/blob/master/media/datetime_picker_with_title.png)](https://github.com/pawarlalit29/SingleDateAndTimePicker)

# Download

<a href='https://ko-fi.com/A160LCC' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://az743702.vo.msecnd.net/cdn/kofi1.png?v=0' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

In your module [![Download](https://api.bintray.com/packages/florent37/maven/SingleDateAndTimePicker/images/download.svg)](https://bintray.com/florent37/maven/SingleDateAndTimePicker/_latestVersion)
```groovy
implementation 'com.github.florent37:SingleDateAndTimePicker:2.2.0'
//compatible with androidX
```

# Credits

Author: Florent Champigny [http://www.florentchampigny.com/](http://www.florentchampigny.com/)

Blog : [http://www.tutos-android-france.com/](http://www.tutos-android-france.com/)

Fiches Plateau Moto : [https://www.fiches-plateau-moto.fr/](https://www.fiches-plateau-moto.fr/)

<a href="https://goo.gl/WXW8Dc">
  <img alt="Android app on Google Play" src="https://developer.android.com/images/brand/en_app_rgb_wo_45.png" />
</a>


<a href="https://plus.google.com/+florentchampigny">
  <img alt="Follow me on Google+"
       src="https://raw.githubusercontent.com/florent37/DaVinci/master/mobile/src/main/res/drawable-hdpi/gplus.png" />
</a>
<a href="https://twitter.com/florent_champ">
  <img alt="Follow me on Twitter"
       src="https://raw.githubusercontent.com/florent37/DaVinci/master/mobile/src/main/res/drawable-hdpi/twitter.png" />
</a>
<a href="https://www.linkedin.com/in/florentchampigny">
  <img alt="Follow me on LinkedIn"
       src="https://raw.githubusercontent.com/florent37/DaVinci/master/mobile/src/main/res/drawable-hdpi/linkedin.png" />
</a>


License
--------

    Copyright 2016 florent37, Inc.

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
