# Testing

For all projects which support PHP 5.5 use [phpunit] 4.8.

Every project will have its own version of phpunit installed using composer.
In the project's root directory run:
```sh
chmod +x phpunit.sh
./phpunit.sh
```

### Tests

- All [possible paths][code coverage] of a program have to be tested
- Use `assertSame` instead of `assertEquals`
- Use `assertTrue`, `assertFalse`, `assertNull` for testing respective types
- Use namespaces for tests (example: `Vendor\Project\Tests`) to avoid conflicts with stubs
- Avoid directly testing methods which depend on complex components like database or system calls
- [Mock][test doubles] complex components to test methods which depend on them
- When a method requires a complex input try to break it down into smaller methods for which inputs can be provided easily in tests

[phpunit]: https://phpunit.de/
[test doubles]: https://phpunit.de/manual/current/en/test-doubles.html
[code coverage]: https://phpunit.de/manual/current/en/code-coverage-analysis.html
