# Improvements Backlog

## Logging
- [ ] Replace basicConfig string format with JSON logging via `python-json-logger`

## Python Tips & Lessons

### List Comprehension vs Generator Expression

```python
# # python# with list comprehension (creates a list first, then sums)
sum([r[field] for r in self.buffer])

# with generator expression (more memory efficient)
sum(r[field] for r in self.buffer)
# The difference is subtle — a generator doesn't build the whole list in memory first. For 60 readings it doesn't matter, but it's a good habit. Add it to docs/improvements.md for now. ✅with list comprehension (creates a list first, then sums)
sum([r[field] for r in self.buffer])

# with generator expression (more memory efficient)
sum(r[field] for r in self.buffer)
```

The difference is subtle — a generator doesn't build the whole list in memory first. For 60 readings it doesn't matter, but it's a good habit. ✅

