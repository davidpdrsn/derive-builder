# Derive builder

```rust
#[macro_use]
extern crate derive_builder;

#[derive(Debug, Builder)]
struct User {
    id: i64,
    firstname: String,
    lastname: String,
}

fn main() {
    let user = User::build()
        .firstname("Bob")
        .lastname("Larsen")
        .id(1337)
        .done();
    println!("{:?}", user); // User { id: 1337, firstname: "Bob", lastname: "Larsen" }
}
```
