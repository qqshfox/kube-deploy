load("@io_bazel_rules_go//proto:def.bzl", "go_proto_library")
load("@io_bazel_rules_go//go:def.bzl", "go_test")

go_test(
    name = "go_default_test",
    srcs = ["sizerconflict_test.go"],
    importpath = "github.com/gogo/protobuf/test/sizerconflict",
)

proto_library(
    name = "sizerconflict_proto",
    srcs = ["sizerconflict.proto"],
    visibility = ["//visibility:public"],
    deps = ["//github.com/gogo/protobuf/gogoproto:gogoproto_proto"],
)

go_proto_library(
    name = "sizerconflict_go_proto",
    importpath = "github.com/gogo/protobuf/test/sizerconflict",
    proto = ":sizerconflict_proto",
    visibility = ["//visibility:public"],
    deps = ["//github.com/gogo/protobuf/gogoproto:go_default_library"],
)
