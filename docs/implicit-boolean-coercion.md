# Implicit boolean coercion

There are times, even when type coercion is disabled, that types will be
interpreted as booleans by PHP even when we don't explicily cast them in our
code. This is called implicit boolean coercion.

A good example is when using expressions:

```php
if ($variable) {
    // identical to if ($variable == true)
}
```

Even with `strict_types = 1` boolean coercion will occur, making the above
equivalent to:

```php
if (
  $variable !== false &&
  $variable !== 0 &&
  $variable !== 0.0 &&
  $variable !== -0.0 &&
  $variable !== '' &&
  $variable !== '0' &&
  $variable !== [] &&
  $variable !== null
) {
}
```
