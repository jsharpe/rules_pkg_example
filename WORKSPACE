load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "dbx_build_tools",
    urls = ["https://github.com/dropbox/dbx_build_tools/archive/1a0fe35a39b874d32f52a7e73d75d37be3115782.tar.gz"],
    strip_prefix = "dbx_build_tools-1a0fe35a39b874d32f52a7e73d75d37be3115782",
)

load('@dbx_build_tools//build_tools/bazel:external_workspace.bzl', 'drte_deps')

drte_deps()

register_toolchains(
    "@dbx_build_tools//thirdparty/cpython:drte-off-27-toolchain",
    "@dbx_build_tools//thirdparty/cpython:drte-off-38-toolchain",
)

http_archive(
    name = "rules_pkg",
    urls = [
        "https://mirror.bazel.build/github.com/bazelbuild/rules_pkg/releases/download/0.5.1/rules_pkg-0.5.1.tar.gz",
        "https://github.com/bazelbuild/rules_pkg/releases/download/0.5.1/rules_pkg-0.5.1.tar.gz",
    ],
    sha256 = "a89e203d3cf264e564fcb96b6e06dd70bc0557356eb48400ce4b5d97c2c3720d",
)

load("@rules_pkg//:deps.bzl", "rules_pkg_dependencies")
rules_pkg_dependencies()
