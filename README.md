Sample of building C based dynamic library with CMAKE and Rust main code to use the library.

## USAGE

```bash
$ cargo build -vv
```

```bash
$ cargo run
```

## BUILD AND RUN PROCESS

```bash
$ cargo build -vv                                                                                                                                                                                           10:01:13
   Compiling cc v1.0.58
     Running `CARGO=/Users/weli/.rustup/toolchains/stable-x86_64-apple-darwin/bin/cargo CARGO_MANIFEST_DIR=/Users/weli/.cargo/registry/src/github.com-1ecc6299db9ec823/cc-1.0.58 CARGO_PKG_AUTHORS='Alex Crichton <alex@alexcrichton.com>' CARGO_PKG_DESCRIPTION='A build-time dependency for Cargo build scripts to assist in invoking the native
C compiler to compile native C code into a static archive to be linked into Rust
code.
' CARGO_PKG_HOMEPAGE='https://github.com/alexcrichton/cc-rs' CARGO_PKG_NAME=cc CARGO_PKG_REPOSITORY='https://github.com/alexcrichton/cc-rs' CARGO_PKG_VERSION=1.0.58 CARGO_PKG_VERSION_MAJOR=1 CARGO_PKG_VERSION_MINOR=0 CARGO_PKG_VERSION_PATCH=58 CARGO_PKG_VERSION_PRE= DYLD_FALLBACK_LIBRARY_PATH='/Users/weli/works/rust_and_cmake_dyn/target/debug/deps:/Users/weli/.rustup/toolchains/stable-x86_64-apple-darwin/lib:/Users/weli/.rustup/toolchains/stable-x86_64-apple-darwin/lib:/Users/weli/lib:/usr/local/lib:/usr/lib' rustc --crate-name cc --edition=2018 /Users/weli/.cargo/registry/src/github.com-1ecc6299db9ec823/cc-1.0.58/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts --crate-type lib --emit=dep-info,metadata,link -Cembed-bitcode=no -C debuginfo=2 -C metadata=1d765c8203084313 -C extra-filename=-1d765c8203084313 --out-dir /Users/weli/works/rust_and_cmake_dyn/target/debug/deps -L dependency=/Users/weli/works/rust_and_cmake_dyn/target/debug/deps --cap-lints warn`
   Compiling cmake v0.1.44
     Running `CARGO=/Users/weli/.rustup/toolchains/stable-x86_64-apple-darwin/bin/cargo CARGO_MANIFEST_DIR=/Users/weli/.cargo/registry/src/github.com-1ecc6299db9ec823/cmake-0.1.44 CARGO_PKG_AUTHORS='Alex Crichton <alex@alexcrichton.com>' CARGO_PKG_DESCRIPTION='A build dependency for running `cmake` to build a native library
' CARGO_PKG_HOMEPAGE='https://github.com/alexcrichton/cmake-rs' CARGO_PKG_NAME=cmake CARGO_PKG_REPOSITORY='https://github.com/alexcrichton/cmake-rs' CARGO_PKG_VERSION=0.1.44 CARGO_PKG_VERSION_MAJOR=0 CARGO_PKG_VERSION_MINOR=1 CARGO_PKG_VERSION_PATCH=44 CARGO_PKG_VERSION_PRE= DYLD_FALLBACK_LIBRARY_PATH='/Users/weli/works/rust_and_cmake_dyn/target/debug/deps:/Users/weli/.rustup/toolchains/stable-x86_64-apple-darwin/lib:/Users/weli/.rustup/toolchains/stable-x86_64-apple-darwin/lib:/Users/weli/lib:/usr/local/lib:/usr/lib' rustc --crate-name cmake /Users/weli/.cargo/registry/src/github.com-1ecc6299db9ec823/cmake-0.1.44/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi --crate-type lib --emit=dep-info,metadata,link -Cembed-bitcode=no -C debuginfo=2 -C metadata=447ad2c68e1e4c90 -C extra-filename=-447ad2c68e1e4c90 --out-dir /Users/weli/works/rust_and_cmake_dyn/target/debug/deps -L dependency=/Users/weli/works/rust_and_cmake_dyn/target/debug/deps --extern cc=/Users/weli/works/rust_and_cmake_dyn/target/debug/deps/libcc-1d765c8203084313.rmeta --cap-lints warn`
   Compiling rust_and_cmake_dyn v0.1.0 (/Users/weli/works/rust_and_cmake_dyn)
     Running `CARGO=/Users/weli/.rustup/toolchains/stable-x86_64-apple-darwin/bin/cargo CARGO_MANIFEST_DIR=/Users/weli/works/rust_and_cmake_dyn CARGO_PKG_AUTHORS='阿男 <l.weinan@gmail.com>' CARGO_PKG_DESCRIPTION= CARGO_PKG_HOMEPAGE= CARGO_PKG_NAME=rust_and_cmake_dyn CARGO_PKG_REPOSITORY= CARGO_PKG_VERSION=0.1.0 CARGO_PKG_VERSION_MAJOR=0 CARGO_PKG_VERSION_MINOR=1 CARGO_PKG_VERSION_PATCH=0 CARGO_PKG_VERSION_PRE= DYLD_FALLBACK_LIBRARY_PATH='/Users/weli/works/rust_and_cmake_dyn/target/debug/deps:/Users/weli/.rustup/toolchains/stable-x86_64-apple-darwin/lib:/Users/weli/.rustup/toolchains/stable-x86_64-apple-darwin/lib:/Users/weli/lib:/usr/local/lib:/usr/lib' rustc --crate-name build_script_build --edition=2018 build.rs --error-format=json --json=diagnostic-rendered-ansi --crate-type bin --emit=dep-info,link -Cembed-bitcode=no -C debuginfo=2 -C metadata=c83ba5ed81b6f250 -C extra-filename=-c83ba5ed81b6f250 --out-dir /Users/weli/works/rust_and_cmake_dyn/target/debug/build/rust_and_cmake_dyn-c83ba5ed81b6f250 -C incremental=/Users/weli/works/rust_and_cmake_dyn/target/debug/incremental -L dependency=/Users/weli/works/rust_and_cmake_dyn/target/debug/deps --extern cmake=/Users/weli/works/rust_and_cmake_dyn/target/debug/deps/libcmake-447ad2c68e1e4c90.rlib`
     Running `/Users/weli/works/rust_and_cmake_dyn/target/debug/build/rust_and_cmake_dyn-c83ba5ed81b6f250/build-script-build`
