## Create random passwords from a set of alphanumeric characters

[![rand-badge]][rand] [![cat-os-badge]][cat-os]

Randomly generates a string of given length ASCII characters in the range `A-Z,
a-z, 0-9`, with [`Alphanumeric`] sample.

```rust,edition2018
use rand::{rng, Rng};
use rand::distributions::Alphanumeric;

fn main() {
    let rand_string: String = rng()
        .sample_iter(&Alphanumeric)
        .take(30)
        .map(char::from)
        .collect();

    println!("{}", rand_string);
}
```

[`Alphanumeric`]: https://docs.rs/rand/*/rand/distributions/struct.Alphanumeric.html
