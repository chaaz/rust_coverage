# Rust Coverage Scripts

This is a simple set of scripts that makes it "easy" to generate
coverage data for Rust unit tests, using
[grcov](ttps://github.com/mozilla/grcov). These scripts include:

- `rustcov`: The top-level script to run in your project directory.
- `genhtml`: Stolen from lcov, this needs to be in your PATH when you
  run `rustcov`. MacOS brew users can use `brew install lcov` instead.
- `wait-for`: A way to wait for another program. Stolen from
  [eficode](https://github.com/eficode/wait-for/), but doesn't mess with
  an app's HOST or PORT environment.

## Requirements

In addition to rustup and cargo installed, you'll need to have the
nightly toolchain and `grcov` installed.

```
rustup toolchain install nightly  # for -Zprofile
cargo install grcov
```

## Troubleshooting

The `rustcov` script isn't that complex, so you should probably be able
to figure out what's going on yourself if you run it manually
step-by-step.
