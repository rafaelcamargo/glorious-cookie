# Glorious Cookie

[![CircleCI](https://circleci.com/gh/glorious-codes/glorious-cookie.svg?style=svg)](https://circleci.com/gh/glorious-codes/glorious-cookie)
[![codecov](https://codecov.io/gh/glorious-codes/glorious-cookie/branch/master/graph/badge.svg)](https://codecov.io/gh/glorious-codes/glorious-cookie)
[![Code Climate](https://codeclimate.com/github/rafaelcamargo/glorious-cookie/badges/gpa.svg)](https://codeclimate.com/github/rafaelcamargo/glorious-cookie)

## Installation

Glorious Cookie is available via npm:
```
npm i @glorious/cookie --save
```

Once installed, you just need import it in your module:
``` javascript
import gcookie from '@glorious/cookie';
```
or you may include it on your html:
``` html
<script src="/node_modules/@glorious/cookie/dist/gcookie.min.js"></script>
```

## Usage

Intending to be as simple as possible, Glorious Cookie has only three methods.

### Set

``` javascript
/*
** @key: String [required]
** @value: String [required]
** @days: Number [optional] - If not provided, cookie is removed when the user closes the browser.
** @path: String [optional] - If not provided, cookie is valid for the entire site.
*/
gcookie.set(key, value, days, path);
```

### Get

``` javascript
/*
** @key: String [optional] - If not provided, all cookies will be returned.
*/
gcookie.get(key);
```

### Remove

``` javascript
/*
** @key: String [required]
** @path: String [optional] - If you have specified a path on gcookie.set(),
**                            it will be required here.
*/
gcookie.remove(key, path);
```

**Note:** If cookies are not available, a warning will be logged when trying to set or remove a cookie.


## Contributing

1. Install [Node](https://nodejs.org/en/). Download the "Recommend for Most Users" version.

2. Clone the repo:
``` bash
git clone git@github.com:glorious-codes/glorious-cookie.git
```

3. Go to the project directory:
``` bash
cd glorious-cookie
```

4. Install the project dependencies:
``` bash
npm install
```

5. Install the gulp globally:
``` bash
npm install --global gulp
```

6. Build the project:
``` bash
gulp start
```

## Tests

Ensure that all code that you have added is covered with unit tests:
``` bash
npm run test
```
> Note: In some cases on Windows needed to `npm install natives` after `npm install`
