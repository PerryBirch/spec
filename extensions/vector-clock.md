# Vector Clock

This extension defines a value which can be included within a CloudEvent
to describe the relative position of an event within an ordered sequence
of events across multiple collaborating sources.

See [Vector clock](https://en.wikipedia.org/wiki/Vector_clock)

### Value
* Type: `String`
* Description: Value expressing the relative order of the event. This enables
  interpretation of data supercedence.
* Constraints
  * REQUIRED
  * MUST be a non-empty lexicographically-orderable string
* The tuple keys MUST be case insensitive ANSI strings.
* The tuple values MUST be string-encoded signed 32-bit Integers.
* Any tuple values wrap around from 2,147,483,647 (2^31 -1) to
  -2,147,483,648 (-2^31).


Other Ordering Extensions:
- [Sequence](./sequence.md)