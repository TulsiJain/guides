# Coding Style
Code should follow the [PSR-2] coding standard and the [PSR-4] autoloading standard.

### Code Style Fixer

You may use the [PHP-CS-Fixer] to fix your code style before committing.

To get started, [install the tool globally][install PHP-CS-Fixer] and check the code style by issuing the following terminal command from your project's root directory:

```sh
php-cs-fixer fix
```

If the project has a `php-cs-fixer.sh` file then in the project's root directory simply run:
```sh
chmod +x php-cs-fixer.sh
./php-cs-fixer.sh
```

See [.php_cs] file for the list of fixers used.

### Editor Plugins

To automatically fix coding style issues while editing a file install these editor plugins.

Install [Sublime Text plugin] and use these settings:
```json
{
    "phpcs_sniffer_run": false,
    "php_cs_fixer_on_save": true,
    "php_cs_fixer_executable_path": "/Users/<username>/.composer/vendor/bin/php-cs-fixer",
    "php_cs_fixer_additional_args": {
        "--fixers": "-psr0,no_useless_return,ordered_use,phpdoc_order,short_array_syntax",
        "--level": "symfony"
    }
}
```

Install [Atom package] and use these settings:
```json
"php-cs-fixer":
  executablePath: "/Users/<username>/.composer/vendor/bin/php-cs-fixer"
  executeOnSave: true
  fixers: "-psr0,no_useless_return,ordered_use,phpdoc_order,short_array_syntax"
  level: "symfony"
```

[.php_cs]: /php/.php_cs
[PSR-2]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md
[PSR-4]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md
[PHP-CS-Fixer]: https://github.com/FriendsOfPHP/PHP-CS-Fixer
[install PHP-CS-Fixer]: https://github.com/FriendsOfPHP/PHP-CS-Fixer#globally-manual
[Sublime Text plugin]: https://github.com/benmatselby/sublime-phpcs
[Atom package]: https://atom.io/packages/php-cs-fixer
