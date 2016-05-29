# Documentation

All class methods and properties should be documented. Each DocBlock should contain these in the given order:
- at least one line of description
- `@param`
- `@throws`
- `@return`

Add tags only if required. For example, don't add `@return` tag to a method that doesn't return anything. Details about DocBlocks and tags can be found below in *Further Reading* section.

### Examples
```php
/**
 * The array of stored values.
 *
 * @var array
 */
protected $storage = [];

/**
 * Read a file and get its contents.
 *
 * @param string $filename
 *
 * @throws \FileNotFoundException when file doesn't exist
 *
 * @return string File contents
 */
public function readFile($filename)
{
    // code...
}

/**
 * Get current year.
 *
 * @return int
 */
public function getYear()
{
    // code...
}

/**
 * Register a binding with the container.
 *
 * @param string|array         $abstract
 * @param \Closure|string|null $concrete
 * @param bool                 $shared
 *
 * @return bool
 */
public function bind($abstract, $concrete = null, $shared = false)
{
    // code...
}
```

Don't worry about the alignment. PHP-CS-FIXER tool will take care of it. Install this [sublimetext plugin] to make your life easy.

## Further Reading
- https://www.phpdoc.org/docs/latest/guides/index.html

[sublimetext plugin]: https://github.com/Warin/Sublime/tree/master/DocBlockr#readme
