# jsonpatch-to-mongodb

Convert [JSON patches](http://jsonpatch.com/) into a MongoDB update.

This repo is a fork of https://github.com/mongodb-js/jsonpatch-to-mongodb maintained by MentorPass.
PRs are welcome.
We endeavour to maintain the package inline with the [IETF preposal](https://tools.ietf.org/html/rfc6902) but will not
merge PRs that could cause breaking changes to our products. 

## Example

```javascript
var toMongodb = require('@mentorpass/jsonpatch-to-mongodb');
var patches = [{
  op: 'replace',
  path: '/name',
  value: 'dave'
}];

console.log(toMongodb(patches));
// {'$set': {name: 'dave'}};
```

Example: [with express and mongoose](http://github.com/imlucas/jsonpatch-to-mongodb/tree/master/examples/express)


## Install

```
npm install --save @mentorpass/jsonpatch-to-mongodb
```

## Test

```
npm test
```

## License

MIT
