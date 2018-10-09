### Conclusion of Results of Lambda Reuse

* Without lambda container reuse  and without `--profile`, 4s plus is used to query:
```
query {
  item {
    subItems {
      edges {
        node {
          id
        }
      }
    }
  }
}
```
* Using `--profile` increases the speed. 1s of time is spent trying to get credentials. This lowers it by 1 second on my machine.
* Using lambda container resuse, speed is further increased by 1 second.
* With both options on, around 2 seconds is reduced

> Timing was done by cProfiler and the network tab in chrome browser
