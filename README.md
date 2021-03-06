# gulp-hjson

[![Build Status](https://img.shields.io/travis/hjson/gulp-hjson.svg?style=flat-square)](http://travis-ci.org/hjson/gulp-hjson)
[![NPM version](https://img.shields.io/npm/v/gulp-hjson.svg?style=flat-square)](http://www.npmjs.com/package/gulp-hjson)

Hjson plugin for gulp, converts from and to JSON.

[Hjson](http://hjson.org), the Human JSON. A configuration file format for humans. Relaxed syntax, fewer mistakes, more comments.

For details and syntax see [hjson.org](http://hjson.org).

## Usage

First, install `gulp-hjson` as a development dependency:

```shell
npm install --save-dev gulp-hjson
```

Then, add it to your `gulpfile.js`:

```javascript
var Hjson = require('gulp-hjson');

gulp.task('hjson', function() {
  gulp.src(['*.hjson'])
    .pipe(Hjson({ to: 'json' }))
    .pipe(gulp.dest('output'));
});
```

## options

### { to: 'json' }

Convert to JSON.

### { to: 'json', jsonSpace: '  ' }

Convert to formatted JSON.

### { to: 'hjson' }

Convert to Hjson.