[rust_and_cmake_dyn 0.1.0] running: "cmake" "/Users/weli/works/rust_and_cmake_dyn/libfoo" "-DCMAKE_INSTALL_PREFIX=/Users/weli/works/rust_and_cmake_dyn/target/debug/build/rust_and_cmake_dyn-beb15972075b789f/out" "-DCMAKE_C_FLAGS= -ffunction-sections -fdata-sections -fPIC -m64 -arch x86_64" "-DCMAKE_C_COMPILER=/usr/bin/cc" "-DCMAKE_CXX_FLAGS= -ffunction-sections -fdata-sections -fPIC -m64 -arch x86_64" "-DCMAKE_CXX_COMPILER=/usr/bin/c++" "-DCMAKE_ASM_FLAGS= -ffunction-sections -fdata-sections -fPIC -m64 -arch x86_64" "-DCMAKE_ASM_COMPILER=/usr/bin/cc" "-DCMAKE_BUILD_TYPE=Debug"
[rust_and_cmake_dyn 0.1.0] -- The C compiler identification is AppleClang 11.0.3.11030032
[rust_and_cmake_dyn 0.1.0] -- Detecting C compiler ABI info
[rust_and_cmake_dyn 0.1.0] -- Detecting C compiler ABI info - done
[rust_and_cmake_dyn 0.1.0] -- Check for working C compiler: /usr/bin/cc - skipped
[rust_and_cmake_dyn 0.1.0] -- Detecting C compile features
[rust_and_cmake_dyn 0.1.0] -- Detecting C compile features - done
[rust_and_cmake_dyn 0.1.0] -- Configuring done
[rust_and_cmake_dyn 0.1.0] -- Generating done
[rust_and_cmake_dyn 0.1.0] CMake Warning:
[rust_and_cmake_dyn 0.1.0]   Manually-specified variables were not used by the project:
[rust_and_cmake_dyn 0.1.0]
[rust_and_cmake_dyn 0.1.0]     CMAKE_ASM_COMPILER
[rust_and_cmake_dyn 0.1.0]     CMAKE_ASM_FLAGS
[rust_and_cmake_dyn 0.1.0]     CMAKE_CXX_COMPILER
[rust_and_cmake_dyn 0.1.0]     CMAKE_CXX_FLAGS
[rust_and_cmake_dyn 0.1.0]
[rust_and_cmake_dyn 0.1.0]
[rust_and_cmake_dyn 0.1.0] -- Build files have been written to: /Users/weli/works/rust_and_cmake_dyn/target/debug/build/rust_and_cmake_dyn-beb15972075b789f/out/build
[rust_and_cmake_dyn 0.1.0] running: "cmake" "--build" "." "--target" "install" "--config" "Debug" "--"
[rust_and_cmake_dyn 0.1.0] Scanning dependencies of target foo
[rust_and_cmake_dyn 0.1.0] [ 50%] Building C object CMakeFiles/foo.dir/foo.c.o
[rust_and_cmake_dyn 0.1.0] [100%] Linking C shared library libfoo.dylib
[rust_and_cmake_dyn 0.1.0] [100%] Built target foo
[rust_and_cmake_dyn 0.1.0] Install the project...
[rust_and_cmake_dyn 0.1.0] -- Install configuration: "Debug"
[rust_and_cmake_dyn 0.1.0] -- Installing: /Users/weli/works/rust_and_cmake_dyn/target/debug/build/rust_and_cmake_dyn-beb15972075b789f/out/./libfoo.dylib
[rust_and_cmake_dyn 0.1.0] cargo:root=/Users/weli/works/rust_and_cmake_dyn/target/debug/build/rust_and_cmake_dyn-beb15972075b789f/out
[rust_and_cmake_dyn 0.1.0] cargo:rustc-link-search=native=/Users/weli/works/rust_and_cmake_dyn/target/debug/build/rust_and_cmake_dyn-beb15972075b789f/out
[rust_and_cmake_dyn 0.1.0] cargo:rustc-link-lib=dylib=foo
     Running `CARGO=/Users/weli/.rustup/toolchains/stable-x86_64-apple-darwin/bin/cargo CARGO_MANIFEST_DIR=/Users/weli/works/rust_and_cmake_dyn CARGO_PKG_AUTHORS='阿男 <l.weinan@gmail.com>' CARGO_PKG_DESCRIPTION= CARGO_PKG_HOMEPAGE= CARGO_PKG_NAME=rust_and_cmake_dyn CARGO_PKG_REPOSITORY= CARGO_PKG_VERSION=0.1.0 CARGO_PKG_VERSION_MAJOR=0 CARGO_PKG_VERSION_MINOR=1 CARGO_PKG_VERSION_PATCH=0 CARGO_PKG_VERSION_PRE= DYLD_FALLBACK_LIBRARY_PATH='/Users/weli/works/rust_and_cmake_dyn/target/debug/deps:/Users/weli/.rustup/toolchains/stable-x86_64-apple-darwin/lib:/Users/weli/.rustup/toolchains/stable-x86_64-apple-darwin/lib:/Users/weli/lib:/usr/local/lib:/usr/lib' OUT_DIR=/Users/weli/works/rust_and_cmake_dyn/target/debug/build/rust_and_cmake_dyn-beb15972075b789f/out rustc --crate-name rust_and_cmake_dyn --edition=2018 src/main.rs --error-format=json --json=diagnostic-rendered-ansi --crate-type bin --emit=dep-info,link -Cembed-bitcode=no -C debuginfo=2 -C metadata=429ce10f42fb0f6e --out-dir /Users/weli/works/rust_and_cmake_dyn/target/debug/deps -C incremental=/Users/weli/works/rust_and_cmake_dyn/target/debug/incremental -L dependency=/Users/weli/works/rust_and_cmake_dyn/target/debug/deps -L native=/Users/weli/works/rust_and_cmake_dyn/target/debug/build/rust_and_cmake_dyn-beb15972075b789f/out -l dylib=foo`
    Finished dev [unoptimized + debuginfo] target(s) in 2.93s
```

```bash
$ cargo run                                                                                                                                                                                                 10:01:43
    Finished dev [unoptimized + debuginfo] target(s) in 0.00s
     Running `target/debug/rust_and_cmake_dyn`
Hello, world from Rust!
Hello, world from C! Value passed: 3.141590
$                                                                                                                                                                                                           10:01:45
```

## RELATIVE PROJECT

* [Sample of building C based STATIC library with CMAKE and Rust main code to use the library.](https://github.com/liweinan/rust_and_cmake)
