load("@rules_python//python:defs.bzl", "py_library", "py_test")
load("//:repositories.bzl", "requirement")

py_library(
    name = "lib",
    visibility = ["//extract_wheels:__subpackages__"],
    srcs = [
        "bazel.py",
        "namespace_pkgs.py",
        "purelib.py",
        "requirements.py",
        "wheel.py",
    ],
    deps = [
        requirement("pkginfo"),
        requirement("setuptools"),
    ],
)

py_test(
    name = "namespace_pkgs_test",
    size = "small",
    srcs = [
        "namespace_pkgs_test.py",
    ],
    tags = ["unit"],
    deps = [
        ":lib",
    ],
)

py_test(
    name = "requirements_test",
    size = "small",
    srcs = [
        "requirements_test.py",
    ],
    tags = ["unit"],
    deps = [
        ":lib",
    ],
)
