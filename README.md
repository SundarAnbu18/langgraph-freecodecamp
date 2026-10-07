# langgraph-freecodecamp

## Type annotations with TypedDict

A regular dictionary can hold values of any type. `TypedDict` exists so a dictionary can have a fixed set of keys, each with a known type. That gives type safety: a type checker can catch a wrong type or a missing key before the code runs.

```python
from typing import TypedDict


class Movie(TypedDict):
    name: str
    year: int


movie = Movie(name="Iron Man", year=2019)
```

Here `name` must be a string and `year` must be an integer. Both keys are required.

A field can also be optional, so the value does not have to be passed when the dictionary is created. Mark it with `NotRequired`:

```python
from typing import NotRequired, TypedDict


class Movie(TypedDict):
    name: str
    year: int
    director: NotRequired[str]


movie = Movie(name="Iron Man", year=2019)
```
