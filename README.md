#HistoRange
==========

Range selector based on jQuery UI slider with a bar chart for a background ala Google Finance.

## Styling
I have preserved the existing jquery ui styles, so by default the range selector handles should work
with the jQuery UI handles. However, I have also added new style class

## Usage
Takes all the same options as the jQuery UI slider. See here: http://api.jqueryui.com/slider/
Exceptions:
- takes a histogramData array of data points. It will draw a bar graph to scale for each datapoint. Negative numbers aren't supported yet, and probably won't be until someone asks. 
- the `range` option is defaulted to `true`

Make your javascript like this

```
var histogramData = [8, 7, 5, 6, 3, 11, 9, 13, 21, 34, 55, 21, 13, 8, 13, 3, 2, 8, 1, 5];

$(function() {
  $(".rangepicker").historange({
    histogramData: histogramData,
    min: 0,
    max: 4000,
    values: [1400, 2800]
  });
});
```

And a DOM element like whaaaa

```
<div class="rangepicker"></div>
```
