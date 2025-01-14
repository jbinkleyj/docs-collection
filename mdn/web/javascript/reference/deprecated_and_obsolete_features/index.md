---
title: Deprecated and obsolete features
slug: Web/JavaScript/Reference/Deprecated_and_obsolete_features
tags:
  - Deprecated
  - Guide
  - JavaScript
  - Deprecated
---

{{JsSidebar("More")}}

This page lists features of JavaScript that are deprecated (that is, still available but planned for removal) and obsolete (that is, no longer usable).

## Deprecated features

These deprecated features can still be used, but should be used with caution because they are expected to be removed entirely sometime in the future. You should work to remove their use from your code.

### RegExp properties

the following properties are deprecated. This does not affect their use in {{jsxref("String.replace", "replacement strings", "", 1)}}:

<table class="standard-table">
  <tbody>
    <tr>
      <th>Property</th>
      <th>Description</th>
    </tr>
    <tr>
      <td>{{jsxref("RegExp.n", "$1-$9")}}</td>
      <td>
        <p>
          Parenthesized substring matches, if any.<br /><strong
            >Warning:</strong
          >
          Using these properties can result in problems, since browser
          extensions can modify them. Avoid them!
        </p>
      </td>
    </tr>
    <tr>
      <td>{{jsxref("RegExp.input", "$_")}}</td>
      <td>See <code>input</code>.</td>
    </tr>
    <tr>
      <td>{{jsxref("RegExp.multiline", "$*")}}</td>
      <td>See <code>multiline</code>.</td>
    </tr>
    <tr>
      <td>{{jsxref("RegExp.lastMatch", "$&amp;")}}</td>
      <td>See <code>lastMatch</code>.</td>
    </tr>
    <tr>
      <td>{{jsxref("RegExp.lastParen", "$+")}}</td>
      <td>See <code>lastParen</code>.</td>
    </tr>
    <tr>
      <td>{{jsxref("RegExp.leftContext", "$`")}}</td>
      <td>See <code>leftContext</code>.</td>
    </tr>
    <tr>
      <td>{{jsxref("RegExp.rightContext", "$'")}}</td>
      <td>See <code>rightContext</code>.</td>
    </tr>
    <tr>
      <td>{{jsxref("RegExp.input", "input")}}</td>
      <td>The string against which a regular expression is matched.</td>
    </tr>
    <tr>
      <td>{{jsxref("RegExp.lastMatch", "lastMatch")}}</td>
      <td>The last matched characters.</td>
    </tr>
    <tr>
      <td>{{jsxref("RegExp.lastParen", "lastParen")}}</td>
      <td>The last parenthesized substring match, if any.</td>
    </tr>
    <tr>
      <td>{{jsxref("RegExp.leftContext", "leftContext")}}</td>
      <td>The substring preceding the most recent match.</td>
    </tr>
    <tr>
      <td>{{jsxref("RegExp.rightContext", "rightContext")}}</td>
      <td>The substring following the most recent match.</td>
    </tr>
  </tbody>
</table>

The following are now properties of `RegExp` instances, no longer of the `RegExp` object:

| Property                                      | Description                                                                                                        |
| --------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| {{jsxref("RegExp.global", "global")}}         | Whether or not to test the regular expression against all possible matches in a string, or only against the first. |
| {{jsxref("RegExp.ignoreCase", "ignoreCase")}} | Whether or not to ignore case while attempting a match in a string.                                                |
| {{jsxref("RegExp.lastIndex", "lastIndex")}}   | The index at which to start the next match.                                                                        |
| {{jsxref("RegExp.multiline", "multiline")}}   | Whether or not to search in strings across multiple lines.                                                         |
| {{jsxref("RegExp.source", "source")}}         | The text of the pattern.                                                                                           |

### RegExp methods

- The {{jsxref("RegExp.compile", "compile()")}} method is deprecated.
- The `valueOf` method is no longer specialized for `RegExp`. Use {{jsxref("Object.valueOf()")}}.

### Function properties

