load("@io_bazel_rules_scala//scala:scala.bzl", "scala_binary")

scala_binary(
    name = "test",
    srcs = ["Test.scala"],
    scalacopts =["-Ywarn-unused:imports"],
    main_class = "com.andrefmrocha.test"
)
