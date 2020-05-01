OxIRI
=====

[![actions status](https://github.com/oxigraph/oxiri/workflows/build/badge.svg)](https://github.com/oxigraph/oxiri/actions)
[![Latest Version](https://img.shields.io/crates/v/oxiri.svg)](https://crates.io/crates/oxiri)
[![Released API docs](https://docs.rs/oxiri/badge.svg)](https://docs.rs/oxiri)

OxIRI is a simple and fast implementation of IRIs based on [RFC 3987](https://www.ietf.org/rfc/rfc3987).

It allows zero stack allocation IRI validation and resolution.

Example:
```rust
use oxiri::Iri;

// Parse and validate base IRI
let base_iri = Iri::parse("http://foo.com/bar/baz").unwrap();

// Validate and resolve relative IRI
let iri = base_iri.resolve("bat#foo").unwrap();
assert_eq!("http://foo.com/bar/bat#foo", iri.into_inner());
```


## License

This project is licensed under either of

 * Apache License, Version 2.0, ([LICENSE-APACHE](LICENSE-APACHE) or
   http://www.apache.org/licenses/LICENSE-2.0)
 * MIT license ([LICENSE-MIT](LICENSE-MIT) or
   http://opensource.org/licenses/MIT)
   
at your option.


### Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted for inclusion in Futures by you, as defined in the Apache-2.0 license, shall be dual licensed as above, without any additional terms or conditions.
