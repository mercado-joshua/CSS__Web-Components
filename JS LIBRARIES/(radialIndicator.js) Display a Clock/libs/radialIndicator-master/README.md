# radialIndicator

A simple and lightweight circular indicator plugin. Also works on Internet Explorer. It supports duration, color range, interpolation, formatting, percentage value and much more. Does work well with jQuery and AngularJS.

### Installation

Through npm:
```
npm install @sudhanshu/radial-indicator
```

### For Devs

When updating the documentation, checkout the repository and run `npm install` and then `npm start` to run examples locally.

### Major updates

##### 2.0.0

- Added the option to specify an easing function
- Added the option to specify an animation duration
- `animate(value, anmDuration)` has now an optional second parameter to define a duration from current value to the target value. While the `duration` property on the indicator is the duration from your `minValue` to `maxValue`. If you did not set those values default is 0-100.
- Replaced `setInterval` with `requestAnimationFrame`
- Fixed: Formatter not handling decimal places correctly
- Fixed: Animation issue when the `minValue` is negative #11
- Fixed: Using decimal value in indicator #25

###### Release Notes

- Since `setInterval()` was replaced with `requestAnimationFrame()` there are most likely, but depending on your setup, more iterations than before. Causing a smoother animation. Before this release if no precision property was set, default was depending on the step after each iteration. This is no longer the case since we have smaller steps with more decimal places. If you do not specify precision on the indicator, default number of decimals is 0. If you want decimal places, you have to set the `precision` property.
- When a `format` pattern is set, decimal places in the format will take precedence over `precision` property
- `frameTime` and `frameNum` properties on the indicator are now deprecated. Those fields are only used when no `duration` property is set and will be removed in a future release.

##### 1.4.0

- Added option to support rendering in the opposite direction.

##### 1.2.0

- Added option to allow user interaction on mouse and touch events.
- Added `precision` option to support float value.

##### 1.1.0

- Fixed draw issue on iPad and Android devices and added `onAnimationComplete` callback.
