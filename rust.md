## Rust

### Print

```rust
println!("Hello, {}!", "world");
println!("The value of a is: {}", a);
```

### Variables

```rust
let x; // declare
x = 4; // assign value
let x = 4;
let x: i32 = 4;
let _x = 4; // compiler won't warn about variable being unused
let x = x + 1; // shadowing
let mut x = 5; // mutable
let r#fn = "name"; // raw identifier
&'a i32; // reference with an explicit lifetime
let k: &'static str = "I have a static lifetime."; // string literal
let c: char = 'ℤ'; // character
```

### Data types

```rust
let x: i32;
let x: i64;
let x: u32;
let x: u64;
let x: &str;
let x: String;

// Array
let arr: [i32; 5] = [1, 2, 3, 4, 5];
let first_arr = arr[0];

// Tuple
let tup: (i32, f64, u8) = (500, 6.4, 1);
let first_tup = tup.0; // access a tuple element
let (x, y, z ) = tup; // destructuring

// Vector
let vec: Vec<i32> = Vec::new();
let vec = vec![1, 2, 3];
let first_vec = vec.get(0);
let first_vec = &vec[0];
vec.push(5);

// Hash map
let mut scores = HashMap::new();

// Enum (similar to algebraic data types in functional languages)
enum Option<T> {
    Some(T),
    None,
}

enum Result<T, E> {
    Ok(T),
    Err(E),
}

// Struct (custom data type)
struct User {
    username: String,
    email: String,
}

// Instantiation of struct
let user = User {
    email: String::from("someone@example.com"),
    username: String::from("someusername123"),
}
```

### Control flow

```rust
// for loop
for element in set {};

// while loop
while condition {};

// if-else
if condition {} else if {} else {};

// pattern matching
let x: Option<i32>;
match x {
    Some(i) => Some(i + 1),
    None => None,
}

// let if
```

### Functions

```rust
fn plus_y(x: i32) -> i32 {
    let y = 3; // statement
    x + y // expression; return value
}

// Methods
impl Rectangle {
    fn area(&self) -> u32 {
        self.width * self.height
    }
}

// Associated functions
impl Rectangle {
    fn square(size: u32) -> Rectangle {
        Rectangle { width: size, height: size }
    }
}

// Closures
```

### Generics

```rust
fn largest<T>(list: &[T]) -> T {}

impl<T> Point<T> {
    fn x(&self) -> &T {
        &self.x
    }
}
```

### Traits

```rust
// a functionality a particular type has and can share with other types
pub trait Summary {
    fn summarize(&self) -> String;
}
```

### Lifetimes

```rust
/*  every reference has a lifetime
    and lifetime parameters for functions or structs
    that use references have to be specified */
fn longest<'a>(x: &'a str, y: &'a str) -> &'a str {
    if x.len() > y.len() {
        x
    } else {
        y
    }
}
```

### Concurrency

```rust
// Threads
```

### Error handling

```rust
// ? operator (propagating errors)
fn read_username_from_file() -> Result<String, io::Error> {
    let mut s = String::new();
    File::open("hello.txt")?.read_to_string(&mut s)?;
    Ok(s)
}
```

### Packages

```bash
# A Cargo feature that lets you build, test, and share crates
cargo new my-project
```


### Crates

```bash
# A tree of modules that produces a library or executable
cargo new --lib my-lib
cargo new --bin my-bin
```


### Modules

```rust
// Control the organization, scope, and privacy of paths
mod my_mod {}

use crate::front_of_house::hosting;

// Paths
pub fn eat_at_restaurant() { // public
    // Absolute path
    crate::front_of_house::hosting::add_to_waitlist();

    // Relative path
    front_of_house::hosting::add_to_waitlist();
}

super::serve_order();
```

### External packages (Cargo.toml)

```toml
[dependencies]
serde_json = "^1.2.3" # < 2.0.0 (caret)
serde_json = "~1.2.3" # < 1.3.0 (tilde)
serde_json = "1.2.*" # < 1.3.0 (wildcard)
serde_json = "*" # > 0.0.0
```

### Cargo (package manager)

```bash
cargo --version
cargo fmt # Format source code
cargo check # Validate source code
cargo run
cargo run --release
cargo test
cargo build # Compile source code
cargo build --release
cargo clean
```