- The {{jsxref("Global_Objects/Function/caller", "caller")}} and {{jsxref("Global_Objects/Function/arguments", "arguments")}} properties are deprecated, because they leak the function caller. Instead of the arguments property, you should use the {{jsxref("Functions/arguments", "arguments")}} object inside function closures.

### Legacy generator

- {{jsxref("Statements/Legacy_generator_function", "Legacy generator function statement")}} and {{jsxref("Operators/Legacy_generator_function", "Legacy generator function expression")}} are deprecated. Use {{jsxref("Statements/function*", "function* statement")}} and {{jsxref("Operators/function*", "function* expression")}} instead.
- {{jsxref("Operators/Array_comprehensions", "JS1.7/JS1.8 Array comprehension", "#Differences_to_the_older_JS1.7.2FJS1.8_comprehensions")}} and {{jsxref("Operators/Generator_comprehensions", "JS1.7/JS1.8 Generator comprehension", "#Differences_to_the_older_JS1.7.2FJS1.8_comprehensions")}} are deprecated.

### Iterator

- {{jsxref("Global_Objects/StopIteration", "StopIteration")}} is deprecated.
- {{jsxref("Global_Objects/Iterator", "Iterator")}} is deprecated.

### Object methods

- {{jsxref("Object.watch", "watch")}} and {{jsxref("Object.unwatch", "unwatch")}} are deprecated. Use {{jsxref("Proxy")}} instead.
- `__iterator__` is deprecated.
- {{jsxref("Object.noSuchMethod", "__noSuchMethod__")}} is deprecated. Use {{jsxref("Proxy")}} instead.

### Date methods

- {{jsxref("Global_Objects/Date/getYear", "getYear")}} and {{jsxref("Global_Objects/Date/setYear", "setYear")}} are affected by the Year-2000-Problem and have been subsumed by {{jsxref("Global_Objects/Date/getFullYear", "getFullYear")}} and {{jsxref("Global_Objects/Date/setFullYear", "setFullYear")}}.
- You should use {{jsxref("Global_Objects/Date/toUTCString", "toUTCString")}} instead of the deprecated {{jsxref("Global_Objects/Date/toGMTString", "toGMTString")}} method in new code.
- {{jsxref("Global_Objects/Date/toLocaleFormat", "toLocaleFormat")}} is deprecated.

### Functions

- {{jsxref("Operators/Expression_closures", "Expression closures", "", 1)}} are deprecated. Use regular {{jsxref("Operators/function", "functions")}} or {{jsxref("Functions/Arrow_functions", "arrow functions", "", 1)}} instead.

### Proxy

