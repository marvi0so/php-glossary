# Method injection

Sometimes you want to provide dependencies into an object that has already been
instantiated. This can be achieved by passing the dependency as an arg to a
method, often a setter.

A less common approach than [constructor injection](constructor-injection.md).

```php
class ExampleService
{
    private User $user;

    public function setUser(User $user): void
    {
        $this->user = $user;
    }
}
```
