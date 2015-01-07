# gulp-hjson

[![Build Status](https://img.shields.io/travis/laktak/gulp-hjson.svg?style=flat-square)](http://travis-ci.org/laktak/gulp-hjson)
[![NPM version](https://img.shields.io/npm/v/gulp-hjson.svg?style=flat-square)](http://www.npmjs.com/package/gulp-hjson)

Hjson to/from JSON convert plugin for gulp 3.

Hjson, the Human JSON. A configuration file format that caters to humans and helps reduce the errors they make.

It supports `#`, `//` and `/**/` style comments as well as avoiding trailing/missing comma and other mistakes. For details and syntax see http://laktak.github.io/hjson.

## Usage

First, install `gulp-hjson` as a development dependency:

```shell
npm install --save-dev gulp-hjson
```

Then, add it to your `gulpfile.js`:

```javascript
var Hjson = require('gulp-hjson');

gulp.task('json', function() {
  gulp.src(['*.json'])
    .pipe(Hjson({ to: 'hjson' }))
    .pipe(gulp.dest('output'));
});
```

## options

### { to: 'json' }

Convert to JSON.

### { to: 'hjson' }

Convert to Hjson.

