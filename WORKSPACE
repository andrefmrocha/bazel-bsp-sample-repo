load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# bazel-skylib 0.8.0 released 2019.03.20 (https://github.com/bazelbuild/bazel-skylib/releases/tag/0.8.0)
skylib_version = "0.8.0"
http_archive(
    name = "bazel_skylib",
    type = "tar.gz",
    url = "https://github.com/bazelbuild/bazel-skylib/releases/download/{}/bazel-skylib.{}.tar.gz".format (skylib_version, skylib_version),
    sha256 = "2ef429f5d7ce7111263289644d233707dba35e39696377ebab8b0bc701f7818e",
)

# For bazel_bsp aspect
http_archive(
    name = "bazel_bsp",
    url = "https://github.com/illicitonion/bazel-bsp/archive/c64465f6923c8ccc559157851f9d1296d8687d6e.tar.gz",
    strip_prefix = "bazel-bsp-c64465f6923c8ccc559157851f9d1296d8687d6e",
)

# For rules_scala
http_archive(
    name = "io_bazel_rules_scala",
    url = "https://github.com/andrefmrocha/rules_scala/archive/b858a6f95aee970523772257158fe8b259b10c61.tar.gz",
    strip_prefix = "rules_scala-b858a6f95aee970523772257158fe8b259b10c61",
)

load("@io_bazel_rules_scala//scala:toolchains.bzl", "scala_register_toolchains")
scala_register_toolchains()

load("@io_bazel_rules_scala//scala:scala.bzl", "scala_repositories")
scala_repositories((
    "2.12.8",
    {
       "scala_compiler": "f34e9119f45abd41e85b9e121ba19dd9288b3b4af7f7047e86dc70236708d170",
       "scala_library": "321fb55685635c931eba4bc0d7668349da3f2c09aee2de93a70566066ff25c28",
       "scala_reflect": "4d6405395c4599ce04cea08ba082339e3e42135de9aae2923c9f5367e957315a"
    }
))

protobuf_version="09745575a923640154bcf307fba8aedff47f240a"
protobuf_version_sha256="416212e14481cff8fd4849b1c1c1200a7f34808a54377e22d7447efdf54ad758"

http_archive(
    name = "com_google_protobuf",
    url = "https://github.com/protocolbuffers/protobuf/archive/%s.tar.gz" % protobuf_version,
    strip_prefix = "protobuf-%s" % protobuf_version,
    sha256 = protobuf_version_sha256,
)


# Exp
maven_jar(
    name = "com_illicitonion_scalac_composite_reporter",
    artifact = "com.illicitonion:scalac-composite-reporter_2.12:0.0.1",
    sha256 = "9e3655fa282adbc6686805d9a745131f18819a15402b20d08fb39253f3b5a5aa",
)

# For guava
http_archive(
    name = "rules_jvm_external",
    strip_prefix = "rules_jvm_external-2.8",
    sha256 = "79c9850690d7614ecdb72d68394f994fef7534b292c4867ce5e7dec0aa7bdfad",
    url = "https://github.com/bazelbuild/rules_jvm_external/archive/2.8.zip"
)

load("@rules_jvm_external//:defs.bzl", "maven_install")

maven_install(
    name = "maven",
    artifacts = [
        "com.google.guava:guava:28.0-jre",
    ],
    repositories = [
        "https://maven.google.com",
        "https://repo1.maven.org/maven2",
    ],
    fetch_sources = True,
)