- [Proxy.create](/en-US/docs/Archive/Web/Old_Proxy_API) and [Proxy.createFunction](/en-US/docs/Archive/Web/Old_Proxy_API) are deprecated. Use {{jsxref("Proxy")}} instead.
- The following traps are obsolete:

  - `hasOwn` ([bug 980565](https://bugzilla.mozilla.org/show_bug.cgi?id=980565), Firefox 33).
  - `getEnumerablePropertyKeys` ([bug 783829](https://bugzilla.mozilla.org/show_bug.cgi?id=783829), Firefox 37)
  - `getOwnPropertyNames` ([bug 1007334](https://bugzilla.mozilla.org/show_bug.cgi?id=1007334), Firefox 33)
  - `keys` ([bug 1007334](https://bugzilla.mozilla.org/show_bug.cgi?id=1007334), Firefox 33)

### Escape sequences

- Octal escape sequences (\ followed by one, two, or three octal digits) are deprecated in string and regular expression literals.
- The {{jsxref("Global_Objects/escape", "escape")}} and {{jsxref("Global_Objects/unescape", "unescape")}} functions are deprecated. Use {{jsxref("Global_Objects/encodeURI", "encodeURI")}}, {{jsxref("Global_Objects/encodeURIComponent", "encodeURIComponent")}}, {{jsxref("Global_Objects/decodeURI", "decodeURI")}} or {{jsxref("Global_Objects/decodeURIComponent", "decodeURIComponent")}} to encode and decode escape sequences for special characters.

### String methods

- HTML wrapper methods like {{jsxref("String.prototype.fontsize")}} and {{jsxref("String.prototype.big")}}.
- {{jsxref("String.prototype.quote")}} is removed from Firefox 37.
- non standard `flags` parameter in {{jsxref("String.prototype.search")}}, {{jsxref("String.prototype.match")}}, and {{jsxref("String.prototype.replace")}} are deprecated.
- {{jsxref("String.prototype.substr")}} probably won't be removed anytime soon, but it's defined in [Annex B](https://www.ecma-international.org/ecma-262/9.0/index.html#sec-string.prototype.substr) of the ECMA-262 standard, whose [introduction](https://www.ecma-international.org/ecma-262/9.0/index.html#sec-additional-ecmascript-features-for-web-browsers) states: "… Programmers should not use or assume the existence of these features and behaviors when writing new ECMAScript code. …"

## Obsolete features

These obsolete features have been entirely removed from JavaScript and can no longer be used as of the indicated version of JavaScript.

### Object

| Property                                                            | Description                                                                    |
| ------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| {{jsxref("Global_Objects/Object/count", "__count__")}}              | Returns the number of enumerable properties directly on a user-defined object. |
| {{jsxref("Global_Objects/Object/Parent", "__parent__")}}            | Points to an object's context.                                                 |
| {{jsxref("Global_Objects/Object/eval", "Object.prototype.eval()")}} | Evaluates a string of JavaScript code in the context of the specified object.  |
| {{jsxref("Object.observe()")}}                                      | Asynchronously observing the changes to an object.                             |
| {{jsxref("Object.unobserve()")}}                                    | Remove observers.                                                              |
| {{jsxref("Object.getNotifier()")}}                                  | Creates an object that allows to synthetically trigger a change.               |

### Function

| Property                                             | Description                 |
| ---------------------------------------------------- | --------------------------- |
| {{jsxref("Global_Objects/Function/arity", "arity")}} | Number of formal arguments. |

### String

- Non-standard String generic methods like `String.slice(myStr, 0, 12)`, `String.replace(myStr, /\./g, "!")`, etc. have been introduced in Firefox 1.5 (JavaScript 1.6), deprecated in Firefox 53, and removed in Firefox 68. You can use methods on {{jsxref("String", "String.prototype", "instance_methods")}} together with {{jsxref("Function.call")}} instead.

### Array

- Non-standard Array generic methods like `Array.slice(myArr, 0, 12)`, `Array.forEach(myArr, myFn)`, etc. have been introduced in Firefox 1.5 (JavaScript 1.6), deprecated in Firefox 68, and removed in Firefox 71. You can use methods on {{jsxref("Array", "Array.prototype", "instance_methods")}} together with {{jsxref("Function.call")}} instead.

<table class="standard-table">
  <tbody>
    <tr>
      <td>Property</td>
      <td>Description</td>
    </tr>
    <tr>
      <td>{{jsxref("Array.observe()")}}</td>
      <td>Asynchronously observing changes to Arrays.</td>
    </tr>
    <tr>
      <td>{{jsxref("Array.unobserve()")}}</td>
      <td>Remove observers.</td>
    </tr>
  </tbody>
</table>

### Number

- {{jsxref("Number.toInteger()")}}

### ParallelArray

- {{jsxref("ParallelArray")}}

### Statements

- {{jsxref("Statements/for_each...in", "for each...in")}} is deprecated. Use {{jsxref("Statements/for...of", "for...of")}} instead.
- Destructuring {{jsxref("Statements/for...in", "for...in")}} is deprecated. Use {{jsxref("Statements/for...of", "for...of")}} instead.
- let blocks and let expressions are obsolete.

### E4X

See [E4X](/en-US/docs/Archive/Web/E4X) for more information.

### Sharp variables

See [Sharp variables in JavaScript](/en-US/docs/Archive/Web/Sharp_variables_in_JavaScript) for more information.
