load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = ["translate.go"],
    importmap = "k8s.io/kubernetes/vendor/github.com/kubernetes-csi/kubernetes-csi-migration-library",
    importpath = "github.com/kubernetes-csi/kubernetes-csi-migration-library",
    visibility = ["//visibility:public"],
    deps = [
        "//staging/src/k8s.io/api/core/v1:go_default_library",
        "//vendor/github.com/kubernetes-csi/kubernetes-csi-migration-library/plugins:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [
        ":package-srcs",
        "//vendor/github.com/kubernetes-csi/kubernetes-csi-migration-library/plugins:all-srcs",
    ],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
