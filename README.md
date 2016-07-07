# protobuf-wire

This package defines tools for working with protocol buffers version 3 in Haskell.

Specifically, it provides:

- Low-level functions for encoding and decoding messages
- Type classes for encoding and decoding messages, and instances for all
  wire formats identified in the specification
- A higher-level approach to encoding and decoding, based on `GHC.Generics`
- A way of creating `.proto` files from Haskell types.

See the `Data.Protobuf.Wire.Tutorial` module for more details.

# Running the language interop tests

We test inter-language interop using protoc's built-in Python code generation. In
order to successfully run these tests, you'll need to install the google protobuf
Python library. It's best to create a virtualenv and then use pip to install the
right version.

```
$ virtualenv pyenv
$ source pyenv/bin/activate
$ pip install protobuf==3.0.0b3  # Need the latest version for the newest protoc
```

`brew install python` may also work.
