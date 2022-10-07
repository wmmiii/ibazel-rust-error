workspace(name = "ibazel-rust-error")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

###############################################################################
# R U L E S   R U S T
###############################################################################

# To find additional information on this release or newer ones visit:
# https://github.com/bazelbuild/rules_rust/releases
http_archive(
    name = "rules_rust",
    sha256 = "c2ed185ab8c6ba021d5e3922defd2178b5444c18030810664f8cdb8fa0dd6d8b",
    strip_prefix = "rules_rust-59fab4e79f62bfa13551ac851a40696c24c0c3a4",
    urls = [
        "https://github.com/bazelbuild/rules_rust/archive/59fab4e79f62bfa13551ac851a40696c24c0c3a4.tar.gz",
    ],
)

load("@rules_rust//rust:repositories.bzl", "rules_rust_dependencies", "rust_register_toolchains")

rules_rust_dependencies()

rust_register_toolchains(include_rustc_srcs = True)

load("@rules_rust//crate_universe:crates.bzl", "crate_deps_repository")

crate_deps_repository()

load("@rules_rust//crate_universe:crates_deps.bzl", "crate_repositories")

crate_repositories()
