load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "cpu_manager.go",
        "policy.go",
    ],
    visibility = ["//visibility:public"],
    deps = [
        "//pkg/kubelet/apis/cri/v1alpha1/runtime:go_default_library",
        "//pkg/kubelet/cm/cpumanager/state:go_default_library",
        "//pkg/kubelet/status:go_default_library",
        "//vendor/k8s.io/api/core/v1:go_default_library",
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
        "//pkg/kubelet/cm/cpumanager/state:all-srcs",
        "//pkg/kubelet/cm/cpumanager/topology:all-srcs",
    ],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
