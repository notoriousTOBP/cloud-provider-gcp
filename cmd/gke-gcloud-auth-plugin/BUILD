package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_binary",
    "go_library",
)
load("//defs:version.bzl", "version_x_defs")

go_binary(
    name = "gke-gcloud-auth-plugin",
    embed = [":go_default_library"],
    pure = "on",
    x_defs = version_x_defs(),
)

go_library(
    name = "go_default_library",
    srcs = ["main.go"],
    importpath = "k8s.io/cloud-provider-gcp/cmd/gke-gcloud-auth-plugin",
    deps = [
        "//cmd/gke-gcloud-auth-plugin/cred:go_default_library",
        "//vendor/github.com/spf13/pflag:go_default_library",
        "//vendor/k8s.io/component-base/version/verflag:go_default_library",
        "//vendor/k8s.io/klog/v2:go_default_library",
    ],
)
