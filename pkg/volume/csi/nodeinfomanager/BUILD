load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = ["nodeinfomanager.go"],
    importpath = "k8s.io/kubernetes/pkg/volume/csi/nodeinfomanager",
    visibility = ["//visibility:public"],
    deps = [
        "//pkg/features:go_default_library",
        "//pkg/volume/util:go_default_library",
        "//staging/src/k8s.io/api/core/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/api/resource:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/types:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/sets:go_default_library",
        "//staging/src/k8s.io/apiserver/pkg/util/feature:go_default_library",
        "//staging/src/k8s.io/client-go/kubernetes:go_default_library",
        "//staging/src/k8s.io/client-go/util/retry:go_default_library",
        "//staging/src/k8s.io/csi-api/pkg/apis/csi/v1alpha1:go_default_library",
        "//staging/src/k8s.io/csi-api/pkg/client/clientset/versioned:go_default_library",
        "//vendor/github.com/container-storage-interface/spec/lib/go/csi/v0:go_default_library",
        "//vendor/github.com/golang/glog:go_default_library",
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
    srcs = [":package-srcs"],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_test",
    srcs = ["nodeinfomanager_test.go"],
    embed = [":go_default_library"],
    deps = [
        "//pkg/apis/core/helper:go_default_library",
        "//pkg/features:go_default_library",
        "//staging/src/k8s.io/api/core/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/types:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/sets:go_default_library",
        "//staging/src/k8s.io/apiserver/pkg/util/feature:go_default_library",
        "//staging/src/k8s.io/apiserver/pkg/util/feature/testing:go_default_library",
        "//staging/src/k8s.io/client-go/kubernetes/fake:go_default_library",
        "//staging/src/k8s.io/csi-api/pkg/apis/csi/v1alpha1:go_default_library",
        "//staging/src/k8s.io/csi-api/pkg/client/clientset/versioned/fake:go_default_library",
        "//vendor/github.com/container-storage-interface/spec/lib/go/csi/v0:go_default_library",
    ],
)
