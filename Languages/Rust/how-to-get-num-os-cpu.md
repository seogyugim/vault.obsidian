> 참고

# Rust에서 OS CPU 갯수 찾기

## 태초의 방식 (deprecated)

```ini
[dependencies]
num_cpus = "1.0"
```

```rust
extern crate num_cpus;
let num = num_cpus::get();
```

## 그 다음 방식 (deprecated)

```rust
fn main() {
    println!("{}", std::os::num_cpus());
}
```


## 현재 방식 

```rust
// rustc 1.67.0 (fc594f156 2023-01-24)
std::thread::available_parallelism().unwrap().get()
```

