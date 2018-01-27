# @ava/babel-preset-stage-4 [![Build Status](https://travis-ci.org/avajs/babel-preset-stage-4.svg?branch=master)](https://travis-ci.org/avajs/babel-preset-stage-4)

> [Babel] preset for use with [AVA]

Aspires to bring ECMAScript stage 4 proposals to AVA's test and helper files.

Efficiently applies the minimum of transforms to run stage 4 code on Node.js 4, 6 and 8.

Built-ins are not added or extended, so features like Proxies, `Array.prototype.includes` or `String.prototype.padStart` will only be available if the Node.js version running the tests supports it. Consult [node.green] for details.

Sometimes a particular feature is *mostly* implemented in Node.js. In that case transforms are not applied. This applies to `new.target` and iterator closing, which are not supported in Node.js 4 even though classes and iterators are.


## Install

```console
$ npm install --save @ava/babel-preset-stage-4
```


## Usage

Add `@ava/stage-4` to your [Babel] presets.

### Options

For more information on setting options for a preset, refer to the [preset options] documentation.

#### `modules`

By default this preset transform ES2015 modules to CommonJS. Set to `false` to disable this behavior. Other values are ignored.

[AVA]: https://ava.li
[Babel]: https://babeljs.io
[node.green]: http://node.green
[preset options]: http://babeljs.io/docs/plugins/#pluginpreset-options
