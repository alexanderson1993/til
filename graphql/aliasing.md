# Aliasing

It's possible to alias GraphQL queries. This allows you to make multiple queries on the same type at the same time.

```
...

# This gives me the single position I ask for in the argument
positions(positionId: $positionId) {
      errors
      positions {
        id
        name
      }
}

# This lets me query the same type again without an argument
# To get all of the positions
allPositions: positions {
      errors
      positions {
        name
        id
      }
}

...
```
