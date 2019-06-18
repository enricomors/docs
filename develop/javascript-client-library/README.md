# JavaScript Client Library

## Introduction

A JavaScript client library for interacting with a [Radix](https://www.radixdlt.com/) Distributed Ledger.

For an overview of the main components of the library and how they fit together, read this [blog post](https://www.radixdlt.com/post/introducing-the-radix-javascript-library).

{% hint style="info" %}
**Note:** this library and the network itself are currently in **Alpha** development phase. Please report any issues in the [GitHub issue tracker](https://github.com/radixdlt/radixdlt-js/issues).
{% endhint %}

## Features

* Full Typescript support
* Follow the reactive programming pattern using [RxJS](https://rxjs-dev.firebaseapp.com/)
* Cryptography using the [elliptic](https://github.com/indutny/elliptic) library
* Automatically manage connections to the Radix [Universe](../../learn/glossary.md#universe) in a sharded environment
* Communication with the Radix network using RPC over WebSockets
* Read [Atoms](../../learn/glossary.md#atoms) in any address
* Write Atoms to the ledger
* End-to-end data encryption using ECIES

## Installation

To install the library using your preferred package manager:

`yarn add radixdlt` or `npm install radixdlt --save`

## Example applications

* [Front-end example using Vue.js](https://github.com/radixdlt/radixdlt-js-skeleton)
* [Express.js server example](https://github.com/radixdlt/radixdlt-js-server-example)

## Build

To build the library using your preferred package manager:

`yarn install && yarn build` or `npm install && npm build`

### Test

Run tests with `yarn test`.

## Known issues

### Angular

Apparently, on Angular 6+ versions, the node modules `polyfills` from webpack are not bundled. To fix your issue with crypto, path, etc. go to `node_modules/@angular-devkit/build-angular/src/angular-cli-files/models/webpack-configs/browser.js` and do the following change:

```javascript
node: { crypto: true, path: true }
```

{% hint style="warning" %}
**Note:** this is not a reproducible fix. If you install your modules in a new location, you will lose this change.
{% endhint %}

## Join the Radix Community

* ​[Telegram](https://t.me/radix_dlt) for general chat
* ​[Discord](https://discord.gg/7Q7HSZZ) for developer chat
* ​[Reddit](https://reddit.com/r/radix) for general discussion
* ​[Forum](https://forum.radixdlt.com/) for technical discussion
* ​[Twitter](https://twitter.com/radixdlt) for announcements
* ​[Email newsletter](https://radixdlt.typeform.com/to/nyKvMV) for weekly updates
* Mail to [hello@radixdlt.com](mailto:info@radixdlt.com) for general enquiries.

