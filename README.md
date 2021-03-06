# gulp-terser

Gulp plugin, compressed es6+ code.

## Install
```
$ npm install gulp-terser --save-dev
```
or
```
$ yarn add gulp-terser --dev
```

## How to use
```javascript
const gulp = require('gulp');
const terser = require('gulp-terser');

function es(){
  return gulp.src('./src/index.js')
    .pipe(terser())
    .pipe(gulp.dest('./build'))
}

gulp.task('default', es);
```

## Options
Terser configuration can be viewed [https://github.com/fabiosantoscode/terser#minify-options](https://github.com/fabiosantoscode/terser#minify-options).
```javascript
const gulp = require('gulp');
const terser = require('terser');

function es(){
  return gulp.src('./src/index.js')
    .pipe(terser({
      warnings: true,
      ecma: 8
    }))
    .pipe(gulp.dest('./build'))
}

gulp.task('default', es);
```