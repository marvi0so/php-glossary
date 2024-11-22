# Dependency injection

Sometimes a class you are writing needs to use functionality from another class
(also known as a dependency). Generally, it is good practice to provide this
dependency from somewhere outside of the class itself.

Often, your application will have an overarching dependency injection container
that is responsible for providing the correct dependencies to each class.

There are two main ways to implement dependecy injection:

- Constructor injection
- Method injection
