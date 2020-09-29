Something like this:

```python
import random
import time

from rich.console import Console

from rich_sparklines import Graph

console = Console()


def main():
    graph = Graph("connections", lambda: random.randint(0, 20))
    while True:
        graph.update()

        console.clear()

        console.print(graph)

        time.sleep(1)


if __name__ == "__main__":
    main()
```

will produce something like this:

![Example](https://github.com/Mause/rich_sparklines/raw/master/example.png)
