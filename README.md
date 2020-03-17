# countdown.js
A simple and easy-to-use countdown.

## [Download](https://github.com/igorkowalczyk/countdown/archive/master.zip) / [Demo](https://igorkowalczyk.github.io/countdown.js/examples/example-4-coming-soon.html)

## How to use

Compiled and production-ready code can be found in the `download` directory.

### 1. Include countdown.js on your site

```html
<script src="path/to/countdown.min.js"></script>
```

### 2. Set end date
Choose a date that supports `JavaScript` in whatever format you like.

```javascript
var endDate = "2050/01/01";
```

### 3. Initialize countdown.js
In the footer of your page, after the content, initialize countdown.js. And that's it, you're done. Nice work!

```javascript
var myCountDown = new countdown(endDate, function (remaining, finished) {

  if (finished) {
    
    // countdown finished

  } else {

    // do something

  }

});
```

**Example 1**

```javascript
var myCountDown = new countdown("2050/01/01", function (remaining, finished) {

  if (finished) {
    
    document.body.innerHTML = "Expired";

  } else {

    document.body.innerHTML = remaining.hours + "h " + remaining.minutes + "m " + remaining.seconds + "s";

  }

});
```

**Example 2**

```javascript
var myCountDown = new countdown(new Date("2050-01-01T12:05:55Z"), function (remaining, finished) {

  if (finished) {
    
    document.body.innerHTML = "Expired";

  } else {

    document.body.innerHTML = remaining.hours + "h " + remaining.minutes + "m " + remaining.seconds + "s";

  }

});
```


### Use ysCountDown events in your own scripts

You can also call countdown.js events in your own scripts.

#### init()
Initialize countdown.js This is called automatically when you setup your `new countdown` object, but can be used to reinitialize your instance.

```javascript
var myCountDown = new countdown(endDate, myCallback);

myCountDown.init(myDate, myFunction);
```

#### destroy()
Destroy the current `ysCountDown.init()`. This is called automatically during the `init` function to remove any existing initializations.

```javascript
var myCountDown = new ysCountDown(endDate, function (remaining, finished) { });

myCountDown.destroy();
```

### Callback parameters
The callback function has two parameters.

The first parameter contains the following calculations related to the countdown.

| Parameters   |
|--------------|
| seconds      |
| minutes      |
| hours        |
| days         |
| daysToWeek   |
| daysToMonth  |
| weeks        |
| weeksToMonth |
| months       |
| monthsToYear |
| years        |
| totalDays    |
| totalHours   |
| totalMinutes |
| totalSeconds |

The second parameter indicates whether the countdown is over.

# License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details

Created by [Yusuf SEZER](http://www.yusufsezer.com)
