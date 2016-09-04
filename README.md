Nom parser for Rust items
=========================

Parse Rust structs and enums without a Syntex dependency, intended for use with
[Macros 1.1](https://github.com/rust-lang/rfcs/blob/master/text/1681-macros-1.1.md).

```toml
[dependencies]
item = "0.2"
```

```rust
extern crate item;

let raw = "
    #[derive(Debug, Clone)]
    pub struct Item {
        pub ident: Ident,
        pub attrs: Vec<Attribute>,
    }
";

let ast = item::parse(raw);
```

## License

Licensed under either of

 * Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
 * MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.

### Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in this crate by you, as defined in the Apache-2.0 license, shall
be dual licensed as above, without any additional terms or conditions.
