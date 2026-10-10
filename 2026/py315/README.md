# Lazy imports 

Explicit lazy imports, introduced in [PEP 810](https://peps.python.org/pep-0810/), introduce the new keyword lazy so that you can mark an import as lazy. Lazy imports don't run the module you're importing until the imported name is needed.

This feature is very useful if you have applications that have a slow startup time because they import heavy modules. For example, you can speed up the startup time of a CLI by lazy importing the dependencies of the CLI or the startup time of a development server that doesn't need to frontload every single dependency while you're debugging.

A lazy import starts with the keyword `lazy`:

```python
lazy import json
lazy from math import sqrt
```

The snippet of code above imports the module `json` lazily and it imports the function `sqrt`, from the module `math`, lazily.



