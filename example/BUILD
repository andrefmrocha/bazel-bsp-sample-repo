load("@io_bazel_rules_scala//scala:scala.bzl", "scala_binary")

scala_binary(
    name = "example",
    srcs = ["Example.scala"],
    deps = ["//dep:dep"],
    scalacopts =["-Ywarn-unused:imports"],
    main_class = "example.Example"
)
