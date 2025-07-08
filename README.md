# ☑️ Todoify

[![Package Version](https://img.shields.io/hexpm/v/todoify)](https://hex.pm/packages/todoify)
[![Hex Docs](https://img.shields.io/badge/hex-docs-ffaff3)](https://hexdocs.pm/todoify/)

## Work in Progress

**This project is a WIP and is not working yet**

## Introduction

Todoify creates `todo` placeholders for any missing modules or function calls in your gleam program. This is useful for when you are working with codegeneration and might have code relying on modules that errored during generation.

Todoify would be able to resolve these error messages by creating the missing module file and/or a function with a `todo` in
the body.
```sh
error: Unknown module
  ┌─ /root/playground/src/playground.gleam:1:1
  │
1 │ import playground/foo
  │ ^^^^^^^^^^^^^^^^^^^^^

No module has been found with the name `playground/foo`.
```

```sh
error: Unknown module value
  ┌─ /root/playground/src/playground.gleam:4:7
  │
4 │   foo.bar()
  │       ^^^

The module `playground/foo` does not have a `bar` value.
```


⚠️ Since this library modifies source code, please make sure to save your work with a
version control system before running todoify. ⚠️

## Scope

Here is an overview of what Todoify does and not do with your source code:

- ✅ create missing modules
- ✅ create missing functions
- ✅ create missing constants


- ❌ resolve type missmatch
- ❌ create missing variables
- ❌ override existing module files
- ❌ override existing functions with a body

## Usage

```sh
gleam add todoify@1
```

```sh
gleam run -m todoify
```

## Development

```sh
gleam run   # Run the project
gleam test  # Run the tests
```

## Future Work

Ideas and actionable ideas are collected and organised here: https://github.com/daniellionel01/todoify/issues

Contributions are welcomed!
