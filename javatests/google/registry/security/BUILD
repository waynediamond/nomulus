package(
    default_testonly = 1,
    default_visibility = ["//java/google/registry:registry_project"],
)

licenses(["notice"])  # Apache 2.0

load("//java/com/google/testing/builddefs:GenTestRules.bzl", "GenTestRules")


java_library(
    name = "security",
    srcs = glob(
        ["*.java"],
        exclude = glob(["*ServletTest.java"]),
    ),
    deps = [
        "//java/com/google/common/base",
        "//java/com/google/common/collect",
        "//java/com/google/common/net",
        "//third_party/java/appengine:appengine-api-testonly",
        "//third_party/java/appengine:appengine-testing",
        "//third_party/java/joda_time",
        "//third_party/java/json_simple",
        "//third_party/java/junit",
        "//third_party/java/mockito",
        "//third_party/java/servlet/servlet_api",
        "//third_party/java/truth",
        "//java/google/registry/security",
        "//java/google/registry/util",
        "//javatests/google/registry/testing",
    ],
)

GenTestRules(
    name = "GeneratedTestRules",
    test_files = glob(["*Test.java"]),
    deps = [
        ":security",
    ],
)
