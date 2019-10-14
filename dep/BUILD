load("@io_bazel_rules_scala//scala:scala.bzl", "scala_library")

scala_library(
    name = "dep",
    srcs = ["Dep.scala"],
    deps = ["@maven//:com_google_guava_guava"],
    visibility = ["//visibility:public"],
)
