# Dependency Injection

### Introduction

If there is a class `A` which depends on class `D`:

Instead of this:

```php
class A
{
    public function __constrcut()
    {
        $this->d = new D();
    }
}

$a = new A();
```

Do this:

```php
class A
{
    public function __constrcut(D $d) // note the type hinting
    {
        $this->d = $d;
    }
}

$d = new D();
$a = new A($d);
```

This makes testing easier. For example if class `D` is a complex component like a database it can be mocked easily.

Another advantage is same dependency can be passed to multiple objects. For example if class `B` also depends on class `D`:

```php
$d = new D();
$a = new A($d);
$b = new B($d);
```

**Note:** Care should be taken that properties of `D` are NOT getting modified during any method call. Don't change a class variable when using dependency injection. Prefer writing [pure functions]. If a class property has to be changed during a method call then don't use it a dependency.

## Further Reading
- http://php-di.org/doc/understanding-di.html
- https://en.wikipedia.org/wiki/Dependency_injection

[pure functions]: https://en.wikipedia.org/wiki/Pure_function
