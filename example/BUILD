load("@io_bazel_rules_scala//scala:scala.bzl", "scala_library")

scala_library(
    name = "example",
    srcs = ["Example.scala"],
    deps = ["//dep:dep"],
    scalacopts =["-Ywarn-unused:imports"],
)
