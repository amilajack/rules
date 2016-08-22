Rules
=====
A temporarly list of eslint rules to make:

A list of rules inspired by The Most Adeuqantly Guide

## Disallow all mutative array/object methods, ex. .push()

## Disallow `typeof`
Instead, use https://github.com/chaijs/type-detect

## Disalow checking for nil values/"truthiness"
Checking for nil values should be abstracted by monads
Concept [take from elm](http://guide.elm-lang.org/core_language.html)

```js
// Disallow
if (3) {

}

// Allow
if (3 > 2) {

}
```

## Disallow single param parens

```js
// Disallow
return files.find((file) => true);

// Allow
return files.find(file => true);
```

## ES6 shorthand
```js
// Instead of:
const files = torrent.files;

// Do this
const { files } = torrent;
```

## Methods of objects passed as arguments cannot be called
```js

// Instead of:

var punch = function(player, target) {
      return player.get('team') === target.get('team') ? target : decrementHP(target);
};

// Do this:
var punch = function(player, target) {
      return 'red' === 'green' ? target : decrementHP(target);
};

```
