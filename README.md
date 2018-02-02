## TDLIB Json Client Rust FFI Bindings

### Installing TDLIB

In order to generate bindings, `tdjson-sys` needs the TDLIB to be intalled on a developer's system.

Clone the [`tdlib` repo](https://github.com/tdlib/td) and checkout the wanted version.
```bash
git clone git@github.com:tdlib/td.git
cd td
git checkout v1.1.0
```

Install dependencies and build the library as described in the [README.md](https://github.com/tdlib/td/blob/master/README.md)

Then, install the library, from the `build` directory created in the previous step. (as root)
```bash
cmake --build . --target install
```

### Generate Bindings

After installing `tdlib`, just add `tdjson-sys` to your crate's dependencies

```toml
tdlib-sys = "0.1.0"
```

And let the Cargo do it's magick!
```bash
cargo build
```