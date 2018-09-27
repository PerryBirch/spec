# Sequence

This extension defines a value which can be included within a CloudEvent
to describe the relative position of an event within an ordered sequence
of events.

The `value` represents the event's position within a contiguous, ordered
stream of events from a single observable source.

### Value
* Type: `String`
* Description: Value expressing the relative order of the event. This enables
  interpretation of data supercedence.
* Constraints
  * REQUIRED
  * MUST be a non-empty lexicographically-orderable string
  * RECOMMENDED as monotonically increasing and contiguous
* The values MUST be string-encoded signed 32-bit Integers.
* The sequence MUST start with a value of `1` and increase by `1` for each 
  subsequent value (i.e. be contiguous and monotonically increasing).
* The value wraps around from 2,147,483,647 (2^31 -1) to
  -2,147,483,648 (-2^31).

## Other Ordering Extensions:
- [Vector Clock](./vector-clock.md)