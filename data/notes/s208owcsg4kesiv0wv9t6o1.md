## Dates

JavaScript includes a ```Date``` constructor to create objects for dates and times.
```js
> let date = new Date('December 25, 2012')
> date.getDay() // returns day of the week (0-6)
= 2
```
Get the day name example:
```js
function getDayOfWeek(date) {
  let daysOfWeek = [
    'Sunday',
    'Monday',
    'Tuesday',
    'Wednesday',
    'Thursday',
    'Friday',
    'Saturday',
  ];

  return daysOfWeek[date.getDay()];
}

let date = new Date('December 25, 2012');
console.log(getDayOfWeek(date)); // => Tuesday
```