# ibazel rules_rust bug

This repo is intended to reproduce an error in which [Bazel watcher][1] does not
properly detect changes from the `rust_binary` rule from [rules_rust][2]

## Repro

1. Fetch and build the Bazel watcher binary
1. Run the following command
    ```bash
    ibazel run //:binary
    ```
1. Modify the string within `main.rs`
1. Note that Bazel watcher does not rebuild the executable

[1]: https://github.com/bazelbuild/bazel-watcher
[2]: http://bazelbuild.github.io/rules_rust/