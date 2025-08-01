---
title: "SyntaxError: function statement requires a name"
slug: Web/JavaScript/Reference/Errors/Unnamed_function_statement
page-type: javascript-error
sidebar: jssidebar
---

The JavaScript exception "function statement requires a name" occurs
when there is a [function statement](/en-US/docs/Web/JavaScript/Reference/Statements/function)
in the code that requires a name.

## Message

```plain
SyntaxError: Function statements require a function name (V8-based)
SyntaxError: function statement requires a name (Firefox)
SyntaxError: Function statements must have a name. (Safari)
```

## Error type

{{jsxref("SyntaxError")}}

## What went wrong?

There is a [function statement](/en-US/docs/Web/JavaScript/Reference/Statements/function) in the code that requires a name.
You'll need to check how functions are defined and if you need to provide a name for it, or if the function in question needs to be a function expression, an [IIFE](/en-US/docs/Glossary/IIFE), or if the function code is placed correctly in this context at all.

## Examples

### Statements vs. expressions

A _[function statement](/en-US/docs/Web/JavaScript/Reference/Statements/function)_ (or _function declaration_) requires a name.
This won't work:

```js-nolint example-bad
function () {
  return "Hello world";
}
// SyntaxError: function statement requires a name
```

You can use a [function expression](/en-US/docs/Web/JavaScript/Reference/Operators/function) (assignment) instead:

```js example-good
const greet = function () {
  return "Hello world";
};
```

If your function is intended to be an [IIFE](https://en.wikipedia.org/wiki/Immediately-invoked_function_expression) (Immediately Invoked Function Expression, which is a function that runs as soon as it is defined) you will need to add a few more braces:

```js example-good
(function () {
  // …
})();
```

### Labeled functions

[Labels](/en-US/docs/Web/JavaScript/Reference/Statements/label) are an entirely different feature from function names. You can't use a label as a function name.

```js-nolint example-bad
function Greeter() {
  german: function () {
    return "Moin";
  }
}
// SyntaxError: function statement requires a name
```

In addition, labeled function declarations themselves are a deprecated feature. Use regular function declarations instead.

```js example-good
function Greeter() {
  function german() {
    return "Moin";
  }
}
```

### Object methods

If you intended to create a method of an object, you will need to create an object.
The following syntax without a name after the `function` keyword is valid then.

```js example-good
const greeter = {
  german: function () {
    return "Moin";
  },
};
```

You can also use the [method syntax](/en-US/docs/Web/JavaScript/Reference/Functions/Method_definitions).

```js
const greeter = {
  german() {
    return "Moin";
  },
};
```

### Callback syntax

Also, check your syntax when using callbacks.
Braces and commas can quickly get confusing.

```js-nolint example-bad
promise.then(
  function () {
    console.log("success");
  });
  function () {
    console.log("error");
}
// SyntaxError: function statement requires a name
```

Correct would be:

```js example-good
promise.then(
  function () {
    console.log("success");
  },
  function () {
    console.log("error");
  },
);
```

## See also

- [Functions](/en-US/docs/Web/JavaScript/Guide/Functions) guide
- [`function`](/en-US/docs/Web/JavaScript/Reference/Statements/function)
- [`function` expression](/en-US/docs/Web/JavaScript/Reference/Operators/function)
- {{Glossary("IIFE")}}
- [Labeled statement](/en-US/docs/Web/JavaScript/Reference/Statements/label)
