# SharedCount

[![Build Status via Travis CI](https://travis-ci.org/DigitalRockers/sharedcount.svg?branch=master)](https://travis-ci.org/DigitalRockers/sharedcount)
[![NPM version](http://img.shields.io/npm/v/sharedcount.svg)](https://www.npmjs.org/package/sharedcount)

[SharedCount](https://sharedcount.com) module for [nodejs](https://nodejs.org)

SharedCount API documentation: [https://www.sharedcount.com/api-docs/getting-started](https://www.sharedcount.com/api-docs/getting-started)

This software is released under the MIT license. See `LICENSE` for more details

## Download and Installation

From the command line

	$ yarn add sharedcount

or

	$ npm install sharedcount


## Example use

```javascript
var SharedCount = require('sharedcount');

var sc = new SharedCount({ apikey: 'YOUR_API_KEY' });

const result = await sc.url('www.yahoo.com')}
```

## Documentation

Initialize SharedCount object:
```javascript
var SharedCount = require('sharedcount');
var sc = new SharedCount({
	apiKey: 'YOUR_API_KEY' || process.env.SharedcountApiKey,
});
```

### url(url)
Resolve with share counts for a URL.

```javascript
sc.url('sharedcount.com')
```

### quota()
Resolve with information about your quota allocation for the day.

 ```javascript
sc.quota();
```

### usage()
Resolve with historical quota usage information.

```javascript
sc.usage();
```

### domain_whitelist()
Resolve with a list of domains added to your domain whitelist, and whether the domain whitelist is currently being enforced.

```javascript
sc.domainWhitelist();
```

### status()
Check to see if the SharedCount API is currently up.

```javascript
sc.status();
```
