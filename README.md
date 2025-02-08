# delta-rs-with-encryption
This repo collects forks of multiple repos needed to add encryption to delta-rs

The needed modules are all git submodules.
See here (https://git-scm.com/book/en/v2/Git-Tools-Submodules) for an overview of using submodules.
In short, after you clone this project you will want to run:
```
git submodule init
git submodule update
```

To update all the submodules with changes from others run
```
git pull --recurse-submodules
```

For now, we are testing with a modified version of the example code in delta-rs. That is 
```
delta-rs/crates/deltalake/examples/basic_operations.rs
```
To run it via cargo we can, from the delta-rs directory, run
```
cargo run --package deltalake --example basic_operations --features="datafusion"
```
