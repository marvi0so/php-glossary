# Constructor injection

A common way of providing [dependency injection](dependecy-injection.md) to an
object when it is first instantiated. Dependencies are passed as args in the
`__construct()` method of a class.

Often this is managed by your application's service container which will likely
also provide the correct dependencies for you using autowiring.

```php
class ExampleService
{
    public function __construct(private readonly User $user)
    {
    }
}
```
