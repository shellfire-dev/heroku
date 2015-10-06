# `heroku`: functions module for [shellfire]

This module provides a simple framework for using `heroku` with a [shellfire] application.

## Compatibility

* Not yet tagged

## Overview

TODO.

## Importing

To import this module, add a git submodule to your repository. From the root of your git repository in the terminal, type:-
```bash
mkdir -p lib/shellfire
cd lib/shellfire
git submodule add "https://github.com/shellfire-dev/heroku.git"
cd -
git submodule init --update
```

You may need to change the url `https://github.com/shellfire-dev/heroku.git` above if using a fork.

You will also need to add paths - include the module [paths.d].

You will also need to import the [curl] module and its dependencies.


## Namespace `heroku`

### To use in code

If calling from another [shellfire] module, add to your shell code the line
```bash
core_usesIn heroku
```
in the global scope (ie outside of any functions). A good convention is to put it above any function that depends on functions in this module. If using it directly in a program, put this line _inside_ the `_program()` function:-

```bash
_program()
{
	core_usesIn heroku
	…
}
```

### Functions

***
#### `heroku_create`

* Takes no parameters
* Designed for internal use

## Namespace `heroku_validate`

### To use in code

If calling from another [shellfire] module, add to your shell code the line
```bash
core_usesIn heroku validate
```
in the global scope (ie outside of any functions). A good convention is to put it above any function that depends on functions in this module. If using it directly in a program, put this line _inside_ the `_program()` function:-

```bash
_program()
{
	core_usesIn heroku validate
	…
}
```

### Functions

This is an internal API.


[swaddle]: https://github.com/raphaelcohn/swaddle "Swaddle homepage"
[shellfire]: https://github.com/shellfire-dev "shellfire homepage"
[core]: https://github.com/shellfire-dev/core "shellfire core module homepage"
[paths.d]: https://github.com/shellfire-dev/paths.d "paths.d shellfire module homepage"
[curl]: https://github.com/shellfire-dev/curl "curl shellfire module homepage"
[version]: https://github.com/shellfire-dev/version "version shellfire module homepage"
