# Type Error Not Caught in TypeScript

This repository demonstrates a scenario where a TypeScript type error is not caught during compilation or runtime.  The function `add` is explicitly typed to accept two numbers and return a number, but the call to `add(5, '10')` passes a string as the second argument, resulting in type coercion instead of a type error. This highlights a potential pitfall in TypeScript's type system if not handled appropriately.

## Bug Description

The `add` function is designed to only add two numbers together. When a string is passed as an argument, instead of throwing an error, TypeScript performs type coercion, potentially resulting in unexpected behavior.

## Solution

The solution involves adding stricter type checks to ensure that the function only accepts numeric arguments, thereby preventing type coercion and throwing an appropriate error when incorrect data is passed.