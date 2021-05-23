load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library")

go_library(
    name = "go_default_library",
    srcs = ["main.go"],
    importpath = "github.com/motiejus/code/undocker",
    visibility = ["//visibility:private"],
    deps = [
        "//src/undocker/rootfs:rootfs_lib",
        "@com_github_jessevdk_go_flags//:go_default_library",
    ],
)

go_binary(
    name = "undocker",
    embed = [":go_default_library"],
    visibility = ["//visibility:public"],
)
