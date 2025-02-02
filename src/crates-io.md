# crates.io Dependencies

The Rust compiler supports building with some dependencies from `crates.io`.
Examples are `log` and `env_logger`.

In general,
you should avoid adding dependencies to the compiler for several reasons:

- The dependency may not be of high quality or well-maintained.
- The dependency may not be using a compatible license.
- The dependency may have transitive dependencies that have one of the above
  problems.

<!-- date-check: Feb 2023 -->
Note that there is no official policy for vetting new dependencies to the compiler.
Decisions are made on a case-by-case basis, during code review.

## Permitted dependencies

The `tidy` tool has a list of crates that are allowed (called PERMITTED_RUSTC_DEPENDENCIES)
in [its deps.rs file](https://github.com/rust-lang/rust/blob/master/src/tools/tidy/src/deps.rs).
To add a dependency that is not already in the compiler, you will need to add it to the list.
