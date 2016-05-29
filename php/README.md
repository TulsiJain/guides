# PHP

### General

- These are not to be blindly followed; strive to understand these and ask when in doubt
- Don't duplicate the functionality of a built-in library
- Don't swallow exceptions or "fail silently"

### Object-Oriented Design

- Avoid global variables
- Avoid long parameter lists
- Prefer small methods
- Prefer [pure functions]
- Prefer small classes with a single, well-defined responsibility. When a class exceeds 100 lines, it may be doing too many things

### PHP

- Use [dependency injection]
- Use strict equality checks (`===` and `!==`)
- Always turn on all errors and notices during development

## Coding Style
See [coding style].

## Testing
See [testing].

## Documentation
See [documentation].

[pure functions]: https://en.wikipedia.org/wiki/Pure_function
[dependency injection]: /php/di.md
[coding style]: /php/cs.md
[testing]: /php/testing.md
[documentation]: /php/doc.md
