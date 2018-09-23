# Mean Stack JS _ Mongo Express

[![npm][npm-image]][npm-url]
[![downloads][downloads-image]][downloads-url]
[![dependencies](https://david-dm.org/greenpioneersolutions/meanstackjs_mongo-express.svg)](https://david-dm.org/greenpioneersolutions/meanstackjs_mongo-express)
[![npm-issues](https://img.shields.io/github/issues/greenpioneersolutions/meanstackjs_mongo-express.svg)](https://github.com/greenpioneersolutions/meanstackjs_mongo-express/issues)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com/)
[![Build Status](https://travis-ci.org/greenpioneersolutions/meanstackjs_mongo-express.svg?branch=master)](https://travis-ci.org/greenpioneersolutions/meanstackjs_mongo-express)
[![js-standard-style](https://nodei.co/npm/meanstackjs_mongo-express.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/meanstackjs_mongo-express.png?downloads=true&downloadRank=true&stars=true)

[npm-image]: https://img.shields.io/npm/v/meanstackjs_mongo-express.svg?style=flat
[npm-url]: https://npmjs.org/package/meanstackjs_mongo-express
[downloads-image]: https://img.shields.io/npm/dt/meanstackjs_mongo-express.svg?style=flat
[downloads-url]: https://npmjs.org/package/meanstackjs_mongo-express

## What is `meanstackjs_mongo-express`

This is a tool for the [meanstackjs](http://meanstackjs.com/). It uses [mongo-express](https://www.npmjs.com/package/mongo-express) to give you a web-based MongoDB admin interface written with Node.js, Express and Bootstrap3

## Installation

``` bash
# NPM
npm install meanstackjs_mongo-express --save
# YARN
yarn add meanstackjs_mongo-express
```

## Usage

``` js
// USAGE
function tool (self) {
  require('meanstackjs_mongo-express')(self)
}
```

## Settings

``` js
const mongoexpress = {
  mongodb: {
    server: process.env.MONGODB_SERVER || mongodbUri.hosts[0].host,
    port: process.env.MONGODB_PORT || mongodbUri.hosts[0].port || 27017,
    useSSL: process.env.MONGODB_SSL || false,
    poolSize: self.settings.mongodb.size || 1,
    admin: process.env.MONGODB_ENABLE_ADMIN ? process.env.MONGODB_ENABLE_ADMIN.toLowerCase() === 'true' : false,
    auth: [
      {
        database: process.env.MONGODB_AUTH_DATABASE || mongodbUri.database,
        username: process.env.MONGODB_AUTH_USERNAME || mongodbUri.username,
        password: process.env.MONGODB_AUTH_PASSWORD || mongodbUri.password
      }
    ],
    adminUsername: process.env.MONGODB_ADMINUSERNAME || '',
    adminPassword: process.env.MONGODB_ADMINPASSWORD || ''
  },

  site: {
    baseUrl: process.env.SITE_BASEURL || '/',
    cookieKeyName: 'mongo-express',
    cookieSecret: process.env.SITE_COOKIESECRET || 'cookiesecret',
    host: process.env.VCAP_APP_HOST || 'localhost',
    port: process.env.VCAP_APP_PORT || 8081,
    requestSizeLimit: process.env.REQUEST_SIZE || '50mb',
    sessionSecret: process.env.SITE_SESSIONSECRET || 'sessionsecret',
    sslCert: process.env.SITE_SSL_CRT_PATH || '',
    sslEnabled: process.env.SITE_SSL_ENABLED || false,
    sslKey: process.env.SITE_SSL_KEY_PATH || ''
  },
  useBasicAuth: process.env.BASICAUTH_USERNAME !== '',
  basicAuth: {
    username: process.env.BASICAUTH_USERNAME || 'admin',
    password: process.env.BASICAUTH_PASSWORD || 'pass'
  },
  options: {
    editorTheme: process.env.OPTIONS_EDITORTHEME || 'rubyblue'
  },
  defaultKeyNames: process.env.DEFAULT_KEY_NAMES,
}
```

## License

The MIT License (MIT)

Copyright (c) 2014-2018 Green Pioneer

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Created by ![Green Pioneer](http://greenpioneersolutions.com/img/icons/apple-icon-180x180.png)

#### This is [on GitHub](https://github.com/greenpioneersolutions/meanstackjs_mongo-express)
#### Find us [on GitHub](https://github.com/greenpioneersolutions)
#### Find us [on Twitter](https://twitter.com/greenpioneerdev)
#### Find us [on Facebook](https://www.facebook.com/Green-Pioneer-Solutions-1023752974341910)
#### Find us [on The Web](http://greenpioneersolutions.com/)
