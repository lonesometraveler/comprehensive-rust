# `for` expressions

The `for` expression is closely related to the `while let` expression. It will
automatically call `into_iter()` on the expression and then iterate over it:

```rust,editable
fn main() {
    let v = vec![10, 20, 30];

    for x in v {
        println!("x: {x}");
    }
    
    for i in (0..10).step_by(2) {
        println!("i: {i}");
    }
}
```

You can use `break` and `continue` here as usual.

<details>
    
* Index iteration is not a special syntax in Rust for just that case.
* `(0..10)` is a range that implements an `Iterator` trait. 
* `step_by` is a method that returns another `Iterator` that skips every other element. 
    
</details>
