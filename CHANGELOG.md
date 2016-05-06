# Changelog

## v0.10.0 - May 2, 2016

### Notable changes:

- [22ff905]: No more default semantic action for _terminal.
  * To duplicate the old behavior, you can write a "_terminal" semantic action that just
    returns `this.primitiveValue`, as [in the math example](https://github.com/cdglabs/ohm/commit/22ff905b5842d52a8c8a63ef8186f574e01bf2e4#diff-215507e52f6cd81b5c49dc9cd72aae2eR390).
- [8efa687]: Expose pexprs as part of the public API (`ohm.pexprs`).
- [3ce66ea]: Allow leading pipe in rule bodies (suggested by Jason Merrill).
  * In rule definitions, the body may optionally begin with a `|` character, which will be ignored.
- #63: Semantics instances now include a built-in attribute named 'asIteration'.
  * This simplifies working with the built-in `ListOf` rule.
  * Needs documentation (#93)
- [761d6ef]: `ListOf_some` and `ListOf_none` renamed to `NonemptyListOf` and `EmptyListOf`.
- [7590d82]: Add "extras" module, with toAST() operation.
  * See the [documentation](./doc/extras.md) for more information.
- [e24a146]: New `isOptional` method on parse nodes.
  * See the [documentation](./doc/api-reference.md#parse-nodes) for more information.
- [c548f01]: The built-in `spaces_` rule has been renamed to `spaces`.
- [64ee822]: New `getDiscardedSpaces` method on MatchResult, which makes Alex happy.
  * Needs documentation (#92)
