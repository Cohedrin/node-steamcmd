# steamcmd [![Build Status](https://travis-ci.org/mathphreak/node-steamcmd.svg?branch=master)](https://travis-ci.org/mathphreak/node-steamcmd)

> My solid module

## Install

```
$ npm install --save steamcmd
```

## Usage

```js
const steamcmd = require('steamcmd');

steamcmd.download();
//=> returns a Promise for downloading steamcmd locally
steamcmd.touch();
//=> returns a Promise for ensuring that steamcmd is updated and dependencies exist
steamcmd.getAppInfo(730)
//=> returns a Promise for the app info of appID 730
```

## API

### steamcmd.download([opts])
Downloads steamcmd for the current OS into `opts.binDir`

### steamcmd.touch([opts])
Runs steamcmd and immediately exits

### steamcmd.getAppInfo(appid[, opts])
Asks steamcmd to get the app info for the given app

## Configuration

All functions take an optional options parameter.

#### binDir

type: string  
default: `path.join(__dirname, 'steamcmd_bin')`

The directory to use when downloading and running `steamcmd` itself.
Defaults to `steamcmd_bin` in the same directory where this package is installed.

## License

MIT © [Matt Horn](http://mathphreak.me)
