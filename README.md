Rules
=====
A list of rules inspired by [The Most Adeuqantly Guide](https://github.com/MostlyAdequate/mostly-adequate-guide)

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
// Disallow:
const files = torrent.files;

// Allow
const { files } = torrent;
```

## Methods of objects passed as arguments cannot be called
```js
// Disallow:
const result = function(n) {
  return n.callSomeMethod() + 'some';
};

// Allow
const result = function(callSomeMethod) {
  return callSomeMethod() + 'some';
};

```
